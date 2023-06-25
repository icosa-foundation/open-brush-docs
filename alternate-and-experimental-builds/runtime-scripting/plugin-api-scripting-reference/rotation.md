
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
<tr><td>zero</td><td>Rotation</td><td></td></tr>
<tr><td>left</td><td>Rotation</td><td></td></tr>
<tr><td>right</td><td>Rotation</td><td></td></tr>
<tr><td>up</td><td>Rotation</td><td></td></tr>
<tr><td>down</td><td>Rotation</td><td></td></tr>
<tr><td>anticlockwise</td><td>Rotation</td><td></td></tr>
<tr><td>clockwise</td><td>Rotation</td><td></td></tr>
<tr><td>normalized</td><td>Rotation</td><td></td></tr>
<tr><td>kEpsilon</td><td>number</td><td></td></tr>
<tr><td></td><td></td><td></td></tr></tbody></table>




## Methods


### Rotation:New



**Returns:** Rotation


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>x</td><td>number</td><td></td></tr>
<tr><td>y</td><td>number</td><td></td></tr>
<tr><td>z</td><td>number</td><td></td></tr></tbody></table>






### Rotation:SetFromToRotation



**Returns:** Rotation


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>fromDirection</td><td>Vector3</td><td></td></tr>
<tr><td>toDirection</td><td>Vector3</td><td></td></tr></tbody></table>






### Rotation:SetLookRotation



**Returns:** Rotation


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>view</td><td>Vector3</td><td></td></tr></tbody></table>






### Rotation:SetLookRotation



**Returns:** Rotation


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>view</td><td>Vector3</td><td></td></tr>
<tr><td>up</td><td>Vector3</td><td></td></tr></tbody></table>






### Rotation:ToAngleAxis



**Returns:** Number, Vector3






### Rotation:Angle



**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td>Rotation</td><td></td></tr>
<tr><td>b</td><td>Rotation</td><td></td></tr></tbody></table>






### Rotation:AngleAxis



**Returns:** Rotation


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>angle</td><td>number</td><td></td></tr>
<tr><td>axis</td><td>Vector3</td><td></td></tr></tbody></table>






### Rotation:Dot



**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td>Rotation</td><td></td></tr>
<tr><td>b</td><td>Rotation</td><td></td></tr></tbody></table>






### Rotation:FromToRotation



**Returns:** Rotation


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>from</td><td>Vector3</td><td></td></tr>
<tr><td>to</td><td>Vector3</td><td></td></tr></tbody></table>






### Rotation:Inverse



**Returns:** Rotation


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td>Rotation</td><td></td></tr></tbody></table>






### Rotation:Lerp



**Returns:** Rotation


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td>Rotation</td><td></td></tr>
<tr><td>b</td><td>Rotation</td><td></td></tr>
<tr><td>t</td><td>number</td><td></td></tr></tbody></table>






### Rotation:LerpUnclamped



**Returns:** Rotation


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td>Rotation</td><td></td></tr>
<tr><td>b</td><td>Rotation</td><td></td></tr>
<tr><td>t</td><td>number</td><td></td></tr></tbody></table>






### Rotation:LookRotation



**Returns:** Rotation


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>forward</td><td>Vector3</td><td></td></tr></tbody></table>






### Rotation:LookRotation



**Returns:** Rotation


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>forward</td><td>Vector3</td><td></td></tr>
<tr><td>up</td><td>Vector3</td><td></td></tr></tbody></table>






### Rotation:Normalize



**Returns:** Rotation


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td>Rotation</td><td></td></tr></tbody></table>






### Rotation:RotateTowards



**Returns:** Rotation


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>from</td><td>Rotation</td><td></td></tr>
<tr><td>to</td><td>Rotation</td><td></td></tr>
<tr><td>maxDegreesDelta</td><td>number</td><td></td></tr></tbody></table>






### Rotation:Slerp



**Returns:** Rotation


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td>Rotation</td><td></td></tr>
<tr><td>b</td><td>Rotation</td><td></td></tr>
<tr><td>t</td><td>number</td><td></td></tr></tbody></table>






### Rotation:SlerpUnclamped



**Returns:** Rotation


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td>Rotation</td><td></td></tr>
<tr><td>b</td><td>Rotation</td><td></td></tr>
<tr><td>t</td><td>number</td><td></td></tr></tbody></table>






### Rotation:Multiply



**Returns:** Rotation


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>b</td><td>Rotation</td><td></td></tr></tbody></table>






### Rotation:Multiply



**Returns:** Rotation


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>x</td><td>number</td><td></td></tr>
<tr><td>y</td><td>number</td><td></td></tr>
<tr><td>z</td><td>number</td><td></td></tr></tbody></table>






### Rotation:Scale



**Returns:** Rotation


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td>number</td><td></td></tr></tbody></table>






### Rotation:Multiply



**Returns:** Rotation


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td>Rotation</td><td></td></tr>
<tr><td>b</td><td>Rotation</td><td></td></tr></tbody></table>






