
# Image

## Summary

A reference image widget


## Properties

<table>
<thead><tr><th width="225">Name</th><th width="160">Return Type</th><th>Description</th></tr></thead>
<tbody>
<tr><td>index</td><td>number</td><td></td></tr>
<tr><td>transform</td><td><a href="transform.md">Transform</a></td><td></td></tr>
<tr><td>position</td><td><a href="vector3.md">Vector3</a></td><td></td></tr>
<tr><td>rotation</td><td><a href="rotation.md">Rotation</a></td><td></td></tr>
<tr><td>scale</td><td>number</td><td></td></tr>
<tr><td></td><td></td><td></td></tr></tbody></table>




## Methods


### Image:Extrude



**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>depth</td><td>number</td><td></td></tr>
<tr><td>color</td><td><a href="color.md">Color</a></td><td></td></tr></tbody></table>






### Image:Import



**Returns:** <a href="image.md">Image</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>location</td><td>string</td><td></td></tr></tbody></table>






### Image:Select



**Returns:** nil






### Image:Delete



**Returns:** nil






### Image:FormEncode



**Returns:** string






### Image:SaveBase64

Saves an image as a png based on base64 data

**Returns:** string


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>base64</td><td>string</td><td>The base64 data for the image</td></tr>
<tr><td>filename</td><td>string</td><td>The filename to save as</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>App:SaveBase64(someData, "image.png")</strong></code></pre>




