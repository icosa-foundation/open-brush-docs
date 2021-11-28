# Differences between Standard and Experimental Mode

#### Experimental Only Panels: <a href="_o0pvobu1sw3y" id="_o0pvobu1sw3y"></a>

* ExperimentalPanel
* BrushesPanel\_experimental

#### Code differences: <a href="_lwesmp5fivvb" id="_lwesmp5fivvb"></a>

* **BrushDescriptor.cs:**
  * m\_DescriptionExtra;
* **BrushTypeButton.cs**
  * m\_DescriptionExtra used
  * m\_ExperimentalIcon overlay
* **DropperTool.cs**
  * m\_DescriptionExtra used
* **Export.cs:**
  * wrl and stl support
  * .obj support (behind fbx flag)
* **ImportUsd.cs:**
  * USD\_SUPPORTED (still behind a flag)
* **PanelManager.cs:**
  * m\_ModeVrExperimental (handles showing/hiding experimental only panels)
  * m\_UxExploration prefab (not used)
* **ControllerConsoleScript.cs:**
  * m\_AutosaveIcon?
* **SaveLoadScript.cs:**
  * jsonData.CanvasTransformInSceneSpace (experimental Canvas Transform)
* **SketchWriter.cs**
  * m\_ReplaceBrushesOnLoad (Config.m\_BrushReplacement is currently empty so does nothing)
* **MulticamTool.cs**
  * Extra Gif presets: SlowFollow, Stationary, Wobble, Circular
* **InputManager.cs**
  * Slowfollow Smoothing keyboard shortcuts (E and R)
  * ToggleHeadStationaryOrWobble/ToggleHeadStationaryOrFollow shortcuts (Q and W)
* **DropCamWidget.cs:**
  * Handle ToggleHeadStationaryOrWobble shortcuts
* **TeleportTool.cs**
  * Jogging (needs JOGGING\_ENABLED also which isn’t)
* **ColorPickerUtils.cs**
  * Extra ColorPickerMode modes
* **App.cs**
  * Animated intro sketches
* **Config.cs**
  * More brush replacement stuff: m\_BrushReplacementMap
* **SceneScript.cs**
  * Sketch Layers (keyboard only)
* **SketchControlsScript.cs**
  * m\_HeadOffset?
  * hidePanelsDelay set to 0 instead of 1
  * GlobalCommands.StraightEdgeShape Circle, Sphere (doesn’t appear to be called from anywhere)
  * Keyboard shortcuts enabled in Experimental mode:
    * SaveNew
    * ExportAll
    * SwitchCamera
    * CycleCanvas
    * ViewOnly
    * ToggleScreenMirroring
    * PreviousTool
    * NextTool
    * CycleSymmetryMode
    * Export
    * StoreHeadTransform
    * RecallHeadTransform
    * ToggleLightType
    * TossWidget
    * Reset
    * ToggleProfile
