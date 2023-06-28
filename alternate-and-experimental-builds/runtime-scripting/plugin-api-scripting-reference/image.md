
# Image

## Summary

A reference image widget


## Properties

<table>
<thead><tr><th width="225">Name</th><th width="160">Return Type</th><th>Description</th></tr></thead>
<tbody>
<tr><td>index</td><td>number</td><td>The index of the active widget</td></tr>
<tr><td>transform</td><td><a href="transform.md">Transform</a></td><td>Gets or sets the transform of the image widget</td></tr>
<tr><td>position</td><td><a href="vector3.md">Vector3</a></td><td>The 3D position of the Image Widget</td></tr>
<tr><td>rotation</td><td><a href="rotation.md">Rotation</a></td><td>The 3D orientation of the Image Widget</td></tr>
<tr><td>scale</td><td>number</td><td>The scale of the image widget</td></tr>
<tr><td></td><td></td><td></td></tr></tbody></table>




## Methods


### Image:Extrude(depth, color)

Extrudes the image widget with the specified depth and color

**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>depth</td><td>number</td><td>The depth of the extrusion</td></tr>
<tr><td>color</td><td><a href="color.md">Color</a></td><td>The color of the extrusion</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>Image:Extrude(5, Color.green)</strong></code></pre>




### Image:Import(location)

Imports an image widget based on the specified location

**Returns:** <a href="image.md">Image</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>location</td><td>string</td><td>The location of the image</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>Image:Import("test.png")</strong></code></pre>




### Image:Select()

Selects the image widget

**Returns:** nil




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>myImage:Select()</strong></code></pre>




### Image:Delete()

Deletes the image widget

**Returns:** nil




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>myImage:Delete()</strong></code></pre>




### Image:FormEncode()

Encodes the image as a form

**Returns:** string




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>formdata = myImage:FormEncode()</strong></code></pre>




### Image:SaveBase64(base64, filename)

Saves an image as a png based on base64 data

**Returns:** string


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>base64</td><td>string</td><td>The base64 data for the image</td></tr>
<tr><td>filename</td><td>string</td><td>The filename to save as</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>Image:SaveBase64(someData, "image.png")</strong></code></pre>




