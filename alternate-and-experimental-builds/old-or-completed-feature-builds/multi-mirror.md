# Feature: Multi-Mirror

#### Status: Released in [v2.4](broken-reference)

![](<../../.gitbook/assets/image (14).png>) ![](<../../.gitbook/assets/image (2) (3).png>)

![](<../../.gitbook/assets/image (2) (4).png>) ![](<../../.gitbook/assets/image (7) (4).png>)

## Downloads

This feature has now been merged into the [beta release](../open-brush-beta-docs.md)

### What does it do?

Big expansion to the mirror to support many different types of symmetry:

**Point symmetry:** Symmetry around a point. 7 familiies of axial symmetry plus 3 (soon to be 7) unique polyhedral symmetries.

**Wallpaper symmetry:** 17 types of tiling symmetry

**Duplicate selections using symmetry:** Create multiple clones of a selection aligned in a pattern

**Draw with multiple colours at the same time:** The colour of each stroke can be varied in interesting new ways

### What's it good for?

Creating symmetrical patterns. Drawing multiple strokes at the same time. Arranging models or images into grids or other regular patterns.

### How do I install it?

Download a build for your headset from the link above and unzip it. You can run the Windows exe directly. To install the Quest apk use SideQuest: [https://uploadvr.com/sideloading-quest-how-to/](https://uploadvr.com/sideloading-quest-how-to/)

### How do I use it?

Hold down the mirror button on the Experimental Panel for a second or two:

![](<../../.gitbook/assets/image (9) (1).png>)

This will bring up the Symmetry settings panel which contains three tabs:

#### Point Symmetry

<figure><img src="../../.gitbook/assets/image (25).png" alt=""><figcaption></figcaption></figure>

Point symmetry creates copies arranged around the center of the mirror widget. Each icon selects one of the 14 different types of symmetry. This is the symmetry of molecules and polyhedra. It can create shapes such as stars, explosions, vases, octopi or plants and flowers.

For the first 7 point symmetry types, the slider controls how many copies are arranged around the center axis. (The other 7 types are based on tetrahedra, cubes and icosohedron and have a fixed number of copies)

#### Wallpaper Symmetry

![](<../../.gitbook/assets/image (1) (1) (2) (1).png>)

Wallpaper symmetry repeats your strokes in various types grid pattern - reflecting or rotating in specific ways. You can create wallpaper, floor tiles crystal lattices or any other repeating patterns.

For all symmetry types you have control over the number of copies in x and y directions. For some you can also change the scale of the grid in both the x and y directions and skew the grid cells themselves in either direction.

#### Options

![](<../../.gitbook/assets/image (7) (3).png>)

This screen allows you to vary the colour of each stroke based on waveforms of your choosing. Colors can cycle based on hue, saturation or brightness and the amount, frequency and type of the variance can be precisely controlled.

### Creating Patterns From Existing Brush Strokes

(This feature currently has some bugs. See [known issues](multi-mirror.md#known-issues))

~~You can also create symmetrical copies from existing strokes. Simple select the strokes you want to use and duplicate them in the same way you do without the mirror (Press the secondary button on the controller you paint with)~~

_Currently disabled while I iron out the bugs_

### Creating Symmetrical Patterns from Imported Objects

~~As well as duplicating brush strokes, if you have~~ [~~imported some media~~](../../user-guide/using-reference-images-on-oculus-quest.md) ~~such as images, video or 3D objects then you can select those and create copies that follow the current symmetry settings.~~

~~Be aware that there are currently no limits in place. If you create copies of complex objects or even if you create lots and lots of copies of simple objects, then Open Brush can become unresponsive or even crash.~~

_Currently disabled while I iron out the bugs_

### Known Issues

1. It's very easy to create so many strokes or duplicates of 3D models that Open Brush becomes unresponsive or even crashes. We plan to add limits and warnings once we figure out how best to calculate them.
2. Duplicating brush strokes currently positions copies incorrectly if you've transformed the selection since selecting it. A workaround is to deselect and reselect first.
3. Duplicating brush strokes can position things incorrectly if you've scaled the world or moved the symmetry widget.
4. A few symmetry modes move the main pointer so your main stroke is rotated somewhere else. It takes a bit of getting used to but it doesn't actually prevent you painting in these modes.
5. The slider on the settings panel can glitch the Open Brush UI if you drag it past it's limits.

## How do I get help

Come over to the Open Brush Discord: [https://discord.com/invite/fS69VdFXpk](https://discord.com/invite/fS69VdFXpk) and chat to me ( andybak#5425 ).

I'm on UK time but I check in fairly regularly.

### Can I see it in action?

{% embed url="https://www.youtube.com/watch?v=khsI-7rl2yg" %}
Some early experiments with spinning mirrors
{% endembed %}

{% embed url="https://youtu.be/VxVjkV_CkFs" %}
Another early test of the feature
{% endembed %}

<div>

<figure><img src="../../.gitbook/assets/Untitled_1_00.png" alt=""><figcaption></figcaption></figure>

 

<figure><img src="../../.gitbook/assets/Untitled_2_00.png" alt=""><figcaption></figcaption></figure>

 

<figure><img src="../../.gitbook/assets/Untitled_6_00.png" alt=""><figcaption></figcaption></figure>

 

<figure><img src="../../.gitbook/assets/Untitled_5_00.png" alt=""><figcaption></figcaption></figure>

 

<figure><img src="../../.gitbook/assets/Untitled_9_00.png" alt=""><figcaption></figcaption></figure>

 

<figure><img src="../../.gitbook/assets/Untitled_117_00.png" alt=""><figcaption></figcaption></figure>

 

<figure><img src="../../.gitbook/assets/Untitled_118_01.png" alt=""><figcaption></figcaption></figure>

 

<figure><img src="../../.gitbook/assets/Untitled_127_00.png" alt=""><figcaption></figcaption></figure>

</div>
