
# Guide

## Summary

A guide widget


## Properties

<table>
<thead><tr><th width="225">Name</th><th width="160">Return Type</th><th>Description</th></tr></thead>
<tbody>
<tr><td>index</td><td>number</td><td>The index of the active widget</td></tr>
<tr><td>transform</td><td><a href="transform.md">Transform</a></td><td>The transform of the Guide Widget</td></tr>
<tr><td>position</td><td><a href="vector3.md">Vector3</a></td><td>The 3D position of the Guide Widget</td></tr>
<tr><td>rotation</td><td><a href="rotation.md">Rotation</a></td><td>The 3D orientation of the Guide Widget</td></tr>
<tr><td>scale</td><td>number</td><td>The scale of the Guide Widget</td></tr>
<tr><td></td><td></td><td></td></tr></tbody></table>




## Methods


### Guide:NewCube(transform)

Creates a new cube guide with a default size using the transform for position and orientation

**Returns:** <a href="guide.md">Guide</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>transform</td><td><a href="transform.md">Transform</a></td><td>The transform of the Guide Widget</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>myGuide = Guide:NewCube(Transform:New(0, 5, 2)</strong></code></pre>




### Guide:NewSphere(transform)

Creates a new sphere guide with a default size using the transform for position and orientation

**Returns:** <a href="guide.md">Guide</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>transform</td><td><a href="transform.md">Transform</a></td><td>The transform of the Guide Widget</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>myGuide = Guide:NewSphere(Transform:New(0, 5, 2)</strong></code></pre>




### Guide:NewCapsule(transform)

Creates a new capsule guide with a default size using the transform for position and orientation

**Returns:** <a href="guide.md">Guide</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>transform</td><td><a href="transform.md">Transform</a></td><td>The transform of the Guide Widget</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>myGuide = Guide:NewCapsule(Transform:New(0, 5, 2)</strong></code></pre>




### Guide:NewCone(transform)

Creates a new cone guide with a default size using the transform for position and orientation

**Returns:** <a href="guide.md">Guide</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>transform</td><td><a href="transform.md">Transform</a></td><td>The transform of the Guide Widget</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>myGuide = Guide:NewCone(Transform:New(0, 5, 2)</strong></code></pre>




### Guide:NewEllipsoid(transform)

Creates a new ellipsoid guide with a default size using the transform for position and orientation

**Returns:** <a href="guide.md">Guide</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>transform</td><td><a href="transform.md">Transform</a></td><td>The transform of the Guide Widget</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>myGuide = Guide:NewEllipsoid(Transform:New(0, 5, 2)</strong></code></pre>




### Guide:NewCustom(transform, model)

Creates a new custom guide with a default size using the transform for position and orientation

**Returns:** <a href="guide.md">Guide</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>transform</td><td><a href="transform.md">Transform</a></td><td>The transform of the Guide Widget</td></tr>
<tr><td>model</td><td><a href="model.md">Model</a></td><td>The ModelApiWrapper to use for the custom stencil</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>myGuide = Guide:NewCustom(Transform:New(0, 5, 2), myModel</strong></code></pre>




### Guide:Select()

Adds the guide to the current selection

**Returns:** nil




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>myGuide:Select()</strong></code></pre>




### Guide:Delete()

Deletes the guide

**Returns:** nil




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>myGuide:Delete()</strong></code></pre>




### Guide:Scale(scale)

Scales the guide (scale can be non-uniform as some guide types can be stretched)

**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>scale</td><td><a href="vector3.md">Vector3</a></td><td>The scale vector for scaling the Guide Widget</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>myGuide:Scale(Vector3:New(2, 0, 0)</strong></code></pre>




