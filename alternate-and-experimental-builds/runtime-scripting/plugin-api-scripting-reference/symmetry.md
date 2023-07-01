
# Symmetry

## Summary
Functions for controlling the mirror symmetry mode

## Class Properties

<table>
<thead><tr><th width="225">Name</th><th width="160">Return Type</th><th width="80">Read/Write?</th><th>Description</th></tr></thead>
<tbody>
<tr><td>transform</td><td><a href="transform.md">Transform</a></td><td>Read/Write</td><td>The transform of the Symmetry Widget</td></tr>
<tr><td>position</td><td><a href="vector3.md">Vector3</a></td><td>Read/Write</td><td>The 3D position of the Symmetry Widget</td></tr>
<tr><td>rotation</td><td><a href="rotation.md">Rotation</a></td><td>Read/Write</td><td>The 3D orientation of the Symmetry Widget</td></tr>
<tr><td>brushOffset</td><td><a href="vector3.md">Vector3</a></td><td>Read-only</td><td></td></tr>
<tr><td>wandOffset</td><td><a href="vector3.md">Vector3</a></td><td>Read-only</td><td></td></tr>
<tr><td>direction</td><td><a href="vector3.md">Vector3</a></td><td>Read-only</td><td></td></tr>
</tbody></table>




## Class Methods

        
### Symmetry:Mirror()



**Returns:** nil






### Symmetry:DoubleMirror()



**Returns:** nil






### Symmetry:TwoHandeded()



**Returns:** nil






### Symmetry:SummonWidget()



**Returns:** nil






### Symmetry:Spin(xSpeed, ySpeed, zSpeed)



**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>xSpeed</td><td>number</td><td></td></tr>
<tr><td>ySpeed</td><td>number</td><td></td></tr>
<tr><td>zSpeed</td><td>number</td><td></td></tr></tbody></table>






### Symmetry:Ellipse(angle, minorRadius)



**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>angle</td><td>number</td><td></td></tr>
<tr><td>minorRadius</td><td>number</td><td></td></tr></tbody></table>






### Symmetry:Square(angle)



**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>angle</td><td>number</td><td></td></tr></tbody></table>






### Symmetry:Superellipse(angle, n, a, b)



**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>angle</td><td>number</td><td></td></tr>
<tr><td>n</td><td>number</td><td></td></tr>
<tr><td>a</td><td>number</td><td></td></tr>
<tr><td>b</td><td>number</td><td></td></tr></tbody></table>






### Symmetry:Rsquare(angle, halfSideLength, cornerRadius)



**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>angle</td><td>number</td><td></td></tr>
<tr><td>halfSideLength</td><td>number</td><td></td></tr>
<tr><td>cornerRadius</td><td>number</td><td></td></tr></tbody></table>






### Symmetry:Polygon(angle, numSides, radius)



**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>angle</td><td>number</td><td></td></tr>
<tr><td>numSides</td><td>number</td><td></td></tr>
<tr><td>radius</td><td>number</td><td></td></tr></tbody></table>






### Symmetry:ClearColors(colors)



**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>colors</td><td>Color[]</td><td></td></tr></tbody></table>






### Symmetry:AddColor(color)



**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>color</td><td><a href="color.md">Color</a></td><td></td></tr></tbody></table>






### Symmetry:SetColors(colors)



**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>colors</td><td>Color[]</td><td></td></tr></tbody></table>






### Symmetry:GetColors()



**Returns:** Color[]






### Symmetry:AddBrush(brush)



**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>brush</td><td>string</td><td></td></tr></tbody></table>






### Symmetry:ClearBrushes(brushes)



**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>brushes</td><td>string[]</td><td></td></tr></tbody></table>






### Symmetry:SetBrushes(brushes)



**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>brushes</td><td>string[]</td><td></td></tr></tbody></table>






### Symmetry:GetBrushNames()



**Returns:** string[]






### Symmetry:GetBrushGuids()



**Returns:** string[]






### Symmetry:PathToPolar(path)



**Returns:** <a href="path.md">Path</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>path</td><td><a href="ipath.md">IPath</a></td><td></td></tr></tbody></table>





    

