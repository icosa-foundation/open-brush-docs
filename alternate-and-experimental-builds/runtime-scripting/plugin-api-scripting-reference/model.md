
# Model

## Summary
A 3D model widget


## Instance Properties

<table>
<thead><tr><th width="225">Name</th><th width="160">Return Type</th><th width="80">Read/Write?</th><th>Description</th></tr></thead>
<tbody>
<tr><td>index</td><td>number</td><td>Read-only</td><td>No</td><td></td></tr>
<tr><td>transform</td><td><a href="transform.md">Transform</a></td><td>Read/Write</td><td>No</td><td></td></tr>
<tr><td>position</td><td><a href="vector3.md">Vector3</a></td><td>Read/Write</td><td>No</td><td>The 3D position of the Model Widget</td></tr>
<tr><td>rotation</td><td><a href="rotation.md">Rotation</a></td><td>Read/Write</td><td>No</td><td>The 3D orientation of the Model Widget</td></tr>
<tr><td>scale</td><td>number</td><td>Read/Write</td><td>No</td><td>The scale of the Model Widget</td></tr>
</tbody></table>



## Class Methods

        
### Model:Import(location)

Method to import a new model at a specific location. Returns a wrapper of the imported model's API

**Returns:** <a href="model.md">Model</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>location</td><td>string</td><td></td></tr></tbody></table>





    

## Instance Methods

        
### model:Select()

Method to select the current Model Widget in the API

**Returns:** nil






### model:Delete()

Method to delete the current Model Widget from the API

**Returns:** nil





    
