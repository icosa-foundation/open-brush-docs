# Writing a Pointer Plugin

Pointer Plugins can modify the pointer position and/or rotation every frame. You have acceess to the current position and rotation so you can simply add an offset - or you could create an entirely new position or rotation based on any of the other context variables that are available to the script.

Name a Pointer Script with the prefix "PointerScript". For example: _PointerScript.Wiggle.lua_

A Pointer Script should return x, y, z for pointer rotation and x, y, z for pointer rotation.

For example:

```lua
function Main()
    if Brush.triggerIsPressed then
        speed = 5
        angle = App.time * speed
        radius = Brush.pressure * 0.25;
        pos = Vector3:New(Math:Sin(angle) * r, Math:Cos(angle) * radius, 0)
        return Transform:New(pos)
    end
end
```
