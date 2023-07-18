# Writing Plugins

Plugins are written in the scripting language [Lua](https://www.lua.org) which is designed to be simple to learn and easy to understand. There's plenty of tutorials online and Lua is widely used in games and applications such as [Factorio](https://wiki.factorio.com/Tutorial:Scripting), [Garry's Mod](https://wiki.facepunch.com/gmod/Beginner\_Tutorial\_Intro)_,_ [Roblox](https://create.roblox.com/docs/tutorials/scripting/basic-scripting/intro-to-scripting), [LÖVR](https://lovr.org/) and many others.

If you've written scripts in any other language then you'll find it easy to pick up.&#x20;

If you've never programmed at all then Lua is a great place to start. Copy an example script to your Open Brush folder (there's a button next to each Plugin type that does this for you), open it up in a text editor and try changing things.

As soon as you save your changes, Open Brush will load the new version. If you've made a mistake then the console on the back of your brush hand will tell you what line the error is on.

## Libraries

In addition to the API commands you can use most of the [Lua Standard Library](https://www.moonsharp.org/MoonSharpStdLib.pdf) also.&#x20;

Another available library is [Lume](https://github.com/rxi/lume)

## Plugin Types

The type of script is determined by the filename prefix. Script types are as follows:

#### Pointer Scripts

Pointer Scripts can modify the pointer position and/or rotation every frame. You have acceess to the current position and rotation so you can simply add an offset - or you could create an entirely new position or rotation based on any of the other context variables that are available to the script.

Name a Pointer Script with the prefix "PointerScript". For example: _PointerScript.Wiggle.lua_

A Pointer Script should return x, y, z for pointer rotation and x, y, z for pointer rotation.

For example:

```lua
function WhileTriggerPressed()
    speed = 5
    radius = 0.25
    angle = App.time * speed
    r = Brush.pressure * radius;
    pos = Vector3:New(Math:Sin(angle) * r, Math:Cos(angle) * r, 0)
    return Transform:New(pos)
end

```

#### Tool Scripts

Tool Scripts are run when you release the trigger and they have access to the position and rotation of the controller when the trigger was first pressed as well as the position and rotation of the controller when the trigger is released.&#x20;

Name a Tool Script with the prefix "ToolScript". For example: _ToolScript.Circle.lua_

Tool Scripts should return a list of points (and optionally rotations) that define a brush stroke.

For example:

```lua
function WhileTriggerPressed()
    speed = 16
    radius = 1
    angle = App.time * speed
    r = 0
    if (Brush.triggerIsPressed) then
        r = radius * Brush.timeSincePressed
    end
    pos = Vector3:New(Math:Sin(angle) * r, Math:Cos(angle) * r, 0)
    return Transform:New(pos)
end
```

#### Symmetry Scripts

Symmetry Scripts should return a list of positions and/or rotations that represent additional pointers that will create their own strokes as the user draws with the primary pointer.

The number of pointers should not change once a brush stroke has begun, but may change between each brush stroke.

Name a Symmetry Script with the prefix "SymmetryScript". For example SymmetryScript.FourCopies.lua

Symmetry Scripts should return a list of positions (and optionally rotations) for each additional pointer.

For example:

```lua
function Main()
    copies = 12
    pointers = Path:New()
    theta = 360.0 / copies
    for i = 1, copies - 1 do
        pointer = Transform:New(
            Symmetry.brushOffset,
            Rotation:New(0, i * theta, 0)
        )
        pointers.Insert(pointer)
    end
    return pointers
end
```

Note the use of S`ymmetry.brushOffset` instead of the usual `Brush.position`. This is because by default, symmetry scripts use coordinates centered on the symmetry widget and you'd have to do a some complicated calculations to get from there to the current brush position. If you use `symmetry.brushOffset` this is done for you.

#### Background Scripts

Background Scripts run constantly. They are useful for animating layers or continually generating new shapes. You can still check for user actions such as pressing the trigger and change the action accordingly. They are very versatile but because the run all the time, they can affect performance if you're not careful. Always use one of the other script types in preference if it is suitable.&#x20;

```lua
function Main()
    x = Math:Lerp(0, 1, App.time % 1)
    Sketch.layers[1].position = Vector3:New(x, 0, 0)
end
```

### Built-in functions and properties

The following realtime values from the sketch are examples of values available to use in your scripts.&#x20;

Here are some common properties. You can also see a [full list of methods and properties for each type.](../plugin-api-scripting-reference/)

* **Brush.position:** \
  The current position of the brush pointer relative to the canvas
* **Brush.rotation:** \
  The current orientation of the brush pointer relative to the canvas
* **Brush.colorRgb:** \
  The current brush color
* **Brush.colorHsv:** \
  The current brush colour converted to HSV
* **Brush.size:** \
  The current brush size
* **Brush.pressure:** \
  The current pressure of the brush pointer (how hard the trigger is being pressed)
* **Brush.type:** \
  The current brush name
* **App.time:** \
  The time in seconds since Open Brush was launched
* **App.currentScale:** \
  The current scale of the canvas
* **Sketch.strokes**\
  A list of strokes in the current sketch

### Script Parameters

Scripts can specify parameters that appear as UI widgets such as sliders. These appear in a popup when you click the "3 dots" button on the right of each row.  For example you might want a script to have sliders to control "speed" or "wigglyness".

You define the widgets for each parameter in your script. Here's an example:

```lua
Parameters = {
    speed={label="Speed", type="float", min=0.01, max=32, default=16},
    radius={label="Radius", type="float", min=0.01, max=5, default=1},
}

function Main()
    angle = App.time * speed
    r = Brush.pressure * radius;
    pos = Vector3:New(Math.Sin(angle) * r, Math:Cos(angle) * r, 0)
    return Transform:New(pos)
end
```

Here we have defined two widgets. Both are floats (rather than integers) and we have defined a minimum, a maximum and a default value. You can set the ltext abel that appears when you hover over each slider.

The name of each widget (here "speed" and "radius") are then available to the script as variables.

### Coordinate Spaces

By default each script type works relative to an origin and has a rotation that makes sense for each of the three types. Pointer and Tool Scripts are relative to the user's brush hand and Symmetry Scripts are relative to the Symmetry Widget.

You can override this. For example, here's a PointerScript that is relative to the canvas. We can then position the pointer so it is always at y=0 (the floor) but still tracks the pointer in the x and z directions:

```lua
Settings = {space="canvas"}

function Main()
    return Transform:New(
        Vector3:New(Brush.position.x, 0, Brush.position.z)
    )
end
```

Note that we have to manually specific pointer.position.x and pointer.position.y. If we were using space="pointer" (the default) then we wouldn't need to as coordinates are automatically relative to pointer.position

Valid spaces are currently "pointer" or "canvas".

