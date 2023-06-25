
# Rotation

## Summary




## Properties

<table>
<thead><tr><th width="225">Name</th><th width="160">Return Type</th><th>Description</th></tr></thead>
<tbody>
<tr><td>Item</td><td>number</td><td></td></tr>
<tr><td>x</td><td>number</td><td></td></tr>
<tr><td>y</td><td>number</td><td></td></tr>
<tr><td>z</td><td>number</td><td></td></tr>
<tr><td>zero</td><td><a href="rotation.md">Rotation</a></td><td></td></tr>
<tr><td>left</td><td><a href="rotation.md">Rotation</a></td><td></td></tr>
<tr><td>right</td><td><a href="rotation.md">Rotation</a></td><td></td></tr>
<tr><td>up</td><td><a href="rotation.md">Rotation</a></td><td></td></tr>
<tr><td>down</td><td><a href="rotation.md">Rotation</a></td><td></td></tr>
<tr><td>anticlockwise</td><td><a href="rotation.md">Rotation</a></td><td></td></tr>
<tr><td>clockwise</td><td><a href="rotation.md">Rotation</a></td><td></td></tr>
<tr><td>normalized</td><td><a href="rotation.md">Rotation</a></td><td></td></tr>
<tr><td>kEpsilon</td><td>number</td><td></td></tr>
<tr><td></td><td></td><td></td></tr></tbody></table>




## Methods


### Rotation:New



**Returns:** <a href="rotation.md">Rotation</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>x</td><td>number</td><td></td></tr>
<tr><td>y</td><td>number</td><td></td></tr>
<tr><td>z</td><td>number</td><td></td></tr></tbody></table>






### Rotation:SetFromToRotation



**Returns:** <a href="rotation.md">Rotation</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>fromDirection</td><td><a href="vector3.md">Vector3</a></td><td></td></tr>
<tr><td>toDirection</td><td><a href="vector3.md">Vector3</a></td><td></td></tr></tbody></table>






### Rotation:SetLookRotation



**Returns:** <a href="rotation.md">Rotation</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>view</td><td><a href="vector3.md">Vector3</a></td><td></td></tr></tbody></table>






### Rotation:SetLookRotation



**Returns:** <a href="rotation.md">Rotation</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>view</td><td><a href="vector3.md">Vector3</a></td><td></td></tr>
<tr><td>up</td><td><a href="vector3.md">Vector3</a></td><td></td></tr></tbody></table>






### Rotation:ToAngleAxis



**Returns:** <a href="number, vector3.md">Number, Vector3</a>






### Rotation:Angle



**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td><a href="rotation.md">Rotation</a></td><td></td></tr>
<tr><td>b</td><td><a href="rotation.md">Rotation</a></td><td></td></tr></tbody></table>






### Rotation:AngleAxis



**Returns:** <a href="rotation.md">Rotation</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>angle</td><td>number</td><td></td></tr>
<tr><td>axis</td><td><a href="vector3.md">Vector3</a></td><td></td></tr></tbody></table>






### Rotation:Dot



**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td><a href="rotation.md">Rotation</a></td><td></td></tr>
<tr><td>b</td><td><a href="rotation.md">Rotation</a></td><td></td></tr></tbody></table>






### Rotation:FromToRotation



**Returns:** <a href="rotation.md">Rotation</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>from</td><td><a href="vector3.md">Vector3</a></td><td></td></tr>
<tr><td>to</td><td><a href="vector3.md">Vector3</a></td><td></td></tr></tbody></table>






### Rotation:Inverse



**Returns:** <a href="rotation.md">Rotation</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td><a href="rotation.md">Rotation</a></td><td></td></tr></tbody></table>






### Rotation:Lerp



**Returns:** <a href="rotation.md">Rotation</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td><a href="rotation.md">Rotation</a></td><td></td></tr>
<tr><td>b</td><td><a href="rotation.md">Rotation</a></td><td></td></tr>
<tr><td>t</td><td>number</td><td></td></tr></tbody></table>






### Rotation:LerpUnclamped



**Returns:** <a href="rotation.md">Rotation</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td><a href="rotation.md">Rotation</a></td><td></td></tr>
<tr><td>b</td><td><a href="rotation.md">Rotation</a></td><td></td></tr>
<tr><td>t</td><td>number</td><td></td></tr></tbody></table>






### Rotation:LookRotation



**Returns:** <a href="rotation.md">Rotation</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>forward</td><td><a href="vector3.md">Vector3</a></td><td></td></tr></tbody></table>






### Rotation:LookRotation



**Returns:** <a href="rotation.md">Rotation</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>forward</td><td><a href="vector3.md">Vector3</a></td><td></td></tr>
<tr><td>up</td><td><a href="vector3.md">Vector3</a></td><td></td></tr></tbody></table>






### Rotation:Normalize



**Returns:** <a href="rotation.md">Rotation</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td><a href="rotation.md">Rotation</a></td><td></td></tr></tbody></table>






### Rotation:RotateTowards



**Returns:** <a href="rotation.md">Rotation</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>from</td><td><a href="rotation.md">Rotation</a></td><td></td></tr>
<tr><td>to</td><td><a href="rotation.md">Rotation</a></td><td></td></tr>
<tr><td>maxDegreesDelta</td><td>number</td><td></td></tr></tbody></table>






### Rotation:Slerp



**Returns:** <a href="rotation.md">Rotation</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td><a href="rotation.md">Rotation</a></td><td></td></tr>
<tr><td>b</td><td><a href="rotation.md">Rotation</a></td><td></td></tr>
<tr><td>t</td><td>number</td><td></td></tr></tbody></table>






### Rotation:SlerpUnclamped



**Returns:** <a href="rotation.md">Rotation</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td><a href="rotation.md">Rotation</a></td><td></td></tr>
<tr><td>b</td><td><a href="rotation.md">Rotation</a></td><td></td></tr>
<tr><td>t</td><td>number</td><td></td></tr></tbody></table>






### Rotation:Multiply



**Returns:** <a href="rotation.md">Rotation</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>b</td><td><a href="rotation.md">Rotation</a></td><td></td></tr></tbody></table>






### Rotation:Multiply



**Returns:** <a href="rotation.md">Rotation</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>x</td><td>number</td><td></td></tr>
<tr><td>y</td><td>number</td><td></td></tr>
<tr><td>z</td><td>number</td><td></td></tr></tbody></table>






### Rotation:Scale



**Returns:** <a href="rotation.md">Rotation</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td>number</td><td></td></tr></tbody></table>






### Rotation:Multiply



**Returns:** <a href="rotation.md">Rotation</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td><a href="rotation.md">Rotation</a></td><td></td></tr>
<tr><td>b</td><td><a href="rotation.md">Rotation</a></td><td></td></tr></tbody></table>






