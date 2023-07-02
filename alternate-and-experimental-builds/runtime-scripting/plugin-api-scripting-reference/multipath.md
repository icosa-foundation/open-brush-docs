
# MultiPath

## Summary
Multiple disconnected path segments


## Instance Properties

<table data-full-width="false">
<thead><tr><th>Name</th><th>Return Type</th><th>Description</th></tr></thead>
<tbody>
<tr><td>count</td><td>number<br>Read-only</td><td>Gets the number of paths in the multipath</td></tr>
<tr><td>pointCount</td><td>number<br>Read-only</td><td>Gets the number of points in all paths in the multipath</td></tr>
</tbody></table>



## Class Methods

        
### MultiPath:New()

Creates a new empty MultiPath

**Returns:** <a href="multipath.md">MultiPath</a> 




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>MultiPathApiWrapper:New()</strong></code></pre>




### MultiPath:New(pathList)

Creates a new MultiPath from a list of Paths

**Returns:** <a href="multipath.md">MultiPath</a> 


**Parameters:**

<table data-full-width="false">
<thead><tr><th>Name</th><th>Type</th><th>Description</th></tr></thead>
<tbody><tr><td>pathList</td><td>Path[]</td><td>A list of pathApiWrapper objects.</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>MultiPathApiWrapper:New(pathList)</strong></code></pre>




### MultiPath:FromText(text)

Creates a new MultiPath from a text

**Returns:** <a href="multipath.md">MultiPath</a> 


**Parameters:**

<table data-full-width="false">
<thead><tr><th>Name</th><th>Type</th><th>Description</th></tr></thead>
<tbody><tr><td>text</td><td>string</td><td>Input text to generate a path.</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>MultiPathApiWrapper.FromText('example')</strong></code></pre>



    

## Instance Methods

        
### multiPath:Draw()

Draws this multipath using current settings

**Returns:** nil 




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>myPaths:Draw()</strong></code></pre>




### multiPath:Insert(path)

Inserts a path at the end of the multipath

**Returns:** nil 


**Parameters:**

<table data-full-width="false">
<thead><tr><th>Name</th><th>Type</th><th>Description</th></tr></thead>
<tbody><tr><td>path</td><td><a href="path.md">Path</a></td><td>The path to be inserted.</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>myPaths:Insert(myPath)</strong></code></pre>




### multiPath:Insert(path, index)

Inserts a path at the specified index of the multipath

**Returns:** nil 


**Parameters:**

<table data-full-width="false">
<thead><tr><th>Name</th><th>Type</th><th>Description</th></tr></thead>
<tbody><tr><td>path</td><td><a href="path.md">Path</a></td><td>The path to be inserted</td></tr>
<tr><td>index</td><td>number</td><td>Inserts the new path at this position in the list of paths</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>myPaths:Insert(myPath, 3)</strong></code></pre>




### multiPath:InsertPoint(transform)

Inserts a point at the end of the last path in the multipath

**Returns:** nil 


**Parameters:**

<table data-full-width="false">
<thead><tr><th>Name</th><th>Type</th><th>Description</th></tr></thead>
<tbody><tr><td>transform</td><td><a href="transform.md">Transform</a></td><td>The point to be inserted</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>myPaths:InsertPoint(myTransform)</strong></code></pre>




### multiPath:InsertPoint(transform, pathIndex, pointIndex)

Inserts a point at the specified index of the specified path

**Returns:** nil 


**Parameters:**

<table data-full-width="false">
<thead><tr><th>Name</th><th>Type</th><th>Description</th></tr></thead>
<tbody><tr><td>transform</td><td><a href="transform.md">Transform</a></td><td>The point to be inserted</td></tr>
<tr><td>pathIndex</td><td>number</td><td>Index of the path to add the point to</td></tr>
<tr><td>pointIndex</td><td>number</td><td>Inserts the point at this index in the list of points</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>myPaths:InsertPoint(myTransform, 3, 0)</strong></code></pre>




### multiPath:TransformBy(transform)

Transforms the whole set of paths

**Returns:** nil 


**Parameters:**

<table data-full-width="false">
<thead><tr><th>Name</th><th>Type</th><th>Description</th></tr></thead>
<tbody><tr><td>transform</td><td><a href="transform.md">Transform</a></td><td>A Transform specifying the translation, rotation and scale to apply</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>myPaths:TransformBy(myTransform)</strong></code></pre>




### multiPath:TranslateBy(amount)

Translates the whole set of paths by a given amount

**Returns:** nil 


**Parameters:**

<table data-full-width="false">
<thead><tr><th>Name</th><th>Type</th><th>Description</th></tr></thead>
<tbody><tr><td>amount</td><td><a href="vector3.md">Vector3</a></td><td>The amount to move the paths by</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>myPaths:TranslateBy(Vector3.up:Multiply(4))</strong></code></pre>




### multiPath:RotateBy(rotation)

Rotates the whole set of paths by a specified amount

**Returns:** nil 


**Parameters:**

<table data-full-width="false">
<thead><tr><th>Name</th><th>Type</th><th>Description</th></tr></thead>
<tbody><tr><td>rotation</td><td><a href="rotation.md">Rotation</a></td><td>The amount to rotate the paths by</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>myPaths:RotateBy(Rotation.anticlockwise)</strong></code></pre>




### multiPath:ScaleBy(scale)

Scales the whole set of paths by a specified factor

**Returns:** nil 


**Parameters:**

<table data-full-width="false">
<thead><tr><th>Name</th><th>Type</th><th>Description</th></tr></thead>
<tbody><tr><td>scale</td><td><a href="vector3.md">Vector3</a></td><td>The amount to scale the paths by</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>myPaths:ScaleBy(vector3)</strong></code></pre>




### multiPath:Center()

Offsets all points on the path so that their common center is at the origin

**Returns:** nil 




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>myPaths:Center()</strong></code></pre>




### multiPath:Normalize(size)

Scales the whole multipath to fit inside a cube of given size at the origin

**Returns:** nil 


**Parameters:**

<table data-full-width="false">
<thead><tr><th>Name</th><th>Type</th><th>Description</th></tr></thead>
<tbody><tr><td>size</td><td>number</td><td>The size of the cube to fit inside</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>myPaths:Normalize(1.5)</strong></code></pre>




### multiPath:Resample(spacing)

Resamples all paths with a specified spacing between points

**Returns:** nil 


**Parameters:**

<table data-full-width="false">
<thead><tr><th>Name</th><th>Type</th><th>Description</th></tr></thead>
<tbody><tr><td>spacing</td><td>number</td><td>The distance between each new point</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>myPaths:Resample(0.2)</strong></code></pre>




### multiPath:Join()

Joins all the paths in order connecting each end to the following start

**Returns:** <a href="path.md">Path</a>  (A single path)




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>myPaths:Join()</strong></code></pre>




### multiPath:Longest()

Returns the longest path in the multipath

**Returns:** <a href="path.md">Path</a>  (The path with the most control points)




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>path = myPaths:Longest()</strong></code></pre>



    
