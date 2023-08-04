
# Symmetry

## Summary
Functions for controlling the mirror symmetry mode

## Class Properties

<table data-full-width="false">
<thead><tr><th>Name</th><th>Return Type</th><th>Description</th></tr></thead>
<tbody>
<tr><td>brushOffset</td><td><a href="vector3.md">Vector3</a><br>Read-only</td><td>Gets the offset betwen the current brush position and the symmetry widget</td></tr>
<tr><td>wandOffset</td><td><a href="vector3.md">Vector3</a><br>Read-only</td><td>Gets the offset betwen the current wand position and the symmetry widget</td></tr>
<tr><td>settings</td><td><a href="symmetrysettings.md">SymmetrySettings</a><br>Read/Write</td><td>The current symmetry settings</td></tr>
</tbody></table>




## Class Methods

        
### Symmetry:SummonWidget()



**Returns:** nil 






### Symmetry:Ellipse(angle, minorRadius)



**Returns:** number 


**Parameters:**

<table data-full-width="false">
<thead><tr><th>Name</th><th>Type</th><th>Description</th></tr></thead>
<tbody><tr><td>angle</td><td>number</td><td></td></tr>
<tr><td>minorRadius</td><td>number</td><td></td></tr></tbody></table>






### Symmetry:Square(angle)



**Returns:** number 


**Parameters:**

<table data-full-width="false">
<thead><tr><th>Name</th><th>Type</th><th>Description</th></tr></thead>
<tbody><tr><td>angle</td><td>number</td><td></td></tr></tbody></table>






### Symmetry:Superellipse(angle, n, a, b)



**Returns:** number 


**Parameters:**

<table data-full-width="false">
<thead><tr><th>Name</th><th>Type</th><th>Description</th></tr></thead>
<tbody><tr><td>angle</td><td>number</td><td></td></tr>
<tr><td>n</td><td>number</td><td></td></tr>
<tr><td>a</td><td>number</td><td></td></tr>
<tr><td>b</td><td>number</td><td></td></tr></tbody></table>






### Symmetry:Rsquare(angle, halfSideLength, cornerRadius)



**Returns:** number 


**Parameters:**

<table data-full-width="false">
<thead><tr><th>Name</th><th>Type</th><th>Description</th></tr></thead>
<tbody><tr><td>angle</td><td>number</td><td></td></tr>
<tr><td>halfSideLength</td><td>number</td><td></td></tr>
<tr><td>cornerRadius</td><td>number</td><td></td></tr></tbody></table>






### Symmetry:Polygon(angle, numSides, radius)



**Returns:** number 


**Parameters:**

<table data-full-width="false">
<thead><tr><th>Name</th><th>Type</th><th>Description</th></tr></thead>
<tbody><tr><td>angle</td><td>number</td><td></td></tr>
<tr><td>numSides</td><td>number</td><td></td></tr>
<tr><td>radius</td><td>number</td><td></td></tr></tbody></table>






### Symmetry:ClearColors(colors)



**Returns:** nil 


**Parameters:**

<table data-full-width="false">
<thead><tr><th>Name</th><th>Type</th><th>Description</th></tr></thead>
<tbody><tr><td>colors</td><td>Color[]</td><td></td></tr></tbody></table>






### Symmetry:AddColor(color)



**Returns:** nil 


**Parameters:**

<table data-full-width="false">
<thead><tr><th>Name</th><th>Type</th><th>Description</th></tr></thead>
<tbody><tr><td>color</td><td><a href="color.md">Color</a></td><td></td></tr></tbody></table>






### Symmetry:SetColors(colors)



**Returns:** nil 


**Parameters:**

<table data-full-width="false">
<thead><tr><th>Name</th><th>Type</th><th>Description</th></tr></thead>
<tbody><tr><td>colors</td><td>Color[]</td><td></td></tr></tbody></table>






### Symmetry:GetColors()



**Returns:** Color[] 






### Symmetry:AddBrush(brush)



**Returns:** nil 


**Parameters:**

<table data-full-width="false">
<thead><tr><th>Name</th><th>Type</th><th>Description</th></tr></thead>
<tbody><tr><td>brush</td><td>string</td><td></td></tr></tbody></table>






### Symmetry:ClearBrushes(brushes)



**Returns:** nil 


**Parameters:**

<table data-full-width="false">
<thead><tr><th>Name</th><th>Type</th><th>Description</th></tr></thead>
<tbody><tr><td>brushes</td><td>string[]</td><td></td></tr></tbody></table>






### Symmetry:SetBrushes(brushes)



**Returns:** nil 


**Parameters:**

<table data-full-width="false">
<thead><tr><th>Name</th><th>Type</th><th>Description</th></tr></thead>
<tbody><tr><td>brushes</td><td>string[]</td><td></td></tr></tbody></table>






### Symmetry:GetBrushNames()



**Returns:** string[] 






### Symmetry:GetBrushGuids()



**Returns:** string[] 






### Symmetry:PathToPolar(path)



**Returns:** <a href="path.md">Path</a> 


**Parameters:**

<table data-full-width="false">
<thead><tr><th>Name</th><th>Type</th><th>Description</th></tr></thead>
<tbody><tr><td>path</td><td><a href="ipath.md">IPath</a></td><td></td></tr></tbody></table>





    

