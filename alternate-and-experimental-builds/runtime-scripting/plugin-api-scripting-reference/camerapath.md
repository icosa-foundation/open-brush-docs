
# CameraPath

## Summary

A camera path and it's position, speed or FOV knots


## Properties

<table>
<thead><tr><th width="225">Name</th><th width="160">Return Type</th><th>Description</th></tr></thead>
<tbody>
<tr><td>index</td><td>number</td><td></td></tr>
<tr><td>active</td><td>boolean</td><td></td></tr>
<tr><td>transform</td><td><a href="transform.md">Transform</a></td><td></td></tr>
<tr><td>position</td><td><a href="vector3.md">Vector3</a></td><td></td></tr>
<tr><td>rotation</td><td><a href="rotation.md">Rotation</a></td><td></td></tr>
<tr><td>scale</td><td>number</td><td></td></tr>
<tr><td></td><td></td><td></td></tr></tbody></table>




## Methods


### CameraPath:RenderActivePath



**Returns:** nil






### CameraPath:ShowAll



**Returns:** nil






### CameraPath:HideAll



**Returns:** nil






### CameraPath:PreviewActivePath



**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>active</td><td>boolean</td><td></td></tr></tbody></table>






### CameraPath:Delete



**Returns:** nil






### CameraPath:New



**Returns:** <a href="camerapath.md">CameraPath</a>






### CameraPath:FromPath



**Returns:** <a href="camerapath.md">CameraPath</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>path</td><td><a href="ipath.md">IPath</a></td><td></td></tr>
<tr><td>looped</td><td>boolean</td><td></td></tr></tbody></table>






### CameraPath:AsPath



**Returns:** <a href="path.md">Path</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>step</td><td>number</td><td></td></tr></tbody></table>






### CameraPath:Duplicate



**Returns:** <a href="camerapathwidget.md">CameraPathWidget</a>






### CameraPath:InsertPosition



**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>position</td><td><a href="vector3.md">Vector3</a></td><td></td></tr>
<tr><td>rotation</td><td><a href="rotation.md">Rotation</a></td><td></td></tr>
<tr><td>smoothing</td><td>number</td><td></td></tr></tbody></table>






### CameraPath:InsertPosition



**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>t</td><td>number</td><td></td></tr>
<tr><td>rotation</td><td><a href="rotation.md">Rotation</a></td><td></td></tr>
<tr><td>smoothing</td><td>number</td><td></td></tr></tbody></table>






### CameraPath:InsertRotation



**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>pos</td><td><a href="vector3.md">Vector3</a></td><td></td></tr>
<tr><td>rot</td><td><a href="rotation.md">Rotation</a></td><td></td></tr></tbody></table>






### CameraPath:InsertRotation



**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>t</td><td>number</td><td></td></tr>
<tr><td>rot</td><td><a href="rotation.md">Rotation</a></td><td></td></tr></tbody></table>






### CameraPath:InsertFov



**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>pos</td><td><a href="vector3.md">Vector3</a></td><td></td></tr>
<tr><td>fov</td><td>number</td><td></td></tr></tbody></table>






### CameraPath:InsertFov



**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>t</td><td>number</td><td></td></tr>
<tr><td>fov</td><td>number</td><td></td></tr></tbody></table>






### CameraPath:InsertSpeed



**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>pos</td><td><a href="vector3.md">Vector3</a></td><td></td></tr>
<tr><td>speed</td><td>number</td><td></td></tr></tbody></table>






### CameraPath:InsertSpeed



**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>t</td><td>number</td><td></td></tr>
<tr><td>speed</td><td>number</td><td></td></tr></tbody></table>






### CameraPath:Extend



**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>position</td><td><a href="vector3.md">Vector3</a></td><td></td></tr>
<tr><td>rotation</td><td><a href="rotation.md">Rotation</a></td><td></td></tr>
<tr><td>smoothing</td><td>number</td><td></td></tr>
<tr><td>atStart</td><td>boolean</td><td></td></tr></tbody></table>






### CameraPath:Loop



**Returns:** nil






### CameraPath:RecordActivePath



**Returns:** nil






### CameraPath:Sample



**Returns:** <a href="transform.md">Transform</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>time</td><td>number</td><td></td></tr>
<tr><td>loop</td><td>boolean</td><td></td></tr>
<tr><td>pingpong</td><td>boolean</td><td></td></tr></tbody></table>






### CameraPath:Simplify



**Returns:** <a href="camerapath.md">CameraPath</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>tolerance</td><td>number</td><td></td></tr>
<tr><td>smoothing</td><td>number</td><td></td></tr></tbody></table>






