
# Stroke

## Summary
A specific brush stroke


## Instance Properties

<table>
<thead><tr><th width="225">Name</th><th width="160">Return Type</th><th width="80">Read/Write?</th><th>Description</th></tr></thead>
<tbody>
<tr><td>path</td><td><a href="path.md">Path</a></td><td>Read/Write</td><td>Gets or sets the control points of this stroke from a Path</td></tr>
<tr><td>brushType</td><td>string</td><td>Read/Write</td><td>Gets or sets the stroke's brush type</td></tr>
<tr><td>brushSize</td><td>number</td><td>Read/Write</td><td>Gets or sets the stroke's size</td></tr>
<tr><td>brushColor</td><td><a href="color.md">Color</a></td><td>Read/Write</td><td>Gets or sets the stroke's Color</td></tr>
<tr><td>layer</td><td><a href="layer.md">Layer</a></td><td>Read/Write</td><td>Gets or sets the layer the stroke is on</td></tr>
<tr><td>Item</td><td><a href="transform.md">Transform</a></td><td>Read/Write</td><td>Gets or sets a control point by index</td></tr>
<tr><td>count</td><td>number</td><td>Read-only</td><td>The number of control points in this stroke</td></tr>
</tbody></table>



## Class Methods

        
### Stroke:SelectRange(from, to)

Adds multiple strokes to the current selection

**Returns:** nil 


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>from</td><td>number</td><td>Start stroke index (0 is the first stroke that was drawn</td></tr>
<tr><td>to</td><td>number</td><td>End stroke index</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>Stroke:SelectMultiple(0, 4) --Adds the first 5 strokes on the sketch</strong></code></pre>



    

## Instance Methods

        
### stroke:ChangeMaterial(brushName)

Assigns the material from another brush type to this stroke (Experimental. Results are unpredictable and are not saved with the scene)

**Returns:** nil 


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>brushName</td><td>string</td><td>The name (or guid) of the brush to get the material from</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>myStroke.ChangeMaterial("Light")</strong></code></pre>




### stroke:Delete()

Deletes the current stroke

**Returns:** nil 




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>myStroke:Delete()</strong></code></pre>




### stroke:Select()

Adds this stroke to the current selection

**Returns:** nil 




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>myStroke:Select()</strong></code></pre>




### stroke:JoinRange(from, to)

Joins joins multiple strokes into one stroke

**Returns:** <a href="stroke.md">Stroke</a> 


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>from</td><td>number</td><td>Start stroke index (0 is the first stroke that was drawn</td></tr>
<tr><td>to</td><td>number</td><td>End stroke index</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>newStroke = Stroke:Join(0, 10)</strong></code></pre>




### stroke:JoinToPrevious()

Joins a stroke with the previous stroke

**Returns:** <a href="stroke.md">Stroke</a> 




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>newStroke = myStroke:JoinPrevious()</strong></code></pre>




### stroke:Join(stroke2)

Joins a stroke with the previous stroke

**Returns:** <a href="stroke.md">Stroke</a> 


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>stroke2</td><td><a href="stroke.md">Stroke</a></td><td>The stroke to join to this one</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>newStroke = myStroke:JoinPrevious()</strong></code></pre>




### stroke:MergeFrom(name)

Imports the file with the specified name from the user's Sketches folder and merges it's strokes into the current sketch

**Returns:** nil 


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>name</td><td>string</td><td>Name of the file to be merged</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>Stroke:MergeFrom(string name)</strong></code></pre>



    
