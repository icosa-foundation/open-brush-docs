
# Vector3

## Summary

A position or offset in 3D space


## Properties

<table>
<thead><tr><th width="225">Name</th><th width="160">Return Type</th><th>Description</th></tr></thead>
<tbody>
<tr><td>Item</td><td>number</td><td></td></tr>
<tr><td>x</td><td>number</td><td></td></tr>
<tr><td>y</td><td>number</td><td></td></tr>
<tr><td>z</td><td>number</td><td></td></tr>
<tr><td>magnitude</td><td>number</td><td></td></tr>
<tr><td>normalized</td><td><a href="vector3.md">Vector3</a></td><td></td></tr>
<tr><td>sqrMagnitude</td><td>number</td><td></td></tr>
<tr><td>back</td><td><a href="vector3.md">Vector3</a></td><td></td></tr>
<tr><td>down</td><td><a href="vector3.md">Vector3</a></td><td></td></tr>
<tr><td>forward</td><td><a href="vector3.md">Vector3</a></td><td></td></tr>
<tr><td>left</td><td><a href="vector3.md">Vector3</a></td><td></td></tr>
<tr><td>negativeInfinity</td><td><a href="vector3.md">Vector3</a></td><td></td></tr>
<tr><td>one</td><td><a href="vector3.md">Vector3</a></td><td></td></tr>
<tr><td>positiveInfinity</td><td><a href="vector3.md">Vector3</a></td><td></td></tr>
<tr><td>right</td><td><a href="vector3.md">Vector3</a></td><td></td></tr>
<tr><td>up</td><td><a href="vector3.md">Vector3</a></td><td></td></tr>
<tr><td>zero</td><td><a href="vector3.md">Vector3</a></td><td></td></tr>
<tr><td></td><td></td><td></td></tr></tbody></table>




## Methods


### Vector3:New(x, y, z)



**Returns:** <a href="vector3.md">Vector3</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>x</td><td>number</td><td></td></tr>
<tr><td>y</td><td>number</td><td></td></tr>
<tr><td>z</td><td>number</td><td></td></tr></tbody></table>






### Vector3:Angle(a, b)



**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td><a href="vector3.md">Vector3</a></td><td></td></tr>
<tr><td>b</td><td><a href="vector3.md">Vector3</a></td><td></td></tr></tbody></table>






### Vector3:ClampMagnitude(v, maxLength)



**Returns:** <a href="vector3.md">Vector3</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>v</td><td><a href="vector3.md">Vector3</a></td><td></td></tr>
<tr><td>maxLength</td><td>number</td><td></td></tr></tbody></table>






### Vector3:Cross(a, b)



**Returns:** <a href="vector3.md">Vector3</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td><a href="vector3.md">Vector3</a></td><td></td></tr>
<tr><td>b</td><td><a href="vector3.md">Vector3</a></td><td></td></tr></tbody></table>






### Vector3:Distance(a, b)



**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td><a href="vector3.md">Vector3</a></td><td></td></tr>
<tr><td>b</td><td><a href="vector3.md">Vector3</a></td><td></td></tr></tbody></table>






### Vector3:Magnitude(a)



**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td><a href="vector3.md">Vector3</a></td><td></td></tr></tbody></table>






### Vector3:SqrMagnitude(a)



**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td><a href="vector3.md">Vector3</a></td><td></td></tr></tbody></table>






### Vector3:Dot(a, b)



**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td><a href="vector3.md">Vector3</a></td><td></td></tr>
<tr><td>b</td><td><a href="vector3.md">Vector3</a></td><td></td></tr></tbody></table>






### Vector3:Lerp(a, b, t)



**Returns:** <a href="vector3.md">Vector3</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td><a href="vector3.md">Vector3</a></td><td></td></tr>
<tr><td>b</td><td><a href="vector3.md">Vector3</a></td><td></td></tr>
<tr><td>t</td><td>number</td><td></td></tr></tbody></table>






### Vector3:LerpUnclamped(a, b, t)



**Returns:** <a href="vector3.md">Vector3</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td><a href="vector3.md">Vector3</a></td><td></td></tr>
<tr><td>b</td><td><a href="vector3.md">Vector3</a></td><td></td></tr>
<tr><td>t</td><td>number</td><td></td></tr></tbody></table>






### Vector3:Max(a, b)



**Returns:** <a href="vector3.md">Vector3</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td><a href="vector3.md">Vector3</a></td><td></td></tr>
<tr><td>b</td><td><a href="vector3.md">Vector3</a></td><td></td></tr></tbody></table>






### Vector3:Min(a, b)



**Returns:** <a href="vector3.md">Vector3</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td><a href="vector3.md">Vector3</a></td><td></td></tr>
<tr><td>b</td><td><a href="vector3.md">Vector3</a></td><td></td></tr></tbody></table>






### Vector3:MoveTowards(current, target, maxDistanceDelta)



**Returns:** <a href="vector3.md">Vector3</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>current</td><td><a href="vector3.md">Vector3</a></td><td></td></tr>
<tr><td>target</td><td><a href="vector3.md">Vector3</a></td><td></td></tr>
<tr><td>maxDistanceDelta</td><td>number</td><td></td></tr></tbody></table>






### Vector3:Normalize(a)



**Returns:** <a href="vector3.md">Vector3</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td><a href="vector3.md">Vector3</a></td><td></td></tr></tbody></table>






### Vector3:Project(a, b)



**Returns:** <a href="vector3.md">Vector3</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td><a href="vector3.md">Vector3</a></td><td></td></tr>
<tr><td>b</td><td><a href="vector3.md">Vector3</a></td><td></td></tr></tbody></table>






### Vector3:ProjectOnPlane(vector, planeNormal)



