
# Brush

## Summary




## Properties

<table>
<thead><tr><th width="225">Name</th><th width="160">Return Type</th><th>Description</th></tr></thead>
<tbody>
<tr><td>timeSincePressed</td><td>number</td><td></td></tr>
<tr><td>timeSinceReleased</td><td>number</td><td></td></tr>
<tr><td>triggerIsPressed</td><td>boolean</td><td></td></tr>
<tr><td>triggerIsPressedThisFrame</td><td>boolean</td><td></td></tr>
<tr><td>distanceMoved</td><td>number</td><td></td></tr>
<tr><td>distanceDrawn</td><td>number</td><td></td></tr>
<tr><td>position</td><td><a href="vector3.md">Vector3</a></td><td></td></tr>
<tr><td>rotation</td><td><a href="rotation.md">Rotation</a></td><td></td></tr>
<tr><td>direction</td><td><a href="vector3.md">Vector3</a></td><td></td></tr>
<tr><td>size</td><td>number</td><td></td></tr>
<tr><td>pressure</td><td>number</td><td></td></tr>
<tr><td>type</td><td>string</td><td></td></tr>
<tr><td>speed</td><td>number</td><td></td></tr>
<tr><td>colorRgb</td><td><a href="color.md">Color</a></td><td></td></tr>
<tr><td>colorHsv</td><td><a href="vector3.md">Vector3</a></td><td></td></tr>
<tr><td>colorHtml</td><td>string</td><td></td></tr>
<tr><td>lastColorPicked</td><td><a href="color.md">Color</a></td><td></td></tr>
<tr><td>currentPath</td><td><a href="path.md">Path</a></td><td></td></tr>
<tr><td>LastColorPickedHsv</td><td><a href="vector3.md">Vector3</a></td><td></td></tr>
<tr><td></td><td></td><td></td></tr></tbody></table>




## Methods


### Brush:JitterColor



**Returns:** nil






### Brush:ResizeHistory



**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>size</td><td>number</td><td></td></tr></tbody></table>






### Brush:SetHistorySize



**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>size</td><td>number</td><td></td></tr></tbody></table>






### Brush:GetPastPosition



**Returns:** <a href="vector3.md">Vector3</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>back</td><td>number</td><td></td></tr></tbody></table>






### Brush:GetPastRotation



**Returns:** <a href="rotation.md">Rotation</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>back</td><td>number</td><td></td></tr></tbody></table>






### Brush:ForcePaintingOn



**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>active</td><td>boolean</td><td></td></tr></tbody></table>






### Brush:ForcePaintingOff



**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>active</td><td>boolean</td><td></td></tr></tbody></table>






### Brush:ForceNewStroke



**Returns:** nil






