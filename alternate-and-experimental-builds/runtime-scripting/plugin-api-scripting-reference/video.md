
# Video

## Summary
A video widget


## Instance Properties

<table>
<thead><tr><th width="225">Name</th><th width="160">Return Type</th><th width="80">Read/Write?</th><th>Description</th></tr></thead>
<tbody>
<tr><td>index</td><td>number</td><td>Read-only</td><td>Gets the index of this Video</td></tr>
<tr><td>transform</td><td><a href="transform.md">Transform</a></td><td>Read/Write</td><td>Gets or sets the Transform (position, rotation, scale) of the Video Widget</td></tr>
<tr><td>position</td><td><a href="vector3.md">Vector3</a></td><td>Read/Write</td><td>The 3D position of the Video Widget</td></tr>
<tr><td>rotation</td><td><a href="rotation.md">Rotation</a></td><td>Read/Write</td><td>The 3D orientation of the Video Widget</td></tr>
<tr><td>scale</td><td>number</td><td>Read/Write</td><td>Gets or sets the scale of the Video Widget</td></tr>
</tbody></table>



## Class Methods

        
### Video:Import(location)

Imports a video file from the user's MediaLibrary/Videos folder

**Returns:** <a href="video.md">Video</a> 


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>location</td><td>string</td><td>The filename of the video file to import from the user's MediaLibrary/Videos folder</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>myVideo = Video.Import("myVideo.mp4")</strong></code></pre>



    

## Instance Methods

        
### video:Select()

Adds this Video Widget to the current selection

**Returns:** nil 




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>myVideo:Select()</strong></code></pre>




### video:Delete()

Deletes this Video Widget

**Returns:** nil 




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>myVideo:Delete()</strong></code></pre>



    
