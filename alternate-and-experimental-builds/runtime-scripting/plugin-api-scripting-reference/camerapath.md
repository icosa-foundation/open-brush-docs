
# CameraPath

## Summary
A camera path and its position, speed or FOV knots


## Instance Properties

<table data-full-width="false">
<thead><tr><th>Name</th><th>Return Type</th><th>Description</th></tr></thead>
<tbody>
<tr><td>index</td><td>number<br>Read-only</td><td>Returns the index of this Camera Path in Sketch.cameraPaths</td></tr>
<tr><td>active</td><td>boolean<br>Read/Write</td><td>Gets or sets whether this Camera Path is active</td></tr>
<tr><td>transform</td><td><a href="transform.md">Transform</a><br>Read/Write</td><td>The transform of the camera path</td></tr>
<tr><td>position</td><td><a href="vector3.md">Vector3</a><br>Read/Write</td><td>The 3D position of the Camera Path (usually but not always its first position knot)</td></tr>
<tr><td>rotation</td><td><a href="rotation.md">Rotation</a><br>Read/Write</td><td>The 3D orientation of the Brush Camera Path</td></tr>
<tr><td>scale</td><td>number<br>Read/Write</td><td>The scale of the camera path</td></tr>
</tbody></table>



## Class Methods

        
### CameraPath:RenderActivePath()

Renders the currently active path

**Returns:** nil 




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>CameraPath:RenderActivePath()</strong></code></pre>




### CameraPath:ShowAll()

Shows all camera paths

**Returns:** nil 




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>CameraPath:ShowAll()</strong></code></pre>




### CameraPath:HideAll()

Hides all camera paths

**Returns:** nil 




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>CameraPath:HideAll()</strong></code></pre>




### CameraPath:PreviewActivePath(active)

Turns previews on or off for the active path

**Returns:** nil 


**Parameters:**

<table data-full-width="false">
<thead><tr><th>Name</th><th>Type</th><th>Description</th></tr></thead>
<tbody><tr><td>active</td><td>boolean</td><td>On is true, off is false</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>CameraPath:PreviewActivePath(true)</strong></code></pre>




### CameraPath:New()

Creates a new empty camera path

**Returns:** <a href="camerapath.md">CameraPath</a> 




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>CameraPath:New()</strong></code></pre>




### CameraPath:FromPath(path, looped)

Creates a camera path from a Path and whether it should be looped

**Returns:** <a href="camerapath.md">CameraPath</a> 


**Parameters:**

<table data-full-width="false">
<thead><tr><th>Name</th><th>Type</th><th>Description</th></tr></thead>
<tbody><tr><td>path</td><td><a href="ipath.md">IPath</a></td><td>The Path to convert</td></tr>
<tr><td>looped</td><td>boolean</td><td>Whether the resulting CameraPath should loop</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>myCameraPath = Camera:FromPath(myPath, false)</strong></code></pre>




### CameraPath:RecordActivePath()

Records the active camera path

**Returns:** nil 




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>CameraPath:</strong></code></pre>



    

## Instance Methods

        
### cameraPath:Delete()

Deletes a camera path

**Returns:** nil 




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>mycameraPath:Delete()</strong></code></pre>




### cameraPath:AsPath(step)

Converts the camera path to a path with the specified step size

**Returns:** <a href="path.md">Path</a> 


**Parameters:**

<table data-full-width="false">
<thead><tr><th>Name</th><th>Type</th><th>Description</th></tr></thead>
<tbody><tr><td>step</td><td>number</td><td>A control point is created at time=0, time=step, time=step x 2 etc</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>myPath = myCameraPath:AsPath(5)</strong></code></pre>




### cameraPath:Duplicate()

Duplicates the camera path

**Returns:** <a href="camerapath.md">CameraPath</a> 




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>mynewPath = myOldPath:Duplicate()</strong></code></pre>




### cameraPath:InsertPosition(position, rotation, smoothing)

Inserts a new position knot. (Position must be close to the existing path)

**Returns:** number 


**Parameters:**

