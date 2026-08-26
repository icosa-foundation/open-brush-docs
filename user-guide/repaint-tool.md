# Repaint Tool and Jitter

### What does it do?

It expands on the previous Recolor tool which is now renamed to "Repaint". The following features can be used individually or in any combination:

#### Recolor

Same as before (but see the "jitter" feature below which adds new functionality to Recolo)

#### Rebrush

Similar to "Recolor" except it repaints existings strokes with a different brush. This is the same as the"Rebrush" tool in previous experimental builds. That feature is now part of this Repaint Tool)

#### Resize

Change the brush size of existing strokes.

#### Jitter

When this option is turned on, recolor and resize will add random variations based on your current Jitter settings.

### Jitter Improvements

Open the Jitter settings from the dice button near the bottom of the colour picker. These settings affect new strokes and can also be applied by the Repaint tool.

#### Colour Jitter

The Hue, Saturation and Value sliders control how much those colour components can vary from one stroke to the next. A value at the far left adds no variation; increasing a slider widens the random range around the selected colour.

#### Jitter Brush Size

This slider controls how much the stroke size varies from stroke to stroke. The far-left position adds no variation; moving it right increases the random size range.

#### Jitter Positions

![](<../.gitbook/assets/image-017.png>)

This slider controls how much randomness is applied to each point on a brush stroke. The far-left position adds no variation; moving it right shifts points farther from their usual positions. At higher settings, some brushes appear to split into multiple small strokes.

### Things to try

1. Try a high setting for "Jitter positions" and press the trigger to draw but don't move your hand. You'll get a small spherical "squiggle" that can be very interesting with some brushes.
2. Draw something regular with the Hull brush and make copies of it. Then use the "Repaint Tool" with a low setting for "Jitter positions" to add random variation to each copy
3. Position jitter can cause strokes to break into many small strokes. This depends on the brush you use and amount of jitter. Try really low jitter settings, try smaller brush sizes and try different brush types such as tube brushes (they tend not to break up as much)

### What's it good for?

Modifying parts of existing sketches. Adding random variation after you've already painted something. Trying out different brushes and reusing parts of a sketch with different properties. (try duplicating some strokes and then repainting the duplicate)

### How do I use it?

The Recolor button on the Tools Panel has been replaced with "Repaint". When you select it, a side panel appears with 4 toggle buttons: Recolor, Resize, Rebrush and Jitter.

Any combination of these 4 options can be selected at any time. If you choose "jitter" then set your chosen amount of jitter using the button with the dice icon at the bottom of the Color Picker Panel

## Repaint Selection

Instead of repainting strokes one at a time, you can select multiple strokes and apply repaint operations to all of them at once:

1. Use the Selection tool to select the strokes you want to modify.
2. Open the Repaint options and enable the operations you want: Recolor, Resize, Rebrush or Jitter.
3. Choose the new colour, brush and size, and configure jitter if required.
4. Select **Repaint Selected** on the selection controls to apply those settings to every selected stroke.

This is particularly useful for:

1. Changing the colour scheme of multiple strokes at once.
2. Applying consistent size changes to a group of strokes.
3. Converting multiple strokes to a different brush type.
4. Adding jitter variation to duplicated elements.

### Can I see it in action?

{% embed url="https://youtu.be/mScGKQke4QA" %}

![Hull brush drawn with the Polyhedra tool with color and position jitter added](<../.gitbook/assets/image-014.png>)
