# Exporting Open Brush sketches to other apps

Open Brush sketches can be exported by clicking the ‘Export’ button found on the Labs panel. The Labs panel can be found under ‘More…’ on the Tools panel.

Each sketch exported from Open Brush creates a separate folder in **Documents/Open Brush/Exports** which contains the geometry in the following formats:

* .glb (Standalone and PC)
* .fbx (PC only)
* .usd (PC only)
* .json (PC only)
* .latk (Standalone and PC)
* .wrl (PC only)

(.glb is closely related to .gltf and most software will support both. We output binary glTF version 2)

.latk is an interchange format for 3d brush strokes: [https://lightningartist.org/](https://lightningartist.org/)

The .json is a “raw” format which you can use if you need a different file format. See the [Open Brush Toolkit](https://github.com/icosa-gallery/open-brush-toolkit) for sample [Python 2.7](https://www.python.org/download/releases/2.7/) scripts that convert the raw .json to .obj.

python convert\_to\_fbx.py "c:\Users\\_username_\Documents\Open Brush\Exports\Untitled\_1.json"

Each script has a set of command-line options that fine-tune the generated file.

The USD contains both geometry and curve information. If your DCC tool doesn’t support USD, the [Open Brush Toolkit](https://github.com/icosa-gallery/open-brush-toolkit) contains a Python 2.7 script that can convert the .tilt file to a Collada .dae containing the curves.

## Maya <a href="#maya" id="maya"></a>

After importing the FBX file into Maya you will need to turn off the _Alpha is Luminance_ attribute in the _Color Balance_ section for each texture node. To see the brush colors in the viewport turn on the _Display Colors_ attribute and set _Material Blend_ to Multiply in the _Mesh Component Display_ section on each mesh shape node.

To render with the vertex colors you can use the mentalrayVertexColors shader node to access the stroke color in your material.

## Mozilla Hubs

Mozilla Spoke (the Hubs editor) gives an error when you try to import our .glb file directly. However importing first into Blender and then re-exporting will fix this. Not all brushes work correctly but the simpler brushes should import fairly well.

## Sketchfab <a href="#sketchfab" id="sketchfab"></a>

To post to Sketchfab you will need to upload the FBX file and the textures.

We are working with Sketchfab to have Open Brush import correctly, but if the strokes look wrong you can try opening the 3D Settings Editor in Sketchfab and under the Materials tab set the material properties manually.

## Unity <a href="#unity" id="unity"></a>

We recommend using the [Open Brush Toolkit](open-brush-unity-sdk.md) and the .glb format. Open Brush Toolkit also understands the .fbx format. More info

## Unity WebGL

You'll need to delete the following 2 scripts if you want to build for Unity WebGL targets: `GenericAudioInputEditor.cs` and `GenericAudioInput.cs`&#x20;

## Flipside XR

1. Follow the instructions for installing and configuring [Flipside Creator Tools](https://www.flipsidexr.com/docs/2023.1/creator-tools/getting-started)
2. Download the .unitypackage for the latest release of the [Open Brush Unity SDK](open-brush-unity-sdk.md#\_iqjwk94xwdgd)
3. You'll also need the [Json.Net.for.open.brush.toolkit.unitypackage](https://github.com/icosa-gallery/open-brush-toolkit/releases/download/v24.0.0/Json.Net.for.open.brush.toolkit.unitypackage)  from the same page
4. Add both to your Flipside Unity project
5. Export your Open Brush sketch and import the .glb file into the Flipside project
6. Follow the Flipside instructions for uploading a Unity scene as a Flipside Set

## Styly

To upload your work to Styly, you'll need to remove all traces of the audio-reactivity scripts in the Open Brush toolkit.

1. Follow the instructions for setting up Styly in Unity here: [https://styly.cc/manual/unity-asset-uploader/](https://styly.cc/manual/unity-asset-uploader/) but stop when you get to the section about half-way through headed "Upload from Unity to STYLY"
2. Download the Open Brush Unity SDK unitypackage as described here: [https://docs.openbrush.app/user-guide/open-brush-unity-sdk](https://docs.openbrush.app/user-guide/open-brush-unity-sdk)
3. Delete the following folders from your Unity project window:
   1. ThirdParty/CSCore
   2. ThirdParty/Reaktion
4. Delete the following files from you Unity project window:
   1. TiltBrush/Scripts:/VisualizerAudioInput
   2. TiltBrush/Scripts:/VisualizerManager
   3. TiltBrush/Scripts/Editor/VisualizerManagerEditor
5. Also in the project window, drag the entire TiltBrush/Scripts/Gltf folder so it's inside TiltBrush/Scripts/Editor
6. Carry on where you left off with the Styly docs.

## Command-line Exporting <a href="#command-line-exporting" id="command-line-exporting"></a>

To export sketches from the command line, use the --export option to specify a file or set of files to export. --export supports wildcards, and multiple files can be specified with a single --export flag. Filenames without a path are assumed to be found in the Open Brush Sketches directory.

You can override the destination folder of exports using the --exportPath flag.

We suggest you also specify the -batchmode option if you don’t want the Open Brush window to appear.

```
OpenBrush.exe --export Untitled_15.tilt Untitled_2*.tilt C:\Downloads\downloaded.tilt --exportPath C:\Temp -batchmode
```
