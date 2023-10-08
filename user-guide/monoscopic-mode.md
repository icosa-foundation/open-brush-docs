# Using Open Brush on PC or Mac without a VR headset: “Monoscopic mode”

Open Brush has got a secret mode where it can be used without a VR headset - and even works on Mac! This mode was never released to the public and is clunky in places.

@rapka is currently working on some major enhancements which will hopefully make this mode more generally useful: [https://github.com/rapka/open-brush/tree/monoscopic-controls](https://github.com/rapka/open-brush/tree/monoscopic-controls)

It also works very nicely when using Open Brush via the [experimental API](open-brush-api/) allowing you to control Open Brush from a browser and create procedural designs using simple javascript.

## Getting the Monoscopic version of Open Brush

We don't currently publish the monoscopic version alongside other releases but our automated build system always creates them every time we build a new testing version.

(Note that you'll need to be logged in to Github to download files)

1. Go to this page: [https://github.com/icosa-foundation/open-brush/actions](https://github.com/icosa-foundation/open-brush/actions) and look through the list of builds until you see one with "main" in the middle column:

![](<../.gitbook/assets/image (7) (2).png>)

2\. Once you've found one then click on the first column ("Builds" in this case but that might differ) and you'll see something similar to this:

![](<../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1).png>)

3\. The number underneath "Artifacts" on the right takes you to the list of downloads at the bottom of the page:

![](<../.gitbook/assets/image (2) (1) (1) (1).png>)

4\. Assuming you're logged in, the text on the left of any of the rows will start a download. In this case you want one with "Monoscopic" in the name - for example "Windows Monoscopic Experimental"

5\. When the download is complete unzip it and look for an executable file. There will probably be two executables one folder deep. One will be called "UnityCrashHandler64" - **you want the other one!**

## Controlling Monoscopic mode

1. Alt+mousing will rotate your viewpoint.
2. Panels become focussed when roughly centered to the viewport. Your cursor is then locked to the panel boundary making it easier to click the buttons.
3. Dragging with the right button down will bring the drawing plane nearer or further.
4. Ctrl+mouse will rotate the drawing plane
5. Clicking in the game window will capture your mouse cursor. Escape will return full control (so you can interact with Unity etc)
6. In most cases you can alt+mouse to left or right to view the tool panels and choose tools/brushes with the mouse.
7. Rotating with “Alt” whilst pressing shift will allow you to move the panel you were currently focussed on.
8. Sometimes panels appear in weird places. Try looking behind you or down at your feet.

The file Scripts/InputManager.cs at line 160 lists all the keyboard controls. Also see [Open Brush: Keyboard Controls and VR Input](https://docs.google.com/spreadsheets/d/1D7vIerfSz1vtyDS\_dPdvHiANluEr60VFrxhzE7ZbfAU)

However many aren’t relevant, aren’t implemented or only apply in particular modes.

Here are the useful ones:

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
