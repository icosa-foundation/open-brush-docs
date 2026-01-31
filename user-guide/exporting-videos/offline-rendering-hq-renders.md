---
description: Re-render recorded videos via .bat files or the command line.
---

# Offline rendering (HQ renders)

Offline rendering lets you re-render a recorded camera move. You can output higher resolution and/or higher FPS.

It works by saving the camera motion to a USD file. Then Open Brush can replay that motion later.

### Enable camera path saving

Set `"SaveCameraPath": true` in your config. See [The Open Brush config file](../the-open-brush-config-file.md).

### What files you get

When you record a video with `SaveCameraPath` enabled, Open Brush writes extra files. On Windows, you’ll see a batch file next to the video in `Documents\Open Brush\Videos`.

Example:

```
Untitled_13_00.mp4
Untitled_13_00.HQ_Render.bat
```

### Re-render using the Windows .bat

Double-click the `.bat`. Pick an option from the menu.

![](<../../.gitbook/assets/image-125.png>)

Open Brush will:

1. Launch
2. Load your sketch
3. Render the video
4. Exit

Higher quality settings can make the framerate choppy. Don’t wear the headset during the render.

#### “No Quick Load” option

The “No Quick Load” option forces a full load. Use it when your render finishes before the sketch fully loads.

### Render a saved camera path from the command line

The camera path is saved in ASCII USD (`.usda`). If you have other USD tools, you may be able to edit it.

To render directly:

```
Openbrush.exe --renderCameraPath <path/to/camerapath.usda> <path/to/sketchfile.tilt>
```

### Video camera paths vs Camera Paths tools

These are different concepts:

* **Camera Paths tools** create a path that Open Brush records.
* **Video camera paths** are the saved motion data used for offline re-rendering.

The saved `.usda` path can be combined with USD exports. That can recreate camera motion in other pipelines.