<table data-full-width="false">
<thead><tr><th>Name</th><th>Type</th><th>Description</th></tr></thead>
<tbody><tr><td>position</td><td><a href="vector3.md">Vector3</a></td><td>The position of the new knot</td></tr>
<tr><td>rotation</td><td><a href="rotation.md">Rotation</a></td><td>The rotation of the new knot</td></tr>
<tr><td>smoothing</td><td>number</td><td>Controls the spline curvature for this knot</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>myCameraPath:InsertPosition(pos, rot, 0.5</strong></code></pre>




### cameraPath:InsertPositionAtTime(t, rotation, smoothing)

Inserts a new position knot into the path at the specified time

**Returns:** number 


**Parameters:**

<table data-full-width="false">
<thead><tr><th>Name</th><th>Type</th><th>Description</th></tr></thead>
<tbody><tr><td>t</td><td>number</td><td>The time along the path to insert the new knot</td></tr>
<tr><td>rotation</td><td><a href="rotation.md">Rotation</a></td><td>The rotation of the new knot</td></tr>
<tr><td>smoothing</td><td>number</td><td>Controls the spline curvature for this knot</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>myCameraPath:InsertPositionAtTime(1.5, rot, 0.5</strong></code></pre>




### cameraPath:InsertRotation(position, rotation)

Inserts a rotation knot at the specified position close to the existing path

**Returns:** number 


**Parameters:**

<table data-full-width="false">
<thead><tr><th>Name</th><th>Type</th><th>Description</th></tr></thead>
<tbody><tr><td>position</td><td><a href="vector3.md">Vector3</a></td><td>The position of the new knot</td></tr>
<tr><td>rotation</td><td><a href="rotation.md">Rotation</a></td><td>The rotation of the new knot</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>myCameraPath:InsertRotation(pos, rot</strong></code></pre>




### cameraPath:InsertRotationAtTime(t, rotation)

Inserts a rotation knot at the specified time

**Returns:** number 


**Parameters:**

<table data-full-width="false">
<thead><tr><th>Name</th><th>Type</th><th>Description</th></tr></thead>
<tbody><tr><td>t</td><td>number</td><td>The time along the path to insert the new knot</td></tr>
<tr><td>rotation</td><td><a href="rotation.md">Rotation</a></td><td>The rotation of the new knot</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>myCameraPath:InsertRotationAtTime(1.5, rot</strong></code></pre>




### cameraPath:InsertFov(position, fov)

Inserts a field of view knot at the specified position close to the existing path

**Returns:** number 


**Parameters:**

<table data-full-width="false">
<thead><tr><th>Name</th><th>Type</th><th>Description</th></tr></thead>
<tbody><tr><td>position</td><td><a href="vector3.md">Vector3</a></td><td>The position of the new knot</td></tr>
<tr><td>fov</td><td>number</td><td>The field of view of the new knot</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>myCameraPath:InsertFov(pos, 45</strong></code></pre>




### cameraPath:InsertFovAtTime(t, fov)

Inserts a fov knot at the specified time

**Returns:** number 


**Parameters:**

<table data-full-width="false">
<thead><tr><th>Name</th><th>Type</th><th>Description</th></tr></thead>
<tbody><tr><td>t</td><td>number</td><td>The time along the path to insert the new knot</td></tr>
<tr><td>fov</td><td>number</td><td>The field of view of the new knot</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>myCameraPath:InsertFovAtTime(2.5, 45</strong></code></pre>




### cameraPath:InsertSpeed(position, speed)

Inserts a speed knot at the specified position close to the existing path

**Returns:** number 


**Parameters:**

<table data-full-width="false">
<thead><tr><th>Name</th><th>Type</th><th>Description</th></tr></thead>
<tbody><tr><td>position</td><td><a href="vector3.md">Vector3</a></td><td>The position of the new knot</td></tr>
<tr><td>speed</td><td>number</td><td>The speed of the new knot</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>myCameraPath:InsertSpeed(position, 1.5</strong></code></pre>




### cameraPath:InsertSpeedAtTime(t, speed)

Inserts a speed knot at the specified time

**Returns:** number 


**Parameters:**

<table data-full-width="false">
<thead><tr><th>Name</th><th>Type</th><th>Description</th></tr></thead>
<tbody><tr><td>t</td><td>number</td><td>The time along the path to insert the new knot</td></tr>
<tr><td>speed</td><td>number</td><td>The speed of the new knot</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>myCameraPath:InsertSpeedAtTime(2.5, 2</strong></code></pre>




### cameraPath:Extend(position, rotation, smoothing, atStart)

Extends the camera path

**Returns:** nil 


**Parameters:**

<table data-full-width="false">
<thead><tr><th>Name</th><th>Type</th><th>Description</th></tr></thead>
<tbody><tr><td>position</td><td><a href="vector3.md">Vector3</a></td><td>The position to extend the camera path to</td></tr>
<tr><td>rotation</td><td><a href="rotation.md">Rotation</a></td><td>The rotation of the camera path at the extended position</td></tr>
<tr><td>smoothing</td><td>number</td><td>The smoothing factor applied to the new point</td></tr>
<tr><td>atStart</td><td>boolean</td><td>Determines whether the extension is done at the start or end of the camera path. True=start, false=end</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>myCameraPath:Extend(pos, rot, 1.2, true</strong></code></pre>




### cameraPath:Loop()

Loops the camera path

**Returns:** nil 




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>myCameraPath:Loop</strong></code></pre>




### cameraPath:Sample(time, loop, pingpong)

Samples the camera path at the specified time

**Returns:** <a href="transform.md">Transform</a>  (The sampled transform of the camera at the specified time)


**Parameters:**

<table data-full-width="false">
<thead><tr><th>Name</th><th>Type</th><th>Description</th></tr></thead>
<tbody><tr><td>time</td><td>number</td><td>The time at which to sample the camera path</td></tr>
<tr><td>loop</td><td>boolean</td><td>Determines whether the camera path should loop</td></tr>
<tr><td>pingpong</td><td>boolean</td><td>Determines whether the camera path should pingpong (reverse direction every loop</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>myTransform = myCameraPath:Sample(2.5, true, false)</strong></code></pre>




### cameraPath:Simplify(tolerance, smoothing)

Simplifies the camera path

**Returns:** <a href="camerapath.md">CameraPath</a>  (A new simplified Camera Path)


**Parameters:**

<table data-full-width="false">
<thead><tr><th>Name</th><th>Type</th><th>Description</th></tr></thead>
<tbody><tr><td>tolerance</td><td>number</td><td>The tolerance used for simplification</td></tr>
<tr><td>smoothing</td><td>number</td><td>The smoothing factor used for simplification</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>newPath = oldPath:Simplify(1.2, 1)</strong></code></pre>



    
