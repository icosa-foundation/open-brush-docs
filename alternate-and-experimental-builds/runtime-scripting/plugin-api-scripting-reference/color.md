
# Color

## Summary

An RGB color


## Properties

<table>
<thead><tr><th width="225">Name</th><th width="160">Return Type</th><th width="120">Read/Write?</th><th>Description</th></tr></thead>
<tbody>
<tr><td>item</td><td>number</td><td>Read/Write</td><td>Gets or sets the color component at the specified index</td></tr>
<tr><td>r</td><td>number</td><td>Read-only</td><td>Gets the red component of the color</td></tr>
<tr><td>g</td><td>number</td><td>Read-only</td><td>Gets the green component of the color</td></tr>
<tr><td>b</td><td>number</td><td>Read-only</td><td>Gets the blue component of the color</td></tr>
<tr><td>a</td><td>number</td><td>Read-only</td><td>Gets the alpha component of the color</td></tr>
<tr><td>grayscale</td><td>number</td><td>Read-only</td><td>Gets the grayscale value of the color</td></tr>
<tr><td>gamma</td><td><a href="color.md">Color</a></td><td>Read-only</td><td>Gets the gamma color space representation of the color</td></tr>
<tr><td>linear</td><td><a href="color.md">Color</a></td><td>Read-only</td><td>Gets the linear color space representation of the color</td></tr>
<tr><td>maxcolorcomponent</td><td>number</td><td>Read-only</td><td>Gets the maximum color component value of the color</td></tr>
<tr><td>black</td><td><a href="color.md">Color</a></td><td>Read-only</td><td>Gets the black color</td></tr>
<tr><td>blue</td><td><a href="color.md">Color</a></td><td>Read-only</td><td>Gets the blue color</td></tr>
<tr><td>clear</td><td><a href="color.md">Color</a></td><td>Read-only</td><td>Gets the clear color</td></tr>
<tr><td>cyan</td><td><a href="color.md">Color</a></td><td>Read-only</td><td>Gets the cyan color</td></tr>
<tr><td>gray</td><td><a href="color.md">Color</a></td><td>Read-only</td><td>Gets the gray color</td></tr>
<tr><td>green</td><td><a href="color.md">Color</a></td><td>Read-only</td><td>Gets the green color</td></tr>
<tr><td>grey</td><td><a href="color.md">Color</a></td><td>Read-only</td><td>Gets the grey color</td></tr>
<tr><td>magenta</td><td><a href="color.md">Color</a></td><td>Read-only</td><td>Gets the magenta color</td></tr>
<tr><td>red</td><td><a href="color.md">Color</a></td><td>Read-only</td><td>Gets the red color</td></tr>
<tr><td>white</td><td><a href="color.md">Color</a></td><td>Read-only</td><td>Gets the white color</td></tr>
<tr><td>yellow</td><td><a href="color.md">Color</a></td><td>Read-only</td><td>Gets the yellow color</td></tr>
<tr><td></td><td></td><td></td></tr></tbody></table>




## Methods


### Color:New(r, g, b)

Creates a new instance of a color with the specified RGB values

**Returns:** <a href="color.md">Color</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>r</td><td>number</td><td>The red component of the color. Default is 0</td></tr>
<tr><td>g</td><td>number</td><td>The green component of the color. Default is 0</td></tr>
<tr><td>b</td><td>number</td><td>The blue component of the color. Default is 0</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>myColor = Color:New(0.5, 0, 1)</strong></code></pre>




### Color:New(html)

Creates a new instance of the Color with the color parsed from the specified HTML string

**Returns:** <a href="color.md">Color</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>html</td><td>string</td><td>The HTML string representing the color</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>myColor = Color:New("D3B322")</strong></code></pre>




### Color:Greyscale(color)

Calculates the grayscale value of the specified color

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>color</td><td><a href="color.md">Color</a></td><td></td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>grayAmount = myColor:Greyscale()</strong></code></pre>




### Color:MaxColorComponent(color)

Gets the maximum color component value of the specified color

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>color</td><td><a href="color.md">Color</a></td><td></td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>amount = myColor:MaxColorComponent()</strong></code></pre>




### Color:ToHtmlString(col)

Converts the specified color to its HTML string representation

**Returns:** string


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>col</td><td><a href="color.md">Color</a></td><td>The color</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>htmlColor = myColor:ToHtmlString()</strong></code></pre>




### Color:ParseHtmlString(html)

Parses the specified HTML string and returns the color

**Returns:** <a href="color.md">Color</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>html</td><td>string</td><td>The HTML string representing the color</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>myColor = Color:ParseHtmlString(htmlColor)</strong></code></pre>




### Color:Lerp(a, b, t)

Performs a linear interpolation between two colors

**Returns:** <a href="color.md">Color</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td><a href="color.md">Color</a></td><td>The start color</td></tr>
<tr><td>b</td><td><a href="color.md">Color</a></td><td>The end color</td></tr>
<tr><td>t</td><td>number</td><td>The interpolation value. Should be between 0 and 1</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>newColor = Color:Lerp(color1, color2, 0.5)</strong></code></pre>




### Color:LerpUnclamped(a, b, t)

Performs a linear interpolation between two colors without clamping the interpolation parameter

**Returns:** <a href="color.md">Color</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td><a href="color.md">Color</a></td><td>The start color</td></tr>
<tr><td>b</td><td><a href="color.md">Color</a></td><td>The end color</td></tr>
<tr><td>t</td><td>number</td><td>The interpolation value</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>newColor = Color:Lerp(color1, color2, 1.5)</strong></code></pre>




