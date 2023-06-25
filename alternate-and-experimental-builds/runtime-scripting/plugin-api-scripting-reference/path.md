
# Path

## Summary




## Properties

<table>
<thead><tr><th width="225">Name</th><th width="160">Return Type</th><th>Description</th></tr></thead>
<tbody>
<tr><td>Item</td><td>Transform</td><td></td></tr>
<tr><td>last</td><td>Transform</td><td></td></tr>
<tr><td>count</td><td>number</td><td></td></tr>
<tr><td></td><td></td><td></td></tr></tbody></table>




## Methods


### Path:New



**Returns:** Path






### Path:New



**Returns:** Path


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>transformList</td><td>Transform[]</td><td></td></tr></tbody></table>






### Path:New



**Returns:** Path


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>positionList</td><td>Vector3[]</td><td></td></tr></tbody></table>






### Path:GetDirection



**Returns:** Vector3


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>index</td><td>number</td><td></td></tr></tbody></table>






### Path:GetNormal



**Returns:** Vector3


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>index</td><td>number</td><td></td></tr></tbody></table>






### Path:GetTangent



**Returns:** Vector3


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
<tbody><tr><td>transform</td><td>Transform</td><td></td></tr></tbody></table>






### Path:TransformBy



**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>transform</td><td>Transform</td><td></td></tr></tbody></table>






### Path:TranslateBy



**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>amount</td><td>Vector3</td><td></td></tr></tbody></table>






### Path:RotateBy



**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>amount</td><td>Rotation</td><td></td></tr></tbody></table>






### Path:ScaleBy



**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>scale</td><td>Vector3</td><td></td></tr></tbody></table>






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
<tbody><tr><td>point</td><td>Vector3</td><td></td></tr></tbody></table>






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



**Returns:** Path


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>startTransform</td><td>Transform</td><td></td></tr>
<tr><td>endTransform</td><td>Transform</td><td></td></tr>
<tr><td>startTangent</td><td>Vector3</td><td></td></tr>
<tr><td>endTangent</td><td>Vector3</td><td></td></tr>
<tr><td>resolution</td><td>number</td><td></td></tr>
<tr><td>tangentStrength</td><td>number</td><td></td></tr></tbody></table>






