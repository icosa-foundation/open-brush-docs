# 3D Shapes Tool

(These docs are a work in progress)

#### Status: Ready for beta testing

## Downloads

(These links aren't all currently working. I'm working on getting this fixed ASAP)

* [Oculus Quest](https://nightly.link/IxxyXR/open-brush/workflows/build/features%2Feditable-models-openxr/Oculus%20Quest%20Experimental.zip)~~~~\
  ~~~~(This build is sometimes slightly behind the PC versions because of some issues we're having with Github's build service)
* [Oculus PC VR](https://nightly.link/IxxyXR/open-brush/workflows/build/features%2Feditable-models-openxr/Windows%20Rift%20Experimental.zip) (Rift, Quest via Link cable...)
* [SteamVR](https://nightly.link/IxxyXR/open-brush/workflows/build/features%2Feditable-models-openxr/Windows%20OpenXR%20Experimental.zip) (Vive, Index, Reverb...)
* [Other Builds](https://nightly.link/IxxyXR/open-brush/workflows/build/features%2Feditable-models-openxr) (Non-VR, Linux, Mac...)

### What does it do?

The core feature is support for low-poly 3d models that can be modified directly inside Open Brush. Currently the focus is on procedural shapes based on symmetry and repeating patterns.

### What's it good for?

Creating symmetrical patterns, geometric forms and complex 3d shapes.

### How do I install it?

Download a build for your headset from the link above and unzip it. You can run the Windows exe directly. To install the Quest apk use SideQuest: [https://uploadvr.com/sideloading-quest-how-to/](https://uploadvr.com/sideloading-quest-how-to/)

### How do I use the 3D Shapes tool?

![](<../../.gitbook/assets/image (15).png>)

1. (Make sure you've switch off beginner mode) Find the "Experimental Tools" panel which is usually attached to your wand.
2. There will be a new icon at the bottom that looks like a wireframe cube. Click that to activate the 3D shape tool.
3. A tray will appear on the right of the panel with some new buttons. You can pick from a range of shapes by clicking the top button "Shape Gallery".
4. Draw your chosen shape using the trigger on your drawing hand. Click once to start and release when you're happy with the size.

<mark style="color:red;">**WARNING!**</mark> There are currently no limits in place preventing you creating very complex shapes. It's quite easy to make everything super slow and potentially even cause Open Brush to crash.

### The main "3D Shape Tool" buttons

There are four buttons on the tray that appears when the Polyhedra tool is active:

#### 1. Shape Gallery

This opens a popup with a selection of built-in shapes to get you started.

#### 2. "Create" action

Clicking this button cycles through the options for what kind of object you create when you click and drag the trigger on your drawing hand:

* **Create a 3D Shape:** This will create a 3D shape in the scene based on your current choice of shape. A 3D shape is similar to an imported 3D model except it is generated on the fly based on settings that you choose.
* **Create brush strokes based on shape faces:** Instead of creating a 3D shape this uses your current chosen shape as a template to draw brush strokes around the edges of each face.
* **Create brush strokes based on shape edges:** This is similar to the above except it creates shorter brush strokes (but more of them). One for each edge in the shape. Experiment with these two different modes. Some will work better for one combination of brush and shape than the other.
* **Create a new custom guide:** This creates a new guide based on your current chosen shape. It has the limitation that only convex shapes are allowed so if you have a concave shape the the "convex hull" of it will be used to make the guide.
* **Create a custom mirror:** This creates a custom mirror that works in a similar way to the normal mirror tool. However instead of two copies of your brush strokes, the custom mirror can create multiple strokes - one for every face of your chosen shape.

#### 3. "Modify" action

Clicking this button cycles through the options for what the secondary button on your drawing hand does (the "A" button on the Oculus controller or trackpad click on the Vive controller). In all cases you press the secondary button whilst moving your controller over existing editable models in your scene:

1. **Apply settings**: picks up the Shape Designer settings from the model and loads those settings into the Shape Designer panel.
2. **Grab settings**: Applies the current Shape Designer Settings to the model.
3. **Apply color**: Changes all faces on the model to the current selected brush color.
4. **Draw brush strokes on faces**: Create brush strokes on the model. One brush stroke for every face.
5. **Draw brush strokes on edges**: Create brush strokes on the model. One brush stroke for every edge.

#### 4. Shape Designer

This opens a new panel that gives you access to the powerful underlying procedural generation engine. See the section below for detailed information on the Shape Designer

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

![The "Generate" panel showing the main shape categories](<../../.gitbook/assets/image (13).png>)

![The "Modify" panel showing 3 modifiers applied to the shape.](<../../.gitbook/assets/image (14).png>)

![The "Appearance" panel showing color and material options.](<../../.gitbook/assets/image (18).png>)

![The "Presets" popup where you can save the shapes you've created.](<../../.gitbook/assets/image (16).png>)

(docs coming soon)

###

## How do I get help

Come over to the Open Brush Discord: [https://discord.com/invite/fS69VdFXpk](https://discord.com/invite/fS69VdFXpk) and chat to me ( andybak#5425 ).

I'm on UK time (currently UTC+1) but I check in fairly regularly.

### Can I see it in action?

(docs coming soon)
