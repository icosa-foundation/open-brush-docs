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
    "ForceFrameSequenceRender": false,
    "UsePngForFrameSequence": false,
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

### Offline panorama resolution

`OfflineResolution` controls the width used when rendering an offline ODS panorama. Open Brush accepts values from `640` to `8000` pixels. If the field is omitted, ODS rendering uses its existing default width of `4096` pixels.

The ODS preview mode remains at `1024` pixels and is not enlarged by this setting. An 8K render requires substantially more GPU memory and takes longer to complete than the default.

For example:

```json
{
  "Video": {
    "OfflineResolution": 8000
  }
}
```

See the [360° / ODS video workflow](360-ods-video-workflow.md) for the complete process.

### Frame-sequence rendering

Standalone builds automatically save Camera Path renders as numbered still images because they do not include a video encoder. Two `Video` settings control this workflow:

1. `ForceFrameSequenceRender` makes desktop builds write a frame sequence instead of an encoded video when set to `true`.
2. `UsePngForFrameSequence` uses lossless PNG frames when set to `true`. The default value, `false`, uses JPG frames and requires less storage.

Each render creates a `<recording-name>_frames` folder and a matching `<recording-name>_sequence.txt` file in the Open Brush `Videos` directory. The text file records the frame rate, resolution and an example ffmpeg command.

See [Quest and other standalone headsets](quest-and-other-standalone-headsets.md#option-1-render-frames-on-quest-then-compile) for the complete workflow.

### When to use offline rendering

Offline rendering is best for:

* Higher resolution output
* Higher FPS output
* More stable output on complex sketches

See [Offline rendering (HQ renders)](offline-rendering-hq-renders.md) for the workflow.
