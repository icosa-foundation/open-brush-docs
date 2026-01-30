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

## JSON Exports Include Sketch Metadata

When you export to JSON format, Open Brush now includes additional metadata about your sketch:

- Sketch creation date and modification time
- Author information (if configured)
- Sketch title and description
- Stroke count and complexity metrics
- Brush types used
- Camera information

This metadata is useful for:
- Cataloging and organizing exported sketches
- Analyzing sketch complexity and composition
- Building tools that process Open Brush exports
- Archiving and documentation purposes

The JSON export provides a complete data representation of your sketch that can be parsed by external tools and scripts.

* **KeepStrokes**: Each stroke will be exported as a separate mesh rather than grouped by brush type (export will take longer and may fail on complex scenes)
* **KeepGroups**: Maintains groups on export (export will take longer and may fail on complex scenes)
* **Formats**: Each item in here corresponds to an existing export format except for "newglb". This is also a glb file but we use the new export code to generate it.

Note that formats not supported on your platform will be ignored. See below for platform support.

### Supported GLTF Extensions with New GLB exports

**Extensions supported**

* KHR\_materials\_clearcoat
* KHR\_materials\_emissive\_strength
* KHR\_materials\_ior
* KHR\_materials\_iridescence
* KHR\_materials\_specular
* KHR\_materials\_transmission (soon)
* KHR\_materials\_volume (soon)
* MSFT\_lod
* KHR\_draco\_mesh\_compression
* KHR\_lights\_punctual
* KHR\_materials\_unlit
* KHR\_mesh\_quantization
* KHR\_texture\_basisu
* KHR\_texture\_transform

(The above list may change as we implement missing features in UnityGLTF.&#x20;

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

This build supports a new feature - The existing "group/ungroup" button on the pop-out tray that appears when you activate the [Selection Tool](../using-the-open-brush-tools-quick-tools-and-menu-panels/tools-panel/selection-options.md) now works on imported models - if they consist of multiple parts. Just select a single imported model and if it does have sub-parts the button will show "ungroup" as an option - the same as if you select a normal grouped set of objects.

### Importing Lights

If your imported model contains lights then these will appear in the scene and will act upon other objects the same as the [Environment Lights](../using-the-open-brush-tools-quick-tools-and-menu-panels/extras-panel/lights-panel.md). Furthermore imported lights support point lights and spot lights - whereas the existing environment lights only support directional lights.

These additional lights will only affect imported 3d models - they will not affect brush strokes which ignore lights other than the ones configured in your [environment settings](../using-the-open-brush-tools-quick-tools-and-menu-panels/extras-panel/lights-panel.md)

{% embed url="https://www.youtube.com/watch?v=98drHT5DD7Y" %}
