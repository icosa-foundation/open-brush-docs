
# Transform

## Summary
Represents a position, rotation and scale in one object

## Class Properties

<table>
<thead><tr><th width="225">Name</th><th width="160">Return Type</th><th width="80">Read/Write?</th><th>Description</th></tr></thead>
<tbody>
<tr><td>identity</td><td><a href="transform.md">Transform</a></td><td>Read-only</td><td>A transform that does nothing. No translation, rotation or scaling</td></tr>
</tbody></table>



## Instance Properties

<table>
<thead><tr><th width="225">Name</th><th width="160">Return Type</th><th width="80">Read/Write?</th><th>Description</th></tr></thead>
<tbody>
<tr><td>inverse</td><td><a href="transform.md">Transform</a></td><td>Read-only</td><td>The inverse of this transform</td></tr>
<tr><td>up</td><td><a href="vector3.md">Vector3</a></td><td>Read-only</td><td>A translation of 1 in the y axis</td></tr>
<tr><td>down</td><td><a href="vector3.md">Vector3</a></td><td>Read-only</td><td>A translation of -1 in the y axis</td></tr>
<tr><td>right</td><td><a href="vector3.md">Vector3</a></td><td>Read-only</td><td>A translation of 1 in the x axis</td></tr>
<tr><td>left</td><td><a href="vector3.md">Vector3</a></td><td>Read-only</td><td>A translation of -1 in the x axis</td></tr>
<tr><td>forward</td><td><a href="vector3.md">Vector3</a></td><td>Read-only</td><td>A translation of 1 in the z axis</td></tr>
<tr><td>back</td><td><a href="vector3.md">Vector3</a></td><td>Read-only</td><td>A translation of -1 in the z axis</td></tr>
<tr><td>position</td><td><a href="vector3.md">Vector3</a></td><td>Read/Write</td><td>Get or set the position of this transform</td></tr>
<tr><td>rotation</td><td><a href="rotation.md">Rotation</a></td><td>Read/Write</td><td>Get or set the rotation of this transform</td></tr>
<tr><td>scale</td><td>number</td><td>Read/Write</td><td>Get or set the scale of this transform</td></tr>
</tbody></table>



## Class Methods

        
### Transform:NewTRS(translation, rotation, scale)

Creates a new translation, rotation and scale transform

**Returns:** <a href="transform.md">Transform</a> 


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>translation</td><td><a href="vector3.md">Vector3</a></td><td>The translation amount</td></tr>
<tr><td>rotation</td><td><a href="rotation.md">Rotation</a></td><td>The rotation amount</td></tr>
<tr><td>scale</td><td>number</td><td>The scale amount</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>myTransform = Transform:New(Vector3(1, 2, 3), Rotation.identity, 2)</strong></code></pre>




### Transform:New(translation)

Creates a new translation transform

**Returns:** <a href="transform.md">Transform</a> 


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>translation</td><td><a href="vector3.md">Vector3</a></td><td>The translation amount</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>myTransform = Transform:New(Vector3(1, 2, 3))</strong></code></pre>




### Transform:New(translation, scale)

Creates a new translation and scale transform

**Returns:** <a href="transform.md">Transform</a> 


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>translation</td><td><a href="vector3.md">Vector3</a></td><td>The translation amount</td></tr>
<tr><td>scale</td><td>number</td><td>The scale amount</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>myTransform = Transform:New(Vector3(1, 2, 3), 2)</strong></code></pre>




### Transform:New(x, y, z)

Creates a new translation transform based on the x, y, z values

**Returns:** <a href="transform.md">Transform</a> 


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>x</td><td>number</td><td>The x translation amount</td></tr>
<tr><td>y</td><td>number</td><td>The y translation amount</td></tr>
<tr><td>z</td><td>number</td><td>The z translation amount</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>myTransform = Transform:New(1, 2, 3)</strong></code></pre>



    

## Instance Methods

        
### transform:TransformBy(transform)

Applies another transform to this transform

**Returns:** <a href="transform.md">Transform</a> 


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>transform</td><td><a href="transform.md">Transform</a></td><td>The transform to apply</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>newTransform = myTransform:TransformBy(myOtherTransform)</strong></code></pre>




### transform:TranslateBy(translation)

Applies a translation to this transform

**Returns:** <a href="transform.md">Transform</a> 


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>translation</td><td><a href="vector3.md">Vector3</a></td><td>The translation to apply</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>newTransform = myTransform:TranslateBy(Vector3(1, 2, 3))</strong></code></pre>




### transform:RotateBy(rotation)

Applies a rotation to this transform

**Returns:** <a href="transform.md">Transform</a> 


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>rotation</td><td><a href="rotation.md">Rotation</a></td><td>The rotation to apply</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>newTransform = myTransform:RotateBy(Rotation.New(0, 45, 0))</strong></code></pre>




### transform:ScaleBy(scale)

Applies a scale to this transform

**Returns:** <a href="transform.md">Transform</a> 


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>scale</td><td>number</td><td>The scale value to apply</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>newTransform = myTransform:ScaleBy(2)</strong></code></pre>




### transform:Multiply(other)

Combines another transform with this one (Does the same as "TransformBy")

**Returns:** <a href="transform.md">Transform</a> 


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>other</td><td><a href="transform.md">Transform</a></td><td>The Transform to apply to this one</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>newTransform = myTransform:Multiply(Transform.up)</strong></code></pre>



    
