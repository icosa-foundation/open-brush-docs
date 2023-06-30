
# Math

## Summary
Various maths functions. See https://docs.unity3d.com/ScriptReference/Mathf.html for further documentation

## Class Properties

<table>
<thead><tr><th width="225">Name</th><th width="160">Return Type</th><th width="80">Read/Write?</th><th>Description</th></tr></thead>
<tbody>
<tr><td>deg2Rad</td><td>number</td><td>Read-only</td><td>A constant that you multiply with a value in degrees to convert it to radians</td></tr>
<tr><td>epsilon</td><td>number</td><td>Read-only</td><td>The smallest value that a float can have such that 1.0 plus this does not equal 1.0</td></tr>
<tr><td>positiveInfinity</td><td>number</td><td>Read-only</td><td>Positive Infinity</td></tr>
<tr><td>negativeInfinity</td><td>number</td><td>Read-only</td><td>Negative Infinity</td></tr>
<tr><td>pi</td><td>number</td><td>Read-only</td><td>The value of Pi</td></tr>
<tr><td>rad2Deg</td><td>number</td><td>Read-only</td><td>A constant that you multiply with a value in radians to convert it to degrees</td></tr>
</tbody></table>




## Class Methods

        
### Math:Abs(f)

The absolute value function

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>f</td><td>number</td><td>The input value</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>result = Math:Abs(0.1)</strong></code></pre>




### Math:Acos(f)

The arc-cosine function

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>f</td><td>number</td><td>The input value</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>result = Math:Acos(0.1)</strong></code></pre>




### Math:Approximately(a, b)

Compares two floating point values if they are similar

**Returns:** boolean


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td>number</td><td>The first value</td></tr>
<tr><td>b</td><td>number</td><td>The second value</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>nearlySame = Math:Approximately(0.1000000000000000011, 0.100000000000000001)</strong></code></pre>




### Math:Asin(f)

The arc-sine function

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>f</td><td>number</td><td>The input value</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>result = Math:Asin(0.1)</strong></code></pre>




### Math:Atan(f)

The arc-tangent function

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>f</td><td>number</td><td>The input value</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>result = Math:Atan(0.1)</strong></code></pre>




### Math:Atan2(y, x)

The two argument arc-tangent function

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>y</td><td>number</td><td>The numerator value</td></tr>
<tr><td>x</td><td>number</td><td>The denominator value</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>result = Math:Atan2(0.1, 3)</strong></code></pre>




### Math:Ceil(f)

The ceiling function

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>f</td><td>number</td><td>The input value</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>result = Math:Ceil(0.1)</strong></code></pre>




### Math:Clamp(f, min, max)

Clamps the given value between the given minimum float and maximum float values. Returns the given value if it is within the min and max range

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>f</td><td>number</td><td>The input value</td></tr>
<tr><td>min</td><td>number</td><td>The minimum value</td></tr>
<tr><td>max</td><td>number</td><td>The maximum value</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>result = Math:Clamp(input, -1, 1)</strong></code></pre>




### Math:Clamp01(value)

Clamps value between 0 and 1 and returns value

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>value</td><td>number</td><td>The input value</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>result = Math:Clamp01(1.3)</strong></code></pre>




### Math:ClosestPowerOfTwo(value)

Calculates the closest power of two

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>value</td><td>number</td><td>The input value</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>result = Math:ClosestPowerOfTwo(13)</strong></code></pre>




### Math:Cos(f)

The cosine function

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>f</td><td>number</td><td>The input value in radians</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>result = Math:Cos(0.1)</strong></code></pre>




### Math:DeltaAngle(a, b)

Calculates the shortest difference between two given angles

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td>number</td><td>The first value in degrees</td></tr>
<tr><td>b</td><td>number</td><td>The second value in degrees</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>result = Math:DeltaAngle(1080, 90)</strong></code></pre>




### Math:Exp(power)

The exponent function

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>power</td><td>number</td><td>The input value</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>result = Math:Exp(100)</strong></code></pre>




### Math:Floor(f)

The floor function

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>f</td><td>number</td><td>The input value</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>result = Math:Floor(2.1)</strong></code></pre>




### Math:InverseLerp(min, max, t)

Inverse linear interpolation between two values by given ratio

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>min</td><td>number</td><td>The minimum value</td></tr>
<tr><td>max</td><td>number</td><td>The maximum value</td></tr>
<tr><td>t</td><td>number</td><td>The input value</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>result = Math:InverseLerp(min, max, 23)</strong></code></pre>




### Math:IsPowerOfTwo(value)

Determines whether a value is a power of two

**Returns:** boolean


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>value</td><td>number</td><td>The input value</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>isPower = Math:IsPowerOfTwo(value)</strong></code></pre>




### Math:Lerp(min, max, t)

Linearly interpolates two floats by a ratio

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>min</td><td>number</td><td>The minimum value</td></tr>
<tr><td>max</td><td>number</td><td>The maximum value</td></tr>
<tr><td>t</td><td>number</td><td>The input value</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>result = Math:Lerp(-1, 1, 0.25)</strong></code></pre>




### Math:LerpAngle(min, max, a)

Same as Lerp but takes the shortest path between the specified angles wrapping around a circle

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>min</td><td>number</td><td>The start angle in degrees</td></tr>
<tr><td>max</td><td>number</td><td>The end angle in degrees</td></tr>
<tr><td>a</td><td>number</td><td>The input value in degrees</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>result = Math:LerpAngle(-30, 90, angle)</strong></code></pre>




