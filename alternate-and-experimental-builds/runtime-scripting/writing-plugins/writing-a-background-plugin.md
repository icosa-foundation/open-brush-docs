# Writing a Background Plugin

Background Plugins run all the time when activated. They are useful for animating layers or continually generating new shapes. You can still check for user actions such as pressing the trigger and change the action accordingly. They are very versatile but because the run all the time, they can affect performance if you're not careful. Always use one of the other script types in preference if it is suitable.&#x20;

```lua
function Main()
    x = Math:Lerp(0, 1, App.time % 1)
    Sketch.layers[1].position = Vector3:New(x, 0, 0)
end
```
