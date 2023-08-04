# Group

## Summary
Modifies grouped items


## Instance Properties

<table data-full-width="false">
<thead><tr><th>Name</th><th>Return Type</th><th>Description</th></tr></thead>
<tbody>
<tr><td>images</td><td><a href="imagelist.md">ImageList</a><br>Read-only</td><td>All the images in this group</td></tr>
<tr><td>videos</td><td><a href="videolist.md">VideoList</a><br>Read-only</td><td>All the videos in this group</td></tr>
<tr><td>models</td><td><a href="modellist.md">ModelList</a><br>Read-only</td><td>All the models in this group</td></tr>
<tr><td>guides</td><td><a href="guidelist.md">GuideList</a><br>Read-only</td><td>All the guides in this group</td></tr>
<tr><td>cameraPaths</td><td><a href="camerapathlist.md">CameraPathList</a><br>Read-only</td><td>All the camera paths in this group</td></tr>
</tbody></table>



## Class Methods

        
### Group:New()

Creates and returns a new empty group

**Returns:** <a href="group.md">Group</a>  (The new group)




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>myGroup = Group:New()</strong></code></pre>



    

## Instance Methods

        
### group:Add(widget)

Adds an image to this group moving it to the group's layer if necessary

**Returns:** nil 


**Parameters:**

<table data-full-width="false">
<thead><tr><th>Name</th><th>Type</th><th>Description</th></tr></thead>
<tbody><tr><td>widget</td><td><a href="image.md">Image</a></td><td></td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>myGroup:Add(myImage)</strong></code></pre>




### group:Add(widget)

Adds a video to this group moving it to the group's layer if necessary

**Returns:** nil 


**Parameters:**

<table data-full-width="false">
<thead><tr><th>Name</th><th>Type</th><th>Description</th></tr></thead>
<tbody><tr><td>widget</td><td><a href="video.md">Video</a></td><td></td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>myGroup:Add(myVideo)</strong></code></pre>




### group:Add(widget)

Adds a model to this group moving it to the group's layer if necessary

**Returns:** nil 


**Parameters:**

<table data-full-width="false">
<thead><tr><th>Name</th><th>Type</th><th>Description</th></tr></thead>
<tbody><tr><td>widget</td><td><a href="model.md">Model</a></td><td></td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>myGroup:Add(myModel)</strong></code></pre>




### group:Add(widget)

Adds a guide to this group moving it to the group's layer if necessary

**Returns:** nil 


**Parameters:**

<table data-full-width="false">
<thead><tr><th>Name</th><th>Type</th><th>Description</th></tr></thead>
<tbody><tr><td>widget</td><td><a href="guide.md">Guide</a></td><td></td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>myGroup:Add(myGuide)</strong></code></pre>




### group:Add(widget)

Adds an image to this group moving it to the group's layer if necessary

**Returns:** nil 


**Parameters:**

<table data-full-width="false">
<thead><tr><th>Name</th><th>Type</th><th>Description</th></tr></thead>
<tbody><tr><td>widget</td><td><a href="camerapath.md">CameraPath</a></td><td></td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>myGroup:Add(myCameraPath)</strong></code></pre>




### group:_Add(widget)



**Returns:** nil 


**Parameters:**

<table data-full-width="false">
<thead><tr><th>Name</th><th>Type</th><th>Description</th></tr></thead>
<tbody><tr><td>widget</td><td><a href="grabwidget.md">GrabWidget</a></td><td></td></tr></tbody></table>






### group:Add(widget)

Adds a stroke to this group moving it to the group's layer if necessary

**Returns:** nil 


**Parameters:**

<table data-full-width="false">
<thead><tr><th>Name</th><th>Type</th><th>Description</th></tr></thead>
<tbody><tr><td>widget</td><td><a href="grabwidget.md">GrabWidget</a></td><td></td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>myGroup:Add(mystroke)</strong></code></pre>



    
