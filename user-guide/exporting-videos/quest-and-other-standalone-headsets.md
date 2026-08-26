---
description: Current limitations and the best workarounds.
---

# Quest and other standalone headsets

{% hint style="info" %}
Standalone headsets (Quest, etc.) cannot encode a video file directly inside Open Brush. Camera Paths can instead render a numbered still-frame sequence that you compile into a video afterward.
{% endhint %}

### Option 1: Render frames on Quest, then compile

This workflow was added in Open Brush v2.13.

1. Create or select a [Camera Path](camera-paths-tool.md).
2. Select **Record Path** and wait for the camera to complete the route.
3. Open the Open Brush `Videos` directory on the headset.
4. Copy the `<recording-name>_frames` folder and the matching `<recording-name>_sequence.txt` file to a computer.
5. Open the sequence text file to see its frame rate, resolution and an example [ffmpeg](https://ffmpeg.org/) command.
6. Run that command from the frames folder, or import the numbered images into a video editor as an image sequence.

The frame sequence contains images only; it does not contain an audio track. Open Brush uses JPG frames by default. You can change the image format or force the same workflow on desktop in [Video settings](video-settings-open-brush.cfg.md#frame-sequence-rendering).

### Option 2: Draw the camera path on Quest, render on a computer

Camera paths are saved with the sketch. If you want Open Brush to create the encoded video file, copy the sketch to a PC or Mac and render it there.

The computer does **not** need VR hardware. You can run Open Brush without a headset.

#### Example script workflow

1. Launch Open Brush once on the computer.
2. Copy your sketch from the headset to `Open Brush/Sketches`.
3. Copy any referenced media (images/videos/models) to the matching Media Library folders.
4. With Open Brush running, open: [http://localhost:40074/help/](http://localhost:40074/help/)
5. Go to **Example Scripts**.
6. Open **/examplescripts/record\_camera\_path.html**.
7. Select your sketch.
8. Click **Go**.

### Option 3: Use the Quest system recorder

Record the headset view using Quest’s built-in recording.

Quality will be lower. You may want to hide UI elements. The [Open Brush API](../open-brush-api/) can help with scripted UI control.
