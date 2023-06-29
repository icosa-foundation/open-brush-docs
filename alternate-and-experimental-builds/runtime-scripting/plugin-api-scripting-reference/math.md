
# Math

## Summary
Various maths functions

## Class Properties

<table>
<thead><tr><th width="225">Name</th><th width="160">Return Type</th><th width="80">Read/Write?</th><th>Description</th></tr></thead>
<tbody>
<tr><td>deg2Rad</td><td>number</td><td>Read-only</td><td>Yes</td><td>A constant that when multiplied by a value in degrees converts it to radians</td></tr>
<tr><td>epsilon</td><td>number</td><td>Read-only</td><td>Yes</td><td>The smallest value that a float can have such that 1.0+ ε != 1.0</td></tr>
<tr><td>positiveInfinity</td><td>number</td><td>Read-only</td><td>Yes</td><td>Positive Infinity</td></tr>
<tr><td>negativeInfinity</td><td>number</td><td>Read-only</td><td>Yes</td><td>Negative Infinity</td></tr>
<tr><td>pi</td><td>number</td><td>Read-only</td><td>Yes</td><td>The value of Pi</td></tr>
<tr><td>rad2Deg</td><td>number</td><td>Read-only</td><td>Yes</td><td>A constant that when multiplied by a value in radians converts it to degrees</td></tr>
</tbody></table>




## Class Methods

        
### Math:Abs(f)

Returns the absolute value of f

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>f</td><td>number</td><td></td></tr></tbody></table>






### Math:Acos(f)

Returns the arc-cosine of f - the angle in radians whose cosine is f

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>f</td><td>number</td><td></td></tr></tbody></table>






### Math:Approximately(a, b)

Compares two floating point values if they are similar

**Returns:** boolean


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td>number</td><td></td></tr>
<tr><td>b</td><td>number</td><td></td></tr></tbody></table>






### Math:Asin(f)

Returns the arc-sine of f - the angle in radians whose sine is f

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>f</td><td>number</td><td></td></tr></tbody></table>






### Math:Atan(f)

Returns the arc-tangent of f - the angle in radians whose tangent is f

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>f</td><td>number</td><td></td></tr></tbody></table>






### Math:Atan2(y, x)

Returns the angle in radians whose tan is y/x

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>y</td><td>number</td><td></td></tr>
<tr><td>x</td><td>number</td><td></td></tr></tbody></table>






### Math:Ceil(f)

Returns the smallest integer greater to or equal to f

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>f</td><td>number</td><td></td></tr></tbody></table>






### Math:Clamp(value, min, max)

Clamps the given value between the given minimum float and maximum float values. Returns the given value if it is within the min and max range

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>value</td><td>number</td><td></td></tr>
<tr><td>min</td><td>number</td><td></td></tr>
<tr><td>max</td><td>number</td><td></td></tr></tbody></table>






### Math:Clamp01(value)

Clamps value between 0 and 1 and returns value

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>value</td><td>number</td><td></td></tr></tbody></table>






### Math:ClosestPowerOfTwo(value)

Returns the closest power of two value

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>value</td><td>number</td><td></td></tr></tbody></table>






### Math:Cos(f)

Returns the cosine of angle f

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>f</td><td>number</td><td></td></tr></tbody></table>






### Math:DeltaAngle(current, target)

Calculates the shortest difference between two given angles

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>current</td><td>number</td><td></td></tr>
<tr><td>target</td><td>number</td><td></td></tr></tbody></table>






### Math:Exp(power)

Returns e raised to the specified power

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>power</td><td>number</td><td></td></tr></tbody></table>






### Math:Floor(f)

Rounds a float down to the largest integer less than or equal to it

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>f</td><td>number</td><td></td></tr></tbody></table>






### Math:InverseLerp(a, b, value)

Inverse linear interpolation between two values by given ratio

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td>number</td><td></td></tr>
<tr><td>b</td><td>number</td><td></td></tr>
<tr><td>value</td><td>number</td><td></td></tr></tbody></table>






### Math:IsPowerOfTwo(value)

Determines whether a value is a power of two

**Returns:** boolean


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>value</td><td>number</td><td></td></tr></tbody></table>






### Math:Lerp(a, b, t)

