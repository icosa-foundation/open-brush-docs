
# Vector3

## Summary
A position or offset in 3D space

## Class Properties

<table>
<thead><tr><th width="225">Name</th><th width="160">Return Type</th><th width="80">Read/Write?</th><th>Description</th></tr></thead>
<tbody>
<tr><td>back</td><td><a href="vector3.md">Vector3</a></td><td>Read-only</td><td>A vector of -1 in the z axis</td></tr>
<tr><td>down</td><td><a href="vector3.md">Vector3</a></td><td>Read-only</td><td>A vector of -1 in the y axis</td></tr>
<tr><td>forward</td><td><a href="vector3.md">Vector3</a></td><td>Read-only</td><td>A vector of 1 in the z axis</td></tr>
<tr><td>left</td><td><a href="vector3.md">Vector3</a></td><td>Read-only</td><td>A vector of -1 in the x axis</td></tr>
<tr><td>negativeInfinity</td><td><a href="vector3.md">Vector3</a></td><td>Read-only</td><td>A vector of -infinity in all axes</td></tr>
<tr><td>one</td><td><a href="vector3.md">Vector3</a></td><td>Read-only</td><td>A vector of 1 in all axes</td></tr>
<tr><td>positiveInfinity</td><td><a href="vector3.md">Vector3</a></td><td>Read-only</td><td>A vector of infinity in all axes</td></tr>
<tr><td>right</td><td><a href="vector3.md">Vector3</a></td><td>Read-only</td><td>A vector of 1 in the x axis</td></tr>
<tr><td>up</td><td><a href="vector3.md">Vector3</a></td><td>Read-only</td><td>A vector of 1 in the y axis</td></tr>
<tr><td>zero</td><td><a href="vector3.md">Vector3</a></td><td>Read-only</td><td>A vector of 0 in all axes</td></tr>
</tbody></table>



## Instance Properties

<table>
<thead><tr><th width="225">Name</th><th width="160">Return Type</th><th width="80">Read/Write?</th><th>Description</th></tr></thead>
<tbody>
<tr><td>Item</td><td>number</td><td>Read/Write</td><td></td></tr>
<tr><td>x</td><td>number</td><td>Read/Write</td><td>Gets or sets the x coordinate</td></tr>
<tr><td>y</td><td>number</td><td>Read/Write</td><td>Gets or sets the y coordinate</td></tr>
<tr><td>z</td><td>number</td><td>Read/Write</td><td>Gets or sets the z coordinate</td></tr>
<tr><td>magnitude</td><td>number</td><td>Read-only</td><td>Returns the length of this vector</td></tr>
<tr><td>sqrMagnitude</td><td>number</td><td>Read-only</td><td>Returns the squared length of this vector</td></tr>
<tr><td>normalized</td><td><a href="vector3.md">Vector3</a></td><td>Read-only</td><td>Returns a vector with the same direction but with a length of 1</td></tr>
</tbody></table>



## Class Methods

        
### Vector3:New(x, y, z)



**Returns:** <a href="vector3.md">Vector3</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>x</td><td>number</td><td></td></tr>
<tr><td>y</td><td>number</td><td></td></tr>
<tr><td>z</td><td>number</td><td></td></tr></tbody></table>






### Vector3:Angle(a, b)

Returns the angle in degrees between two points and the origin

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td><a href="vector3.md">Vector3</a></td><td></td></tr>
<tr><td>b</td><td><a href="vector3.md">Vector3</a></td><td></td></tr></tbody></table>






### Vector3:Cross(a, b)

Returns the cross product of two vectors

**Returns:** <a href="vector3.md">Vector3</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td><a href="vector3.md">Vector3</a></td><td></td></tr>
<tr><td>b</td><td><a href="vector3.md">Vector3</a></td><td></td></tr></tbody></table>






### Vector3:Distance(a, b)

Returns the distance between two points

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td><a href="vector3.md">Vector3</a></td><td></td></tr>
<tr><td>b</td><td><a href="vector3.md">Vector3</a></td><td></td></tr></tbody></table>






