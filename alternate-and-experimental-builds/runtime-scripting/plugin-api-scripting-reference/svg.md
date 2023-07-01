
# Svg

## Summary
Functions related to SVG images



## Class Methods

        
### Svg:ParsePathString(svgPath)

Parses an SVG path string

**Returns:** <a href="multipath.md">MultiPath</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>svgPath</td><td>string</td><td>The SVG path string to parse</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>myPaths = SVG:ParsePathString('M 100 100 L 200 200')</strong></code></pre>




### Svg:ParseDocument(svg, offsetPerPath, includeColors)

Parses an SVG document

**Returns:** <a href="multipath.md">MultiPath</a>


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>svg</td><td>string</td><td>A text string that is valid SVG document</td></tr>
<tr><td>offsetPerPath</td><td>number</td><td>Each path can be lifted to form a layered result</td></tr>
<tr><td>includeColors</td><td>boolean</td><td>Whether the colors from the SVG are used</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>myPaths = SVG:ParseDocument('<svg>...</svg>')</strong></code></pre>




### Svg:DrawPathString(svg, tr)

Draws an SVG path string

**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>svg</td><td>string</td><td>The SVG path string to draw</td></tr>
<tr><td>tr</td><td><a href="transform.md">Transform</a></td><td>The transform to apply to the result</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>SVG:DrawPathString('M 100 100 L 200 200')</strong></code></pre>




### Svg:DrawDocument(svg, tr)

Draws an SVG document

**Returns:** nil


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>svg</td><td>string</td><td>A text string that is a valid SVG document</td></tr>
<tr><td>tr</td><td><a href="transform.md">Transform</a></td><td>The transform (position, rotation and scale) to apply to the result</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>SVG:Draw('<svg>...</svg>')</strong></code></pre>



    

