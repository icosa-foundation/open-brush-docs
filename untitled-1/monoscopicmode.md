# MonoscopicMode

Monoscopic mode is a non-VR mode that useful if you either do not have VR gear, or if you perhaps have mobile VR gear which is difficult to debug. Monoscopic apps can be built from the Build Window. They can then be launched, and a debugger attached.

**Note:** you must be using the **experimental** build for this otherwise the tool palettes won't appear and most of the keys won't work.

## Controls

* Mouse moves pointer.
  * `Alt` controls camera. Look at the brush and colour menus and release `Alt` to chose a brush or colour.
  * `Ctrl` shows the reticle, which orients the drawing plane.
  * Hold right mouse button to move cursor back and forth.
* `Space` resets the pointer.
* `Z` is undo. `X` is redo.
* `S` is save. `L` is load.

```csharp
  private static readonly KeyMap m_KeyMap = new KeyMap {
    { (int)KeyboardShortcut.LockToHead,                   new[] { KeyCode.LeftShift } },
    { (int)KeyboardShortcut.PivotRotation,                new[] { KeyCode.LeftControl } },
    { (int)KeyboardShortcut.Scale,                        new[] { KeyCode.Tab } },

    { (int)KeyboardShortcut.RewindTimeline,               new[] { KeyCode.Minus } },
    { (int)KeyboardShortcut.AdvanceTimeline,              new[] { KeyCode.Plus } },
    { (int)KeyboardShortcut.TimelineHome,                 new[] { KeyCode.Home } },
    { (int)KeyboardShortcut.TimelineEnd,                  new[] { KeyCode.End } },
    { (int)KeyboardShortcut.Reset,                        new[] { KeyCode.Space } },
    { (int)KeyboardShortcut.Undo,                         new[] { KeyCode.Z } },
    { (int)KeyboardShortcut.Redo,                         new[] { KeyCode.X } },
    { (int)KeyboardShortcut.Delete,                       new[] { KeyCode.Delete } },
    { (int)KeyboardShortcut.Abort,                        new[] { KeyCode.Escape } },

    { (int)KeyboardShortcut.SaveNew,                      new[] { KeyCode.S } },
    { (int)KeyboardShortcut.ExportAll,                    new[] { KeyCode.A } },
    { (int)KeyboardShortcut.ToggleProfile,                new[] { KeyCode.K } },
    // Context-dependent
    { (int)KeyboardShortcut.SwitchCamera,                 new[] { KeyCode.C } },
    { (int)KeyboardShortcut.CycleCanvas,                  new[] { KeyCode.C } },
    { (int)KeyboardShortcut.ViewOnly,                     new[] { KeyCode.H } },
    { (int)KeyboardShortcut.ToggleScreenMirroring,        new[] { KeyCode.M } },
    { (int)KeyboardShortcut.PreviousTool,                 new[] { KeyCode.LeftArrow } },
    { (int)KeyboardShortcut.NextTool,                     new[] { KeyCode.RightArrow } },
    { (int)KeyboardShortcut.CycleSymmetryMode,            new[] { KeyCode.F2 } },
    { (int)KeyboardShortcut.Export,                       new[] { KeyCode.E } },
    { (int)KeyboardShortcut.StoreHeadTransform,           new[] { KeyCode.O } }, // Also checks for shift
    { (int)KeyboardShortcut.RecallHeadTransform,          new[] { KeyCode.O } },
    { (int)KeyboardShortcut.ToggleLightType,              new[] { KeyCode.P } },

    { (int)KeyboardShortcut.CheckStrokes,                 new[] { KeyCode.V } },

    { (int)KeyboardShortcut.ResetScene,                   new[] { KeyCode.Return } },
    { (int)KeyboardShortcut.StraightEdge,                 new[] { KeyCode.CapsLock } },

    { (int)KeyboardShortcut.Save,                         new[] { KeyCode.S } },
    { (int)KeyboardShortcut.Load,                         new[] { KeyCode.L } },

    { (int)KeyboardShortcut.Forward,                      new[] { KeyCode.N } },
    { (int)KeyboardShortcut.Backward,                     new[] { KeyCode.M } },

    { (int)KeyboardShortcut.PositionMonoCamera,           new[] { KeyCode.LeftAlt, KeyCode.RightAlt } },

    { (int)KeyboardShortcut.ToggleHeadStationaryOrWobble, new[] { KeyCode.Q } },
    { (int)KeyboardShortcut.ToggleHeadStationaryOrFollow, new[] { KeyCode.W } },

    { (int)KeyboardShortcut.DecreaseSlowFollowSmoothing,  new[] { KeyCode.E } },
    { (int)KeyboardShortcut.IncreaseSlowFollowSmoothing,  new[] { KeyCode.R } },

    { (int)KeyboardShortcut.ToggleGVRAudio,               new[] { KeyCode.BackQuote } },

    { (int)KeyboardShortcut.TossWidget,                   new[] { KeyCode.Y } },
  };

  // Separate keymap for when demo mode is enabled.
  // Determined by DemoManager.m_Instance.DemoModeEnabled == true
  private static readonly KeyMap m_DemoKeyMap = new KeyMap {
    { (int)KeyboardShortcut.ResetEverything, new KeyCode[] { KeyCode.Delete, KeyCode.Backspace } },
    { (int)KeyboardShortcut.GotoInitialPosition, new KeyCode[] { KeyCode.P } },
    { (int)KeyboardShortcut.ExtendDemoTimer, new KeyCode[] { KeyCode.E } },
    { (int)KeyboardShortcut.InstantUpload, new KeyCode[] { KeyCode.U } },
  };
```

