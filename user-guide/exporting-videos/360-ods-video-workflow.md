---
description: Render stereoscopic 360 videos and inject metadata for YouTube.
---

# 360° / ODS video workflow

Open Brush can render ODS (stereoscopic 360) videos via offline rendering. This is a PC workflow.

You’ll typically:

1. Record a camera move with `SaveCameraPath` enabled.
2. Re-render offline at high quality.
3. Inject 360 metadata for YouTube.

### Fix clipping by changing eyeScale

On ODS renders, you may see:

* Missing floor
* Geometry clipping

This often happens when the scene is scaled down. Objects end up too close to the camera for ODS.

Open the saved `.usda` camera path in a text editor. Look for:

```
uniform float eyeScale = 1
```

Try:

```
uniform float eyeScale = 0.1
```

{% hint style="info" %}
Reducing `eyeScale` also reduces stereo strength. Scaling your scene is often better for stereo.
{% endhint %}

### Inject 360 metadata

YouTube needs metadata to recognize 360 and stereo layout.

1. Download the 360° Video Metadata tool:
   * [Mac](https://github.com/google/spatial-media/releases/download/v2.0/360.Video.Metadata.Tool.mac.zip)
   * [Windows](https://github.com/google/spatial-media/releases/tag/v2.0)
2. Unzip it.
3. Launch the app.
   * On macOS you may need right-click → **Open**.
4. Select your rendered video.
5. Check **My Video is stereoscopic 3D (top/bottom layout)**.
6. Click **Inject Metadata**.
7. Save the new file.

### Upload to YouTube

Upload the “injected” file. YouTube takes extra time to process 360 video.

Until processing finishes, you may see the raw over/under output. After processing, YouTube will show the 360 viewer.
