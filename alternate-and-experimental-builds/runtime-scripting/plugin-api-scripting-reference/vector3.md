
# Vector3

## Summary




## Properties

<table>
<thead><tr><th width="225">Name</th><th width="160">Return Type</th><th>Description</th></tr></thead>
<tbody>
<tr><td>Item</td><td>number</td><td></td></tr>
<tr><td>x</td><td>number</td><td></td></tr>
<tr><td>y</td><td>number</td><td></td></tr>
<tr><td>z</td><td>number</td><td></td></tr>
<tr><td>magnitude</td><td>number</td><td></td></tr>
<tr><td>normalized</td><td>Vector3</td><td></td></tr>
<tr><td>sqrMagnitude</td><td>number</td><td></td></tr>
<tr><td>back</td><td>Vector3</td><td></td></tr>
<tr><td>down</td><td>Vector3</td><td></td></tr>
<tr><td>forward</td><td>Vector3</td><td></td></tr>
<tr><td>left</td><td>Vector3</td><td></td></tr>
<tr><td>negativeInfinity</td><td>Vector3</td><td></td></tr>
<tr><td>one</td><td>Vector3</td><td></td></tr>
<tr><td>positiveInfinity</td><td>Vector3</td><td></td></tr>
<tr><td>right</td><td>Vector3</td><td></td></tr>
<tr><td>up</td><td>Vector3</td><td></td></tr>
<tr><td>zero</td><td>Vector3</td><td></td></tr>
<tr><td></td><td></td><td></td></tr></tbody></table>




## Methods


### Vector3:New



**Returns:** Vector3


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>x</td><td>number</td><td></td></tr>
<tr><td>y</td><td>number</td><td></td></tr>
<tr><td>z</td><td>number</td><td></td></tr></tbody></table>






### Vector3:Angle



**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td>Vector3</td><td></td></tr>
<tr><td>b</td><td>Vector3</td><td></td></tr></tbody></table>






### Vector3:ClampMagnitude



**Returns:** Vector3


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>v</td><td>Vector3</td><td></td></tr>
<tr><td>maxLength</td><td>number</td><td></td></tr></tbody></table>






### Vector3:Cross



**Returns:** Vector3


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td>Vector3</td><td></td></tr>
<tr><td>b</td><td>Vector3</td><td></td></tr></tbody></table>






### Vector3:Distance



**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td>Vector3</td><td></td></tr>
<tr><td>b</td><td>Vector3</td><td></td></tr></tbody></table>






### Vector3:Magnitude



**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td>Vector3</td><td></td></tr></tbody></table>






### Vector3:SqrMagnitude



**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td>Vector3</td><td></td></tr></tbody></table>






### Vector3:Dot



**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td>Vector3</td><td></td></tr>
<tr><td>b</td><td>Vector3</td><td></td></tr></tbody></table>






### Vector3:Lerp



**Returns:** Vector3


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td>Vector3</td><td></td></tr>
<tr><td>b</td><td>Vector3</td><td></td></tr>
<tr><td>t</td><td>number</td><td></td></tr></tbody></table>






### Vector3:LerpUnclamped



**Returns:** Vector3


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td>Vector3</td><td></td></tr>
<tr><td>b</td><td>Vector3</td><td></td></tr>
<tr><td>t</td><td>number</td><td></td></tr></tbody></table>






### Vector3:Max



**Returns:** Vector3


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td>Vector3</td><td></td></tr>
<tr><td>b</td><td>Vector3</td><td></td></tr></tbody></table>






### Vector3:Min



**Returns:** Vector3


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td>Vector3</td><td></td></tr>
<tr><td>b</td><td>Vector3</td><td></td></tr></tbody></table>






### Vector3:MoveTowards



**Returns:** Vector3


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>current</td><td>Vector3</td><td></td></tr>
<tr><td>target</td><td>Vector3</td><td></td></tr>
<tr><td>maxDistanceDelta</td><td>number</td><td></td></tr></tbody></table>






### Vector3:Normalize



**Returns:** Vector3


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td>Vector3</td><td></td></tr></tbody></table>






### Vector3:Project



**Returns:** Vector3


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td>Vector3</td><td></td></tr>
<tr><td>b</td><td>Vector3</td><td></td></tr></tbody></table>






### Vector3:ProjectOnPlane



