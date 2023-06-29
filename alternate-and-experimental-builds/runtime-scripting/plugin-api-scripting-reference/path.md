
# Path

## Summary
A set of transforms that form a path in 3D space. These form the basis for brush strokes and camera paths


## Instance Properties

<table>
<thead><tr><th width="225">Name</th><th width="160">Return Type</th><th width="80">Read/Write?</th><th>Description</th></tr></thead>
<tbody>
<tr><td>count</td><td>number</td><td>Read-only</td><td>No</td><td>Returns the number of points in this path</td></tr>
<tr><td>Item</td><td><a href="transform.md">Transform</a></td><td>Read-only</td><td>No</td><td></td></tr>
<tr><td>last</td><td><a href="transform.md">Transform</a></td><td>Read-only</td><td>No</td><td>Returns the last point in this path</td></tr>
</tbody></table>



## Class Methods

        
### Path:New()



**Returns:** <a href="path.md">Path</a>






### Path:New(transformList)



**Returns:** <a href="path.md">Path</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>transformList</td><td>Transform[]</td><td></td></tr></tbody></table>






### Path:New(positionList)



**Returns:** <a href="path.md">Path</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>positionList</td><td>Vector3[]</td><td></td></tr></tbody></table>






### Path:Subdivide(trs, parts)



**Returns:** Transform[]


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>trs</td><td>Transform[]</td><td></td></tr>
<tr><td>parts</td><td>number</td><td></td></tr></tbody></table>






### Path:Hermite(startTransform, endTransform, startTangent, endTangent, resolution, tangentStrength)

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





    

## Instance Methods

        
### path:GetDirection(index)

Returns a vector representing the direction of the path at the given point

**Returns:** <a href="vector3.md">Vector3</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>index</td><td>number</td><td></td></tr></tbody></table>






### path:GetNormal(index)

Returns a vector representing the normal of the path at the given point

**Returns:** <a href="vector3.md">Vector3</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>index</td><td>number</td><td></td></tr></tbody></table>






### path:GetTangent(index)

Returns a vector representing the tangent of the path at the given point

**Returns:** <a href="vector3.md">Vector3</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>index</td><td>number</td><td></td></tr></tbody></table>






### path:Draw()

Draws this path as a brush stroke using current settings

**Returns:** nil






### path:Insert(transform)

Inserts a new point at the end of the path

**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>transform</td><td><a href="transform.md">Transform</a></td><td></td></tr></tbody></table>






### path:Insert(transform, index)

Inserts a new point at the given path index

**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>transform</td><td><a href="transform.md">Transform</a></td><td></td></tr>
<tr><td>index</td><td>number</td><td></td></tr></tbody></table>






### path:TransformBy(transform)

Transforms all points in the path by the given amount

**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>transform</td><td><a href="transform.md">Transform</a></td><td></td></tr></tbody></table>






### path:TranslateBy(amount)

Changes the position of all points in the path by a given amount

**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>amount</td><td><a href="vector3.md">Vector3</a></td><td></td></tr></tbody></table>






### path:RotateBy(amount)

Rotates all points in the path around the origin by a given amount

**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>amount</td><td><a href="rotation.md">Rotation</a></td><td></td></tr></tbody></table>






### path:ScaleBy(scale)

Scales all points the path away or towards the origin

**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>scale</td><td><a href="vector3.md">Vector3</a></td><td></td></tr></tbody></table>






### path:Center()

Offsets all points on the path so that their common center is at the origin

**Returns:** nil






### path:StartingFrom(index)

Reorders the points so that point at the given index is shifted to be the first point

**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>index</td><td>number</td><td></td></tr></tbody></table>






### path:FindClosest(point)

Returns the index of the point closest to the given position

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>point</td><td><a href="vector3.md">Vector3</a></td><td></td></tr></tbody></table>






### path:FindMinimumX()

Returns the index of the point with the smallest X value

**Returns:** number






### path:FindMinimumY()

Returns the index of the point with the smallest Y value

**Returns:** number






### path:FindMinimumZ()

Returns the index of the point with the smallest Z value

**Returns:** number






### path:FindMaximumX()

Returns the index of the point with the biggest X value

**Returns:** number






### path:FindMaximumY()

Returns the index of the point with the biggest Y value

**Returns:** number






### path:FindMaximumZ()

Returns the index of the point with the biggest Z value

**Returns:** number






### path:Normalize(scale)

Scales and shifts all points so that they fit in a 1 unit cube at the origin

**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>scale</td><td>number</td><td></td></tr></tbody></table>






### path:Resample(spacing)

Resamples the path at a specified spacing

**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>spacing</td><td>number</td><td></td></tr></tbody></table>






### path:Subdivide(parts)

Splits each path segment into smaller parts

**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>parts</td><td>number</td><td></td></tr></tbody></table>





    
