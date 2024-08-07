# Configuring Export

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

* **ExportBinaryFbx**: This setting specifies the version of the FBX file format to be used when exporting 3D models. Users can choose from FBX201600, FBX201400, FBX201300, FBX2012, or FBX201100. If not specified in the config file, the default version is FBX201400. If users experience issues importing the FBX file into older software, they may need to select an older version.
* **ExportFbxVersion**: Controls whether exported FBX files will be in binary format. When set to true, binary FBX files will be exported; when set to false, ASCII FBX files will be exported.
* **ExportStrokeTimestamp:** (true | false) This will put timing information into texcoord2 for all GLB exports. Timestamps are a vec3: x,y = the earliest/latest timestamp in the stroke which contains that vertex. z = the timestamp for that vertex. This setting defaults to true but can be disabled to reduce file size.
* **ExportStrokeMetadata**: includes extra information with each stroke that might be useful to developers writing their own importers
* **KeepStrokes**: Each stroke will be exported as a separate mesh rather than grouped by brush type  (export will take longer and may fail on complex scenes)
* **KeepGroups**: Maintains groups on export (export will take longer and may fail on complex scenes)
* **Formats**: Each item in here corresponds to an existing export format except for "newglb". This is also a glb file but we use the new export code to generate it.

Note that formats not supported on your platform will be ignored. See below for platform support.

### Import Differences between GLTFast (old) and UnityGLTF (new) formats

**Extensions supported by GLTFast but not UnityGLTF:**

* EXT\_mesh\_gpu\_instancing
* KHR\_materials\_pbrSpecularGlossiness (legacy extension - superseded by KHR\_materials\_specular which is only supported by UnityGLTF)

**Extensions supported by UnityGLTF but not GLTFast:**

* KHR\_materials\_clearcoat&#x20;
* KHR\_materials\_emissive\_strength
* KHR\_materials\_ior&#x20;
* KHR\_materials\_iridescence
* KHR\_materials\_specular
* KHR\_materials\_transmission (soon)
* KHR\_materials\_volume (soon)
* MSFT\_lod

**Extensions supported by both:**

* KHR\_draco\_mesh\_compression&#x20;
* KHR\_lights\_punctual&#x20;
* KHR\_materials\_unlit&#x20;
* KHR\_mesh\_quantization&#x20;
* KHR\_texture\_basisu&#x20;
* KHR\_texture\_transform

(The above list may change as we implement missing features in UnityGLTF. GLTFast also has announced plans to support KHR\_materials\_variants, EXT\_lights\_image\_based and KHR\_materials\_transmission)

UnityGLTF has some other differences:

* Model hierarchy should be faithfully preserved. GLTFast on the other hand doesn't support sub-meshes so any mesh that contains multiple materials will be split into separate objects. (this might be desirable in some cases)
* In general 3d models should be more robustly handled if you round-trip between Open Brush and other 3D apps

Please report any other differences you find. The reason we are keeping both importers around is to gather feedback on their strengths and weaknesses.

### Choosing between the new and old GLTF formats

The use of the new exporter is currently optional and we will continue to support the old exporter until the new one is a full replacement.

* If you're using the existing [Open Brush Unity Toolkit/SDK](../open-brush-unity-sdk.md) then use the older GLB format
* If you're manually uploading to [Icosa Gallery](https://icosa.gallery/) then use the older GLB format
* If you're use the [Icosa three.js loader](https://github.com/icosa-foundation/three-icosa) this also works best with the older exporter.
* The new GLB export format should work better in Blender and other 3D animation apps although we still have work to do to fix support for particle brushes, transparent brushes and other features.
* Imported 3D models will export much better with the new GLB exporter
* In general new features in the [beta](../../alternate-and-experimental-builds/open-brush-beta-docs.md) or from other [experimental branches](../../alternate-and-experimental-builds/) will work better using the new exporter.

### Platform Support

<table><thead><tr><th width="151">Format</th><th align="center">Android/iOS (Standalone VR)</th><th align="center">PC (Tethered VR)</th></tr></thead><tbody><tr><td>FBX</td><td align="center"><mark style="color:red;">✘</mark></td><td align="center"><mark style="color:green;">✔</mark></td></tr><tr><td>GLB</td><td align="center"><mark style="color:green;">✔</mark></td><td align="center"><mark style="color:green;">✔</mark></td></tr><tr><td>NEWGLB</td><td align="center"><mark style="color:green;">✔</mark></td><td align="center"><mark style="color:green;">✔</mark></td></tr><tr><td>JSON</td><td align="center"><mark style="color:green;">✔</mark></td><td align="center"><mark style="color:green;">✔</mark></td></tr><tr><td>LATK</td><td align="center"><mark style="color:green;">✔</mark></td><td align="center"><mark style="color:green;">✔</mark></td></tr><tr><td>OBJ</td><td align="center"><mark style="color:red;">✘</mark></td><td align="center"><mark style="color:green;">✔</mark></td></tr><tr><td>STL</td><td align="center"><mark style="color:green;">✔</mark></td><td align="center"><mark style="color:green;">✔</mark></td></tr><tr><td>USD</td><td align="center"><mark style="color:red;">✘</mark></td><td align="center"><mark style="color:green;">✔</mark></td></tr><tr><td>WRL</td><td align="center"><mark style="color:green;">✔</mark></td><td align="center"><mark style="color:green;">✔</mark></td></tr><tr><td></td><td align="center"></td><td align="center"></td></tr></tbody></table>

### Breaking Apart Imported Models

This build supports a new feature - The existing "group/ungroup" button on the pop-out tray that appears when you activate the [Selection Tool](../using-the-open-brush-tools-quick-tools-and-menu-panels/tools-panel/selection-options.md) now works on imported models - if they consist of multiple parts. Just select a single imported model and if it does have sub-parts the button will show "ungroup" as an option - the same as if you select a normal grouped set of objects.&#x20;

### Importing Lights

If your imported model contains lights then these will appear in the scene and will act upon other objects the same as the [Environment Lights](../using-the-open-brush-tools-quick-tools-and-menu-panels/extras-panel/lights-panel.md). Furthermore imported lights support point lights and spot lights - whereas the existing environment lights only support directional lights.

### Known Issues

{% hint style="info" %}
If you break apart a model containing lights, the lights themselves can't be selected or moved.
{% endhint %}

{% embed url="https://www.youtube.com/watch?v=98drHT5DD7Y" %}
