
# Headset

## Summary
The user's headset



## Class Methods

        
### Headset:ResizeHistory(size)

Clears the history and sets it's size

**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>size</td><td>number</td><td>How many frames of position/rotation to remember</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>Headset.size = 4</strong></code></pre>




### Headset:SetHistorySize(size)

Sets the size of the history. Only clears it if the size has changed

**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>size</td><td>number</td><td>How many frames of position/rotation to remember</td></tr></tbody></table>






### Headset:PastPosition(back)

Recalls previous positions of the Headset from the history buffer

**Returns:** <a href="vector3.md">Vector3</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>back</td><td>number</td><td>How many frames back in the history to look</td></tr></tbody></table>






### Headset:PastRotation(back)

Recalls previous orientations of the Headset from the history buffer

**Returns:** <a href="rotation.md">Rotation</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>back</td><td>number</td><td>How many frames back in the history to look</td></tr></tbody></table>





    

