
# Rotation

## Summary
Represents a rotation or orientation in 3D space. See https://docs.unity3d.com/ScriptReference/Quaternion.html for further documentation

## Class Properties

<table>
<thead><tr><th width="225">Name</th><th width="160">Return Type</th><th width="80">Read/Write?</th><th>Description</th></tr></thead>
<tbody>
<tr><td>zero</td><td><a href="rotation.md">Rotation</a></td><td>Read-only</td><td>A rotation of zero in all axes</td></tr>
<tr><td>left</td><td><a href="rotation.md">Rotation</a></td><td>Read-only</td><td>A 90 degree anti-clockwise rotation in the y axis (yaw)</td></tr>
<tr><td>right</td><td><a href="rotation.md">Rotation</a></td><td>Read-only</td><td>A 90 degree clockwise rotation in the y axis (yaw)</td></tr>
<tr><td>up</td><td><a href="rotation.md">Rotation</a></td><td>Read-only</td><td>A 90 degree clockwise rotation in the x axis (pitch)</td></tr>
<tr><td>down</td><td><a href="rotation.md">Rotation</a></td><td>Read-only</td><td>A 90 degree anti-clockwise rotation in the x axis (pitch)</td></tr>
<tr><td>anticlockwise</td><td><a href="rotation.md">Rotation</a></td><td>Read-only</td><td>A 90 degree anti-clockwise rotation in the z axis (roll)</td></tr>
<tr><td>clockwise</td><td><a href="rotation.md">Rotation</a></td><td>Read-only</td><td>A 90 degree clockwise rotation in the z axis (roll)</td></tr>
</tbody></table>



## Instance Properties

<table>
<thead><tr><th width="225">Name</th><th width="160">Return Type</th><th width="80">Read/Write?</th><th>Description</th></tr></thead>
<tbody>
<tr><td>Item</td><td>number</td><td>Read/Write</td><td>The amount of rotation in degrees around a single axis (0=x, 1=y, 2=z)</td></tr>
<tr><td>x</td><td>number</td><td>Read/Write</td><td>The amount of rotation around the x axis in degrees</td></tr>
<tr><td>y</td><td>number</td><td>Read/Write</td><td>The amount of rotation around the y axis in degrees</td></tr>
<tr><td>z</td><td>number</td><td>Read/Write</td><td>The amount of rotation around the z axis in degrees</td></tr>
<tr><td>normalized</td><td><a href="rotation.md">Rotation</a></td><td>Read-only</td><td>Converts this rotation to one with the same orientation but with a magnitude of 1</td></tr>
</tbody></table>



## Class Methods

        
### Rotation:New(x, y, z)



**Returns:** <a href="rotation.md">Rotation</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>x</td><td>number</td><td></td></tr>
<tr><td>y</td><td>number</td><td></td></tr>
<tr><td>z</td><td>number</td><td></td></tr></tbody></table>






### Rotation:Angle(a, b)

Returns the angle in degrees between two rotations

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td><a href="rotation.md">Rotation</a></td><td>The first rotation angle</td></tr>
<tr><td>b</td><td><a href="rotation.md">Rotation</a></td><td>The second rotation angle</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>result = Rotation:Angle(a, b)</strong></code></pre>




### Rotation:AngleAxis(angle, axis)

Creates a rotation which rotates angle degrees around axis

**Returns:** <a href="rotation.md">Rotation</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>angle</td><td>number</td><td>The angle in degrees</td></tr>
<tr><td>axis</td><td><a href="vector3.md">Vector3</a></td><td>The axis of rotation</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>result = Rotation:AngleAxis(angle, axis)</strong></code></pre>




### Rotation:Dot(a, b)

The dot product between two rotations

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td><a href="rotation.md">Rotation</a></td><td>The first rotation</td></tr>
<tr><td>b</td><td><a href="rotation.md">Rotation</a></td><td>The second rotation</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>result = Rotation:Dot(a, b)</strong></code></pre>




### Rotation:FromToRotation(from, to)

Creates a rotation which rotates from fromDirection to toDirection

**Returns:** <a href="rotation.md">Rotation</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>from</td><td><a href="vector3.md">Vector3</a></td><td>The initial direction vector</td></tr>
<tr><td>to</td><td><a href="vector3.md">Vector3</a></td><td>The target direction vector</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>result = Rotation:FromToRotation(from, to)</strong></code></pre>




### Rotation:Inverse(a)

Returns the Inverse of a rotation

**Returns:** <a href="rotation.md">Rotation</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td><a href="rotation.md">Rotation</a></td><td>The rotation to invert</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>result = Rotation:Inverse(a)</strong></code></pre>




### Rotation:Lerp(a, b, t)

Interpolates between a and b by t and normalizes the result afterwards. The parameter t is clamped to the range [0, 1]

**Returns:** <a href="rotation.md">Rotation</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td><a href="rotation.md">Rotation</a></td><td>The first rotation</td></tr>
<tr><td>b</td><td><a href="rotation.md">Rotation</a></td><td>The second rotation</td></tr>
<tr><td>t</td><td>number</td><td>A ratio between 0 and 1</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>result = Rotation:Lerp(a, b, t)</strong></code></pre>




