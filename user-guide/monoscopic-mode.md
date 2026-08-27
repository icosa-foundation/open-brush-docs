# Monoscopic Mode

Monoscopic mode runs the painting interface without a VR headset. It is intended for specialist workflows that need access to tools and panels; use View-only mode if you only want to explore sketches.

Unlike [View-only Mode](view-only-mode.md), Monoscopic mode retains the painting and editing tools. Enabling it also disables XR.

<figure><img src="../.gitbook/assets/image-077.png" alt=""><figcaption></figcaption></figure>

It can be used with the [HTTP API](open-brush-api/) and [Plugins](using-plugins/) to control Open Brush from scripts or a web browser. Open [http://localhost:40074/examplescripts/remotecontrol.html](http://localhost:40074/examplescripts/remotecontrol.html) while Open Brush is running to use the included browser-based remote control.

## Activating Monoscopic Mode

You can access Monoscopic mode by adding a "EnableMonoscopicMode" entry to your [Open Brush config file](the-open-brush-config-file.md) in the "Flags" section and setting it to true. For example:

```json
{
  "Flags": {
    "EnableMonoscopicMode": true
  }
}
```

You can return to normal either by removing the entry or by setting it to false.

## Controlling Monoscopic Mode

1. Alt+mousing will rotate your viewpoint.
2. Panels become focused when roughly centered in your view. Your cursor is then locked to the panel boundary making it easier to click the buttons.
3. Dragging with the right button down will bring the drawing plane nearer or further.
4. Ctrl+mouse drag will rotate the drawing plane
5. Clicking in the game window will capture your mouse cursor. Escape will return full control (so you can interact with Unity etc)
6. In most cases you can alt+mouse to left or right to view the tool panels and choose tools/brushes with the mouse.
7. Rotating with “Alt” whilst pressing shift will allow you to move the panel you were currently focused on.
8. Sometimes panels appear in weird places. Try looking behind you or down at your feet.

## Other Keyboard Shortcuts

{% hint style="info" %}
The file Scripts/InputManager.cs lists all the keyboard controls. Also see [Open Brush: Keyboard Controls and VR Input](https://docs.google.com/spreadsheets/d/1D7vIerfSz1vtyDS_dPdvHiANluEr60VFrxhzE7ZbfAU) However many aren’t relevant, aren’t implemented or only apply in particular modes. The more useful ones are listed below.
{% endhint %}

| **Action**          | **Shortcut** | **Notes**                                                                                   |
| ------------------- | ------------ | ------------------------------------------------------------------------------------------- |
|                     |              |                                                                                             |
| LockToHead          | LeftShift    | Use with Alt. Can move panels with this.                                                    |
| PivotRotation       | LeftControl  | Use with Alt                                                                                |
| Scale               | Tab          | Only when not drawing. Hold tab and move mouse up or down to scale tool                     |
| Reset               | Space        | Resets the UI not the sketch                                                                |
| Undo                | Z            |                                                                                             |
| Redo                | X            |                                                                                             |
| SaveNew             | S            |                                                                                             |
| ViewOnly            | H            | Doesn't disable drawing. Just hidesUI                                                       |
| PreviousTool        | LeftArrow    | 5 tools are available: sketch surface, brush selection, color selection, BrushNColor, Erase |
| NextTool            | RightArrow   |                                                                                             |
| CycleSymmetryMode   | F2           |                                                                                             |
| Export              | E            |                                                                                             |
| StoreHeadTransform  | O            | Use with Right Shift                                                                        |
| RecallHeadTransform | O            | (without Right Shift)                                                                       |
| ResetScene          | Return       | Doesn't delete sketch                                                                       |
| StraightEdge        | CapsLock     | Buggy                                                                                       |
| Save                | S            |                                                                                             |
| PositionMonoCamera  | Alt          |                                                                                             |
