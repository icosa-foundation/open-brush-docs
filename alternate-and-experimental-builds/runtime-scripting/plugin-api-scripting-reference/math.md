
# Math

## Summary

Various maths functions


## Properties

<table>
<thead><tr><th width="225">Name</th><th width="160">Return Type</th><th>Description</th></tr></thead>
<tbody>
<tr><td>deg2Rad</td><td>number</td><td>A constant that when multiplied by a value in degrees converts it to radians</td></tr>
<tr><td>epsilon</td><td>number</td><td>The smallest value that a float can have such that 1.0+ ε != 1.0</td></tr>
<tr><td>positiveInfinity</td><td>number</td><td>Positive Infinity</td></tr>
<tr><td>negativeInfinity</td><td>number</td><td>Negative Infinity</td></tr>
<tr><td>pi</td><td>number</td><td>The value of Pi</td></tr>
<tr><td>rad2Deg</td><td>number</td><td>A constant that when multiplied by a value in radians converts it to degrees</td></tr>
<tr><td></td><td></td><td></td></tr></tbody></table>




## Methods


### Math:Abs

Returns the absolute value of f

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>f</td><td>number</td><td></td></tr></tbody></table>






### Math:Acos

Returns the arc-cosine of f - the angle in radians whose cosine is f

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>f</td><td>number</td><td></td></tr></tbody></table>






### Math:Approximately

Compares two floating point values if they are similar

**Returns:** boolean


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td>number</td><td></td></tr>
<tr><td>b</td><td>number</td><td></td></tr></tbody></table>






### Math:Asin

Returns the arc-sine of f - the angle in radians whose sine is f

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>f</td><td>number</td><td></td></tr></tbody></table>






### Math:Atan

Returns the arc-tangent of f - the angle in radians whose tangent is f

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>f</td><td>number</td><td></td></tr></tbody></table>






### Math:Atan2

Returns the angle in radians whose tan is y/x

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>y</td><td>number</td><td></td></tr>
<tr><td>x</td><td>number</td><td></td></tr></tbody></table>






### Math:Ceil

Returns the smallest integer greater to or equal to f

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>f</td><td>number</td><td></td></tr></tbody></table>






### Math:Clamp

Clamps the given value between the given minimum float and maximum float values. Returns the given value if it is within the min and max range

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>value</td><td>number</td><td></td></tr>
<tr><td>min</td><td>number</td><td></td></tr>
<tr><td>max</td><td>number</td><td></td></tr></tbody></table>






### Math:Clamp01

Clamps value between 0 and 1 and returns value

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>value</td><td>number</td><td></td></tr></tbody></table>






### Math:ClosestPowerOfTwo

Returns the closest power of two value

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>value</td><td>number</td><td></td></tr></tbody></table>






### Math:Cos

Returns the cosine of angle f

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>f</td><td>number</td><td></td></tr></tbody></table>






### Math:DeltaAngle

Calculates the shortest difference between two given angles

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>current</td><td>number</td><td></td></tr>
<tr><td>target</td><td>number</td><td></td></tr></tbody></table>






### Math:Exp

Returns e raised to the specified power

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>power</td><td>number</td><td></td></tr></tbody></table>






### Math:Floor

Rounds a float down to the largest integer less than or equal to it

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>f</td><td>number</td><td></td></tr></tbody></table>






### Math:InverseLerp

Inverse linear interpolation between two values by given ratio

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td>number</td><td></td></tr>
<tr><td>b</td><td>number</td><td></td></tr>
<tr><td>value</td><td>number</td><td></td></tr></tbody></table>






### Math:IsPowerOfTwo

Determines whether a value is a power of two

**Returns:** boolean


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>value</td><td>number</td><td></td></tr></tbody></table>






### Math:Lerp

Linearly interpolates two floats by a ratio

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td>number</td><td></td></tr>
<tr><td>b</td><td>number</td><td></td></tr>
<tr><td>t</td><td>number</td><td></td></tr></tbody></table>






### Math:LerpAngle

