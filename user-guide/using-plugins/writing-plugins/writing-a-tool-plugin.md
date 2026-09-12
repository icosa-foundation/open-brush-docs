# Writing a Tool Plugin

Tool Plugins can do many different things but they are often used for drawing a lot of brush strokes all in one go. For example you could draw an entire spiral shape whenever the user clicks the trigger. Or you could use the positions: where they first pressed the trigger in and where their brush controller was when they released the trigger - to get the size of a region and create a shape that filled that space.

To create a Tool Plugin name your script with the prefix "ToolScript". For example: _ToolScript.Circle.lua_

Tool Scripts should usually return a list of transforms. If they do then this defines an entire brush stroke that is then created for you.

## Previewing the returned brush stroke

By default, a Tool Plugin can display a simple mesh preview such as a cube, sphere or quad. If the path itself is the most useful preview, set `previewType` to `"stroke"`:

```lua
Settings = {
    description = "Draws a circle",
    previewType = "stroke"
}

local function buildCircle()
    local points = Path:New()
    for angle = 0, 360, 10 do
        local position2d = Vector2:PointOnCircle(angle)
        local rotation = Rotation:New(0, 0, angle * 180)
        points:Insert(Transform:New(position2d:OnZ(), rotation))
    end
    points:Insert(points[0])
    return points
end

function Main()
    if Brush.triggerIsPressed or Brush.triggerReleasedThisFrame then
        return buildCircle()
    end
end
```

While the trigger is held, Open Brush renders the returned path using the active brush. The preview is regenerated whenever `Main()` returns another path, then the most recent result is committed once when the trigger is released. Return the path while `Brush.triggerIsPressed` if you want the preview to follow the controller. Returning no path, an empty path or a path that cannot produce at least two brush control points clears the preview.

For expensive paths, `Tool.isPreview` lets the plugin generate a lower-resolution live path and retain its full resolution for the final stroke. It is `true` when `Main()` is generating a stroke preview and `false` when `Main()` runs on release to generate the path that will be committed:

```lua
local pointCount = Parameters.points
if Tool.isPreview then
    pointCount = Math:Min(pointCount, 200)
end
```

Set `previewInterval` to limit how often Open Brush runs `Main()` and rebuilds the live preview. The value is a minimum interval in seconds. The initial preview runs immediately, skipped updates retain the previous preview, and the release execution is never throttled. If the setting is omitted or is not positive, preview generation continues every frame:

```lua
Settings = {
    previewType = "stroke",
    previewInterval = 0.1
}
```

`previewInterval` applies only to `previewType = "stroke"`. It does not throttle Tool Scripts that use a mesh preview or scripts that intentionally emit output continuously.

The preview type is deliberately singular. If the script returns a `PathList`, `previewType = "stroke"` previews only its first drawable path. `Tool.latestControlPoints` also refers only to this selected path. All paths in the result are still drawn when the trigger is released. The active symmetry mode is applied only when the result is committed, so symmetry copies are not shown in this live preview.

The plural `previewType = "strokes"` is reserved for future multipath preview support and is not currently available.

The scale of each transform remains that control point's pressure. The overall size determined by the tool gesture is applied as the stroke's scale, so the preview uses the same pressure and scale values as the committed stroke.

## Reading the generated control points

Open Brush converts the single path selected by the latest Tool Plugin stroke preview into brush control points and exposes them through `Tool.latestControlPoints`. This is the most recently completed evaluation of the active Tool Plugin. It is empty when the plugin returns no drawable path.

`Tool.latestControlPoints` is a `ControlPointList` with these members:

* `count` - the number of control points
* `[index]` - a zero-based control-point lookup
* `items` - an enumerable collection of all control points

Each `ControlPoint` provides:

* `position` - its position as a `Vector3`
* `rotation` - its orientation as a `Quaternion`
* `pressure` - its pressure value
* `timestampMs` - its timestamp in milliseconds

`Tool.latestControlPointSpace` reports the coordinate space used by the list. Preview control points are currently returned in canvas space, even when the Tool Plugin returned a path in the default or pointer coordinate space.

## Quick snap

