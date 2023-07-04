# Example Symmetry Plugins

### AlongStroke

The previous stroke you drew is used as a template and multiple copies of the pointer are spread along it as you draw

#### Parameters

* **Point Spacing:** The distance to space out the copies along the stroke

### AutoLathe

Like spinning the mirror by hand but with precise control

#### Parameters

* **Speed:** How fast to spin
* **Angle X:** The axis tilt in the X direction
* **Angle Y:** The axis tilt in the Y direction

### Boids

A flock of pointers follows your hand using simple rules to control how they fly

#### Parameters

* **Number of copies:** How many boids in the flock
* **Separation Amount:** How strongly each boid tries to stay away from others
* **Alignment Amount:** How closely the boids try and follow the flocks path
* **Pointer Attraction:** How strongly each boid is attracted to your brush position

### Ducklings

{% embed url="https://www.youtube.com/watch?v=WkGY_nXPehc" %}

The pointers follow your brush position but each one moves towards a point where your hand was further back in time

#### Parameters

* **Copies:** The number of strokes to draw at once
* **Delay per copy:** How far back in time (in frames) for each copy
* **Amount:** How far between the current and past position to move towards. 0.5 is the midpoint between past and current

### EllipseAround

{% embed url="https://www.youtube.com/watch?v=e3JXcvarGkI" %}

Copies of your stroke forming an ellipse - with optional color shifts

#### Parameters

* **Copies:** The number of strokes to draw at once
* **Eccentricity:** How elliptical the shape is
* **Axis Consistency**

### Frame

A simple frame of points following your brush position

### HoldFirstClick

{% embed url="https://www.youtube.com/watch?v=JS06ssbbCi0" %}

Like [Many Around](example-symmetry-plugins.md#manyaround) except the widget always moves to where you start drawing

#### Parameters

* **Copies:** The number of strokes to draw at once

### ManyAlong

Linear copies of your stroke with optional color shifts

#### Parameters

* **Copies:** The number of strokes to draw at once
* **Distance:** How far each copy is from the next

### ManyAround

Radial copies of your stroke with optional color shifts

#### Parameters

* **Copies:** The number of strokes to draw at once

### MultiLathe

Autolathe but with multiple lathes"

#### Parameters

* **Speed**
* **Angle X:** The axis tilt in the X direction
* **Angle Y:** The axis tilt in the Y direction

### OmniLathe

Like [Autolathe ](example-symmetry-plugins.md#autolathe)but you can vary the axis orientation

#### Parameters

* **Speed X:** How fast to spin the X axis
* **Speed Y:** How fast to spin the Y axis

### Pole

{% embed url="https://www.youtube.com/watch?v=7YxjNvCY8ak" %}

Multiple copies of your brush spaced between your left and right hand positions

#### Parameters

* **Copies:** The number of strokes to draw at once

### PolygonAround

Copies of your stroke forming an polygon

#### Parameters

* **Copies:** The number of strokes to draw at once
* **Sides:** The number of sides of the polygon

### RectangleAround

Copies of your stroke forming an rectangle

#### Parameters

* **Number of points along width:** How many points along the sides
* **Number of points along height:** How many points along the top and bottom
* **Spacing:** The distance between each point
* **Exterior Only:** Whether to create copies just around the perimeter or also fill in the middle

### Spin

Multiple copies of your brush spinning around your actual brush position

#### Parameters

* **Copies:** The number of strokes to draw at once
* **Speed:**&#x20;
* **Radius:**&#x20;

### SuperEllipseAround

Copies of your stroke forming a [superellipse](https://en.wikipedia.org/wiki/Superellipse)

#### Parameters

* **Copies:** The number of strokes to draw at once
* **n:** The parameter that controls the overall shape of the superellipse
* **Eccentricity:** How elliptical to make the shape
* **Axis Consistency:**&#x20;

### Svg

An example of using an SVG file as a template for symmetry patterns

### SvgAround

Similar to [SVG](example-symmetry-plugins.md#svg) but centered around the Symmetry Widget

#### Parameters

* **Point Spacing**

### ToGuide

A line of copies between a guide and the symmetry widget

#### Parameters

* **Copies:** The number of strokes to draw at once

### TooManyAround

Based on [Many Around](example-symmetry-plugins.md#manyaround) - this was originally a bug but I liked it so here it is.

#### Parameters

* **Copies:** The number of strokes to draw at once

###