Linearly interpolates two angles by a ratio

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td>number</td><td></td></tr>
<tr><td>b</td><td>number</td><td></td></tr>
<tr><td>t</td><td>number</td><td></td></tr></tbody></table>






### Math:LerpUnclamped

Linearly interpolates two floats by a ratio. The interpolation is not clamped

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td>number</td><td></td></tr>
<tr><td>b</td><td>number</td><td></td></tr>
<tr><td>t</td><td>number</td><td></td></tr></tbody></table>






### Math:Log

Returns the logarithm of a specified number in a specified base

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>f</td><td>number</td><td></td></tr>
<tr><td>p</td><td>number</td><td></td></tr></tbody></table>






### Math:Log10

Returns the base 10 logarithm of a specified number

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>f</td><td>number</td><td></td></tr></tbody></table>






### Math:Max

Returns the larger of two float numbers

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td>number</td><td></td></tr>
<tr><td>b</td><td>number</td><td></td></tr></tbody></table>






### Math:Max

Returns the largest value in a sequence of float numbers

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>values</td><td>number[]</td><td></td></tr></tbody></table>






### Math:Min

Returns the smaller of two float numbers

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>a</td><td>number</td><td></td></tr>
<tr><td>b</td><td>number</td><td></td></tr></tbody></table>






### Math:Min

Returns the smallest value in a sequence of float numbers

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>values</td><td>number[]</td><td></td></tr></tbody></table>






### Math:MoveTowards

Moves a value current towards target

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>current</td><td>number</td><td></td></tr>
<tr><td>target</td><td>number</td><td></td></tr>
<tr><td>maxDelta</td><td>number</td><td></td></tr></tbody></table>






### Math:NextPowerOfTwo

Returns the smallest power of two greater than or equal to the specified number

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>value</td><td>number</td><td></td></tr></tbody></table>






### Math:PerlinNoise

Creates a two-dimensional Perlin noise map

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>x</td><td>number</td><td></td></tr>
<tr><td>y</td><td>number</td><td></td></tr></tbody></table>






### Math:PingPong

Loops the value t, so that it is never larger than length and never smaller than 0

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>t</td><td>number</td><td></td></tr>
<tr><td>length</td><td>number</td><td></td></tr></tbody></table>






### Math:Pow

Returns f raised to the specified power

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>f</td><td>number</td><td></td></tr>
<tr><td>p</td><td>number</td><td></td></tr></tbody></table>






### Math:Repeater

Loops the value t, so that it is never larger than length and never smaller than 0

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>t</td><td>number</td><td></td></tr>
<tr><td>length</td><td>number</td><td></td></tr></tbody></table>






### Math:Round

Rounds a float to the nearest integer

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>f</td><td>number</td><td></td></tr></tbody></table>






### Math:Sign

Returns the sign of a float

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>f</td><td>number</td><td></td></tr></tbody></table>






### Math:Sin

Returns the sine of an angle

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>f</td><td>number</td><td></td></tr></tbody></table>






### Math:Sqrt

Returns the square root of a float

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>f</td><td>number</td><td></td></tr></tbody></table>






### Math:SmoothStep

Smoothly interpolates between the range [from, to] by the ratio t

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>from</td><td>number</td><td></td></tr>
<tr><td>to</td><td>number</td><td></td></tr>
<tr><td>t</td><td>number</td><td></td></tr></tbody></table>






### Math:Tan

Returns the tangent of an angle

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>f</td><td>number</td><td></td></tr></tbody></table>






### Math:Sinh

Returns the hyperbolic sine of a float

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>f</td><td>number</td><td></td></tr></tbody></table>






### Math:Cosh

Returns the hyperbolic cosine of a float

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>f</td><td>number</td><td></td></tr></tbody></table>






### Math:Tanh

Returns the hyperbolic tangent of a float

**Returns:** number


**Parameters:**

<table data-full-width="false">
<thead><tr><th width="217">Name</th><th width="134">Type</th><th>Description</th></tr></thead>
<tbody><tr><td>f</td><td>number</td><td></td></tr></tbody></table>






