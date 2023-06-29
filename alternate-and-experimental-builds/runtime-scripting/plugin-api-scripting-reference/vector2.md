
# Vector2

## Summary
A position or offset in 2D space

## Class Properties

<table>
<thead><tr><th width="225">Name</th><th width="160">Return Type</th><th width="80">Read/Write?</th><th>Description</th></tr></thead>
<tbody>
<tr><td>down</td><td><a href="vector2.md">Vector2</a></td><td>Read-only</td><td></td></tr>
<tr><td>left</td><td><a href="vector2.md">Vector2</a></td><td>Read-only</td><td></td></tr>
<tr><td>negativeInfinity</td><td><a href="vector2.md">Vector2</a></td><td>Read-only</td><td></td></tr>
<tr><td>one</td><td><a href="vector2.md">Vector2</a></td><td>Read-only</td><td></td></tr>
<tr><td>positiveInfinity</td><td><a href="vector2.md">Vector2</a></td><td>Read-only</td><td></td></tr>
<tr><td>right</td><td><a href="vector2.md">Vector2</a></td><td>Read-only</td><td></td></tr>
<tr><td>up</td><td><a href="vector2.md">Vector2</a></td><td>Read-only</td><td></td></tr>
<tr><td>zero</td><td><a href="vector2.md">Vector2</a></td><td>Read-only</td><td></td></tr>
</tbody></table>



## Instance Properties

<table>
<thead><tr><th width="225">Name</th><th width="160">Return Type</th><th width="80">Read/Write?</th><th>Description</th></tr></thead>
<tbody>
<tr><td>Item</td><td>number</td><td>Read/Write</td><td></td></tr>
<tr><td>x</td><td>number</td><td>Read/Write</td><td></td></tr>
<tr><td>y</td><td>number</td><td>Read/Write</td><td></td></tr>
</tbody></table>



## Class Methods

        
### Vector2:New(x, y)



**Returns:** <a href="vector2.md">Vector2</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>x</td><td>number</td><td></td></tr>
<tr><td>y</td><td>number</td><td></td></tr></tbody></table>






### Vector2:Angle(a, b)



**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td><a href="vector2.md">Vector2</a></td><td></td></tr>
<tr><td>b</td><td><a href="vector2.md">Vector2</a></td><td></td></tr></tbody></table>






### Vector2:ClampMagnitude(v, maxLength)



**Returns:** <a href="vector2.md">Vector2</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>v</td><td><a href="vector2.md">Vector2</a></td><td></td></tr>
<tr><td>maxLength</td><td>number</td><td></td></tr></tbody></table>






### Vector2:Distance(a, b)



**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td><a href="vector2.md">Vector2</a></td><td></td></tr>
<tr><td>b</td><td><a href="vector2.md">Vector2</a></td><td></td></tr></tbody></table>






### Vector2:Magnitude(a)



**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td><a href="vector2.md">Vector2</a></td><td></td></tr></tbody></table>






### Vector2:SqrMagnitude(a)



**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td><a href="vector2.md">Vector2</a></td><td></td></tr></tbody></table>






### Vector2:Dot(a, b)



**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td><a href="vector2.md">Vector2</a></td><td></td></tr>
<tr><td>b</td><td><a href="vector2.md">Vector2</a></td><td></td></tr></tbody></table>






### Vector2:Lerp(a, b, t)



**Returns:** <a href="vector2.md">Vector2</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td><a href="vector2.md">Vector2</a></td><td></td></tr>
<tr><td>b</td><td><a href="vector2.md">Vector2</a></td><td></td></tr>
<tr><td>t</td><td>number</td><td></td></tr></tbody></table>






### Vector2:LerpUnclamped(a, b, t)



**Returns:** <a href="vector2.md">Vector2</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td><a href="vector2.md">Vector2</a></td><td></td></tr>
<tr><td>b</td><td><a href="vector2.md">Vector2</a></td><td></td></tr>
<tr><td>t</td><td>number</td><td></td></tr></tbody></table>






### Vector2:Max(a, b)



**Returns:** <a href="vector2.md">Vector2</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td><a href="vector2.md">Vector2</a></td><td></td></tr>
<tr><td>b</td><td><a href="vector2.md">Vector2</a></td><td></td></tr></tbody></table>






### Vector2:Min(a, b)



**Returns:** <a href="vector2.md">Vector2</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td><a href="vector2.md">Vector2</a></td><td></td></tr>
<tr><td>b</td><td><a href="vector2.md">Vector2</a></td><td></td></tr></tbody></table>