Linearly interpolates two floats by a ratio

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td>number</td><td></td></tr>
<tr><td>b</td><td>number</td><td></td></tr>
<tr><td>t</td><td>number</td><td></td></tr></tbody></table>






### Math:LerpAngle(a, b, t)

Linearly interpolates two angles by a ratio

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td>number</td><td></td></tr>
<tr><td>b</td><td>number</td><td></td></tr>
<tr><td>t</td><td>number</td><td></td></tr></tbody></table>






### Math:LerpUnclamped(a, b, t)

Linearly interpolates two floats by a ratio. The interpolation is not clamped

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td>number</td><td></td></tr>
<tr><td>b</td><td>number</td><td></td></tr>
<tr><td>t</td><td>number</td><td></td></tr></tbody></table>






### Math:Log(f, p)

Returns the logarithm of a specified number in a specified base

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>f</td><td>number</td><td></td></tr>
<tr><td>p</td><td>number</td><td></td></tr></tbody></table>






### Math:Log10(f)

Returns the base 10 logarithm of a specified number

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>f</td><td>number</td><td></td></tr></tbody></table>






### Math:Max(a, b)

Returns the larger of two float numbers

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td>number</td><td></td></tr>
<tr><td>b</td><td>number</td><td></td></tr></tbody></table>






### Math:Max(values)

Returns the largest value in a sequence of float numbers

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>values</td><td>number[]</td><td></td></tr></tbody></table>






### Math:Min(a, b)

Returns the smaller of two float numbers

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td>number</td><td></td></tr>
<tr><td>b</td><td>number</td><td></td></tr></tbody></table>






### Math:Min(values)

Returns the smallest value in a sequence of float numbers

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>values</td><td>number[]</td><td></td></tr></tbody></table>






### Math:MoveTowards(current, target, maxDelta)

Moves a value current towards target

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>current</td><td>number</td><td></td></tr>
<tr><td>target</td><td>number</td><td></td></tr>
<tr><td>maxDelta</td><td>number</td><td></td></tr></tbody></table>






### Math:NextPowerOfTwo(value)

Returns the smallest power of two greater than or equal to the specified number

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>value</td><td>number</td><td></td></tr></tbody></table>






### Math:PerlinNoise(x, y)

Creates a two-dimensional Perlin noise map

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>x</td><td>number</td><td></td></tr>
<tr><td>y</td><td>number</td><td></td></tr></tbody></table>






### Math:PingPong(t, length)

Loops the value t, so that it is never larger than length and never smaller than 0

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>t</td><td>number</td><td></td></tr>
<tr><td>length</td><td>number</td><td></td></tr></tbody></table>






### Math:Pow(f, p)

Returns f raised to the specified power

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>f</td><td>number</td><td></td></tr>
<tr><td>p</td><td>number</td><td></td></tr></tbody></table>






### Math:Repeater(t, length)

Loops the value t, so that it is never larger than length and never smaller than 0

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>t</td><td>number</td><td></td></tr>
<tr><td>length</td><td>number</td><td></td></tr></tbody></table>






### Math:Round(f)

Rounds a float to the nearest integer

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>f</td><td>number</td><td></td></tr></tbody></table>






### Math:Sign(f)

Returns the sign of a float

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>f</td><td>number</td><td></td></tr></tbody></table>






### Math:Sin(f)

Returns the sine of an angle

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>f</td><td>number</td><td></td></tr></tbody></table>






### Math:Sqrt(f)

Returns the square root of a float

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>f</td><td>number</td><td></td></tr></tbody></table>






### Math:SmoothStep(from, to, t)

Smoothly interpolates between the range [from, to] by the ratio t

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>from</td><td>number</td><td></td></tr>
<tr><td>to</td><td>number</td><td></td></tr>
<tr><td>t</td><td>number</td><td></td></tr></tbody></table>






### Math:Tan(f)

Returns the tangent of an angle

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>f</td><td>number</td><td></td></tr></tbody></table>






### Math:Sinh(f)

Returns the hyperbolic sine of a float

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>f</td><td>number</td><td></td></tr></tbody></table>






### Math:Cosh(f)

Returns the hyperbolic cosine of a float

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>f</td><td>number</td><td></td></tr></tbody></table>






### Math:Tanh(f)

Returns the hyperbolic tangent of a float

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>f</td><td>number</td><td></td></tr></tbody></table>





    

