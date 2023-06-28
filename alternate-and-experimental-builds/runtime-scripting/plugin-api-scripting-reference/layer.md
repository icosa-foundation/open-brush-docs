
# Layer

## Summary

A layer in the current sketch


## Properties

<table>
<thead><tr><th width="225">Name</th><th width="160">Return Type</th><th>Description</th></tr></thead>
<tbody>
<tr><td>index</td><td>number</td><td>Gets the index of the layer in the layer canvases</td></tr>
<tr><td>active</td><td>boolean</td><td>Gets or sets a value indicating whether the layer is active</td></tr>
<tr><td>transform</td><td><a href="transform.md">Transform</a></td><td>Gets or sets the transform of the layer</td></tr>
<tr><td>position</td><td><a href="vector3.md">Vector3</a></td><td>The 3D position of the Layer (specifically the position of it's anchor point</td></tr>
<tr><td>rotation</td><td><a href="rotation.md">Rotation</a></td><td>Gets or sets the rotation of the layer in 3D space</td></tr>
<tr><td>scale</td><td>number</td><td>Gets or sets the scale of the layer</td></tr>
<tr><td></td><td></td><td></td></tr></tbody></table>




## Methods


### Layer:New()

Creates and returns a new instance of a Layer

**Returns:** <a href="layer.md">Layer</a>






### Layer:CenterPivot()

Centers the pivot of the layer

**Returns:** nil






### Layer:ShowPivot()

Shows the pivot of the layer

**Returns:** nil






### Layer:HidePivot()

Hides the pivot of the layer

**Returns:** nil






### Layer:Clear()

Clears the layer

**Returns:** nil






### Layer:Delete()

Deletes the layer

**Returns:** nil






### Layer:Squash()

Squashes the layer and returns the resulting LayerApiWrapper instance

**Returns:** <a href="layer.md">Layer</a>






### Layer:SquashTo(destinationLayer)

Squashes the layer to the specified destination layer and returns the destination layer

**Returns:** <a href="layer.md">Layer</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>destinationLayer</td><td><a href="layer.md">Layer</a></td><td>The destination layer</td></tr></tbody></table>






### Layer:Show()

Shows the layer

**Returns:** nil






### Layer:Hide()

Hides the layer

**Returns:** nil






### Layer:Toggle()

Toggles the visibility of the layer

**Returns:** nil






