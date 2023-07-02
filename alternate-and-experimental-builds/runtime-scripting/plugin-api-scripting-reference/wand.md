
# Wand

## Summary
Represents the user's wand (the controller that isn't the brush controller)

## Class Properties

<table>
<thead><tr><th width="225">Name</th><th width="160">Return Type</th><th width="80">Read/Write?</th><th>Description</th></tr></thead>
<tbody>
<tr><td>position</td><td><a href="vector3.md">Vector3</a></td><td>Read-only</td><td>The 3D position of the Wand Controller</td></tr>
<tr><td>rotation</td><td><a href="rotation.md">Rotation</a></td><td>Read-only</td><td>The 3D orientation of the Wand</td></tr>
<tr><td>direction</td><td><a href="vector3.md">Vector3</a></td><td>Read-only</td><td>The vector representing the forward direction of the wand controller</td></tr>
<tr><td>pressure</td><td>number</td><td>Read-only</td><td>How far the trigger on the wand contrller is pressed in</td></tr>
<tr><td>speed</td><td><a href="vector3.md">Vector3</a></td><td>Read-only</td><td>How fast the wand contrller is currently moving</td></tr>
</tbody></table>




## Class Methods

        
### Wand:ResizeHistory(size)

Clears the history and sets it's size

**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>size</td><td>number</td><td>The size of the history buffer</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>Wand.ResizeHistory(100)</strong></code></pre>




### Wand:SetHistorySize(size)

Sets the size of the history. Only clears it if the size has changed

**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>size</td><td>number</td><td>The size of the history buffer</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>Wand.SetHistorySize(100)</strong></code></pre>




### Wand:PastPosition(back)

Recalls previous positions of the Wand from the history buffer

**Returns:** <a href="vector3.md">Vector3</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>back</td><td>number</td><td>How far back in the history to get the position from</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>myPosition = Wand.PastPosition(5)</strong></code></pre>




### Wand:PastRotation(back)

Recalls previous orientations of the Wand from the history buffer

**Returns:** <a href="rotation.md">Rotation</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>back</td><td>number</td><td>How far back in the history to get the rotation from</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>myRotation = Wand.PastRotation(5)</strong></code></pre>



    