### Rotation:LerpUnclamped(a, b, t)

Interpolates between a and b by t and normalizes the result afterwards. The parameter t is not clamped

**Returns:** <a href="rotation.md">Rotation</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td><a href="rotation.md">Rotation</a></td><td>The first rotation</td></tr>
<tr><td>b</td><td><a href="rotation.md">Rotation</a></td><td>The second rotation</td></tr>
<tr><td>t</td><td>number</td><td>A ratio between 0 and 1</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>result = Rotation:LerpUnclamped(a, b, t)</strong></code></pre>




### Rotation:LookRotation(forward)

Creates a rotation with the specified forward and upwards directions

**Returns:** <a href="rotation.md">Rotation</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>forward</td><td><a href="vector3.md">Vector3</a></td><td>Vector3 forward direction</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>result = Rotation:LookRotation(forward)</strong></code></pre>




### Rotation:LookRotation(forward, up)

Creates a rotation with the specified forward and upwards directions

**Returns:** <a href="rotation.md">Rotation</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>forward</td><td><a href="vector3.md">Vector3</a></td><td>Vector3 forward direction</td></tr>
<tr><td>up</td><td><a href="vector3.md">Vector3</a></td><td>Vector3 up direction</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>result = Rotation:LookRotation(forward, up)</strong></code></pre>




### Rotation:Normalize(a)

Converts this quaternion to one with the same orientation but with a magnitude of 1

**Returns:** <a href="rotation.md">Rotation</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td><a href="rotation.md">Rotation</a></td><td>The input rotation</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>result = Rotation:Normalize(a)</strong></code></pre>




### Rotation:RotateTowards(from, to, maxDegreesDelta)

Rotates a rotation from towards to

**Returns:** <a href="rotation.md">Rotation</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>from</td><td><a href="rotation.md">Rotation</a></td><td>Rotation from</td></tr>
<tr><td>to</td><td><a href="rotation.md">Rotation</a></td><td>Rotation to</td></tr>
<tr><td>maxDegreesDelta</td><td>number</td><td>Max degrees delta</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>result = Rotation:RotateTowards(to, maxDegreesDelta)</strong></code></pre>




### Rotation:Slerp(a, b, t)

Spherically interpolates between quaternions a and b by ratio t. The parameter t is clamped to the range [0, 1]

**Returns:** <a href="rotation.md">Rotation</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td><a href="rotation.md">Rotation</a></td><td>The first rotation</td></tr>
<tr><td>b</td><td><a href="rotation.md">Rotation</a></td><td>The second rotation</td></tr>
<tr><td>t</td><td>number</td><td>A ratio between 0 and 1</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>result = Rotation:Slerp(a, b, t)</strong></code></pre>




### Rotation:SlerpUnclamped(a, b, t)

Spherically interpolates between a and b by t. The parameter t is not clamped

**Returns:** <a href="rotation.md">Rotation</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td><a href="rotation.md">Rotation</a></td><td>The first rotation</td></tr>
<tr><td>b</td><td><a href="rotation.md">Rotation</a></td><td>The second rotation</td></tr>
<tr><td>t</td><td>number</td><td>A ratio</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>result = Rotation:SlerpUnclamped(a, b, t)</strong></code></pre>



    

## Instance Methods

        
### rotation:SetFromToRotation(fromDirection, toDirection)

Creates a rotation which rotates from one direction to another

**Returns:** <a href="rotation.md">Rotation</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>fromDirection</td><td><a href="vector3.md">Vector3</a></td><td>The starting direction</td></tr>
<tr><td>toDirection</td><td><a href="vector3.md">Vector3</a></td><td>The target direction</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>newRot = myRotation:SetFromToRotation(Vector3:New(0, 5, 5), Vector3:New(5, 5, 0))</strong></code></pre>




### rotation:SetLookRotation(view)

Creates a rotation with the specified forward directions

**Returns:** <a href="rotation.md">Rotation</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>view</td><td><a href="vector3.md">Vector3</a></td><td>The direction to look in</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>result = myRotation:SetLookRotation(view)</strong></code></pre>




### rotation:SetLookRotation(view, up)

Creates a rotation with the specified forward and upwards directions

**Returns:** <a href="rotation.md">Rotation</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>view</td><td><a href="vector3.md">Vector3</a></td><td>The direction to look in</td></tr>
<tr><td>up</td><td><a href="vector3.md">Vector3</a></td><td>The vector that defines in which direction is up</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>result = myRotation:SetLookRotation(view, up)</strong></code></pre>




### rotation:ToAngleAxis()

Converts a rotation to angle-axis representation

**Returns:** <a href="system.collections.generic.list`1[system.single].md">System.Collections.Generic.List`1[System.Single]</a>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>result = myRotation:ToAngleAxis()</strong></code></pre>




### rotation:Multiply(other)

Combines two rotations

**Returns:** <a href="rotation.md">Rotation</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>other</td><td><a href="rotation.md">Rotation</a></td><td>The other rotation</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>result = myRotation:Multiply(anotherRotation)</strong></code></pre>



    
