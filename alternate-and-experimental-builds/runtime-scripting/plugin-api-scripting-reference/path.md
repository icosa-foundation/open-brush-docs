
# Path

## Summary

A set of transforms that form a path in 3D space. These form the basis for brush strokes and camera paths


## Properties

<table>
<thead><tr><th width="225">Name</th><th width="160">Return Type</th><th>Description</th></tr></thead>
<tbody>
<tr><td>count</td><td>number</td><td>Returns the number of points in this path</td></tr>
<tr><td>Item</td><td><a href="transform.md">Transform</a></td><td></td></tr>
<tr><td>last</td><td><a href="transform.md">Transform</a></td><td>Returns the last point in this path</td></tr>
<tr><td></td><td></td><td></td></tr></tbody></table>




## Methods


### Path:New



**Returns:** <a href="path.md">Path</a>






### Path:New



**Returns:** <a href="path.md">Path</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>transformList</td><td>Transform[]</td><td></td></tr></tbody></table>






### Path:New



**Returns:** <a href="path.md">Path</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>positionList</td><td>Vector3[]</td><td></td></tr></tbody></table>






### Path:GetDirection

Returns a vector representing the direction of the path at the given point

**Returns:** <a href="vector3.md">Vector3</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>index</td><td>number</td><td></td></tr></tbody></table>






### Path:GetNormal

Returns a vector representing the normal of the path at the given point

**Returns:** <a href="vector3.md">Vector3</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>index</td><td>number</td><td></td></tr></tbody></table>






### Path:GetTangent

Returns a vector representing the tangent of the path at the given point

**Returns:** <a href="vector3.md">Vector3</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>index</td><td>number</td><td></td></tr></tbody></table>






### Path:Draw

Draws this path as a brush stroke using current settings

**Returns:** nil






### Path:Insert

Inserts a new point at the end of the path

**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>transform</td><td><a href="transform.md">Transform</a></td><td></td></tr></tbody></table>






### Path:Insert

Inserts a new point at the given path index

**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>transform</td><td><a href="transform.md">Transform</a></td><td></td></tr>
<tr><td>index</td><td>number</td><td></td></tr></tbody></table>






### Path:TransformBy

Transforms all points in the path by the given amount

**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>transform</td><td><a href="transform.md">Transform</a></td><td></td></tr></tbody></table>






### Path:TranslateBy

Changes the position of all points in the path by a given amount

**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>amount</td><td><a href="vector3.md">Vector3</a></td><td></td></tr></tbody></table>






### Path:RotateBy

Rotates all points in the path around the origin by a given amount

**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>amount</td><td><a href="rotation.md">Rotation</a></td><td></td></tr></tbody></table>






### Path:ScaleBy

Scales all points the path away or towards the origin

**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>scale</td><td><a href="vector3.md">Vector3</a></td><td></td></tr></tbody></table>






### Path:Center

Offsets all points on the path so that their common center is at the origin

**Returns:** nil






### Path:StartingFrom

Reorders the points so that point at the given index is shifted to be the first point

**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>index</td><td>number</td><td></td></tr></tbody></table>






### Path:FindClosest

Returns the index of the point closest to the given position

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>point</td><td><a href="vector3.md">Vector3</a></td><td></td></tr></tbody></table>






### Path:FindMinimumX

Returns the index of the point with the smallest X value

**Returns:** number






### Path:FindMinimumY

Returns the index of the point with the smallest Y value

**Returns:** number






### Path:FindMinimumZ

Returns the index of the point with the smallest Z value

**Returns:** number






### Path:FindMaximumX

Returns the index of the point with the biggest X value

**Returns:** number






### Path:FindMaximumY

Returns the index of the point with the biggest Y value

**Returns:** number






### Path:FindMaximumZ

Returns the index of the point with the biggest Z value

**Returns:** number






### Path:Normalize

Scales and shifts all points so that they fit in a 1 unit cube at the origin

**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>scale</td><td>number</td><td></td></tr></tbody></table>






### Path:Subdivide



**Returns:** Transform[]


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>trs</td><td>Transform[]</td><td></td></tr>
<tr><td>parts</td><td>number</td><td></td></tr></tbody></table>






### Path:Resample

Resamples the path at a specified spacing

**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>spacing</td><td>number</td><td></td></tr></tbody></table>






### Path:Subdivide

Splits each path segment into smaller parts

**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>parts</td><td>number</td><td></td></tr></tbody></table>






### Path:Hermite

Generates a hermite spline

**Returns:** <a href="path.md">Path</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>startTransform</td><td><a href="transform.md">Transform</a></td><td></td></tr>
<tr><td>endTransform</td><td><a href="transform.md">Transform</a></td><td></td></tr>
<tr><td>startTangent</td><td><a href="vector3.md">Vector3</a></td><td></td></tr>
<tr><td>endTangent</td><td><a href="vector3.md">Vector3</a></td><td></td></tr>
<tr><td>resolution</td><td>number</td><td></td></tr>
<tr><td>tangentStrength</td><td>number</td><td></td></tr></tbody></table>






