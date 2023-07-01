
# Brush

## Summary
The user's brush

## Class Properties

<table>
<thead><tr><th width="225">Name</th><th width="160">Return Type</th><th width="80">Read/Write?</th><th>Description</th></tr></thead>
<tbody>
<tr><td>timeSincePressed</td><td>number</td><td>Read-only</td><td>Time in seconds since the brush trigger was last pressed</td></tr>
<tr><td>timeSinceReleased</td><td>number</td><td>Read-only</td><td>Time in seconds since the brush trigger was last released</td></tr>
<tr><td>triggerIsPressed</td><td>boolean</td><td>Read-only</td><td>Check whether the brush trigger is currently pressed</td></tr>
<tr><td>triggerIsPressedThisFrame</td><td>boolean</td><td>Read-only</td><td>Check whether the brush trigger was pressed in the current frame</td></tr>
<tr><td>distanceMoved</td><td>number</td><td>Read-only</td><td>The distance moved by the brush</td></tr>
<tr><td>distanceDrawn</td><td>number</td><td>Read-only</td><td>The distance drawn by the brush (i.e. distance since the trigger was last pressed)</td></tr>
<tr><td>position</td><td><a href="vector3.md">Vector3</a></td><td>Read-only</td><td>The 3D position of the Brush Controller's tip</td></tr>
<tr><td>rotation</td><td><a href="rotation.md">Rotation</a></td><td>Read-only</td><td>The 3D orientation of the Brush Controller's tip</td></tr>
<tr><td>direction</td><td><a href="vector3.md">Vector3</a></td><td>Read-only</td><td>The vector representing the forward direction of the brush</td></tr>
<tr><td>size</td><td>number</td><td>Read/Write</td><td>The current brush size</td></tr>
<tr><td>pressure</td><td>number</td><td>Read-only</td><td>Brush pressure is determined by how far the trigger is pressed in</td></tr>
<tr><td>type</td><td>string</td><td>Read/Write</td><td>The current brush type</td></tr>
<tr><td>types</td><td>string[]</td><td>Read-only</td><td>All available brush types</td></tr>
<tr><td>speed</td><td>number</td><td>Read-only</td><td>How fast the brush is currently moving</td></tr>
<tr><td>colorRgb</td><td><a href="color.md">Color</a></td><td>Read/Write</td><td>Gets or set brush color</td></tr>
<tr><td>colorHsv</td><td><a href="vector3.md">Vector3</a></td><td>Read/Write</td><td>Gets or set brush color using a Vector3 representing hue, saturation and brightness</td></tr>
<tr><td>colorHtml</td><td>string</td><td>Read/Write</td><td>The color of the brush as a valid HTML color string (either hex values or a color name)</td></tr>
<tr><td>lastColorPicked</td><td><a href="color.md">Color</a></td><td>Read-only</td><td>The last color picked by the brush.</td></tr>
<tr><td>LastColorPickedHsv</td><td><a href="vector3.md">Vector3</a></td><td>Read-only</td><td>The last color picked by the brush in HSV.</td></tr>
<tr><td>currentPath</td><td><a href="path.md">Path</a></td><td>Read/Write</td><td>Gets or sets the current path of the brush. Assumes a stroke is in progress.</td></tr>
</tbody></table>




## Class Methods

        
### Brush:JitterColor()

Applies the current jitter settings to the brush color

**Returns:** nil




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>Brush:JitterColor()</strong></code></pre>




### Brush:ResizeHistory(size)

Clears the history and sets it's size

**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>size</td><td>number</td><td>How many frames of position/rotation to remember</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>Brush:ResizeHistory(10)</strong></code></pre>




### Brush:SetHistorySize(size)

Sets the size of the history. Only clears it if the size has changed

**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>size</td><td>number</td><td>How many frames of position/rotation to remember</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>Brush:SetHistorySize(10)</strong></code></pre>




### Brush:GetPastPosition(back)

Recalls previous positions of the Brush from the history buffer

**Returns:** <a href="vector3.md">Vector3</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>back</td><td>number</td><td>How many frames back in the history to look</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>Brush:GetPastPosition(3)</strong></code></pre>




### Brush:GetPastRotation(back)

Recalls previous orientations of the Brush from the history buffer

**Returns:** <a href="rotation.md">Rotation</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>back</td><td>number</td><td>How many frames back in the history to look</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>Brush:GetPastRotation(3)</strong></code></pre>




### Brush:ForcePaintingOn(active)

If set to true then the brush will draw strokes even if the trigger isn't being pressed.

**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>active</td><td>boolean</td><td>True means forced painting, false is normal behaviour</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>Brush:ForcePaintingOn(true)</strong></code></pre>




### Brush:ForcePaintingOff(active)

If set to true then the brush will stop drawing strokes even if the trigger is still pressed.

**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>active</td><td>boolean</td><td>True means painting is forced off, false is normal behaviour</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>Brush:ForcePaintingOff(true)</strong></code></pre>




### Brush:ForceNewStroke()

Forces the start of a new stroke - will stop painting this frame and start again the next.

**Returns:** nil




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>Brush:ForceNewStroke(true)</strong></code></pre>



    

