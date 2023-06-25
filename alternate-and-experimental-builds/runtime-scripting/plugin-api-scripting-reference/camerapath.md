
# CameraPath

## Summary




## Properties

<table>
<thead><tr><th width="225">Name</th><th width="160">Return Type</th><th>Description</th></tr></thead>
<tbody>
<tr><td>index</td><td>number</td><td></td></tr>
<tr><td>active</td><td>boolean</td><td></td></tr>
<tr><td>transform</td><td>Transform</td><td></td></tr>
<tr><td>position</td><td>Vector3</td><td></td></tr>
<tr><td>rotation</td><td>Rotation</td><td></td></tr>
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



**Returns:** CameraPath






### CameraPath:FromPath



**Returns:** CameraPath


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>path</td><td>IPath</td><td></td></tr>
<tr><td>looped</td><td>boolean</td><td></td></tr></tbody></table>






### CameraPath:AsPath



**Returns:** Path


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>step</td><td>number</td><td></td></tr></tbody></table>






### CameraPath:Duplicate



**Returns:** CameraPathWidget






### CameraPath:InsertPosition



**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>position</td><td>Vector3</td><td></td></tr>
<tr><td>rotation</td><td>Rotation</td><td></td></tr>
<tr><td>smoothing</td><td>number</td><td></td></tr></tbody></table>






### CameraPath:InsertPosition



**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>t</td><td>number</td><td></td></tr>
<tr><td>rotation</td><td>Rotation</td><td></td></tr>
<tr><td>smoothing</td><td>number</td><td></td></tr></tbody></table>






### CameraPath:InsertRotation



**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>pos</td><td>Vector3</td><td></td></tr>
<tr><td>rot</td><td>Rotation</td><td></td></tr></tbody></table>






### CameraPath:InsertRotation



**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>t</td><td>number</td><td></td></tr>
<tr><td>rot</td><td>Rotation</td><td></td></tr></tbody></table>






### CameraPath:InsertFov



**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>pos</td><td>Vector3</td><td></td></tr>
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
<tbody><tr><td>pos</td><td>Vector3</td><td></td></tr>
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
<tbody><tr><td>position</td><td>Vector3</td><td></td></tr>
<tr><td>rotation</td><td>Rotation</td><td></td></tr>
<tr><td>smoothing</td><td>number</td><td></td></tr>
<tr><td>atStart</td><td>boolean</td><td></td></tr></tbody></table>






### CameraPath:Loop



**Returns:** nil






### CameraPath:RecordActivePath



**Returns:** nil






### CameraPath:Sample



**Returns:** Transform


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>time</td><td>number</td><td></td></tr>
<tr><td>loop</td><td>boolean</td><td></td></tr>
<tr><td>pingpong</td><td>boolean</td><td></td></tr></tbody></table>






### CameraPath:Simplify



**Returns:** CameraPath


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>tolerance</td><td>number</td><td></td></tr>
<tr><td>smoothing</td><td>number</td><td></td></tr></tbody></table>






