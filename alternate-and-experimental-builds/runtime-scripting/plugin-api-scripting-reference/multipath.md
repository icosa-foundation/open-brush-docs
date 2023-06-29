
# MultiPath

## Summary
Multiple disconnected path segments


## Instance Properties

<table>
<thead><tr><th width="225">Name</th><th width="160">Return Type</th><th width="80">Read/Write?</th><th>Description</th></tr></thead>
<tbody>
<tr><td>count</td><td>number</td><td>Read-only</td><td>No</td><td>Returns number of paths contained in the multipath</td></tr>
<tr><td>pointCount</td><td>number</td><td>Read-only</td><td>No</td><td>Returns the number of points in all paths in the multipath</td></tr>
</tbody></table>



## Class Methods

        
### MultiPath:New()



**Returns:** <a href="multipath.md">MultiPath</a>






### MultiPath:New(pathList)



**Returns:** <a href="multipath.md">MultiPath</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>pathList</td><td>Path[]</td><td></td></tr></tbody></table>






### MultiPath:FromText(text)

Creates a new MultiPath that draws the shape of the given text. Use App:SetFont to set the letter shapes

**Returns:** <a href="multipath.md">MultiPath</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>text</td><td>string</td><td></td></tr></tbody></table>





    

## Instance Methods

        
### multiPath:Draw()

Draws this path as a brush stroke using current settings

**Returns:** nil






### multiPath:Insert(path)

Inserts the given path at the end of the multipath

**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>path</td><td><a href="path.md">Path</a></td><td></td></tr></tbody></table>






### multiPath:Insert(path, index)

Inserts a new path at the given index

**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>path</td><td><a href="path.md">Path</a></td><td></td></tr>
<tr><td>index</td><td>number</td><td></td></tr></tbody></table>






### multiPath:InsertPoint(transform)

Inserts a point at the end of the last path in the multipath

**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>transform</td><td><a href="transform.md">Transform</a></td><td></td></tr></tbody></table>






### multiPath:InsertPoint(transform, pathIndex, pointIndex)

Inserts a point at the given index of the given path

**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>transform</td><td><a href="transform.md">Transform</a></td><td></td></tr>
<tr><td>pathIndex</td><td>number</td><td></td></tr>
<tr><td>pointIndex</td><td>number</td><td></td></tr></tbody></table>






### multiPath:TransformBy(transform)

Transforms all paths in the multipath

**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>transform</td><td><a href="transform.md">Transform</a></td><td></td></tr></tbody></table>






### multiPath:TranslateBy(amount)

Translates all paths by a given offset

**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>amount</td><td><a href="vector3.md">Vector3</a></td><td></td></tr></tbody></table>






### multiPath:RotateBy(amount)

Rotates all paths by a specified amount around the origin

**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>amount</td><td><a href="rotation.md">Rotation</a></td><td></td></tr></tbody></table>






### multiPath:ScaleBy(scale)

Scales all paths by a specified amount towards or away from the origin

**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>scale</td><td><a href="vector3.md">Vector3</a></td><td></td></tr></tbody></table>






### multiPath:Center()

Offsets all points on the path so that their common center is at the origin

**Returns:** nil






### multiPath:Normalize(scale)

Scales all paths to fit inside a 1x1x1 cube at the origin

**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>scale</td><td>number</td><td></td></tr></tbody></table>






### multiPath:Resample(spacing)

Resamples the multipath at a specified spacing

**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>spacing</td><td>number</td><td></td></tr></tbody></table>






### multiPath:Join()

Joins all the paths in the multipath and returns a single Path

**Returns:** <a href="path.md">Path</a>






### multiPath:Longest()

Returns the longest path in the multipath

**Returns:** <a href="path.md">Path</a>





    
