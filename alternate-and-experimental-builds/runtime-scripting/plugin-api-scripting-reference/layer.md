
# Layer

## Summary
A layer in the current sketch


## Instance Properties

<table>
<thead><tr><th width="225">Name</th><th width="160">Return Type</th><th width="80">Read/Write?</th><th>Description</th></tr></thead>
<tbody>
<tr><td>index</td><td>number</td><td>Read-only</td><td>Gets the index of the layer in the layer canvases</td></tr>
<tr><td>active</td><td>boolean</td><td>Read/Write</td><td>Gets or sets a value indicating whether the layer is active</td></tr>
<tr><td>transform</td><td><a href="transform.md">Transform</a></td><td>Read/Write</td><td>Gets or sets the transform of the layer</td></tr>
<tr><td>position</td><td><a href="vector3.md">Vector3</a></td><td>Read/Write</td><td>The 3D position of the Layer (specifically the position of it's anchor point</td></tr>
<tr><td>rotation</td><td><a href="rotation.md">Rotation</a></td><td>Read/Write</td><td>Gets or sets the rotation of the layer in 3D space</td></tr>
<tr><td>scale</td><td>number</td><td>Read/Write</td><td>Gets or sets the scale of the layer</td></tr>
</tbody></table>



## Class Methods

        
### Layer:New()

Creates and returns a new instance of a Layer

**Returns:** <a href="layer.md">Layer</a>  (The new instance of LayerApiWrapper)




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>Layer:New()</strong></code></pre>



    

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
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
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



    
