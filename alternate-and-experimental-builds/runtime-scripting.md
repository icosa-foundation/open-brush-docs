# Feature: Plugin Scripting

#### Status: Mostly working. Missing features and probably buggy in places.

{% embed url="https://youtu.be/z3lb7pjlP9o" %}

## Download

* [Oculus Quest](https://nightly.link/IxxyXR/open-brush/workflows/build/experiments%2Fmoonsharp/Oculus%20Quest.zip)
* [Oculus PC VR ](https://nightly.link/IxxyXR/open-brush/workflows/build/experiments%2Fmoonsharp/Windows%20Rift.zip)(Rift, Quest via Link cable...)
* [SteamVR ](https://nightly.link/IxxyXR/open-brush/workflows/build/experiments%2Fmoonsharp/Windows%20OpenXR.zip)(Vive, Index, Reverb...)
* [Other Builds](https://nightly.link/IxxyXR/open-brush/workflows/build/experiments%2Fmoonsharp) (Pico, Pimax etc)
* [Code](https://github.com/IxxyXR/open-brush/tree/experiments/moonsharp)

### What does it do?

Unlike the existing [OpenBrush API](../user-guide/open-brush-api/), plugin scripting is designed to run small scripts that directly modify the behaviour of various features while you are actually using them. For example a script might move the pointer as you are painting or add new strokes in response to your actions.

### What's it good for?

Changing the way Open Brush responds to user actions. Adding new mirror modes or creating a new custom brush tool.

### How do I install it?

[Download](runtime-scripting.md#download) a build for your headset from the link above and unzip it. You can run the Windows exe directly. To install the Quest apk use SideQuest: [https://uploadvr.com/sideloading-quest-how-to/](https://uploadvr.com/sideloading-quest-how-to/)

### How do I use it?

![](<../.gitbook/assets/image (1).png>)

There are new buttons on the scipts panel that allow you to set an active runtime script in one of four categories. From the top down: [Tool Scripts](runtime-scripting.md#tool-scripts), [Symmetry Scripts](runtime-scripting.md#symmetry-scripts), [Pointer Scripts](runtime-scripting.md#pointer-scripts) and [Background Scripts](runtime-scripting.md#background-scripts). For the first three categories you can use the arrow buttons to choose a script and activate it with the large button on the left of each row.

Background Scripts are a bit different as you can have several active at once. The big button enables/disables all of them and the smaller "eye" button turns the currently selected script on or off.

### How do I write my own plugin scripts?

Note that this is in the early stage of development and I'm still changing my mind about many parts

All scripts are written in [Lua](https://www.lua.org/) (this is different to the [Http Api](../user-guide/open-brush-api/) where you can use any language as commands are simply messages sent over Http)

The best reference is probably the [examples scripts themselves](https://github.com/IxxyXR/open-brush/tree/experiments/moonsharp/Assets/Resources/LuaScriptExamples). Most API commands are listed in the [Lua Autocomplete File](https://github.com/IxxyXR/open-brush/blob/experiments/moonsharp/Assets/Resources/LuaScriptExamples/\_\_autocomplete.lua) (which you can copy to your scripts folder and many code editors will automatically use it to give you some level of autocomplete).

In addition to the commands and properties listed in the autocomplete file, you can use most of the [Lua Standard Library](https://www.moonsharp.org/MoonSharpStdLib.pdf) also.

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
    angle = app.time * speed
    r = brush.pressure * radius;
    pos = {math.sin(angle) * r, math.cos(angle) * r, 0}
    rot = {0, 0, 0}
    return {pos, rot}
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
    angle = app.time * speed
    r = 0
    if (brush.triggerIsPressed) then
        r = radius * brush.timeSincePressed
    end
    pos = {math.sin(angle) * r, math.cos(angle) * r, 0}
    rot = {0, 0, 0}
    return {pos, rot}
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
    pointers = {}
    theta = 360.0 / copies
    for i = 1, copies - 1 do
        table.insert(pointers, {position=symmetry.brushOffset, rotation={0, i * theta, 0}})
    end
    return pointers
end
```

Note the use of `symmetry.brushOffset` instead of the usual `brush.position`. This is because by default, symmetry scripts use coordinates centered on the symmetry widget and you'd have to do a some complicated calculations to get from there to the current brush position. If you use `symmetry.brushOffset` this is done for you.

#### Background Scripts

Background Scripts run constantly. They are useful for animating layers or continually generating new shapes. You can still check for user actions such as pressing the trigger and change the action accordingly. They are very versatile but because the run all the time, they can affect performance if you're not careful. Always use one of the other script types in preference if it is suitable.&#x20;

```lua
function Main()
    --Layers are numbered from 0 so 1 is the second layer
    layerNumber = 1
    position = {
        x = unityMathf.lerp(0, 1, app.time % 1),
        y = 0,
        z = 0
    }
    rotation = {0, 0, 0}
    layers.setPosition(layerNumber, position)
end
```

### Built-in functions and properties

The following realtime values from the sketch are examples of values available to use in your scripts. As the API is changing frequently at the moment this list is incomplete. Check out Scripts\LuaModules\\\_\_autocomplete.lua for an up to date list of available functions and properties.

* **brush.position:** _{float x, float y, float z}_\
  The current position of the brush pointer relative to the canvas
* **brush.rotation:** _{float x, float y, float z}_\
  The current orientation of the brush pointer relative to the canvas
* **brush.colorRgb:** _{float r, float g, float b}_\
  The current brush color
* **brush.colorHsv:** _{float h, float s, float v}_\
  The current brush colour converted to HSV
* **brush.size:** _float_\
  The current brush size
* **brush.pressure:** _float_\
  The current pressure of the brush pointer (how hard the trigger is being pressed)
* **brush.type:** _string_\
  The current brush name
* **app.time:** _float_\
  The time in seconds since Open Brush was launched
* **app.currentScale:** _float_\
  The current scale of the canvas
* **strokes.count:** _int_\
  The total number of strokes

### Script Parameters

Scripts can specify parameters that appear as UI widgets such as sliders. These appear in a popup when you click the "3 dots" button on the right of each row.  For example you might want a script to have sliders to control "speed" or "wigglyness".

You define the widgets for each parameter in your script. Here's an example:

```lua
Parameters = {
    speed={label="Speed", type="float", min=0.01, max=32, default=16},
    radius={label="Radius", type="float", min=0.01, max=5, default=1},
}

function Main()
    angle = app.time * speed
    r = pointer.pressure * radius;
    pos = {math.sin(angle) * r, math.cos(angle) * r, 0}
    rot = {0, 0, 0}
    return {pos, rot}
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
    return {
        {pointer.position.x, 0, pointer.position.z}
    };
end
```

Note that we have to manually specific pointer.position.x and pointer.position.y. If we were using space="pointer" (the default) then we wouldn't need to as coordinates are automatically relative to pointer.position

Valid spaces are currently "pointer" or "canvas".

### Known Issues

There's lots more I want to do with this including scripted jitter and scripted geometry creation.

## How do I get help

Come over to the [Open Brush Discord](https://discord.com/invite/fS69VdFXpk) and chat to me ( @andybak#5425 ). I'm on UK time but I check in fairly regularly.

### Can I see it in action?

{% embed url="https://www.youtube.com/watch?v=7YxjNvCY8ak" %}
