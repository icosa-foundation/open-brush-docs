
# MultiPath

## Summary

Multiple disconnected path segments


## Properties

<table>
<thead><tr><th width="225">Name</th><th width="160">Return Type</th><th width="120">Read/Write?</th><th>Description</th></tr></thead>
<tbody>
<tr><td>count</td><td>number</td><td>Read-only</td><td>Returns number of paths contained in the multipath</td></tr>
<tr><td>pointcount</td><td>number</td><td>Read-only</td><td>Returns the number of points in all paths in the multipath</td></tr>
<tr><td></td><td></td><td></td></tr></tbody></table>




## Methods


### MultiPath:New()



**Returns:** <a href="multipath.md">MultiPath</a>






### MultiPath:New(pathList)



**Returns:** <a href="multipath.md">MultiPath</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>pathList</td><td>Path[]</td><td></td></tr></tbody></table>






### MultiPath:draw()

Draws this path as a brush stroke using current settings

**Returns:** nil






### MultiPath:FromText(text)

Creates a new MultiPath that draws the shape of the given text. Use App:SetFont to set the letter shapes

**Returns:** <a href="multipath.md">MultiPath</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>text</td><td>string</td><td></td></tr></tbody></table>






### MultiPath:insert(path)

Inserts the given path at the end of the multipath

**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>path</td><td><a href="path.md">Path</a></td><td></td></tr></tbody></table>






### MultiPath:insert(path, index)

Inserts a new path at the given index

**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>path</td><td><a href="path.md">Path</a></td><td></td></tr>
<tr><td>index</td><td>number</td><td></td></tr></tbody></table>






### MultiPath:insertpoint(transform)

Inserts a point at the end of the last path in the multipath

**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>transform</td><td><a href="transform.md">Transform</a></td><td></td></tr></tbody></table>






### MultiPath:insertpoint(transform, pathIndex, pointIndex)

Inserts a point at the given index of the given path

**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>transform</td><td><a href="transform.md">Transform</a></td><td></td></tr>
<tr><td>pathIndex</td><td>number</td><td></td></tr>
<tr><td>pointIndex</td><td>number</td><td></td></tr></tbody></table>






### MultiPath:transformby(transform)

Transforms all paths in the multipath

**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>transform</td><td><a href="transform.md">Transform</a></td><td></td></tr></tbody></table>






### MultiPath:translateby(amount)

Translates all paths by a given offset

**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>amount</td><td><a href="vector3.md">Vector3</a></td><td></td></tr></tbody></table>






### MultiPath:rotateby(amount)

Rotates all paths by a specified amount around the origin

**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>amount</td><td><a href="rotation.md">Rotation</a></td><td></td></tr></tbody></table>






### MultiPath:scaleby(scale)

Scales all paths by a specified amount towards or away from the origin

**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>scale</td><td><a href="vector3.md">Vector3</a></td><td></td></tr></tbody></table>






### MultiPath:center()

Offsets all points on the path so that their common center is at the origin

**Returns:** nil






### MultiPath:normalize(scale)

Scales all paths to fit inside a 1x1x1 cube at the origin

**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>scale</td><td>number</td><td></td></tr></tbody></table>






### MultiPath:resample(spacing)

Resamples the multipath at a specified spacing

**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>spacing</td><td>number</td><td></td></tr></tbody></table>






### MultiPath:join()

Joins all the paths in the multipath and returns a single Path

**Returns:** <a href="path.md">Path</a>






### MultiPath:longest()

Returns the longest path in the multipath

**Returns:** <a href="path.md">Path</a>






