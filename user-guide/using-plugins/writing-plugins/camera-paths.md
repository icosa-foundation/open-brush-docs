# Camera Paths from Plugins

Lua plugins can create, inspect and edit the same camera paths that are available in the Open Brush UI. This is useful for procedural camera moves, drawing along paths and automated rendering.

This page introduces the main objects and workflows. The generated [Plugin API Scripting Reference](https://icosa.gitbook.io/open-brush-plugin-scripting-docs/) is the source for every property, method and parameter.

## Get the active camera path

Camera paths are available through `Sketch.cameraPaths`:

```lua
local cameraPath = Sketch.cameraPaths.active

if cameraPath == nil and Sketch.cameraPaths.count > 0 then
    cameraPath = Sketch.cameraPaths.last
end
```

A camera path exposes `positionKnots`, `rotationKnots`, `speedKnots`, `fovKnots` and a combined `knots` list.

## Sample a path

`Sample` returns the camera transform at a time along the path. `SampleFull` also returns the interpolated speed, field of view and position along the path:

```lua
local sample = cameraPath:SampleFull(2.5, true, false)

local position = sample.position
local rotation = sample.rotation
local speed = sample.speed
local fieldOfView = sample.fov
local pathRatio = sample.pathRatio
```

The second argument controls looping. The third enables ping-pong playback, which reverses direction on alternating loops.

## Create a camera path from a Path

If a plugin has already created a `Path`, convert it to a camera path:

```lua
local cameraPath = CameraPath:FromPath(path, false)
```

Use `CameraPath:FromPathWithRotations(path, false)` to create rotation knots from the rotations stored on the path points. The Boolean argument controls whether the result loops.

You can convert a camera path back to a regularly sampled `Path`:

```lua
local path = cameraPath:AsPath(0.1)
```

## Edit knots

Camera-path methods can extend or loop the path and insert position, rotation, speed or FOV knots. You can also edit knot properties directly:

```lua
if cameraPath.speedKnots.count > 0 then
    local speedKnot = cameraPath.speedKnots[0]
    speedKnot.speed = 2.0
end

if cameraPath.fovKnots.count > 0 then
    local fovKnot = cameraPath.fovKnots[0]
    fovKnot.fov = 60
end
```

Speed values use world-space units and FOV values use degrees. Changing a non-position knot's `pathT` moves it along the path and automatically restores the correct knot order.

## Draw or render a path

Draw along a camera path with the current brush:

```lua
local strokes = cameraPath:Draw(0.1)
```

Or supply explicit brush settings:

```lua
local strokes = cameraPath:DrawWithBrush(
    0.1,
    "Ink",
    0.05,
    Color.red,
    0.1
)
```

Use `CameraPath:PreviewActivePath(true)` to preview the active path and `CameraPath:RenderActivePath()` to render it using the current video settings.
