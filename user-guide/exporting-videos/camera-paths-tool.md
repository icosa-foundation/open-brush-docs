---
description: Draw a path, control direction/speed/FOV, then record a guided move.
---

# Camera Paths Tool

Camera Paths lets you record video by moving a camera along a path. It’s the core “virtual cinematography” tool in Open Brush.

Once you start recording a path, other tools are locked. If you cancel mid-recording, the partial video is discarded.

<figure><img src="../../.gitbook/assets/the-camera-paths-tools.png" alt=""><figcaption><p>The Camera Paths tool opens a dedicated panel.</p></figcaption></figure>

### Create a path

If you have no paths yet, select **Add New Path**. You can then create the path in one of three ways.

<figure><img src="../../.gitbook/assets/cp-new-path-tool.png" alt=""><figcaption><p>Create a path first. Other tools unlock after that.</p></figcaption></figure>

#### Place anchor points

Select **Add Anchor Point**, then place at least two points. Add more points to shape the route. Use the direction, speed and FOV tools after creating the path to control how the camera moves along it.

#### Record a flight

Select **By Flying** to switch to the Fly tool and begin recording. Fly through the sketch along the route you want, then select **Stop Recording Flight**. Open Brush turns the recorded movement into an editable camera path.

This is useful when it is easier to perform the camera move than construct it one point at a time. Open Brush simplifies the recording into a manageable number of path knots, so the result may not reproduce every small movement.

#### Draw a path

Select **Draw Camera Path**, hold the trigger and draw the route through the scene. Release the trigger to create the path. The camera initially looks in the direction of travel and remains level with the world horizon.

Drawing creates a new path rather than extending the currently selected path. You can edit the resulting anchors, direction, speed and FOV in the same way as any other camera path.

After that, you’ll see the full set of tools:

<figure><img src="../../.gitbook/assets/camera-paths-palate-and-tools.png" alt=""><figcaption><p>The panel after a path is created.</p></figcaption></figure>

### Tools

#### Select Path

Choose which existing path you want to edit.

<figure><img src="../../.gitbook/assets/cp-select-path.png" alt=""><figcaption><p>Select Path</p></figcaption></figure>

#### Show Paths

Shows paths in the sketch so you can manipulate them.

<figure><img src="../../.gitbook/assets/cp-show-paths.png" alt=""><figcaption><p>Show Paths</p></figcaption></figure>

#### Delete Path

Deletes the entire selected path.

<figure><img src="../../.gitbook/assets/cp-delete-path-tool.png" alt=""><figcaption><p>Delete Path</p></figcaption></figure>

#### Record Path

Renders a video by moving the camera through the full path. The output video appears in `Documents/Open Brush/Videos`.

Recording cannot be paused. Cancel by clicking the **X** on the brush controller while recording.

<figure><img src="../../.gitbook/assets/cp-record-path-tool.png" alt=""><figcaption><p>Record Path</p></figcaption></figure>

#### New Anchor Point

Adds an anchor point to the path. If you add to either end, it stays active for adding more points.

<figure><img src="../../.gitbook/assets/cp-new-anchor-point.png" alt=""><figcaption><p>New Anchor Point</p></figcaption></figure>

#### Delete Anchor Point

Deletes any control point on the timeline. That includes anchor, direction, speed, and zoom points.

<figure><img src="../../.gitbook/assets/cp-delete-point-tool.png" alt=""><figcaption><p>Delete Point</p></figcaption></figure>

#### Camera Direction Point

Controls where the camera points. Direction points blend with nearby direction points for smooth motion.

<figure><img src="../../.gitbook/assets/cp-camera-direction-point.png" alt=""><figcaption><p>Camera Direction Point</p></figcaption></figure>

#### Camera Speed Point

Controls how fast the camera moves. Values range from `0.1` to `100`. Speed blends between points.

<figure><img src="../../.gitbook/assets/cp-camera-speed-points.png" alt=""><figcaption><p>Camera Speed Point</p></figcaption></figure>

#### Camera Zoom (FOV) Point

Controls field of view over time. Values range from `10` to `140`. FOV blends between points.

<figure><img src="../../.gitbook/assets/cp-camera-zoom-point.png" alt=""><figcaption><p>Camera Zoom Point</p></figcaption></figure>

### Practical notes

Camera Paths can be time consuming. Each control point affects the timeline before and after it.

The tool is only accessible after the sketch is fully rendered. So it can’t capture the rendering process itself.
