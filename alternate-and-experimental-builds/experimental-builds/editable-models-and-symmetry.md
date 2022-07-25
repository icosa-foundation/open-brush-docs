# Editable Models & Symmetry

(These docs are a work in progress)

#### Status: Ready for beta testing

## Downloads

(These links aren't all currently working. I'm working on getting this fixed ASAP)

* [Oculus Quest](https://nightly.link/IxxyXR/open-brush/workflows/build/features%2Feditable-models-openxr/Oculus%20Quest%20Experimental.zip)
* [Oculus PC VR](https://nightly.link/IxxyXR/open-brush/workflows/build/features%2Feditable-models-openxr/Windows%20Rift%20Experimental.zip) (Rift, Quest via Link cable...)
* [SteamVR](https://nightly.link/IxxyXR/open-brush/workflows/build/features%2Feditable-models-openxr/Windows%20OpenXR%20Experimental.zip) (Vive, Index, Reverb...)
* [Other Builds](https://nightly.link/IxxyXR/open-brush/workflows/build/features%2Feditable-models-openxr) (Non-VR, Linux, Mac...)

### What does it do?

The core feature is support for low-poly 3d models that can be modified directly inside Open Brush. Currently the focus is on procedural shapes based on symmetry and repeating patterns.

### What's it good for?

Creating regular patterns and geometry forms.

### How do I install it?

Download a build for your headset from the link above and unzip it. You can run the Windows exe directly. To install the Quest apk use SideQuest: [https://uploadvr.com/sideloading-quest-how-to/](https://uploadvr.com/sideloading-quest-how-to/)

### How do I use the Polyhedra tool?

1. Switch out of beginner mode and you'll see the "Experimental Tools" panel on your wand.
2. There is a new icon at the bottom that looks like a wireframe cube. Click that to activate the polyhedra tool.
3. A tray will appear on the right of the panel with some new buttons. You can pick from a range of shapes by clicking the top button "Shape Gallery".
4. Draw your chosen shape using the trigger on your drawing hand. Click once to start and release when you're happy with the size.

There are four buttons on the tray that appears when the Polyhedra tool is active:

#### Shape Gallery

This opens a popup with a selection of built-in shapes to get you started.

#### Shape Designer

This opens a new panel that gives you access to the powerful underlying procedural generation engine. See the section below for detailed information on the Shape Designer

#### Select the "Create" action

Clicking this button cycles through the options for what kind of object you create when you click and drag the trigger on your drawing hand:

* **Create an editable shape:**&#x20;
* **Create brush strokes based on the shape faces:**&#x20;
* **Create brush strokes based on the shape edges:**&#x20;
* **Create a new custom guide:**&#x20;
* **Create a custom mirror:**&#x20;

#### Select the "Modify" action

Clicking this button cycles through the options for what the secondary button on your drawing hand does (the "A" button on the Oculus controller or trackpad click on the Vive controller). In all cases you press the secondary button whilst moving your controller over existing editable models in your scene:

1. **Apply settings**: picks up the Shape Designer settings from the model and loads those settings into the Shape Designer panel.
2. **Grab settings**: Applies the current Shape Designer Settings to the model.
3. **Apply color**: Changes all faces on the model to the current selected brush color.
4. **Draw brush strokes on faces**: Create brush strokes on the model. One brush stroke for every face.
5. **Draw brush strokes on edges**: Create brush strokes on the model. One brush stroke for every edge.

### Known Issues&#x20;

1. There's nothing to stop you creating extremely complex shapes that can slow everything down and even cause Open Brush to crash.&#x20;
2. Exported scenes work best in the gltf/glb format. Face colours will appear correctly. Currently the various materials don't export. Other formats don't support exporting face colours. (FBX actually does but you'll need to edit the material in your 3d app and set it to use "Vertex colours")
3. Duplicating models using the selection tool sometimes produces changes in scale.
4. You can't scale the custom mirror. Instead scale your scene.
5. Custom mirror stroke colours are sometimes unpredictable.

### The Custom Guide

(docs coming soon)

### The Custom Mirror

1. The symmetry mode only affects normal paint strokes. You can't currently use symmetry to create multiple copies of the polyhedra tool.
2. You can grab the symmetry widget and change it's position and orientation.

### Using the Shape Designer

(docs coming soon)

###

## How do I get help

Come over to the Open Brush Discord: [https://discord.com/invite/fS69VdFXpk](https://discord.com/invite/fS69VdFXpk) and chat to me ( andybak#5425 ).

I'm on UK time (currently UTC+1) but I check in fairly regularly.

### Can I see it in action?

(docs coming soon)
