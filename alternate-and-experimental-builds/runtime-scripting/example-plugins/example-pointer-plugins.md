# Example Pointer Plugins

### Connections

Connects the two most recent strokes with a series of lines. Draw one stroke then another. As you finish the second stroke you will see new lines added

#### Parameters

* **Number of sections:** How many connecting lines to draw

### Dashes

Stops and restarts the stroke at regular intervals as you draw resulting in a dashed line.

#### Parameters

* **Frequency:** How many dashes there are in a given distance. Shorter values gives a result closer to a dotted line.
* **Spacing:** Controls the spacing between dashes

#### How it works

The script calls`Brush:ForcePaintingOn` and `Brush:ForcePaintingOn` based on the value of `Brush:DistanceDrawn`

### GridFollow

Locks movement of the pointer to either the x, y or z axis depending on which direction your hand is mostly moving.&#x20;

#### Parameters

* **Speed:** How fast the pointer can move as it tries to keep up with your hand movements
* **Frames Between Changes:**&#x20;

#### Tips

Draw slowly and deliberately. It can be tricky to get the hang of originally

### Lagging

The pointer position cycles back and forth between the current position and where your hand was a short time before. The result is either loops or scribbles depending on the parameters and how quickly you move.

#### Parameters

* **Delay:**
* **Frequency:**
* **Amplitude:**&#x20;

### LaserBeam

The pointer continues moving in the direction you were pointing when you initially pressed the trigger. Pew pew...

#### Parameters

* **Speed:** The speed of the beam

### Loops

The pointer moves around a circlular path with your current hand position as it's center.

#### Parameters

* **Speed:**
* **Radius:**

### Missile

Similar to [LaserBeam](example-pointer-plugins.md#laserbeam) except that you can steer the brush stroke as it moves.

#### Parameters

* **Speed:** The speed of the missile

### Oscilloscope

Control your pointer with multiple waveforms to create patterns

#### Parameters

* **X Waveform Type:**
* **X Frequency:**&#x20;
* **Y Waveform Type:**&#x20;
* **Y Frequency:**&#x20;
* **Y Phase:**&#x20;
* **Radius:**&#x20;

### PolygonBrush

The brush draws a path around your current hand position similar to [Loops](example-pointer-plugins.md#loops) - except the path is a polygon instead of a circle.

#### Parameters

* **Points:**&#x20;
* **Size:**

### RainbowStrokes



#### Parameters

* **Rate:**&#x20;
* **Hue Shift Frequency:**
* **Hue Shift Amount:**

### SineWave

Moves the pointer in a simple wave pattern as you draw.

#### Parameters

* **Frequency**
* **Amplitude**

### Spherograph



#### Parameters

* U Scaling
* V Scaling
* Radius

### Spirals

The brush stroke moves in a circle but the radius increases the longer you keep the trigger pressed.

#### Parameters

* Speed
* Radius

### StringArt

Additional lines are drawn from the initial point you started drawing to your current brush position.

#### Parameters

* Rate

### Terrain

As you draw you only control the x and z position of the stroke. The y position (the height) is determined by a noise function that maps out hills and valleys.

#### Parameters

* Scale
* Height
* Offset

### Twist

As you draw the position is controlled by your hand as normal. However the orientation of the stroke spins around by itself

#### Parameters

* Speed

#### Tips

Try this with a broad flat brush like Paper or a brush that has an interesting profile shape such as Faceted Tube

### WandLerp

The brush position cycles back and forth between your brush hand and your other hand. Paint with both hands for a change...

#### Parameters

* Frequency
* Amplitude

#### Tips

Move your hands close together or further apart to see different effects

### Wander

The brush stroke wanders off in random directions while you hold the trigger

#### Parameters

* Speed
* Frames Per Path

### Wiggle

Randomizes the brush position

#### Parameters

* Wiggle Amount

### Wobble

Like Wiggle but uses a smooth noise function

#### Parameters

* Position Amount
* Rotation Amount
* Frequency