**Returns:** Vector3


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>vector</td><td>Vector3</td><td></td></tr>
<tr><td>planeNormal</td><td>Vector3</td><td></td></tr></tbody></table>






### Vector3:Reflect



**Returns:** Vector3


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td>Vector3</td><td></td></tr>
<tr><td>b</td><td>Vector3</td><td></td></tr></tbody></table>






### Vector3:RotateTowards



**Returns:** Vector3


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>current</td><td>Vector3</td><td></td></tr>
<tr><td>target</td><td>Vector3</td><td></td></tr>
<tr><td>maxRadiansDelta</td><td>number</td><td></td></tr>
<tr><td>maxMagnitudeDelta</td><td>number</td><td></td></tr></tbody></table>






### Vector3:ScaleBy



**Returns:** Vector3


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td>Vector3</td><td></td></tr>
<tr><td>b</td><td>Vector3</td><td></td></tr></tbody></table>






### Vector3:SignedAngle



**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>from</td><td>Vector3</td><td></td></tr>
<tr><td>to</td><td>Vector3</td><td></td></tr>
<tr><td>axis</td><td>Vector3</td><td></td></tr></tbody></table>






### Vector3:Slerp



**Returns:** Vector3


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td>Vector3</td><td></td></tr>
<tr><td>b</td><td>Vector3</td><td></td></tr>
<tr><td>t</td><td>number</td><td></td></tr></tbody></table>






### Vector3:SlerpUnclamped



**Returns:** Vector3


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td>Vector3</td><td></td></tr>
<tr><td>b</td><td>Vector3</td><td></td></tr>
<tr><td>t</td><td>number</td><td></td></tr></tbody></table>






### Vector3:Add



**Returns:** Vector3


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>b</td><td>Vector3</td><td></td></tr></tbody></table>






### Vector3:Add



**Returns:** Vector3


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>x</td><td>number</td><td></td></tr>
<tr><td>y</td><td>number</td><td></td></tr>
<tr><td>z</td><td>number</td><td></td></tr></tbody></table>






### Vector3:Subtract



**Returns:** Vector3


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>b</td><td>Vector3</td><td></td></tr></tbody></table>






### Vector3:Subtract



**Returns:** Vector3


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>x</td><td>number</td><td></td></tr>
<tr><td>y</td><td>number</td><td></td></tr>
<tr><td>z</td><td>number</td><td></td></tr></tbody></table>






### Vector3:Multiply



**Returns:** Vector3


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>b</td><td>number</td><td></td></tr></tbody></table>






### Vector3:ScaleBy



**Returns:** Vector3


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>b</td><td>Vector3</td><td></td></tr></tbody></table>






### Vector3:ScaleBy



**Returns:** Vector3


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>x</td><td>number</td><td></td></tr>
<tr><td>y</td><td>number</td><td></td></tr>
<tr><td>z</td><td>number</td><td></td></tr></tbody></table>






### Vector3:Divide



**Returns:** Vector3


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>b</td><td>number</td><td></td></tr></tbody></table>






### Vector3:NotEquals



**Returns:** boolean


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>b</td><td>Vector3</td><td></td></tr></tbody></table>






### Vector3:NotEquals



**Returns:** boolean


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>x</td><td>number</td><td></td></tr>
<tr><td>y</td><td>number</td><td></td></tr>
<tr><td>z</td><td>number</td><td></td></tr></tbody></table>






### Vector3:Add



**Returns:** Vector3


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td>Vector3</td><td></td></tr>
<tr><td>b</td><td>Vector3</td><td></td></tr></tbody></table>






### Vector3:Subtract



**Returns:** Vector3


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td>Vector3</td><td></td></tr>
<tr><td>b</td><td>Vector3</td><td></td></tr></tbody></table>






### Vector3:Multiply



**Returns:** Vector3


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td>Vector3</td><td></td></tr>
<tr><td>b</td><td>number</td><td></td></tr></tbody></table>






### Vector3:Divide



**Returns:** Vector3


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td>Vector3</td><td></td></tr>
<tr><td>b</td><td>number</td><td></td></tr></tbody></table>






### Vector3:NotEquals



**Returns:** boolean


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td>Vector3</td><td></td></tr>
<tr><td>b</td><td>Vector3</td><td></td></tr></tbody></table>






