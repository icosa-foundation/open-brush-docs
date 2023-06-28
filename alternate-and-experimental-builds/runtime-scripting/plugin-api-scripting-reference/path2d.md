
# Path2d

## Summary

A set of Vector2 points forming a 2D path


## Properties

<table>
<thead><tr><th width="225">Name</th><th width="160">Return Type</th><th>Description</th></tr></thead>
<tbody>
<tr><td>count</td><td>number</td><td>Returns the number of points in this path</td></tr>
<tr><td>Item</td><td><a href="transform.md">Transform</a></td><td></td></tr>
<tr><td>last</td><td><a href="transform.md">Transform</a></td><td></td></tr>
<tr><td></td><td></td><td></td></tr></tbody></table>




## Methods


### Path2d:New



**Returns:** <a href="path2d.md">Path2d</a>






### Path2d:New



**Returns:** <a href="path2d.md">Path2d</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>transformList</td><td>Vector2[]</td><td></td></tr></tbody></table>






### Path2d:New



**Returns:** <a href="path2d.md">Path2d</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>positionList</td><td>Vector3[]</td><td></td></tr></tbody></table>






### Path2d:Insert

Inserts a new point at the end of the path

**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>transform</td><td><a href="vector2.md">Vector2</a></td><td></td></tr></tbody></table>






### Path2d:Insert

Inserts a new point at the given path index

**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>transform</td><td><a href="vector2.md">Vector2</a></td><td></td></tr>
<tr><td>index</td><td>number</td><td></td></tr></tbody></table>






### Path2d:OnX

Converts the 2D path to a 3D path on the YZ plane (i.e. with all x values set to 0)

**Returns:** <a href="path.md">Path</a>






### Path2d:OnY

Converts the 2D path to a 3D path on the XZ plane (i.e. with all y values set to 0)

**Returns:** <a href="path.md">Path</a>






### Path2d:OnZ

Converts the 2D path to a 3D path on the XY plane (i.e. with all z values set to 0)

**Returns:** <a href="path.md">Path</a>






### Path2d:TransformBy

Transforms all points in the path by the given amount

**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>transform</td><td><a href="transform.md">Transform</a></td><td></td></tr></tbody></table>






### Path2d:TranslateBy

Changes the position of all points in the path by a given amount

**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>amount</td><td><a href="vector2.md">Vector2</a></td><td></td></tr></tbody></table>






### Path2d:RotateBy

Rotates all points in the path around the origin by a given amount

**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>amount</td><td><a href="rotation.md">Rotation</a></td><td></td></tr></tbody></table>






### Path2d:ScaleBy

Scales all points the path away or towards the origin

**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>scale</td><td><a href="vector2.md">Vector2</a></td><td></td></tr></tbody></table>






### Path2d:Center

Offsets all points on the path so that their common center is at the origin

**Returns:** nil






### Path2d:StartingFrom

Reorders the points so that point at the given index is shifted to be the first point

**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>index</td><td>number</td><td></td></tr></tbody></table>






### Path2d:FindClosest

Returns the index of the point closest to the given position

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>point</td><td><a href="vector2.md">Vector2</a></td><td></td></tr></tbody></table>






### Path2d:FindMinimumX

Returns the index of the point with the smallest X value

**Returns:** number






### Path2d:FindMinimumY

Returns the index of the point with the smallest Y value

**Returns:** number






### Path2d:FindMaximumX

Returns the index of the point with the biggest X value

**Returns:** number






### Path2d:FindMaximumY

Returns the index of the point with the biggest Y value

**Returns:** number






### Path2d:Normalize

Scales and shifts all points so that they fit in a 1 unit square at the origin

**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>scale</td><td>number</td><td></td></tr></tbody></table>






### Path2d:Polygon



**Returns:** <a href="path2d.md">Path2d</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>sides</td><td>number</td><td></td></tr></tbody></table>






### Path2d:Resample



**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>spacing</td><td>number</td><td></td></tr></tbody></table>






