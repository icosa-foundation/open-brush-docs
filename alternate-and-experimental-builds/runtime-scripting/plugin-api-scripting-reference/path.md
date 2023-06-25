
# Path

## Summary




## Properties

<table>
<thead><tr><th width="225">Name</th><th width="160">Return Type</th><th>Description</th></tr></thead>
<tbody>
<tr><td>Item</td><td><a href="transform.md">Transform</a></td><td></td></tr>
<tr><td>last</td><td><a href="transform.md">Transform</a></td><td></td></tr>
<tr><td>count</td><td>number</td><td></td></tr>
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



**Returns:** <a href="vector3.md">Vector3</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>index</td><td>number</td><td></td></tr></tbody></table>






### Path:GetNormal



**Returns:** <a href="vector3.md">Vector3</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>index</td><td>number</td><td></td></tr></tbody></table>






### Path:GetTangent



**Returns:** <a href="vector3.md">Vector3</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>index</td><td>number</td><td></td></tr></tbody></table>






### Path:Draw



**Returns:** nil






### Path:Insert



**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>transform</td><td><a href="transform.md">Transform</a></td><td></td></tr></tbody></table>






### Path:TransformBy



**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>transform</td><td><a href="transform.md">Transform</a></td><td></td></tr></tbody></table>






### Path:TranslateBy



**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>amount</td><td><a href="vector3.md">Vector3</a></td><td></td></tr></tbody></table>






### Path:RotateBy



**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>amount</td><td><a href="rotation.md">Rotation</a></td><td></td></tr></tbody></table>






### Path:ScaleBy



**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>scale</td><td><a href="vector3.md">Vector3</a></td><td></td></tr></tbody></table>






### Path:Center



**Returns:** nil






### Path:StartingFrom



**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>index</td><td>number</td><td></td></tr></tbody></table>






### Path:FindClosest



**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>point</td><td><a href="vector3.md">Vector3</a></td><td></td></tr></tbody></table>






### Path:FindMinimumX



**Returns:** number






### Path:FindMinimumY



**Returns:** number






### Path:FindMinimumZ



**Returns:** number






### Path:FindMaximumX



**Returns:** number






### Path:FindMaximumY



**Returns:** number






### Path:FindMaximumZ



**Returns:** number






### Path:Normalize



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



**Returns:** Transform[]


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>trs</td><td>Transform[]</td><td></td></tr>
<tr><td>spacing</td><td>number</td><td></td></tr></tbody></table>






### Path:Resample



**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>spacing</td><td>number</td><td></td></tr></tbody></table>






### Path:Subdivide



**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>parts</td><td>number</td><td></td></tr></tbody></table>






### Path:Hermite



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






