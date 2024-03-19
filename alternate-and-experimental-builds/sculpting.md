# Feature: Improved Import/Export

Status: <mark style="color:red;">In Progress</mark>

## Download

* [Oculus Quest 1](https://nightly.link/icosa-foundation/open-brush/workflows/build/feature%2Fsculpting/Oculus%20Quest%20\(2%2B\).zip)
* [Oculus Quest 2 or 3](https://nightly.link/icosa-foundation/open-brush/workflows/build/feature%2Fsculpting/Oculus%20Quest%20\(2%2B\).zip)
* [Oculus PC VR](https://nightly.link/icosa-foundation/open-brush/workflows/build/feature%2Fsculpting/Windows%20Rift.zip)(Rift, Quest via Link cable...)
* [SteamVR and other PC VR](https://nightly.link/icosa-foundation/open-brush/workflows/build/feature%2Fsculpting/Windows%20OpenXR.zip)(Vive, Index, Reverb...)
* [Other Builds](https://nightly.link/icosa-foundation/open-brush/workflows/build/feature%2Fsculpting) (Pico, Pimax etc)
* [Code](https://github.com/icosa-foundation/open-brush/tree/feature/sculpting)

### What does it do?

Adds new optional GLTF import and export workflows. Allow import of lights, breaking apart of imported models and other new features that the updated libraries enable

### How do I install it?

Download a build for your headset from the link above and unzip it. You can run the Windows exe directly. To install the Quest apk use SideQuest: [https://uploadvr.com/sideloading-quest-how-to/](https://uploadvr.com/sideloading-quest-how-to/)

### How do I use it?

To switch to the new importer (which replaces GLTFast that we added in v2.4 with UnityGLTF you need to edit your [Open Brush config file](../user-guide/the-open-brush-config-file.md) and add this entry after "Flags":

```json
 "Import": {
    "UseUnityGltf": true
  }
```

We've changed how export in general is configured. Previously all supported formats were exported whether you needed them or not. Some were pretty slow for large scenes (STL - looking at you) and you probably only needed a couple of them. Now you can choose which are available using the config file:

```json
  "Export": {
    "ExportBinaryFbx": true,
    "ExportFbxVersion": "FBX201400",
    "ExportStrokeMetadata": true,
    "KeepStrokes": true,
    "KeepGroups": false,
    "Formats": {
      "fbx": true,
      "glb": true,
      "newglb": true,
      "json": true,
      "latk": true,
      "obj": true,
      "stl": false,
      "usd": true,
      "wrl": false
    }
```

ExportBinaryFbx and ExportFbxVersion are existing options - but the rest of the entries here are new.

* ExportStrokeMetadata: _todo_
* KeepStrokes: _todo_
* KeepGroups: _todo_
* Formats: Each item in here corresponds to an existing export format except for "newglb" which is a glb file but we use the new export code to generate it. Note that formats not supported on your platform will be ignored. See below for platform support.

### Import Differences between GLTFast (existing) and UnityGLTF (new)

**Extensions supported by GLTFast but not UnityGLTF:**

* KHR\_materials\_variants
* KHR\_xmp\_json\_ld&#x20;
* EXT\_lights\_image\_based&#x20;
* EXT\_mesh\_gpu\_instancing&#x20;
* KHR\_materials\_pbrSpecularGlossiness
* KHR\_materials\_sheen

**Extensions supported by UnityGLTF but not GLTFast:**

* KHR\_materials\_iridescence&#x20;
* MSFT\_lod&#x20;
* KHR\_materials\_emissive\_strength

(The above list may change as we implement missing features in UnityGLTF)

UnityGLTF has some other differences:

* Model hierarchy should be faithfully preserved. GLTFast on the other hand doesn't support sub-meshes so any mesh that contains multiple materials will be split into separate objects. (this might be desirable in some cases)
* In general 3d models should be more robustly handled if you round-trip between Open Brush and other 3D apps

Please report any other differences you find. The reason we are keeping both importers around is to gather feedback on their strengths and weaknesses.

### Differences with the new UnityGLTF export

The use of the new exporter is currently optional and we will continue to support the old exporter until the new one is a full replacement.

* Currently - if you use the Open Brush Toolkit Unity SDK then use the existing exported GLB file
* Use the existing exporter for uploads to [Icosa.](https://icosa.gallery/)
* Similarly - if you use the Icosa three.js loader this works best with the existing exporter
* The new GLB export should work better in Blender and other 3D animation apps although we still have work to do to fix support for particle brushes, transparent brushes and other features.
* Imported 3D models will export much better with the new GLB exporter
* In general new features in the [beta](open-brush-beta-docs.md) or from other [experimental branches](./) will work better using the new exporter.&#x20;

### Platform Support

<table><thead><tr><th width="151">Format</th><th align="center">Android/iOS (Standalone VR)</th><th align="center">PC (Tethered VR)</th></tr></thead><tbody><tr><td>FBX</td><td align="center"><mark style="color:red;">✘</mark></td><td align="center"><mark style="color:green;">✔</mark></td></tr><tr><td>GLB</td><td align="center"><mark style="color:green;">✔</mark></td><td align="center"><mark style="color:green;">✔</mark></td></tr><tr><td>NEWGLB</td><td align="center"><mark style="color:green;">✔</mark></td><td align="center"><mark style="color:green;">✔</mark></td></tr><tr><td>JSON</td><td align="center"><mark style="color:green;">✔</mark></td><td align="center"><mark style="color:green;">✔</mark></td></tr><tr><td>LATK</td><td align="center"><mark style="color:green;">✔</mark></td><td align="center"><mark style="color:green;">✔</mark></td></tr><tr><td>OBJ</td><td align="center"><mark style="color:red;">✘</mark></td><td align="center"><mark style="color:green;">✔</mark></td></tr><tr><td>STL</td><td align="center"><mark style="color:green;">✔</mark></td><td align="center"><mark style="color:green;">✔</mark></td></tr><tr><td>USD</td><td align="center"><mark style="color:red;">✘</mark></td><td align="center"><mark style="color:green;">✔</mark></td></tr><tr><td>WRL</td><td align="center"><mark style="color:green;">✔</mark></td><td align="center"><mark style="color:green;">✔</mark></td></tr><tr><td></td><td align="center"></td><td align="center"></td></tr></tbody></table>

### Known Issues

{% hint style="info" %}
WARNING - Saved files are currently incompatible with official builds of Open Brush. Don't save over any sketches you want to open in other builds.
{% endhint %}

## How do I get help

Come over to the Open Brush Discord: [https://discord.com/invite/fS69VdFXpk](https://discord.com/invite/fS69VdFXpk) and chat to me @andybak).

I'm on UK time but I check in fairly regularly.

### Can I see it in action?

TODO
