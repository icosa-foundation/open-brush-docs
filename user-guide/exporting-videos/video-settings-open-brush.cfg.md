---
description: FPS, resolution, encoder, watermark, and capture flags.
---

# Video settings (Open Brush.cfg)

Several capture and render settings live in the config file. See [The Open Brush config file](../the-open-brush-config-file.md) for location and format rules.

### Video-related fields

This is an example snippet showing the fields that affect capture and rendering:

```json
{
  "Video": {
    "Resolution": 1920,
    "OfflineResolution": 1920,
    "FPS": 30,
    "OfflineFPS": 30,
    "ContainerType": "mp4",
    "CameraSmoothing": 0.98,
    "Encoder": "h.264",
    "SaveCameraPath": true,
    "FOV": 129
  },
  "Flags": {
    "PostEffectsOnCapture": true,
    "ShowWatermark": false,
    "ShowHeadset": false,
    "ShowControllers": true,
    "DisableAudio": false
  }
}
```

### FPS and performance

FPS affects memory use. Each frame must be rendered and encoded.

Live recording is heavier than it looks. VR already renders twice (one per eye). Recording adds another render/encode pass.

If you run out of memory, VR can stutter. Stutter can quickly cause VR sickness.

### When to use offline rendering

Offline rendering is best for:

* Higher resolution output
* Higher FPS output
* More stable output on complex sketches

See [Offline rendering (HQ renders)](offline-rendering-hq-renders.md) for the workflow.
