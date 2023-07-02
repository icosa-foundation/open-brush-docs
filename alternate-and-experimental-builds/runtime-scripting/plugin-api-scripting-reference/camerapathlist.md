
# CameraPathList

## Summary
The list of Camera Paths in the scene. (You don't instantiate this yourself. Access this via Sketch.cameraPaths)


## Instance Properties

<table>
<thead><tr><th width="225">Name</th><th width="160">Return Type</th><th width="80">Read/Write?</th><th>Description</th></tr></thead>
<tbody>
<tr><td>last</td><td><a href="camerapath.md">CameraPath</a></td><td>Read-only</td><td>Returns the last Camera Path</td></tr>
<tr><td>Item</td><td><a href="camerapath.md">CameraPath</a></td><td>Read-only</td><td>Gets a Camera Path by it's index</td></tr>
<tr><td>count</td><td>number</td><td>Read-only</td><td>The number of Camera Paths</td></tr>
<tr><td>active</td><td><a href="camerapathwidget.md">CameraPathWidget</a></td><td>Read/Write</td><td>Gets or sets the active Camera Path</td></tr>
</tbody></table>




## Instance Methods

        
### cameraPathList:ShowAll()

Makes all Camera Paths visible

**Returns:** nil 




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>Sketch.cameraPaths:ShowAll()</strong></code></pre>




### cameraPathList:HideAll()

Hides all Camera Paths

**Returns:** nil 




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>Sketch:cameraPaths:HideAll()</strong></code></pre>




### cameraPathList:PreviewActivePath(active)

Sets whether to preview the active path or not

**Returns:** nil 


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>active</td><td>boolean</td><td>A boolean value indicating whether to preview the active path or not</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>Sketch.cameraPaths:PreviewActivePath(true)</strong></code></pre>



    
