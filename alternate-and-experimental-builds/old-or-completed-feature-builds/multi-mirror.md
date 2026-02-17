# Feature: Multi-Mirror

#### <mark style="color:red;background-color:red;">**THIS BRANCH HAS BEEN RELEASED AND IS PART OF THE REGULAR VERSION OF OPEN BRUSH**</mark>

#### Status: Released in [v2.4](../../release-history/v2.4-prismatic.md)

![](../../.gitbook/assets/image-028.png) ![](../../.gitbook/assets/image-041.png)

![](../../.gitbook/assets/image-042.png) ![](../../.gitbook/assets/image-088.png)

### What does it do?

Big expansion to the mirror to support many different types of symmetry:

**Point symmetry:** Symmetry around a point. 7 familiies of axial symmetry plus 3 (soon to be 7) unique polyhedral symmetries.

**Wallpaper symmetry:** 17 types of tiling symmetry

**Duplicate selections using symmetry:** Create multiple clones of a selection aligned in a pattern

**Draw with multiple colours at the same time:** The colour of each stroke can be varied in interesting new ways

### What's it good for?

Creating symmetrical patterns. Drawing multiple strokes at the same time. Arranging models or images into grids or other regular patterns.

### How do I install it?

This is now part of the regular release of Open Brush

### How do I use it?

Hold down the mirror button on the Experimental Panel for a second or two:

![](../../.gitbook/assets/image-096.png)

This will bring up the Symmetry settings panel which contains three tabs:

#### Point Symmetry

Point symmetry creates copies arranged around the center of the mirror widget. Each icon selects one of the 14 different types of symmetry. This is the symmetry of molecules and polyhedra. It can create shapes such as stars, explosions, vases, octopi or plants and flowers.

For the first 7 point symmetry types, the slider controls how many copies are arranged around the center axis. (The other 7 types are based on tetrahedra, cubes and icosohedron and have a fixed number of copies)

#### Wallpaper Symmetry

![](../../.gitbook/assets/image-006.png)

Wallpaper symmetry repeats your strokes in various types grid pattern - reflecting or rotating in specific ways. You can create wallpaper, floor tiles crystal lattices or any other repeating patterns.

For all symmetry types you have control over the number of copies in x and y directions. For some you can also change the scale of the grid in both the x and y directions and skew the grid cells themselves in either direction.

#### Options

![](../../.gitbook/assets/image-087.png)

This screen allows you to vary the colour of each stroke based on waveforms of your choosing. Colors can cycle based on hue, saturation or brightness and the amount, frequency and type of the variance can be precisely controlled

### Known Issues

1. It's very easy to create so many strokes or duplicates of 3D models that Open Brush becomes unresponsive or even crashes. We plan to add limits and warnings once we figure out how best to calculate them.
2. A few symmetry modes move the main pointer so your main stroke is rotated somewhere else. It takes a bit of getting used to but it doesn't actually prevent you painting in these modes.

## How do I get help

Come over to the Open Brush Discord: [https://discord.openbrush.app](https://discord.openbrush.app) and chat to me ( andybak#5425 ).

I'm on UK time but I check in fairly regularly.

### Can I see it in action?

{% embed url="https://www.youtube.com/watch?v=khsI-7rl2yg" %}
Some early experiments with spinning mirrors
{% endembed %}

{% embed url="https://youtu.be/VxVjkV_CkFs" %}
Another early test of the feature
{% endembed %}
