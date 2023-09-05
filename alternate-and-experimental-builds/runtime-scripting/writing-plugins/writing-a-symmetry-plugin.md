# Writing a Symmetry Plugin

Symmetry Plugins should return a list of positions and/or rotations that represent additional pointers that will create their own strokes as the user draws with the primary pointer.

The number of pointers should not change once a brush stroke has begun, but may change between each brush stroke.

Name a Symmetry Script with the prefix "SymmetryScript". For example SymmetryScript.FourCopies.lua

Symmetry Scripts should return a list of positions (and optionally rotations) for each additional pointer.

For example:

```lua
function Main()
    pointers = Path:New()
    theta = 360.0 / copies
    for i = 0, copies - 1 do
        angle = i * theta
        pointer = Transform:New(Symmetry.brushOffset, Rotation:New(0, angle, 0))
        pointers:Insert(pointer)
    end
    return pointers
end
```

Note the use of`Symmetry.brushOffset` instead of the usual `Brush.position`. This is because by default, symmetry scripts use coordinates centered on the symmetry widget and you'd have to do a some complicated calculations to get from there to the current brush position. If you use `symmetry.brushOffset` this is done for you.
