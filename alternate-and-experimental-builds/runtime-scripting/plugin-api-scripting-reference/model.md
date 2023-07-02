
# Model

## Summary
A 3D model widget


## Instance Properties

<table>
<thead><tr><th width="225">Name</th><th width="160">Return Type</th><th width="80">Read/Write?</th><th>Description</th></tr></thead>
<tbody>
<tr><td>index</td><td>number</td><td>Read-only</td><td>The index of the active Model Widget</td></tr>
<tr><td>transform</td><td><a href="transform.md">Transform</a></td><td>Read/Write</td><td>The transformation of the Model Widget</td></tr>
<tr><td>position</td><td><a href="vector3.md">Vector3</a></td><td>Read/Write</td><td>The 3D position of the Model Widget</td></tr>
<tr><td>rotation</td><td><a href="rotation.md">Rotation</a></td><td>Read/Write</td><td>The 3D orientation of the Model Widget</td></tr>
<tr><td>scale</td><td>number</td><td>Read/Write</td><td>The scale of the Model Widget</td></tr>
</tbody></table>



## Class Methods

        
### Model:Import(filename)

Imports a new model from the MediaLibrary/Models folder

**Returns:** <a href="model.md">Model</a>  (Returns the Model instance)


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>filename</td><td>string</td><td>The filename of the model to be imported</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>ModelApiWrapper:Import("Andy.obj")</strong></code></pre>



    

## Instance Methods

        
### model:Select()

Adds this model to the current selection

**Returns:** nil 




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>myModel:Select()</strong></code></pre>




### model:Delete()

Deletes this model

**Returns:** nil 




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>myModel:Delete()</strong></code></pre>



    
