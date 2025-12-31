---
description: Current limitations and the best workarounds.
---

# Quest and other standalone headsets

{% hint style="info" %}
Standalone headsets (Quest, etc.) can’t currently export video directly inside Open Brush. The workaround depends on what you’re trying to record.
{% endhint %}

### Option 1: Render frames on Quest, then compile

This option shipped near the end of 2025.

You can render camera paths directly on Quest. The output is a folder of frames.

You then compile frames into a video. We generate a helper script for [ffmpeg](https://ffmpeg.org/).

### Option 2: Draw the camera path on Quest, render on a computer

Quest builds have the Camera Paths tool. The **record** button is disabled.

But paths are saved with the sketch. Copy the sketch to a PC or Mac and render there.

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
