# Exporting Open Brush sketches to other apps

Tilt Brush sketches can be exported by clicking the ‘Export’ button found on the Labs panel. The Labs panel can be found under ‘More…’ on the Tools panel.

Each sketch exported from Tilt Brush creates a separate folder in **Documents/Tilt Brush/Exports** which contains the geometry in the following formats:

* .glb \(binary glTF version 2\)
* .fbx \(Desktop only\)
* .usd \(Desktop only\)
* .json \(Desktop only\)

The .json is a “raw” format which you can use if you need a different file format. See the [Tilt Brush Toolkit](https://github.com/googlevr/tilt-brush-toolkit) for sample [Python 2.7](https://www.python.org/download/releases/2.7/) scripts that convert the raw .json to .obj.

python convert\_to\_fbx.py "c:\Users\_username_\Documents\Tilt Brush\Exports\Untitled\_1.json"

Each script has a set of command-line options that fine-tune the generated file.

The USD contains both geometry and curve information. If your DCC tool doesn’t support USD, the [Tilt Brush Toolkit](https://github.com/googlevr/tilt-brush-toolkit) contains a Python 2.7 script that can convert the .tilt file to a Collada .dae containing the curves.

#### Maya <a id="maya"></a>

After importing the FBX file into Maya you will need to turn off the _Alpha is Luminance_ attribute in the _Color Balance_ section for each texture node. To see the brush colors in the viewport turn on the _Display Colors_ attribute and set _Material Blend_ to Multiply in the _Mesh Component Display_ section on each mesh shape node.

To render with the vertex colors you can use the mentalrayVertexColors shader node to access the stroke color in your material.

#### Sketchfab <a id="sketchfab"></a>

To post to Sketchfab you will need to upload the FBX file and the textures.

We are working with Sketchfab to have Tilt Brush import correctly, but if the strokes look wrong you can try opening the 3D Settings Editor in Sketchfab and under the Materials tab set the material properties manually.

#### Unity <a id="unity"></a>

We recommend using the Tilt Brush Toolkit and the .glb format. Tilt Brush Toolkit also understands the .fbx format.

#### Command-line Exporting <a id="command-line-exporting"></a>

To export sketches from the command line, use the --export option to specify a file or set of files to export. --export supports wildcards, and multiple files can be specified with a single --export flag. Filenames without a path are assumed to be found in the Tilt Brush Sketches directory.

You can override the destination folder of exports using the --exportPath flag.

We suggest you also specify the -batchmode option if you don’t want the Tilt Brush window to appear.

```text
TiltBrush.exe --export Untitled_15.tilt Untitled_2*.tilt C:\Downloads\downloaded.tilt --exportPath C:\Temp -batchmode
```