**Returns:** <a href="vector3.md">Vector3</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>vector</td><td><a href="vector3.md">Vector3</a></td><td></td></tr>
<tr><td>planeNormal</td><td><a href="vector3.md">Vector3</a></td><td></td></tr></tbody></table>






### Vector3:Reflect(a, b)



**Returns:** <a href="vector3.md">Vector3</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td><a href="vector3.md">Vector3</a></td><td></td></tr>
<tr><td>b</td><td><a href="vector3.md">Vector3</a></td><td></td></tr></tbody></table>






### Vector3:RotateTowards(current, target, maxRadiansDelta, maxMagnitudeDelta)



**Returns:** <a href="vector3.md">Vector3</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>current</td><td><a href="vector3.md">Vector3</a></td><td></td></tr>
<tr><td>target</td><td><a href="vector3.md">Vector3</a></td><td></td></tr>
<tr><td>maxRadiansDelta</td><td>number</td><td></td></tr>
<tr><td>maxMagnitudeDelta</td><td>number</td><td></td></tr></tbody></table>






### Vector3:ScaleBy(a, b)



**Returns:** <a href="vector3.md">Vector3</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td><a href="vector3.md">Vector3</a></td><td></td></tr>
<tr><td>b</td><td><a href="vector3.md">Vector3</a></td><td></td></tr></tbody></table>






### Vector3:SignedAngle(from, to, axis)



**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>from</td><td><a href="vector3.md">Vector3</a></td><td></td></tr>
<tr><td>to</td><td><a href="vector3.md">Vector3</a></td><td></td></tr>
<tr><td>axis</td><td><a href="vector3.md">Vector3</a></td><td></td></tr></tbody></table>






### Vector3:Slerp(a, b, t)



**Returns:** <a href="vector3.md">Vector3</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td><a href="vector3.md">Vector3</a></td><td></td></tr>
<tr><td>b</td><td><a href="vector3.md">Vector3</a></td><td></td></tr>
<tr><td>t</td><td>number</td><td></td></tr></tbody></table>






### Vector3:SlerpUnclamped(a, b, t)



**Returns:** <a href="vector3.md">Vector3</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td><a href="vector3.md">Vector3</a></td><td></td></tr>
<tr><td>b</td><td><a href="vector3.md">Vector3</a></td><td></td></tr>
<tr><td>t</td><td>number</td><td></td></tr></tbody></table>






### Vector3:Add(b)



**Returns:** <a href="vector3.md">Vector3</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>b</td><td><a href="vector3.md">Vector3</a></td><td></td></tr></tbody></table>






### Vector3:Add(x, y, z)



**Returns:** <a href="vector3.md">Vector3</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>x</td><td>number</td><td></td></tr>
<tr><td>y</td><td>number</td><td></td></tr>
<tr><td>z</td><td>number</td><td></td></tr></tbody></table>






### Vector3:Subtract(b)



**Returns:** <a href="vector3.md">Vector3</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>b</td><td><a href="vector3.md">Vector3</a></td><td></td></tr></tbody></table>






### Vector3:Subtract(x, y, z)



**Returns:** <a href="vector3.md">Vector3</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>x</td><td>number</td><td></td></tr>
<tr><td>y</td><td>number</td><td></td></tr>
<tr><td>z</td><td>number</td><td></td></tr></tbody></table>






### Vector3:Multiply(b)



**Returns:** <a href="vector3.md">Vector3</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>b</td><td>number</td><td></td></tr></tbody></table>






### Vector3:ScaleBy(b)



**Returns:** <a href="vector3.md">Vector3</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>b</td><td><a href="vector3.md">Vector3</a></td><td></td></tr></tbody></table>






### Vector3:ScaleBy(x, y, z)



**Returns:** <a href="vector3.md">Vector3</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>x</td><td>number</td><td></td></tr>
<tr><td>y</td><td>number</td><td></td></tr>
<tr><td>z</td><td>number</td><td></td></tr></tbody></table>






### Vector3:Divide(b)



**Returns:** <a href="vector3.md">Vector3</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>b</td><td>number</td><td></td></tr></tbody></table>






### Vector3:NotEquals(b)



**Returns:** boolean


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>b</td><td><a href="vector3.md">Vector3</a></td><td></td></tr></tbody></table>






### Vector3:NotEquals(x, y, z)



**Returns:** boolean


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>x</td><td>number</td><td></td></tr>
<tr><td>y</td><td>number</td><td></td></tr>
<tr><td>z</td><td>number</td><td></td></tr></tbody></table>






### Vector3:Add(a, b)



**Returns:** <a href="vector3.md">Vector3</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td><a href="vector3.md">Vector3</a></td><td></td></tr>
<tr><td>b</td><td><a href="vector3.md">Vector3</a></td><td></td></tr></tbody></table>






### Vector3:Subtract(a, b)



**Returns:** <a href="vector3.md">Vector3</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td><a href="vector3.md">Vector3</a></td><td></td></tr>
<tr><td>b</td><td><a href="vector3.md">Vector3</a></td><td></td></tr></tbody></table>






### Vector3:Multiply(a, b)



**Returns:** <a href="vector3.md">Vector3</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td><a href="vector3.md">Vector3</a></td><td></td></tr>
<tr><td>b</td><td>number</td><td></td></tr></tbody></table>






### Vector3:Divide(a, b)



**Returns:** <a href="vector3.md">Vector3</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td><a href="vector3.md">Vector3</a></td><td></td></tr>
<tr><td>b</td><td>number</td><td></td></tr></tbody></table>






### Vector3:NotEquals(a, b)



**Returns:** boolean


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td><a href="vector3.md">Vector3</a></td><td></td></tr>
<tr><td>b</td><td><a href="vector3.md">Vector3</a></td><td></td></tr></tbody></table>






