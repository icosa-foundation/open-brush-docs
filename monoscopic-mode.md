# Using Open Brush without a VR headset: “Monoscopic mode”



Entering play mode should now allow you to draw and control the app using the mouse and keyboard

1. Alt+mousing will rotate your viewpoint.
2. Panels become focussed when roughly centered to the viewport. Your cursor is then locked to the panel boundary making it easier to click the buttons.
3. Dragging with the right button down will bring the drawing plane nearer or further.
4. Ctrl+mouse will rotate the drawing plane
5. Clicking in the game window will capture your mouse cursor. Escape will return full control \(so you can interact with Unity etc\)
6. In most cases you can alt+mouse to left or right to view the tool panels and choose tools/brushes with the mouse.
7. Rotating with “Alt” whilst pressing shift will allow you to move the panel you were currently focussed on.
8. Sometimes panels appear in weird places. Try looking behind you or down at your feet.

The file Scripts/InputManager.cs at line 160 lists all the keyboard controls. Also see [Open Brush: Keyboard Controls and VR Input](https://docs.google.com/spreadsheets/d/1D7vIerfSz1vtyDS_dPdvHiANluEr60VFrxhzE7ZbfAU)

However many aren’t relevant, aren’t implemented or only apply in particular modes.

Here are the useful ones:

| **Action** | **Shortcut** | **Notes** |
| :--- | :--- | :--- |
|  |  |  |
| LockToHead | LeftShift | Use with Alt. Can move panels with this. |
| PivotRotation | LeftControl | Use with Alt |
| Scale | Tab | Only when not drawing. Hold tab and move mouse up or down to scale tool |
| Reset | Space | Resets the UI not the sketch |
| Undo | Z |  |
| Redo | X |  |
| SaveNew | S |  |
| ExportAll | A |  |
| ViewOnly | H | Doesn't disable drawing. Just hidesUI |
| PreviousTool | LeftArrow | 5 tools are available: sketch surface, brush selection, color selection, BrushNColor, Erase |
| NextTool | RightArrow |  |
| CycleSymmetryMode | F2 |  |
| Export | E |  |
| StoreHeadTransform | O | Use with Right Shift |
| RecallHeadTransform | O | \(without Right Shift\) |
| ResetScene | Return | Doesn't delete sketch |
| StraightEdge | CapsLock | Buggy |
| Save | S |  |
| PositionMonoCamera | Alt |  |

