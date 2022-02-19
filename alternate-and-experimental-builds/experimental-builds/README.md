# Andybak's Experimental Builds

Note - I'm maintaining each feature as a separate build as some are probably more viable to merge into the official Open Brush than others (or at least - will be viable sooner).

~~However - if you want the kitchen sink version with everything included you can download an~~ [~~integration build~~](https://github.com/IxxyXR/open-brush/wiki/Downloads) ~~and test out all the features together~~

~~That contains all the features mentioned below. In some cases they might intefere with each other to some degree but I'll fix those issues as soon as I spot them.~~

(currently I'm not keeping the integration build up to date. I'll do that again soon)

On to the features...

## Current Feature Builds

### [1. Polyhedra and Symmetry](polyhedra-and-symmetry.md)

[more info and download](polyhedra-and-symmetry.md)

This is basically my other project Polyhydra ( [https://andybak.net/polyhydra](https://andybak.net/polyhydra) ) smushed together with Tilt Brush. Create a wide range of geometric forms and use them as the basis for complex mirroring of your brush strokes.

![](../../.gitbook/assets/polyhedra\_tool.png)

### [2. Snip Tool](snip-tool.md)

[more info and download](snip-tool.md)

Splits existing strokes.

![](<../../.gitbook/assets/image (13).png>)

### [3. Layers](layers.md)

[more info and download](layers.md)

Organize your sketch into layers that can be turned on or off separately.

![](<../../.gitbook/assets/image (11).png>)

### [4. Brush Editing](brush-editing.md)

[more info and download](brush-editing.md)

Edit brushes directly in VR. Change textures, shininess and other parameters

{% embed url="https://www.youtube.com/watch?v=G3LN3OEPqKQ" %}

## Previous Feature Builds

The following features are now merged into the upcoming 1.0 beta

### [1. Open Brush API](../../user-guide/open-brush-api/)

[more info and download](../../user-guide/open-brush-api/)

Create Tilt Brush sketches by sending simple commands from a web browser. Works with any language that can send http requests - including via simple HTML forms. You can even use it without any programming at all by just typing urls into the browser address bar.

It doesn't even need VR. You can create 3D works of art on a desktop machine and export the results without ever putting on a headset.

Contains some cool example scripts showing what's possible.

![](../../.gitbook/assets/parametric1.png)

### [2. Grid and Angle Snapping](../../user-guide/grid-and-angle-snapping.md)

[more info and download](../../user-guide/grid-and-angle-snapping.md)

Selecting and duplicating brush strokes currently doesn't support snapping. This changes that. It also allows snapping to angles other than 90 degrees.

And an entirely new feature is snapping to a grid so you can create regularly spaced duplicates of any selected brush strokes.

![](https://media.discordapp.net/attachments/804251582715265034/846812293177933894/2021-05-25\_19-06-31.gif)

### [3. Repaint Tool and Improved Jitter](https://github.com/IxxyXR/open-brush/wiki/Color-Jitter)

[more info and download](color-jitter.md)

The "Recolor" tool can now change the size, color and brush used for existing strokes. Also we've improved the "color jitter" feature so each brush stroke can have it's colour randomized slightly and also it's size or it's actual shape! This works while painting and also with the "Repaint tool" so you can add natural random variation to existing brush strokes.

{% embed url="https://www.youtube.com/watch?v=as_ty_89Bfk" %}
