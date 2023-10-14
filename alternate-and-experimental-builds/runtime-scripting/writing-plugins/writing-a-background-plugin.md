# Writing a Background Plugin

Background Plugins run all the time when activated. They are useful for animating layers or continually generating new shapes. You can still check for user actions such as pressing the trigger and change the action accordingly. They are very versatile but because they run all the time, they can affect performance if you're not careful. Always use one of the other script types in preference if it is suitable.&#x20;

Unlike other plugin types, Background Plugins don't expect you to return a value and don't do anything with it if you did. In contrast:

1. Pointer Plugins use the returned value to change the pointer position, rotation or scale.
2. Symmetry Plugins use the returned values to create multiple new pointers.
3. Tool Plugins can use the returned value as the path of a new brush stroke which is drawn immediately.

You can draw strokes in a Background Plugin but you have to do it yourself.&#x20;

```lua
function Main()
    if Brush.triggerPressedThisFrame then
        myPath = Path:New()
        position = getRandomPosition()
        myPath:Insert(Transform:New(position))
        myPath:Insert(Transform:New(position))
        myPath:Draw()
    end
end

function getRandomPosition()
    return Brush.position + Random.insideUnitSphere
end
```

There are some new things to be aware of in this:

1. We are defining our own function to generate a random position around the current brush position
2. We are using the `Random` class to generate a point that is never more than a certain distance away from the origin. We then add that to the current brush position
3. We are manually drawing the path with `myPath:Draw()`
