
# CameraPathList

## Summary
The list of Camera Paths in the scene. (You don't instantiate this yourself. Access this via Sketch.cameraPaths 


## Instance Properties

<table>
<thead><tr><th width="225">Name</th><th width="160">Return Type</th><th width="80">Read/Write?</th><th>Description</th></tr></thead>
<tbody>
<tr><td>last</td><td><a href="camerapath.md">CameraPath</a></td><td>Read-only</td><td>Returns the last CameraPathApiWrapper in the list</td></tr>
<tr><td>Item</td><td><a href="camerapath.md">CameraPath</a></td><td>Read-only</td><td>Gets the CameraPathApiWrapper at the specified index</td></tr>
<tr><td>count</td><td>number</td><td>Read-only</td><td>Gets the number of CameraPathWidgets in the list</td></tr>
<tr><td>active</td><td><a href="camerapathwidget.md">CameraPathWidget</a></td><td>Read/Write</td><td>Gets or sets the active CameraPathWidget</td></tr>
</tbody></table>




## Instance Methods

        
### cameraPathList:ShowAll()

Shows all CameraPaths in the list

**Returns:** nil






### cameraPathList:HideAll()

Hides all CameraPaths in the list

**Returns:** nil






### cameraPathList:PreviewActivePath(active)

Previews the active path

**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>active</td><td>boolean</td><td>A boolean value indicating whether to preview the active path or not</td></tr></tbody></table>





    
