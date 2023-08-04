
# Layer

## Summary
A layer in the current sketch


## Instance Properties

<table data-full-width="false">
<thead><tr><th>Name</th><th>Return Type</th><th>Description</th></tr></thead>
<tbody>
<tr><td>strokes</td><td><a href="strokelist.md">StrokeList</a><br>Read-only</td><td>All the strokes on this layer</td></tr>
<tr><td>images</td><td><a href="imagelist.md">ImageList</a><br>Read-only</td><td>All the images on this layer</td></tr>
<tr><td>videos</td><td><a href="videolist.md">VideoList</a><br>Read-only</td><td>All the videos on this layer</td></tr>
<tr><td>models</td><td><a href="modellist.md">ModelList</a><br>Read-only</td><td>All the models on this layer</td></tr>
<tr><td>guides</td><td><a href="guidelist.md">GuideList</a><br>Read-only</td><td>All the guides on this layer</td></tr>
<tr><td>cameraPaths</td><td><a href="camerapathlist.md">CameraPathList</a><br>Read-only</td><td>All the camera paths on this layer</td></tr>
<tr><td>groups</td><td><a href="system.collections.generic.list`1[group].md">System.Collections.Generic.List`1[Group]</a><br>Read-only</td><td>All the groups on this layer</td></tr>
<tr><td>index</td><td>number<br>Read-only</td><td>Gets the index of the layer in the layer canvases</td></tr>
<tr><td>active</td><td>boolean<br>Read/Write</td><td>Is the layer the active layer. Making another layer inactive will make the main layer the active layer again.</td></tr>
<tr><td>transform</td><td><a href="transform.md">Transform</a><br>Read/Write</td><td>The transform of the layer</td></tr>
<tr><td>position</td><td><a href="vector3.md">Vector3</a><br>Read/Write</td><td>The 3D position of the Layer (specifically the position of it's anchor point</td></tr>
<tr><td>rotation</td><td><a href="rotation.md">Rotation</a><br>Read/Write</td><td>The rotation of the layer in 3D space</td></tr>
<tr><td>scale</td><td>number<br>Read/Write</td><td>The scale of the layer</td></tr>
</tbody></table>



## Class Methods

        
### Layer:New()

Creates a new layer

**Returns:** <a href="layer.md">Layer</a>  (The new layer)




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>myLayer = Layer:New()</strong></code></pre>



    

## Instance Methods

        
### layer:CenterPivot()

Move the pivot point of the layer to the average center of it's contents

**Returns:** nil 




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>myLayer:CenterPivot()</strong></code></pre>




### layer:ShowPivot()

Shows a visible widget indicating the pivot point of the layer

**Returns:** nil 




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>myLayer:ShowPivot()</strong></code></pre>




### layer:HidePivot()

Hides the visible widget indicating the pivot point of the layer

**Returns:** nil 




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>myLayer:HidePivot()</strong></code></pre>




### layer:Clear()

Deletes all content from the layer

**Returns:** nil 




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>myLayer:Clear()</strong></code></pre>




### layer:Delete()

Deletes the layer and all it's content

**Returns:** nil 




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>myLayer:Delete()</strong></code></pre>




### layer:Squash()

Combines this layer and the one above it. If this layer is the first layer do nothing

**Returns:** <a href="layer.md">Layer</a>  (The resulting LayerApiWrapper instance)




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>combinedLayer = myLayer:Squash()</strong></code></pre>




### layer:SquashTo(destinationLayer)

Combines this layer with the specified layer

**Returns:** nil 


**Parameters:**

<table data-full-width="false">
<thead><tr><th>Name</th><th>Type</th><th>Description</th></tr></thead>
<tbody><tr><td>destinationLayer</td><td><a href="layer.md">Layer</a></td><td>The destination layer</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>myLayer:SquashTo(otherLayer)</strong></code></pre>




### layer:Show()

Shows the layer

**Returns:** nil 




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>myLayer:Show()</strong></code></pre>




### layer:Hide()

Hides the layer

**Returns:** nil 




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>myLayer:Hide()</strong></code></pre>



    
