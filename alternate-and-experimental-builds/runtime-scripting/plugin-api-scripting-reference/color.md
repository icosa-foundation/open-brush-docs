
# Color

## Summary

An RGB color


## Properties

<table>
<thead><tr><th width="225">Name</th><th width="160">Return Type</th><th>Description</th></tr></thead>
<tbody>
<tr><td>Item</td><td>number</td><td></td></tr>
<tr><td>r</td><td>number</td><td></td></tr>
<tr><td>g</td><td>number</td><td></td></tr>
<tr><td>b</td><td>number</td><td></td></tr>
<tr><td>a</td><td>number</td><td></td></tr>
<tr><td>grayscale</td><td>number</td><td></td></tr>
<tr><td>gamma</td><td><a href="color.md">Color</a></td><td></td></tr>
<tr><td>linear</td><td><a href="color.md">Color</a></td><td></td></tr>
<tr><td>maxColorComponent</td><td>number</td><td></td></tr>
<tr><td>black</td><td><a href="color.md">Color</a></td><td></td></tr>
<tr><td>blue</td><td><a href="color.md">Color</a></td><td></td></tr>
<tr><td>clear</td><td><a href="color.md">Color</a></td><td></td></tr>
<tr><td>cyan</td><td><a href="color.md">Color</a></td><td></td></tr>
<tr><td>gray</td><td><a href="color.md">Color</a></td><td></td></tr>
<tr><td>green</td><td><a href="color.md">Color</a></td><td></td></tr>
<tr><td>grey</td><td><a href="color.md">Color</a></td><td></td></tr>
<tr><td>magenta</td><td><a href="color.md">Color</a></td><td></td></tr>
<tr><td>red</td><td><a href="color.md">Color</a></td><td></td></tr>
<tr><td>white</td><td><a href="color.md">Color</a></td><td></td></tr>
<tr><td>yellow</td><td><a href="color.md">Color</a></td><td></td></tr>
<tr><td></td><td></td><td></td></tr></tbody></table>




## Methods


### Color:New



**Returns:** <a href="color.md">Color</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>r</td><td>number</td><td></td></tr>
<tr><td>g</td><td>number</td><td></td></tr>
<tr><td>b</td><td>number</td><td></td></tr></tbody></table>






### Color:New



**Returns:** <a href="color.md">Color</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>html</td><td>string</td><td></td></tr></tbody></table>






### Color:Greyscale



**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>col</td><td><a href="color.md">Color</a></td><td></td></tr></tbody></table>






### Color:MaxColorComponent



**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>col</td><td><a href="color.md">Color</a></td><td></td></tr></tbody></table>






### Color:ToHtmlString



**Returns:** string


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>col</td><td><a href="color.md">Color</a></td><td></td></tr></tbody></table>






### Color:ParseHtmlString



**Returns:** <a href="color.md">Color</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>html</td><td>string</td><td></td></tr></tbody></table>






### Color:Lerp



**Returns:** <a href="color.md">Color</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td><a href="color.md">Color</a></td><td></td></tr>
<tr><td>b</td><td><a href="color.md">Color</a></td><td></td></tr>
<tr><td>t</td><td>number</td><td></td></tr></tbody></table>






### Color:LerpUnclamped



**Returns:** <a href="color.md">Color</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td><a href="color.md">Color</a></td><td></td></tr>
<tr><td>b</td><td><a href="color.md">Color</a></td><td></td></tr>
<tr><td>t</td><td>number</td><td></td></tr></tbody></table>






### Color:HsvToRgb



**Returns:** <a href="color.md">Color</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>h</td><td>number</td><td></td></tr>
<tr><td>s</td><td>number</td><td></td></tr>
<tr><td>v</td><td>number</td><td></td></tr></tbody></table>






### Color:RgbToHsv



**Returns:** <a href="vector3.md">Vector3</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>rgb</td><td><a href="color.md">Color</a></td><td></td></tr></tbody></table>






### Color:Add



**Returns:** <a href="color.md">Color</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>b</td><td><a href="color.md">Color</a></td><td></td></tr></tbody></table>






### Color:Add



**Returns:** <a href="color.md">Color</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>r</td><td>number</td><td></td></tr>
<tr><td>g</td><td>number</td><td></td></tr>
<tr><td>b</td><td>number</td><td></td></tr></tbody></table>






### Color:Subtract



**Returns:** <a href="color.md">Color</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>b</td><td><a href="color.md">Color</a></td><td></td></tr></tbody></table>






### Color:Subtract



**Returns:** <a href="color.md">Color</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>r</td><td>number</td><td></td></tr>
<tr><td>g</td><td>number</td><td></td></tr>
<tr><td>b</td><td>number</td><td></td></tr></tbody></table>






### Color:Multiply



**Returns:** <a href="color.md">Color</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>b</td><td>number</td><td></td></tr></tbody></table>






### Color:Multiply



**Returns:** <a href="color.md">Color</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>r</td><td>number</td><td></td></tr>
<tr><td>g</td><td>number</td><td></td></tr>
<tr><td>b</td><td>number</td><td></td></tr></tbody></table>






### Color:Divide



**Returns:** <a href="color.md">Color</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>b</td><td>number</td><td></td></tr></tbody></table>






### Color:NotEquals



**Returns:** boolean


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>b</td><td><a href="color.md">Color</a></td><td></td></tr></tbody></table>






### Color:NotEquals



**Returns:** boolean


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>r</td><td>number</td><td></td></tr>
<tr><td>g</td><td>number</td><td></td></tr>
<tr><td>b</td><td>number</td><td></td></tr></tbody></table>






### Color:Add



**Returns:** <a href="color.md">Color</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td><a href="color.md">Color</a></td><td></td></tr>
<tr><td>b</td><td><a href="color.md">Color</a></td><td></td></tr></tbody></table>






### Color:Subtract



**Returns:** <a href="color.md">Color</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td><a href="color.md">Color</a></td><td></td></tr>
<tr><td>b</td><td><a href="color.md">Color</a></td><td></td></tr></tbody></table>






### Color:Multiply



**Returns:** <a href="color.md">Color</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td><a href="color.md">Color</a></td><td></td></tr>
<tr><td>b</td><td>number</td><td></td></tr></tbody></table>






### Color:Divide



**Returns:** <a href="color.md">Color</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td><a href="color.md">Color</a></td><td></td></tr>
<tr><td>b</td><td>number</td><td></td></tr></tbody></table>






### Color:NotEquals



**Returns:** boolean


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td><a href="color.md">Color</a></td><td></td></tr>
<tr><td>b</td><td><a href="color.md">Color</a></td><td></td></tr></tbody></table>






