# Writing a Tool Plugin

Tool Plugins run when you release the trigger and they have access to the position and rotation of the controller when the trigger was first pressed as well as the position and rotation of the controller when the trigger is released.&#x20;

Name a Tool Script with the prefix "ToolScript". For example: _ToolScript.Circle.lua_

Tool Scripts should return a list of points (and optionally rotations) that define a brush stroke.

For example:

```lua
function Main()
    if Brush.triggerReleasedThisFrame then
        points = Path:New()
        for angle = 0, 360, 10 do
            position2d = Vector2:PointOnCircle(angle)
            rotation = Rotation:New(0, 0, angle * 180)
            points:Insert(Transform:New(position2d:OnZ(), rotation))
        end
        return points
    end
end
```
