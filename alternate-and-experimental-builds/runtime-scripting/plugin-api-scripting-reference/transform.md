
# Transform

## Summary
Represents a position, rotation and scale in one object

## Class Properties

<table>
<thead><tr><th width="225">Name</th><th width="160">Return Type</th><th width="80">Read/Write?</th><th>Description</th></tr></thead>
<tbody>
<tr><td>zero</td><td><a href="transform.md">Transform</a></td><td>Read-only</td><td></td></tr>
</tbody></table>



## Instance Properties

<table>
<thead><tr><th width="225">Name</th><th width="160">Return Type</th><th width="80">Read/Write?</th><th>Description</th></tr></thead>
<tbody>
<tr><td>inverse</td><td><a href="transform.md">Transform</a></td><td>Read-only</td><td></td></tr>
<tr><td>up</td><td><a href="vector3.md">Vector3</a></td><td>Read-only</td><td></td></tr>
<tr><td>down</td><td><a href="vector3.md">Vector3</a></td><td>Read-only</td><td></td></tr>
<tr><td>right</td><td><a href="vector3.md">Vector3</a></td><td>Read-only</td><td></td></tr>
<tr><td>left</td><td><a href="vector3.md">Vector3</a></td><td>Read-only</td><td></td></tr>
<tr><td>forward</td><td><a href="vector3.md">Vector3</a></td><td>Read-only</td><td></td></tr>
<tr><td>back</td><td><a href="vector3.md">Vector3</a></td><td>Read-only</td><td></td></tr>
<tr><td>position</td><td><a href="vector3.md">Vector3</a></td><td>Read-only</td><td></td></tr>
<tr><td>rotation</td><td><a href="rotation.md">Rotation</a></td><td>Read-only</td><td></td></tr>
<tr><td>scale</td><td>number</td><td>Read-only</td><td></td></tr>
</tbody></table>



## Class Methods

        
### Transform:New(translation, rotation, scale)



**Returns:** <a href="transform.md">Transform</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>translation</td><td><a href="vector3.md">Vector3</a></td><td></td></tr>
<tr><td>rotation</td><td><a href="rotation.md">Rotation</a></td><td></td></tr>
<tr><td>scale</td><td>number</td><td></td></tr></tbody></table>






### Transform:New(translation, scale)



**Returns:** <a href="transform.md">Transform</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>translation</td><td><a href="vector3.md">Vector3</a></td><td></td></tr>
<tr><td>scale</td><td>number</td><td></td></tr></tbody></table>






### Transform:New(scale)



**Returns:** <a href="transform.md">Transform</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>scale</td><td>number</td><td></td></tr></tbody></table>






### Transform:New(x, y, z)



**Returns:** <a href="transform.md">Transform</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>x</td><td>number</td><td></td></tr>
<tr><td>y</td><td>number</td><td></td></tr>
<tr><td>z</td><td>number</td><td></td></tr></tbody></table>





    

## Instance Methods

        
### transform:TransformBy(transform)



**Returns:** <a href="transform.md">Transform</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>transform</td><td><a href="transform.md">Transform</a></td><td></td></tr></tbody></table>






### transform:TranslateBy(translation)



**Returns:** <a href="transform.md">Transform</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>translation</td><td><a href="vector3.md">Vector3</a></td><td></td></tr></tbody></table>






### transform:RotateBy(rotation)



**Returns:** <a href="transform.md">Transform</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>rotation</td><td><a href="rotation.md">Rotation</a></td><td></td></tr></tbody></table>






### transform:ScaleBy(scale)



**Returns:** <a href="transform.md">Transform</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>scale</td><td>number</td><td></td></tr></tbody></table>






### transform:Multiply(other)



**Returns:** <a href="transform.md">Transform</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>other</td><td><a href="transform.md">Transform</a></td><td></td></tr></tbody></table>





    
