# Feature: Runtime Scripting

#### Status: Pointer and Tool Scripts mostly work. Symmetry Scripts are currently broken. Need lots more examples and better docs.

{% embed url="https://youtu.be/z3lb7pjlP9o" %}

## Download

* [Oculus Quest](https://nightly.link/IxxyXR/open-brush/workflows/build/experiments%2Fmoonsharp/Oculus%20Quest.zip)
* [Oculus PC VR ](https://nightly.link/IxxyXR/open-brush/workflows/build/experiments%2Fmoonsharp/Windows%20Rift.zip)(Rift, Quest via Link cable...)
* [SteamVR ](https://nightly.link/IxxyXR/open-brush/workflows/build/experiments%2Fmoonsharp/Windows%20OpenXR.zip)(Vive, Index, Reverb...)
* [Other Builds](https://nightly.link/IxxyXR/open-brush/workflows/build/experiments%2Fmoonsharp) (Pico, Pimax etc)
* [Code](https://github.com/IxxyXR/open-brush/tree/features/moonsharp)

### What does it do?

Unlike the existing [OpenBrush API](../user-guide/open-brush-api/), runtime scripting is designed to run small scripts that directly modify the behaviour of various features while you are actually using them. For example a script might move the pointer as you are painting or add new strokes in response to your actions.

### What's it good for?

Changing the way Open Brush responds to user actions. Adding new mirror modes or creating a new custom brush tool.

### How do I install it?

Download a build for your headset from the link above and unzip it. You can run the Windows exe directly. To install the Quest apk use SideQuest: [https://uploadvr.com/sideloading-quest-how-to/](https://uploadvr.com/sideloading-quest-how-to/)

### How do I use it?

![](<../.gitbook/assets/image (2).png>)

There are new buttons on the scipts panel that allow you to set an active runtime script in (currently) one of three categories: Tool Scripts, Symmetry Scripts and Pointer Scripts. Use the arrow buttons to choose a script and activate it with the large button on the left of each row.

All scripts are written in [Lua ](https://www.lua.org/)and the type of script is determined by the filename prefix. Script types are as follows:

#### Pointer Scripts

Pointer Scripts can modify the pointer position and/or rotation every frame. You have acceess to the current position and rotation so you can simply add an offset - or you could create an entirely new position or rotation based on any of the other context variables that are available to the script.

Name a Pointer Script with the prefix "PointerScript". For example: _PointerScript.Wiggle.lua_

A Pointer Script should return x, y, z for pointer rotation and x, y, z for pointer rotation.

For example:

```lua
function Main()
    angle = app.time * 16
    radius = pointer.pressure
    pos = {math.sin(angle) * radius, math.cos(angle) * radius, 0}
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
function Main()
    points = {}
    for i = 0, 360, 10 do
        angle = i * math.pi / 180
        pos = {math.cos(angle), math.sin(angle), 0}
        rot = { 0, 0, angle * 180 }
        table.insert(points, {pos, rot})
    end
    return points
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
    return {
        {position={-1, 0, 0}, rotation={0, 0, 0}},
        {position={1, 0, 0}, rotation={0, 0, 0}},
        {position={0, -1, 0}, rotation={0, 0, 0}},
        {position={0, 1, 0}, rotation={0, 0, 0}},
        {position={0, 0, -1}, rotation={0, 0, 0}},
        {position={0, 0, 1}, rotation={0, 0, 0}}
    }
end
```

### Context Variables

The following values from the sketch are available to use in your scripts:

* **pointer.position:** _{float x, float y, float z}_\
  ****The current position of the pointer relative to the canvas
* **pointer.rotation:** _{float x, float y, float z}_\
  ****The current orientation of the pointer relative to the canvas
* **pointer.rgb:** _{float r, float g, float b}_\
  ****The current brush color
* **pointer.hsv:** _{float h, float s, float v}_\
  __The current brush colour converted to HSV
* **pointer.size:** _float_\
  __The current brush size
* **pointer.size01:** _float_\
  __The current brush size normalized to lie in the range 0 to 1
* **pointer.pressure:** _float_\
  _The current pressure of the pointer (how hard the trigger is being pressed)_
* **pointer.brush:** _string_\
  __The current brush name
* **app.time:** _float_\
  __The time in seconds since Open Brush was launched
* **canvas.scale:** _float_\
  __The current scale of the canvas
* **canvas.strokeCount:** _int_\
  __The total number of strokes

### Script Widgets

Scripts can specify parameters that appear as UI widgets such as sliders. These appear in a popup when you click the "3 dots" button on the right of each row.  For example you might want a script to have sliders to control "speed" or "wigglyness".

You define the widgets for each parameter in your script. Here's an example:

```lua
Widgets = {
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

By default each script type works relative to an origin and has a rotation that makes sense for each of the three types. Pointer and Tool Scripts are relative to the user's brush hand and Symmetry Scripts are relative to the Mirror Widget.

You can override this. For example, here's a PointerScript that is relative to the canvas. We can then position the pointer so it is always at y=0 (the floor) but still tracks the pointer in the x and z directions:

```lua
Settings = {
    space="canvas"
}

function Main()
    return {
        {pointer.position.x, 0, pointer.position.z}
    };
end
```

Note that we have to manually specific pointer.position.x and pointer.position.y. If we were using space="pointer" (the default) then we wouldn't need to as coordinates are automatically relative to pointer.position

Valid spaces are "pointer", "canvas" and "widget" (the mirror widget)

### Known Issues

Symmetry scripts are currently broken. There's probably tons of other bugs waiting to be discovered.

There's lots more I want to do with this including scripted jitter and scripted geometry creation.

## How do I get help

Come over to the [Open Brush Discord](https://discord.com/invite/fS69VdFXpk) and chat to me ( @andybak#5425 ). I'm on UK time but I check in fairly regularly.

### Can I see it in action?

I need to make some better videos but here's
