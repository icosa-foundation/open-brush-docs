# App

## Summary

Docs are a work in progress. This is an example page to help me plan the formatting and layout

## Properties

<table><thead><tr><th width="225">Name</th><th width="159.33333333333331">Return Type</th><th>Description</th></tr></thead><tbody><tr><td>App.time</td><td>number</td><td>The time in seconds since Open Brush was launched</td></tr><tr><td>App.frames</td><td>number</td><td>The number of frames that have been rendered since Open Brush was launched</td></tr><tr><td></td><td></td><td></td></tr></tbody></table>

## Methods

### App:TakeSnapshot

**Parameters:**

<table data-full-width="false"><thead><tr><th width="217">Name</th><th width="134">Type</th><th width="123">Default</th><th>Description</th></tr></thead><tbody><tr><td>tr</td><td>Transform</td><td></td><td>The position and orientation of the snapshot camera</td></tr><tr><td>filename</td><td>string</td><td></td><td>The filename to sav as</td></tr><tr><td>width</td><td>number</td><td></td><td>Image width</td></tr><tr><td>height</td><td>number</td><td></td><td>Image height</td></tr><tr><td>supersampling</td><td>boolean</td><td></td><td>supersampling is a form of antialiasing that can improve the appearance of the snapshop</td></tr></tbody></table>

#### Example

<pre class="language-lua"><code class="lang-lua"><strong>App:TakeSnapshop(Transform:New(0, 12, 3), "mysnapshot.png", 1024, 768, true)
</strong></code></pre>

### App:Error

#### Parameters

