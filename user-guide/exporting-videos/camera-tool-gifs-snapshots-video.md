---
description: Auto-GIF, 5-second GIF, conventional, 360° and depth snapshots, and handheld video capture.
---

# Camera tool (GIFs, snapshots, video)

Open Brush has a handheld camera tool for quick captures. You use it for GIFs, conventional or 360° snapshots, depth captures, and (on PC VR) video.

### Where captures are saved

Snapshots and depth captures are saved to:

* `Documents/Open Brush/Snapshots`

Videos and GIFs are saved to:

* `Documents/Open Brush/Videos`

### Beginner mode

In Beginner mode, the camera icon is a single-function tool. It opens camera controls on your brush controller.

The options are:

1. Auto-Gif
2. 5 Second Gif
3. Snapshot
4. 360 Snapshot
5. Depth
6. Video (not present on every platform)

You control the camera like a handheld device.

* Swipe left/right on the thumbpad to switch modes.
* Pull the trigger to capture.

#### 5 Second Gif

Hold the trigger for five seconds. You can release and pull again to stop/start on the same 5-second timeline.

#### Video

Pull the trigger to start. Pull again to stop.

This is true handheld capture. You control camera direction, speed, and orientation.

#### 360 Snapshot

Pull the trigger to create a stereoscopic 360° ODS image from the camera's position. The output is a square PNG with `_360` in its filename and uses the configured `SnapshotWidth`. Capturing takes longer than a conventional snapshot; keep the camera and scene still until it completes.

#### Depth

Pull the trigger to save a colour image and several depth sidecar files with the same base filename:

| Suffix | Contents |
| --- | --- |
| `_depth.png` | Viewable normalized depth; nearer pixels are lighter. |
| `_depth16.png` | 16-bit linear depth suitable for image-processing tools. |
| `_depth.exr` | 32-bit floating-point linear depth in metres. |
| `_depth.json` | Dimensions, clipping planes, FOV and encoding information needed to interpret the depth files. |

Pixels where no geometry was rendered use the invalid value documented in the JSON metadata. Post-processing and the watermark are disabled for the depth data.

Depth captures are limited to 8,192 pixels on their largest side. If the configured snapshot dimensions are larger, Open Brush scales them down while preserving the aspect ratio.

### Automated colour, depth and normal capture

The HTTP API's `app.snapshot` command captures a colour image, depth sidecars and a `_normals.png` image from an explicit camera pose. See the [API Commands List](../open-brush-api/api-commands.md#app.snapshot) for its parameters and an example.

### Advanced mode (Camera Options)

In Advanced mode, the camera icon has a sub-menu. You’ll see a small triangle in the corner.

Click and hold to open the sub-menu. Then choose **Camera Options**.

<figure><img src="../../.gitbook/assets/cameras-icon-in-advanced-mode-with-triangle.png" alt=""><figcaption><p>The Cameras icon in Advanced mode has a sub-menu.</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/camera-options.png" alt=""><figcaption><p>Camera Options is inside the Cameras sub-menu.</p></figcaption></figure>

In **Camera Options**, you can:

* Toggle the Open Brush watermark.
* Adjust field of view (FOV) and smoothing.
* Toggle post effects.

<figure><img src="../../.gitbook/assets/camera-options-tools.png" alt=""><figcaption></figcaption></figure>

#### FOV examples

These examples show FOV set to 140, 70, and 10. The first image has the watermark enabled.

<figure><img src="../../.gitbook/assets/fov-140-watermark-on.jpg" alt=""><figcaption><p>FOV 140 (wide angle), watermark on</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/fov-140-watermark-off.jpg" alt=""><figcaption><p>FOV 140, watermark off</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/fov-70.jpg" alt=""><figcaption><p>FOV 70</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/fov-10.jpg" alt=""><figcaption><p>FOV 10</p></figcaption></figure>

### Demo video

This demo was recorded via the Spectator Camera.

{% embed url="https://youtu.be/C1mUcv5fl9k?si=0mbO3RxIDmGgfzD8" %}