Tool Plugins support the same hold-to-snap control used when grabbing widgets. The lock icon on the brush controller identifies the context button:

* If Snap Settings are off, hold the button to apply a temporary 90-degree rotation snap.
* If angle or position snapping is already enabled in Snap Settings, hold the button to temporarily bypass those settings.

Quick snap affects both the live preview and the stroke committed when the trigger is released.

## Tool Plugins and symmetry

Brush strokes returned by a Tool Plugin are affected by the active symmetry mode. This lets the same generated shape pass through Open Brush's regular mirror or multi-mirror transformation without the plugin having to calculate those copies itself.

If you only want the path returned by the script, turn symmetry off before running the Tool Plugin. If you want scripted symmetry behavior as well, combine the Tool Plugin with a [Symmetry Plugin](writing-a-symmetry-plugin.md).

We previously started by showing the simplest possible plugin script - one that does nothing. Because a tool plugin does nothing by default that would be an empty file! But let's put a bit of scaffolding in so you have a starting point for a plugin that actually does _something._

```lua
function Main()
    if Brush.triggerPressedThisFrame then
        return {}
    end
end
```

It checks to see if the user pressed the trigger and if so it returns an empty list. So this plugin does nothing and it does it every time the user presses the trigger. Great, huh?

Let's make it do something:

```lua
function Main()
    if Brush.triggerPressedThisFrame then
        return {
            Transform:Position(-1, -1, 0),
            Transform:Position(1, -1, 0),
            Transform:Position(1, 1, 0),
            Transform:Position(-1, 1, 0),
            Transform:Position(-1, -1, 0)
        }
    end
end
```

This returns a path with 5 points forming a square. A square has 4 corners so why 5 points? The last point is the same as the first so that the square closes on itself.

If you try this, you'll notice the square isn't very square. This is because Open Brush tries to smooth brush strokes. It expects you to be hand-drawing smooth curvy lines in space - not carefully placing precise geometric paths.

We can fix this by adding extra points:

```lua
function Main()
    if Brush.triggerPressedThisFrame then
        myPath = Path:New({
            Transform:Position(-1, -1, 0),
            Transform:Position(1, -1, 0),
            Transform:Position(1, 1, 0),
            Transform:Position(-1, 1, 0),
            Transform:Position(-1, -1, 0)
        })
        return myPath:SubdivideSegments(5)
    end
end
```

This time we create a `Path` object instead of just using a list of transforms. This allows us to use any of the handy methods that are provided by `Path` - in this case it's the [`SubdivideSegments`](https://icosa.gitbook.io/open-brush-plugin-scripting-docs/readme/path#path-subdividesegments-parts) method. This modifies the path by inserting as many new points as we ask for in each path segment. In this case we ask for 5 new points so the square that previously had 5 points (and thus 4 segments) will now have 4 x 5 = 20 points. (I'll let you work out how many segments!)

Next let's draw a circle:

```lua
function Main()
    if Brush.triggerReleasedThisFrame then
        points = Path:New()
        for angle = 0, 360, 10 do
            position2d = Vector2:PointOnCircle(angle)
            points:Insert(Transform:Position(position2d:OnZ()))
        end
        return points
    end
end
```

There's a few new things here:

1. a loop that begins `for...do`, this is a standard lua construct and works similarly to loops in other languages.
2. we first calculate a 2d vector using `Vector2:PointOnCircle(angle)`. A Vector2 is very similar to the `Vector3` that we used previously for specifying a position. The difference is that it only has two coordinates: x and y.
3. We convert the `Vector2` into a `Vector3` on the next line by using the `OnZ()` method. This creates a `Vector3` where x and y are taken from the `Vector2` the z value is set to 0. Therefore it lies on the plane perpendicular to the z axis (it could probably have been named on `OnXY()` but this sounded better to me)
4. We are using `triggerReleasedThisFrame` instead of `triggerPressedThisFrame`. In this example we wait for the user to release the trigger before we do anything. This means we know both the start point (where they pressed the trigger) and the end point (where they released it). These two points are used to determine how the path we return is scaled and rotated. You don't need to do this scaling and rotating yourself - it happens automatically if you return a value representing a brush stroke.&#x20;
