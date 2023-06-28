
# Wand

## Summary

Represents the user's wand (the controller that isn't the brush controller)


## Properties

<table>
<thead><tr><th width="225">Name</th><th width="160">Return Type</th><th>Description</th></tr></thead>
<tbody>
<tr><td>position</td><td><a href="vector3.md">Vector3</a></td><td>The 3D position of the Wand</td></tr>
<tr><td>rotation</td><td><a href="rotation.md">Rotation</a></td><td>The 3D orientation of the Wand</td></tr>
<tr><td>direction</td><td><a href="vector3.md">Vector3</a></td><td></td></tr>
<tr><td>pressure</td><td>number</td><td></td></tr>
<tr><td>speed</td><td><a href="vector3.md">Vector3</a></td><td></td></tr>
<tr><td></td><td></td><td></td></tr></tbody></table>




## Methods


### Wand:ResizeHistory(size)

Clears the history and sets it's size

**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>size</td><td>number</td><td></td></tr></tbody></table>






### Wand:SetHistorySize(size)

Sets the size of the history. Only clears it if the size has changed

**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>size</td><td>number</td><td></td></tr></tbody></table>






### Wand:PastPosition(back)

Recalls previous positions of the Wand from the history buffer

**Returns:** <a href="vector3.md">Vector3</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>back</td><td>number</td><td></td></tr></tbody></table>






### Wand:PastRotation(back)

Recalls previous orientations of the Wand from the history buffer

**Returns:** <a href="rotation.md">Rotation</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>back</td><td>number</td><td></td></tr></tbody></table>






