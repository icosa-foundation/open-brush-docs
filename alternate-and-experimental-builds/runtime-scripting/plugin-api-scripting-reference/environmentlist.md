
# EnvironmentList

## Summary
The list of available environments. (You don't instantiate this yourself. Access this via Sketch.environments)


## Instance Properties

<table data-full-width="false">
<thead><tr><th>Name</th><th>Return Type</th><th>Description</th></tr></thead>
<tbody>
<tr><td>last</td><td><a href="environment.md">Environment</a><br>Read-only</td><td>Returns the last environment</td></tr>
<tr><td>current</td><td><a href="environment.md">Environment</a><br>Read/Write</td><td>Returns the current environment</td></tr>
<tr><td>this[index]</td><td><a href="environment.md">Environment</a><br>Read-only</td><td>Returns the environment at the given index</td></tr>
<tr><td>count</td><td>number<br>Read-only</td><td>The number of available environments</td></tr>
</tbody></table>




## Instance Methods

        
### environmentList:ByName(name)

Returns the environment with the given name, or nil if no environment has that name

**Returns:** <a href="environment.md">Environment</a> 


**Parameters:**

<table data-full-width="false">
<thead><tr><th>Name</th><th>Type</th><th>Description</th></tr></thead>
<tbody><tr><td>name</td><td>string</td><td>The name of the environment to get</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>env = Sketch.environments:ByName("Pistachio")</strong></code></pre>



    
