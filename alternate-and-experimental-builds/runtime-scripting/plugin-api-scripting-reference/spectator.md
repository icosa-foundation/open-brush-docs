
# Spectator

## Summary
The spectator camera

## Class Properties

<table>
<thead><tr><th width="225">Name</th><th width="160">Return Type</th><th width="80">Read/Write?</th><th>Description</th></tr></thead>
<tbody>
<tr><td>canSeeWidgets</td><td>boolean</td><td>Read/Write</td><td>Sets whether Widgets are visible to the spectator camera</td></tr>
<tr><td>canSeeStrokes</td><td>boolean</td><td>Read/Write</td><td>Sets whether Strokes are visible to the spectator camera</td></tr>
<tr><td>canSeeSelection</td><td>boolean</td><td>Read/Write</td><td>Sets whether Selection are visible to the spectator camera</td></tr>
<tr><td>canSeeHeadset</td><td>boolean</td><td>Read/Write</td><td>Sets whether Headset are visible to the spectator camera</td></tr>
<tr><td>canSeePanels</td><td>boolean</td><td>Read/Write</td><td>Sets whether Panels are visible to the spectator camera</td></tr>
<tr><td>canSeeUi</td><td>boolean</td><td>Read/Write</td><td>Sets whether Ui are visible to the spectator camera</td></tr>
<tr><td>canSeeUsertools</td><td>boolean</td><td>Read/Write</td><td>Sets whether Usertools are visible to the spectator camera</td></tr>
<tr><td>active</td><td>boolean</td><td>Read/Write</td><td>Is the spectator camera currently active?</td></tr>
<tr><td>position</td><td><a href="vector3.md">Vector3</a></td><td>Read/Write</td><td>The 3D position of the Spectator Camera Widget</td></tr>
<tr><td>rotation</td><td><a href="rotation.md">Rotation</a></td><td>Read/Write</td><td>The 3D orientation of the Spectator Camera</td></tr>
<tr><td>lockedToScene</td><td>boolean</td><td>Read/Write</td><td>Sets whether the spectator camera moves with the scene or with the user</td></tr>
</tbody></table>




## Class Methods

        
### Spectator:Direction(direction)

Changes the rotation of the spectator camera to a specific direction vector

**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>direction</td><td><a href="vector3.md">Vector3</a></td><td></td></tr></tbody></table>






### Spectator:LookAt(position)

Changes the rotation of the spectator camera to look towards a specific point

**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>position</td><td><a href="vector3.md">Vector3</a></td><td></td></tr></tbody></table>






### Spectator:Stationary()

Sets the spectator camera's movement mode to stationary

**Returns:** nil






### Spectator:SlowFollow()

Sets the spectator camera's movement mode to slowFollow

**Returns:** nil






### Spectator:Wobble()

Sets the spectator camera's movement mode to wobble

**Returns:** nil






### Spectator:Circular()

Sets the spectator camera's movement mode to circular

**Returns:** nil





    

