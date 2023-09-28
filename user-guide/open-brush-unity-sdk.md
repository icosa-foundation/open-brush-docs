---
description: Using Open Brush with Unity
---

# Open Brush Unity SDK

## About <a href="#_j7bdhxvyulyl" id="_j7bdhxvyulyl"></a>

The Open Brush Unity SDK allows you to import your Open Brush sketches into Unity. The SDK includes:

* **All** of Open Brush’s brush materials
* An importer script that automatically assigns Open Brush materials to imported .glb files
* Open Brush’s audio reactivity functionality that make brushes react to music

## Requirements <a href="#_q9lph11ngm09" id="_q9lph11ngm09"></a>

The SDK has these requirements:

* Your project must use Unity 2019.4 or higher
* Macs running on Apple Silicon (i.e. M1 or M2) need to [remove Audio Reactivity](open-brush-unity-sdk.md#\_nvutjzw2fj1u) to fix errors related to "CSCore".

## Getting the code <a href="#_iqjwk94xwdgd" id="_iqjwk94xwdgd"></a>

Download the latest version of the toolkit from:[\
](https://github.com/icosa-foundation/open-brush-toolkit)[https://github.com/icosa-foundation/open-brush-toolkit/releases](https://github.com/icosa-foundation/open-brush-toolkit/releases)

The SDK comes in the form of a Unity Package. To import:

1. Open Unity
2. Create a project or open an existing one
3. Double click the downloaded .unitypackage file, or go to Assets > Import Package > Custom Package.
4. Import the package

## Importing a sketch <a href="#_6wwms1xya8em" id="_6wwms1xya8em"></a>

To use a Tilt Brush sketch inside of Unity, you need to **export it** and copy the exported .gltf file into your project. You do \_not \_need any of the .png files that come with the export. The SDK will use its own, Tilt Brush materials instead.

The SDK will process .glb files on import and assign the correct materials.

To export a sketch:

1. Open Tilt Brush, load your sketch
2. Click the **\[...]** icon in the settings area of your hand menu
3. Click the \*\*Labs \*\*icon
4. Hit **Export** in the floating window that pops up

To import a sketch into your scene:

1. Find the exported files:
   1. On a PC or Mac look in **Documents/Open Brush/Exports**
   2. If you created the sketch on a standalone Quest thenconnect it to your PC/Mac by following [these instructions](https://www.meta.com/en-gb/help/quest/articles/headsets-and-accessories/using-your-headset/transfer-files-from-computer-to-headset/) and then browse to the Quest in Explorer/Finder and look in **Internal Shared Storage/Open Brush/Exports**
2. Copy the .glb file into your Unity project
3. Drag the file from the Project window into the Hierarchy

_Notes:_

* _The Open Brush Unity SDK doesn’t load .tilt files._
* _You don’t need to copy the textures included with the .glb into your project_

## Tips <a href="#_ibglt4zbyabz" id="_ibglt4zbyabz"></a>

### Fixing CSCore errors (or other errorsrelated to Audio Reactivity) <a href="#_nvutjzw2fj1u" id="_nvutjzw2fj1u"></a>

At the moment the plugin used for Audio Reactivity doesn't work on some platforms. If you see errors related to "CSCore" or anything that looks audio related deleting the following files from your project:

1. The folder ThirdParty\CSCore
2. TiltBrush\Scripts\VisualizerManager
3. TiltBrush\Scripts\VisualizerAudioInput
4. TiltBrush\Scripts\Editor\VisualizerManagerEditor

### "My brushes look different to Open Brush" (Linear vs Gamma) <a href="#_nvutjzw2fj1u" id="_nvutjzw2fj1u"></a>

For historical reasons Open Brush uses gamma mode for color blending. We may offer the option to switch to linear in the future but it will change the appearance of sketches so gamma will always be an option when the hardware allows it.

If your Unity project is set to linear mode (Projects > Player Settings) then imported sketches may look different. For example here's some smoke brush strokes in Open Brush:

<figure><img src="../.gitbook/assets/image (2) (1) (1).png" alt=""><figcaption></figcaption></figure>

And here's the same sketch in Unity set to linear mode:

<figure><img src="../.gitbook/assets/image (2) (1).png" alt=""><figcaption></figcaption></figure>

The v11 toolkit shaders support both sRGB (Gamma) and Linear [color spaces](https://docs.unity3d.com/Manual/LinearRendering-LinearOrGammaWorkflow.html). The shaders are set to Gamma mode by default. **If you wish to use Linear, add this call somewhere in your program**.

```
Shader.EnableKeyword("TBT_LINEAR_TARGET");
```

Note: while this improves the colour accuracy, due to [fundamental differences](https://docs.unity3d.com/Manual/LinearRendering-LinearOrGammaWorkflow.html) between linear and gamma rendering, brushes may still not exactly replicate the look of their gamma counterparts.

### Audio Reactivity <a href="#_st8oph1ghsgx" id="_st8oph1ghsgx"></a>

You can make the brushes wiggle to the audio in your scene:

1. Drag the\*\* \[Tilt Brush Audio Reactivity] prefab\*\* into your scene
2. Add an audio source to your scene, if there’s none

If the brushes aren’t moving, you can select the prefab in Play mode to visualize the audio data the shaders are receiving:

![](../.gitbook/assets/0.gif)

### Bloom <a href="#_7ljsa6ylg4rb" id="_7ljsa6ylg4rb"></a>

![](<../.gitbook/assets/1 (3).png>)\
You can achieve\_ an Open Brush look\_ by adding **Bloom**, using Unity’s built-in shaders:

1. Import the Standard Assets “Effects” package (Assets menu / Import Package / Effects)
2. \*\*Important: \*\*Enable your camera’s HDR checkbox\
   ![](<../.gitbook/assets/2 (3).png>)
3. Add the Bloom post-processing effect, these are recommended settings:\
   ![](<../.gitbook/assets/3 (3).png>)

Internally, Open Brush uses a modified version of Sonic Ether bloom, which has been released as [open source](https://github.com/sonicether/SE-Natural-Bloom-Dirty-Lens).