### Color:HsvToRgb(h, s, v)

Converts an HSV color to an RGB color

**Returns:** <a href="color.md">Color</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>h</td><td>number</td><td>The hue value. Should be between 0 and 1</td></tr>
<tr><td>s</td><td>number</td><td>The saturation value. Should be between 0 and 1</td></tr>
<tr><td>v</td><td>number</td><td>The value value. Should be between 0 and 1</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>newColor = Color:HsvToRgb(0.5, 0.9, 0.5)</strong></code></pre>




### Color:RgbToHsv(rgb)

Converts an RGB color to an HSV color

**Returns:** <a href="vector3.md">Vector3</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>rgb</td><td><a href="color.md">Color</a></td><td>The RGB color</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>myVector = Color:RgbToHsv(myColor</strong></code></pre>




### Color:add(b)

Adds the specified color to this color

**Returns:** <a href="color.md">Color</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>b</td><td><a href="color.md">Color</a></td><td>The color to add</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>newColor = color1:Add(color2)</strong></code></pre>




### Color:add(r, g, b)

Adds the specified RGB values to this color

**Returns:** <a href="color.md">Color</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>r</td><td>number</td><td>The red component value to add</td></tr>
<tr><td>g</td><td>number</td><td>The green component value to add</td></tr>
<tr><td>b</td><td>number</td><td>The blue component value to add</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>newColor = color1:Add(0.5, 0, 0.1)</strong></code></pre>




### Color:subtract(b)

Subtracts the specified color from this color

**Returns:** <a href="color.md">Color</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>b</td><td><a href="color.md">Color</a></td><td>The color to subtract</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>newColor = color1:Subtract(color2)</strong></code></pre>




### Color:subtract(r, g, b)

Subtracts the specified RGB values from this color

**Returns:** <a href="color.md">Color</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>r</td><td>number</td><td>The red component value to subtract</td></tr>
<tr><td>g</td><td>number</td><td>The green component value to subtract</td></tr>
<tr><td>b</td><td>number</td><td>The blue component value to subtract</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>newColor = color1:Subtract(0.5, 0.25, 0)</strong></code></pre>




### Color:multiply(b)

Multiplies this color by the specified value

**Returns:** <a href="color.md">Color</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>b</td><td>number</td><td>The value to multiply</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>newColor = color1:Multiply(0.5)</strong></code></pre>




### Color:multiply(r, g, b)

Multiplies this color by the specified RGB values

**Returns:** <a href="color.md">Color</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>r</td><td>number</td><td>The red component value to multiply</td></tr>
<tr><td>g</td><td>number</td><td>The green component value to multiply</td></tr>
<tr><td>b</td><td>number</td><td>The blue component value to multiply</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>newColor = color1:Multiply(0.85, 0, 0)</strong></code></pre>




### Color:divide(b)

Divides this color by the specified value

**Returns:** <a href="color.md">Color</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>b</td><td>number</td><td>The value to divide</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>newColor = color1:Divide(0.5)</strong></code></pre>




### Color:notequals(b)

Determines whether this color is not equal to the specified color

**Returns:** boolean


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>b</td><td><a href="color.md">Color</a></td><td>The color to compare</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>if color1:NotEquals(color2) then print("colors are different") end</strong></code></pre>




### Color:notequals(r, g, b)

Determines whether this color is not equal to the specified RGB values

**Returns:** boolean


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>r</td><td>number</td><td>The red component value to compare</td></tr>
<tr><td>g</td><td>number</td><td>The green component value to compare</td></tr>
<tr><td>b</td><td>number</td><td>The blue component value to compare</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>if color1:NotEquals(0, 1, 0) then print("color is not green") end</strong></code></pre>




### Color:Add(a, b)

Adds two colors together

**Returns:** <a href="color.md">Color</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td><a href="color.md">Color</a></td><td>The first color</td></tr>
<tr><td>b</td><td><a href="color.md">Color</a></td><td>The second color</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>newColor = Color:Add(color1, color2)</strong></code></pre>




### Color:Subtract(a, b)

Subtracts the second color from the first color

**Returns:** <a href="color.md">Color</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td><a href="color.md">Color</a></td><td>The first color</td></tr>
<tr><td>b</td><td><a href="color.md">Color</a></td><td>The second color</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>newColor = Color:Subtract(color1, color2)</strong></code></pre>




### Color:Multiply(a, b)

Multiplies the color by the specified value

**Returns:** <a href="color.md">Color</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td><a href="color.md">Color</a></td><td>The color</td></tr>
<tr><td>b</td><td>number</td><td>The value to multiply</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>newColor = Color:Multiply(color1, color2)</strong></code></pre>




### Color:Divide(a, b)

Divides the color by the specified value

**Returns:** <a href="color.md">Color</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td><a href="color.md">Color</a></td><td>The color</td></tr>
<tr><td>b</td><td>number</td><td>The value to divide</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>newColor = Color:Divide(color1, color2)</strong></code></pre>




### Color:NotEquals(a, b)

Determines whether two colors are not equal

**Returns:** boolean


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td><a href="color.md">Color</a></td><td>The first color</td></tr>
<tr><td>b</td><td><a href="color.md">Color</a></td><td>The second color</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>colorsAreDifferent = Color:NotEquals(color1, color2)</strong></code></pre>




