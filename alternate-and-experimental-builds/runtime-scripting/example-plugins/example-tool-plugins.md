# Example Tool Plugins

### Circle

Draws a circle centered on the position you first press the trigger with the radius and orientation controlled by where you release the trigger.

### CircularPath

{% embed url="https://www.youtube.com/watch?v=RGpsjA3hUCc" %}

Similar to [Circle ](example-tool-plugins.md#circle)except it creates a camera path instead of a brush stroke

#### Parameters

* **Sides:** The circle is approximated by a polygon. This controls the number of sides.

### Cube

Draws a cube centered on the position you first press the trigger with the size and orientation controlled by where you release the trigger.

#### Parameters

* **Point Spacing:** The distance between control points for the strokes that make up the cube
* **Inset Amount:** How much to inset each face towards it's center

### LowPolyLandscape

{% embed url="https://www.youtube.com/watch?v=uRlrzk91QN4" %}

Draws tiles that follow a hilly landscape as you hold the trigger.

#### Parameters

* **Scale**
* **Height**
* **Offset**
* **Grid Size**

### RandomAvatar

{% embed url="https://www.youtube.com/watch?v=S9TzdMAbAbU" %}

Calls an API to generate a random SVG icon using the [MultiAvatar ](https://multiavatar.com/)library

### RandomIcon

Calls an API to generate a random SVG icon using the [Iconify ](https://iconify.design/docs/api/)library

### Rays

Draws lines from the position you start drawing to your current position.

#### Parameters

* **Spacing:**&#x20;

### ReplayStroke

Instantly draws a brush stroke based on the path of the last brush stroke you drew

### ScatterCubes

Switches to the Hull Brush and draws cubes of random size and color as you move your brush",

#### Parameters

* **Maximum Size**
* **Spread**
* **Amount**

### Spiral

Draws a conical spiral.

#### Parameters

* **Number of turns**
* **Number of steps per turn**

### SpiralSphere

Draws a spherical spiral.

#### Parameters

* **Steps**
* **Turns**

### SuperEllipse

Draws a [superellipse](https://en.wikipedia.org/wiki/Superellipse).

#### Parameters

* **n**

### SuperFormula

Draws a supershape using the [Super Formula](http://paulbourke.net/geometry/supershape/)

#### Parameters

* **Symmetry**
* **n1**
* **n2**
* **n3**

### SvgHeart

Draws a heart shape using an [SVG Path](https://developer.mozilla.org/en-US/docs/Web/SVG/Tutorial/Paths)

#### Parameters

* **Point Spacing**

### VoxelLandscape

Draws a blocky landscape (best used with a hull brush)",

#### Parameters

* **Horizontal Spacing**
* **Verticle Spacing**

### Voxels

Draws regular blocks in space as you draw (best used with the hull brush)

#### Parameters

* **Grid Size**

### Words

{% embed url="https://www.youtube.com/watch?v=x-3K_0jT3Pg" %}

Draws words that follows your brush. Tries to access the clipboard so try copying in some text.

#### Parameters

* **Size**
* **Spacing**

