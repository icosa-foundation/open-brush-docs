# Using Open Brush without a VR headset

{% hint style="info" %}
This page has been update to reflect changes in the current [beta version](../alternate-and-experimental-builds/open-brush-beta-docs.md). Sketch Viewer mode is a new feature and Monoscopic Mode was previously only available as a separate download.
{% endhint %}

## Sketch Viewer Mode

<figure><img src="../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

If you launch Open Brush without a headset attached (platforms where we don't currently have VR support), the app will start in "Sketch Viewer Mode" where you can load any of the available sketches and navigate around with the keyboard and mouse or the touchscreen.

* Use the mouse or touch to look around
* Press I to invert up/down
* W,A,S,D: move forward/back/left/right
* Q,E: move up/down
* Hold shift to move faster

On touchscreen devices there are onscreen buttons to emulate W, A, S and D.

If you do have a VR headset attached you can still access Sketch Viewer Mode by adding a "DisableXrMode" entry to your [Open Brush config file](the-open-brush-config-file.md) in the "Flags" section and setting it to true. For example:

```json
{
  "Flags": {
    "DisableXrMode": true
  }
}
```

You can return to normal either by removing the entry or by setting it to false.

## Monoscopic Mode

Open Brush has got a secret mode where it can be used without a VR headset - and even works on Mac! This mode was never released to the public and is clunky in places.

It also works very nicely when using Open Brush via the [API](open-brush-api/) allowing you to control Open Brush from a web browser.

## Activating Monoscopic mode

You can access Monoscopic mode by adding a "EnableMonoscopicMode" entry to your [Open Brush config file](the-open-brush-config-file.md) in the "Flags" section and setting it to true. For example:

```json
{
  "Flags": {
    "EnableMonoscopicMode": true
  }
}
```

You can return to normal either by removing the entry or by setting it to false.

## Controlling Monoscopic mode

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
The file Scripts/InputManager.cs lists all the keyboard controls. Also see [Open Brush: Keyboard Controls and VR Input](https://docs.google.com/spreadsheets/d/1D7vIerfSz1vtyDS\_dPdvHiANluEr60VFrxhzE7ZbfAU) However many aren’t relevant, aren’t implemented or only apply in particular modes. The more useful ones are listed below.
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
| ExportAll           | A            |                                                                                             |
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