### Vector2:MoveTowards(current, target, maxDistanceDelta)



**Returns:** <a href="vector2.md">Vector2</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>current</td><td><a href="vector2.md">Vector2</a></td><td></td></tr>
<tr><td>target</td><td><a href="vector2.md">Vector2</a></td><td></td></tr>
<tr><td>maxDistanceDelta</td><td>number</td><td></td></tr></tbody></table>






### Vector2:Normalized(a)



**Returns:** <a href="vector2.md">Vector2</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td><a href="vector2.md">Vector2</a></td><td></td></tr></tbody></table>






### Vector2:Reflect(a, b)



**Returns:** <a href="vector2.md">Vector2</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td><a href="vector2.md">Vector2</a></td><td></td></tr>
<tr><td>b</td><td><a href="vector2.md">Vector2</a></td><td></td></tr></tbody></table>






### Vector2:Scale(a, b)



**Returns:** <a href="vector2.md">Vector2</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td><a href="vector2.md">Vector2</a></td><td></td></tr>
<tr><td>b</td><td><a href="vector2.md">Vector2</a></td><td></td></tr></tbody></table>






### Vector2:SignedAngle(from, to, axis)



**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>from</td><td><a href="vector2.md">Vector2</a></td><td></td></tr>
<tr><td>to</td><td><a href="vector2.md">Vector2</a></td><td></td></tr>
<tr><td>axis</td><td><a href="vector2.md">Vector2</a></td><td></td></tr></tbody></table>






### Vector2:Slerp(a, b, t)



**Returns:** <a href="vector2.md">Vector2</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td><a href="vector2.md">Vector2</a></td><td></td></tr>
<tr><td>b</td><td><a href="vector2.md">Vector2</a></td><td></td></tr>
<tr><td>t</td><td>number</td><td></td></tr></tbody></table>






### Vector2:SlerpUnclamped(a, b, t)



**Returns:** <a href="vector2.md">Vector2</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td><a href="vector2.md">Vector2</a></td><td></td></tr>
<tr><td>b</td><td><a href="vector2.md">Vector2</a></td><td></td></tr>
<tr><td>t</td><td>number</td><td></td></tr></tbody></table>






### Vector2:PointOnCircle(degrees)



**Returns:** <a href="vector2.md">Vector2</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>degrees</td><td>number</td><td></td></tr></tbody></table>





    

## Instance Methods

        
### vector2:OnX()



**Returns:** <a href="vector3.md">Vector3</a>






### vector2:OnY()



**Returns:** <a href="vector3.md">Vector3</a>






### vector2:OnZ()



**Returns:** <a href="vector3.md">Vector3</a>






### vector2:Add(other)



**Returns:** <a href="vector2.md">Vector2</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>other</td><td><a href="vector2.md">Vector2</a></td><td></td></tr></tbody></table>






### vector2:Add(x, y)



**Returns:** <a href="vector2.md">Vector2</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>x</td><td>number</td><td></td></tr>
<tr><td>y</td><td>number</td><td></td></tr></tbody></table>






### vector2:Subtract(other)



**Returns:** <a href="vector2.md">Vector2</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>other</td><td><a href="vector2.md">Vector2</a></td><td></td></tr></tbody></table>






### vector2:Subtract(x, y)



**Returns:** <a href="vector2.md">Vector2</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>x</td><td>number</td><td></td></tr>
<tr><td>y</td><td>number</td><td></td></tr></tbody></table>






### vector2:Multiply(value)



**Returns:** <a href="vector2.md">Vector2</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>value</td><td>number</td><td></td></tr></tbody></table>






### vector2:ScaleBy(other)



**Returns:** <a href="vector2.md">Vector2</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>other</td><td><a href="vector2.md">Vector2</a></td><td></td></tr></tbody></table>






### vector2:ScaleBy(x, y)



**Returns:** <a href="vector2.md">Vector2</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>x</td><td>number</td><td></td></tr>
<tr><td>y</td><td>number</td><td></td></tr></tbody></table>






### vector2:Divide(value)



**Returns:** <a href="vector2.md">Vector2</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>value</td><td>number</td><td></td></tr></tbody></table>






### vector2:NotEquals(other)



**Returns:** boolean


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>other</td><td><a href="vector2.md">Vector2</a></td><td></td></tr></tbody></table>






### vector2:NotEquals(x, y)



**Returns:** boolean


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>x</td><td>number</td><td></td></tr>
<tr><td>y</td><td>number</td><td></td></tr></tbody></table>





    
