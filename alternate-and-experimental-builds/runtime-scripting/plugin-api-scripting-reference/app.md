
# App

## Summary




## Properties

<table>
<thead><tr><th width="225">Name</th><th width="160">Return Type</th><th>Description</th></tr></thead>
<tbody>
<tr><td>time</td><td>number</td><td>The time in seconds since Open Brush was launched</td></tr>
<tr><td>frames</td><td>number</td><td>The number of frames that have been rendered since Open Brush was launched</td></tr>
<tr><td>currentScale</td><td>number</td><td></td></tr>
<tr><td>environment</td><td>string</td><td></td></tr>
<tr><td>clipboardText</td><td>string</td><td></td></tr>
<tr><td></td><td></td><td></td></tr></tbody></table>




## Methods


### App:Physics



**Returns:** boolean


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>active</td><td>boolean</td><td></td></tr></tbody></table>






### App:Undo



**Returns:** nil






### App:Redo



**Returns:** nil






### App:AddListener



**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td>string</td><td></td></tr></tbody></table>






### App:ResetPanels



**Returns:** nil






### App:ShowScriptsFolder



**Returns:** nil






### App:ShowExportFolder



**Returns:** nil






### App:ShowSketchesFolder



**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td>number</td><td></td></tr></tbody></table>






### App:StraightEdge



**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>active</td><td>boolean</td><td></td></tr></tbody></table>






### App:AutoOrient



**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>active</td><td>boolean</td><td></td></tr></tbody></table>






### App:ViewOnly



**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>active</td><td>boolean</td><td></td></tr></tbody></table>






### App:AutoSimplify



**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>active</td><td>boolean</td><td></td></tr></tbody></table>






### App:Disco



**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>active</td><td>boolean</td><td></td></tr></tbody></table>






### App:Profiling



**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>active</td><td>boolean</td><td></td></tr></tbody></table>






### App:PostProcessing



**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>active</td><td>boolean</td><td></td></tr></tbody></table>






### App:DraftingVisible



**Returns:** nil






### App:DraftingTransparent



**Returns:** nil






### App:DraftingHidden



**Returns:** nil






### App:Watermark



**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>active</td><td>boolean</td><td></td></tr></tbody></table>






### App:ReadFile



**Returns:** string


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>path</td><td>string</td><td></td></tr></tbody></table>






### App:Error



**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>message</td><td>string</td><td></td></tr></tbody></table>






### App:SetFont



**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>fontData</td><td>string</td><td></td></tr></tbody></table>






### App:TakeSnapshot

Take a snapshot of your scene and save it to your Snapshots folder

**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>tr</td><td>Transform</td><td>A Transform used for the position and orientation of the camera</td></tr>
<tr><td>filename</td><td>string</td><td>The filename to use for the saved snapshot</td></tr>
<tr><td>width</td><td>number</td><td>Image width</td></tr>
<tr><td>height</td><td>number</td><td>Image height</td></tr>
<tr><td>superSampling</td><td>number</td><td></td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>App:TakeSnapshop(Transform:New(0, 12, 3), "mysnapshot.png", 1024, 768, true)</strong></code></pre>




### App:Take360Snapshot



**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>tr</td><td>Transform</td><td></td></tr>
<tr><td>filename</td><td>string</td><td></td></tr>
<tr><td>width</td><td>number</td><td></td></tr></tbody></table>






