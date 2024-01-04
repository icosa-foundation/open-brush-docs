
# SymmetrySettings

## Summary
A collection of settings for the symmetry mode


## Instance Properties

<table data-full-width="false">
<thead><tr><th>Name</th><th>Return Type</th><th>Description</th></tr></thead>
<tbody>
<tr><td>mode</td><td><a href="symmetrymode.md">SymmetryMode</a><br>Read/Write</td><td>The symmetry mode</td></tr>
<tr><td>transform</td><td><a href="transform.md">Transform</a><br>Read/Write</td><td>The transform of the symmetry widget</td></tr>
<tr><td>position</td><td><a href="vector3.md">Vector3</a><br>Read/Write</td><td>The position of the symmetry widget</td></tr>
<tr><td>rotation</td><td><a href="rotation.md">Rotation</a><br>Read/Write</td><td>The rotation of the symmetry widget</td></tr>
<tr><td>spin</td><td><a href="vector3.md">Vector3</a><br>Read/Write</td><td>How fast the symmetry widget is spinning in each axis</td></tr>
<tr><td>pointType</td><td><a href="symmetrypointtype.md">SymmetryPointType</a><br>Read/Write</td><td>The type of point symmetry</td></tr>
<tr><td>pointOrder</td><td>number<br>Read/Write</td><td>The order of point symmetry (how many times it repeats around it's axis)</td></tr>
<tr><td>wallpaperType</td><td><a href="symmetrywallpapertype.md">SymmetryWallpaperType</a><br>Read/Write</td><td>The type of wallpaper symmetry</td></tr>
<tr><td>wallpaperRepeatX</td><td>number<br>Read/Write</td><td>How many times the wallpaper symmetry repeats in the X axis</td></tr>
<tr><td>wallpaperRepeatY</td><td>number<br>Read/Write</td><td>How many times the wallpaper symmetry repeats in the Y axis</td></tr>
<tr><td>wallpaperScale</td><td>number<br>Read/Write</td><td>The overall scale of the wallpaper symmetry</td></tr>
<tr><td>wallpaperScaleX</td><td>number<br>Read/Write</td><td>The scale of the wallpaper symmetry in the X axis</td></tr>
<tr><td>wallpaperScaleY</td><td>number<br>Read/Write</td><td>The scale of the wallpaper symmetry in the Y axis</td></tr>
<tr><td>wallpaperSkewX</td><td>number<br>Read/Write</td><td>The skew of the wallpaper symmetry in the X axis</td></tr>
<tr><td>wallpaperSkewY</td><td>number<br>Read/Write</td><td>The skew of the wallpaper symmetry in the Y axis</td></tr>
</tbody></table>




## Instance Methods

        
### symmetrySettings:Duplicate()

Creates a copy of these symmetry settings

**Returns:** <a href="symmetrysettings.md">SymmetrySettings</a> 




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>newSettings = Symmetry.current:Duplicate()</strong></code></pre>



    
