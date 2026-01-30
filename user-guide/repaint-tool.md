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

In addition to the Repaint Tool, this build adds some new features to the existing "Color Jitter" settings on the Color picker (the Dice icon near the bottom)

#### Jitter Brush Size

This slider controls how much the stroke size varies from stroke to stroke. All the way to the left behaves normally. As you move the slider more to the right, each stroke will have more randomness applied to it's stroke size.

#### Jitter Positions

![](<../.gitbook/assets/image (12) (1) (1) (1) (1) (1).png>)

This slider controls how much randomness is applied to each point on a brush stroke. . All the way to the left behaves normally. As you move the slider more to the right, each point of the stroke will be randomly shifted from it's usual position. At higher settings and with some brushes this will cause the brush stroke to actually split and form multiple small strokes.

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

1. Use the selection tool to select the strokes you want to modify
2. Activate the Repaint tool with your desired settings (Recolor, Resize, Rebrush, or Jitter)
3. The selected strokes will all be repainted with the current settings

This is particularly useful for:
- Changing the color scheme of multiple strokes at once
- Applying consistent size changes to a group of strokes
- Converting multiple strokes to a different brush type
- Adding jitter variation to duplicated elements

### Can I see it in action?

{% embed url="https://youtu.be/mScGKQke4QA" %}

![Hull brush drawn with the Polyhedra tool with color and position jitter added](<../.gitbook/assets/image (11) (1) (1) (1).png>)