### Math:LerpUnclamped(min, max, t)

Same as Math:Lerp but allows extrapolated values

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>min</td><td>number</td><td>The minimum value</td></tr>
<tr><td>max</td><td>number</td><td>The maximum value</td></tr>
<tr><td>t</td><td>number</td><td>The input value</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>result = Math:Lerp(-1, 1, 0.25)</strong></code></pre>




### Math:Log(f, b)

The logarithm of a specified number in a specified base

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>f</td><td>number</td><td>The input value</td></tr>
<tr><td>b</td><td>number</td><td>The base</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>result = Math:Log(input, 2)</strong></code></pre>




### Math:Log10(f)

The base 10 logarithm of a specified number

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>f</td><td>number</td><td>The input value</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>result = Math:Log10(0.1)</strong></code></pre>




### Math:Max(a, b)

The larger of two float numbers

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td>number</td><td>The first input value</td></tr>
<tr><td>b</td><td>number</td><td>The second input value</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>biggest = Math:Max(a, b)</strong></code></pre>




### Math:Max(values)

The largest value in a sequence of float numbers

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>values</td><td>number[]</td><td>A list of numbers</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>biggest = Math:Max({1, 4, 6, 2, -3, 32, 5})</strong></code></pre>




### Math:Min(a, b)

The smaller of two float numbers

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td>number</td><td>The first input value</td></tr>
<tr><td>b</td><td>number</td><td>The second input value</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>smallest = Min:Min(a, b)</strong></code></pre>




### Math:Min(values)

The smallest value in a sequence of float numbers

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>values</td><td>number[]</td><td>A list of numbers</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>smallest = Math:Min({1, 4, 6, 2, -3, 32, 5})</strong></code></pre>




### Math:MoveTowards(current, target, maxDelta)

Moves a value towards a target value by a given amount

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>current</td><td>number</td><td>The input value</td></tr>
<tr><td>target</td><td>number</td><td>The target value</td></tr>
<tr><td>maxDelta</td><td>number</td><td>The largest change allowed each time</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>x = Math:MoveTowards(x, 10, 0.5)</strong></code></pre>




### Math:NextPowerOfTwo(value)

The smallest power of two greater than or equal to the specified number

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>value</td><td>number</td><td>The input value</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>result = Math:NextPowerOfTwo(26)</strong></code></pre>




### Math:PerlinNoise(x, y)

Samples a two-dimensional Perlin noise map

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>x</td><td>number</td><td>The input value</td></tr>
<tr><td>y</td><td>number</td><td>The power to raise to</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>result = Math:PerlinNoise(0.4, 1.2)</strong></code></pre>




### Math:PingPong(t, length)

Similar to Math:Round except the values alternate between forward and backwards in the range

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>t</td><td>number</td><td>The input value</td></tr>
<tr><td>length</td><td>number</td><td>The upper limit</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>result = Math:PingPong(0.4, 1.2)</strong></code></pre>




### Math:Pow(f, p)

The raised to the specified power

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>f</td><td>number</td><td>The input value</td></tr>
<tr><td>p</td><td>number</td><td>The power to raise to</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>result = Math:Pow(0.1, 16)</strong></code></pre>




### Math:Repeater(t, length)

Loops the value t - similar to "clock" arithmetic

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>t</td><td>number</td><td>The input value</td></tr>
<tr><td>length</td><td>number</td><td>The upper limit</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>result = Math:Round(0.1)</strong></code></pre>




### Math:Round(f)

The rounding function

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>f</td><td>number</td><td>The input value</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>result = Math:Round(0.1)</strong></code></pre>




### Math:Sign(f)

The sign function

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>f</td><td>number</td><td>The input value</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>result = Math:Sign(0.1)</strong></code></pre>




### Math:Sin(f)

The sine function

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>f</td><td>number</td><td>The input value in radians</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>result = Math:Sin(0.1)</strong></code></pre>




### Math:Sqrt(f)

The square root function

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>f</td><td>number</td><td>The input value</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>result = Math:Sqrt(0.1)</strong></code></pre>




### Math:SmoothStep(from, to, t)

The smoothstep function

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>from</td><td>number</td><td>The lower range</td></tr>
<tr><td>to</td><td>number</td><td>The upper range</td></tr>
<tr><td>t</td><td>number</td><td>The input value</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>result = Math:SmoothStep(0, 1, 0.5)</strong></code></pre>




### Math:Tan(f)

The tangent of an angle

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>f</td><td>number</td><td>The input value</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>result = Math:Tan(0.1)</strong></code></pre>




### Math:Sinh(f)

The hyperbolic sine function

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>f</td><td>number</td><td>The input value in radians</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>result = Math:Sinh(0.1)</strong></code></pre>




### Math:Cosh(f)

The hyperbolic cosine function

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>f</td><td>number</td><td>The input value in radians</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>result = Math:Cosh(0.1)</strong></code></pre>




### Math:Tanh(f)

The hyperbolic tangent function

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>f</td><td>number</td><td>The input value in radians</td></tr></tbody></table>




#### Example

<pre class="language-lua"><code class="lang-lua"><strong>result = Math:Tanh(0.1)</strong></code></pre>



    

