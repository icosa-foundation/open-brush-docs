---
description: Draw a path, control direction/speed/FOV, then record a guided move.
---

# Camera Paths Tool

Camera Paths lets you record video by moving a camera along a path. It’s the core “virtual cinematography” tool in Open Brush.

Once you start recording a path, other tools are locked. If you cancel mid-recording, the partial video is discarded.

<figure><img src="../../.gitbook/assets/The Camera Paths tools.png" alt=""><figcaption><p>The Camera Paths tool opens a dedicated panel.</p></figcaption></figure>

### Create your first path

If you have no paths yet, you’ll only see **Add New Path**.

<figure><img src="../../.gitbook/assets/CP New Path Tool.png" alt=""><figcaption><p>Create a path first. Other tools unlock after that.</p></figcaption></figure>

Create a path with 2+ anchor points.

After that, you’ll see the full set of tools:

<figure><img src="../../.gitbook/assets/Camera Paths Palate and tools.png" alt=""><figcaption><p>The panel after a path is created.</p></figcaption></figure>

### Tools

#### Select Path

Choose which existing path you want to edit.

<figure><img src="../../.gitbook/assets/CP Select Path.png" alt=""><figcaption><p>Select Path</p></figcaption></figure>

#### Show Paths

Shows paths in the sketch so you can manipulate them.

<figure><img src="../../.gitbook/assets/CP Show paths.png" alt=""><figcaption><p>Show Paths</p></figcaption></figure>

#### Delete Path

Deletes the entire selected path.

<figure><img src="../../.gitbook/assets/CP Delete Path tool.png" alt=""><figcaption><p>Delete Path</p></figcaption></figure>

#### Record Path

Renders a video by moving the camera through the full path. The output video appears in `Documents/Open Brush/Videos`.

Recording cannot be paused. Cancel by clicking the **X** on the brush controller while recording.

<figure><img src="../../.gitbook/assets/CP record path tool.png" alt=""><figcaption><p>Record Path</p></figcaption></figure>

#### New Anchor Point

Adds an anchor point to the path. If you add to either end, it stays active for adding more points.

<figure><img src="../../.gitbook/assets/CP New Anchor Point.png" alt=""><figcaption><p>New Anchor Point</p></figcaption></figure>

#### Delete Anchor Point

Deletes any control point on the timeline. That includes anchor, direction, speed, and zoom points.

<figure><img src="../../.gitbook/assets/CP Delete Point tool.png" alt=""><figcaption><p>Delete Point</p></figcaption></figure>

#### Camera Direction Point

Controls where the camera points. Direction points blend with nearby direction points for smooth motion.

<figure><img src="../../.gitbook/assets/CP Camera Direction Point.png" alt=""><figcaption><p>Camera Direction Point</p></figcaption></figure>

#### Camera Speed Point

Controls how fast the camera moves. Values range from `0.1` to `100`. Speed blends between points.

<figure><img src="../../.gitbook/assets/CP Camera Speed Points.png" alt=""><figcaption><p>Camera Speed Point</p></figcaption></figure>

#### Camera Zoom (FOV) Point

Controls field of view over time. Values range from `10` to `140`. FOV blends between points.

<figure><img src="../../.gitbook/assets/CP Camera Zoom Point.png" alt=""><figcaption><p>Camera Zoom Point</p></figcaption></figure>

### Practical notes

Camera Paths can be time consuming. Each control point affects the timeline before and after it.

The tool is only accessible after the sketch is fully rendered. So it can’t capture the rendering process itself.