### Vector3:Lerp(a, b, t)

Linearly interpolates between two points

**Returns:** <a href="vector3.md">Vector3</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td><a href="vector3.md">Vector3</a></td><td>The first point</td></tr>
<tr><td>b</td><td><a href="vector3.md">Vector3</a></td><td>The second point</td></tr>
<tr><td>t</td><td>number</td><td>The value between 0 and 1 that controls how far between a and b the new point is</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>newPoint = Vector2:Lerp(pointA, PointB, 0.25)</strong></code></pre>




### Vector3:LerpUnclamped(a, b, t)

Linearly interpolates (or extrapolates) between two points

**Returns:** <a href="vector3.md">Vector3</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td><a href="vector3.md">Vector3</a></td><td>The first point</td></tr>
<tr><td>b</td><td><a href="vector3.md">Vector3</a></td><td>The second point</td></tr>
<tr><td>t</td><td>number</td><td>The value that controls how far between (or beyond) a and b the new point is</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>newPoint = Vector3:Lerp(pointA, PointB, 0.25)</strong></code></pre>




### Vector3:Max(a, b)

Creates a vector made from the largest components of the inputs

**Returns:** <a href="vector3.md">Vector3</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td><a href="vector3.md">Vector3</a></td><td></td></tr>
<tr><td>b</td><td><a href="vector3.md">Vector3</a></td><td></td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>result = Vector3:Max(firstVector, secondVector</strong></code></pre>




### Vector3:Min(a, b)

Creates a vector made from the smallest components of the inputs

**Returns:** <a href="vector3.md">Vector3</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td><a href="vector3.md">Vector3</a></td><td></td></tr>
<tr><td>b</td><td><a href="vector3.md">Vector3</a></td><td></td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>result = Vector3:Min(firstVector, secondVector</strong></code></pre>




### Vector3:MoveTowards(current, target, maxDistanceDelta)

Moves a point towards a target point

**Returns:** <a href="vector3.md">Vector3</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>current</td><td><a href="vector3.md">Vector3</a></td><td></td></tr>
<tr><td>target</td><td><a href="vector3.md">Vector3</a></td><td></td></tr>
<tr><td>maxDistanceDelta</td><td>number</td><td></td></tr></tbody></table>






### Vector3:ProjectOnPlane(vector, planeNormal)

Projects this vector onto a plane defined by a normal orthogonal to the plane

**Returns:** <a href="vector3.md">Vector3</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>vector</td><td><a href="vector3.md">Vector3</a></td><td></td></tr>
<tr><td>planeNormal</td><td><a href="vector3.md">Vector3</a></td><td></td></tr></tbody></table>






### Vector3:RotateTowards(current, target, maxRadiansDelta, maxMagnitudeDelta)

Moves this vector towards another with a maximum change in angle

**Returns:** <a href="vector3.md">Vector3</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>current</td><td><a href="vector3.md">Vector3</a></td><td></td></tr>
<tr><td>target</td><td><a href="vector3.md">Vector3</a></td><td></td></tr>
<tr><td>maxRadiansDelta</td><td>number</td><td></td></tr>
<tr><td>maxMagnitudeDelta</td><td>number</td><td></td></tr></tbody></table>






### Vector3:ScaleBy(a, b)

Multiplies two vectors component-wise

**Returns:** <a href="vector3.md">Vector3</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td><a href="vector3.md">Vector3</a></td><td></td></tr>
<tr><td>b</td><td><a href="vector3.md">Vector3</a></td><td></td></tr></tbody></table>






### Vector3:Slerp(a, b, t)

Spherically interpolates between two vectors

**Returns:** <a href="vector3.md">Vector3</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td><a href="vector3.md">Vector3</a></td><td>The first point</td></tr>
<tr><td>b</td><td><a href="vector3.md">Vector3</a></td><td>The second point</td></tr>
<tr><td>t</td><td>number</td><td>The value that controls how far between (or beyond) a and b the new point is</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>newPoint = Vector3:Lerp(pointA, PointB, 0.25)</strong></code></pre>




### Vector3:SlerpUnclamped(a, b, t)

Spherically interpolates (or extrapolates) between two vectors

**Returns:** <a href="vector3.md">Vector3</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td><a href="vector3.md">Vector3</a></td><td>The first point</td></tr>
<tr><td>b</td><td><a href="vector3.md">Vector3</a></td><td>The second point</td></tr>
<tr><td>t</td><td>number</td><td>The value that controls how far between (or beyond) a and b the new point is</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>newPoint = Vector3:Lerp(pointA, PointB, 0.25)</strong></code></pre>



    

## Instance Methods

        
### vector3:ClampMagnitude(maxLength)

Returns a vector with the same direction but with it's length clamped to a maximum

**Returns:** <a href="vector3.md">Vector3</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>maxLength</td><td>number</td><td></td></tr></tbody></table>






### vector3:Project(other)

Projects this vector onto another

**Returns:** <a href="vector3.md">Vector3</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>other</td><td><a href="vector3.md">Vector3</a></td><td></td></tr></tbody></table>






### vector3:Reflect(other)

Reflects a vector off the plane defined by a normal

**Returns:** <a href="vector3.md">Vector3</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>other</td><td><a href="vector3.md">Vector3</a></td><td></td></tr></tbody></table>






### vector3:SignedAngle(other, axis)

Returns the signed angle in degrees between two points and the origin

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>other</td><td><a href="vector3.md">Vector3</a></td><td></td></tr>
<tr><td>axis</td><td><a href="vector3.md">Vector3</a></td><td></td></tr></tbody></table>






### vector3:Add(other)

Adds two vectors

**Returns:** <a href="vector3.md">Vector3</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>other</td><td><a href="vector3.md">Vector3</a></td><td></td></tr></tbody></table>






### vector3:Add(x, y, z)

Adds x, y and z values to this vector

**Returns:** <a href="vector3.md">Vector3</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>x</td><td>number</td><td></td></tr>
<tr><td>y</td><td>number</td><td></td></tr>
<tr><td>z</td><td>number</td><td></td></tr></tbody></table>






### vector3:Subtract(other)

Subtracts a Vector3 from this vector

**Returns:** <a href="vector3.md">Vector3</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>other</td><td><a href="vector3.md">Vector3</a></td><td></td></tr></tbody></table>






### vector3:Subtract(x, y, z)

Subtracts x, y and z values from this vector

**Returns:** <a href="vector3.md">Vector3</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>x</td><td>number</td><td></td></tr>
<tr><td>y</td><td>number</td><td></td></tr>
<tr><td>z</td><td>number</td><td></td></tr></tbody></table>






### vector3:Multiply(value)

Multiplies this vector by a scalar value

**Returns:** <a href="vector3.md">Vector3</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>value</td><td>number</td><td></td></tr></tbody></table>






### vector3:ScaleBy(other)

Multiplies this vector by another vector component-wise

**Returns:** <a href="vector3.md">Vector3</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>other</td><td><a href="vector3.md">Vector3</a></td><td></td></tr></tbody></table>






### vector3:ScaleBy(x, y, z)

Multiplies this vector by x, y and z values component-wise

**Returns:** <a href="vector3.md">Vector3</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>x</td><td>number</td><td></td></tr>
<tr><td>y</td><td>number</td><td></td></tr>
<tr><td>z</td><td>number</td><td></td></tr></tbody></table>






### vector3:Divide(value)

Divides this vector by a scalar value

**Returns:** <a href="vector3.md">Vector3</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>value</td><td>number</td><td></td></tr></tbody></table>






### vector3:NotEquals(other)

Is this vector not equal to another?

**Returns:** boolean


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>other</td><td><a href="vector3.md">Vector3</a></td><td></td></tr></tbody></table>






### vector3:NotEquals(x, y, z)

Is this vector not equal to these x, y and z values?

**Returns:** boolean


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>x</td><td>number</td><td></td></tr>
<tr><td>y</td><td>number</td><td></td></tr>
<tr><td>z</td><td>number</td><td></td></tr></tbody></table>





    
