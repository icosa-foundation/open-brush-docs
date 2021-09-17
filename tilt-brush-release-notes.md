---
description: >-
  These were the last release notes that were put out by Google and contain some
  useful information not found elsewhere
---

# Tilt Brush Version 23 Release Notes

## Version 23

* Added Google Drive Backup \(in Beta for now!\).
  * Requires signing-in with a Google account.
  * Enable Google Drive Backup on Accounts popup or Sketchbook.
  * Can optionally configure Google Drive Backup to backup Sketches, Snapshots, Media Library, Exports, and Videos.
  * Backup is disabled if Google Drive has less than 0.5 Gb of storage free.
* Added upload to Sketchfab.
  * Requires a Sketchfab account.
* Added Camera Path.
  * Open Camera Paths Panel from More Panel.
  * Allows defining a spline to record a video. Spline is defined by various points.
    * Anchor Points define spline position. Use tangent controls to modify curves.
    * Direction Points define camera facing at that point on the path. While manipulating, use trigger to preview camera.
    * Speed Points define camera speed at that point on the path. Use cone control to adjust speed value.
    * Zoom Points define camera zoom at that point on the path. Use frustum control to adjust zoom value. While manipulating, use trigger to preview camera.
* Added support for .glb / .gltf files in the Media Library.
* Added Ellipsoid guide.
* Changed max snapshot dimensions from 8192 to 16000. Note that very large snapshots may crash your computer.
* Changed Profile popup to Accounts popup, to support multiple accounts.
* Modified Upload popup to support multiple accounts.
* Info cards \(like, “Sketch loaded!”\) don’t fall away immediately, allowing you a little more time to read them. Tap them to dismiss.
* Removed h265 support.

## Accessing Autosave Files

Tilt Brush regularly saves your work into your Documents/Tilt Brush/Sketches/Autosave folder. Each sketch you make has a separate autosave file, and Tilt Brush keeps autosaves from your last five sketches. If you need to access an autosave, move it into your Documents/Tilt Brush/Sketches folder using Windows Explorer—it will have a Tilt Brush logo as its thumbnail in the Sketchbook.

## Tilt Brush Config File

### Using the Tilt Brush.cfg File

The Tilt Brush config file can be used to tweak various options for advanced users. A blank Tilt Brush.cfg file will be created in the Tilt Brush folder on application startup if one does not exist.

Example path: **C:\Users\**_&lt;username&gt;_**\Documents\Tilt Brush\Tilt Brush.cfg**.

Contents of the default _Tilt Brush.cfg:_

```text
{
   "User":{
      
   },
   "Video":{
      
   },
   "Flags":{
      
   },
   "Export":{
      
   }
}
```

Sample contents of a _Tilt Brush.cfg_ with various fields filled in:

```text
{
   "User":{
      "Author":"Tiltasaurus"
   },
   "Twitch":{
      "Username":"TiltBrushStreamer",
      "OAuth":"oauth:abcdefghijklmnopqrstuvwxyz0123",
      "Channel":"#tiltbrushchannel"
   },
   "YouTube":{
      "ChannelID":"abcdefghijklmnopqrstuvwx"
   },
   "Video":{
      "Resolution":1280,
      "OfflineResolution":1920,
      "FPS":30,
      "OfflineFPS":60,
      "ContainerType":"mp4",
      "CameraSmoothing":0.98,
      "Encoder":"h.264",
      "SaveCameraPath":true,
      "FOV":80
   },
   "Flags":{
      "PostEffectsOnCapture":true,
      "ShowWatermark":true,
      "ShowHeadset":true,
      "ShowControllers":true,
      "SnapshotWidth":1920,
      "SnapshotHeight":1080,
      "FOV":80,
      "DisableAudio":false,
      "UnlockScale":false
   },
   "Export":{
      "ExportBinaryFbx":true,
      "ExportFbxVersion":"FBX201400"
   }
}
```

### Config file valid values

* [How to get an OAuth key for Twitch.](https://twitchapps.com/tokengen/)
* [How to find your YouTube Channel ID.](https://support.google.com/youtube/answer/3250431)
* PostEffectsOnCapture: true \| false
* ShowWatermark: true \| false
* ShowHeadset: true \| false
* UnlockScale: true \| false
* SnapshotWidth: 1 - some reasonably large number
* SnapshotHeight: 1 - some reasonably large number
* FOV: 1 - 179
* DisableAudio: true \| false
* ExportBinaryFbx: true \| false
* ExportFbxVersion: FBX201600 \| FBX201400 \| FBX201300 \| FBX2012 \| FBX201100 Unless set in the config file it will default to the 2014 version. If you have older software that has problems importing the FBX file try an older version.
* Encoder: h.264

### Setting config values from the command line

Any of the above settings in the Tilt Brush.cfg file can also be specified on the command line. The format is --Section.Setting &lt;value&gt;. For example:

```text
--Flags.ShowWatermark true

--Video.CameraSmoothing 0.99

--User.Author "Captain Tilt Brush"
```

### Exporting Tilt Brush Sketches

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

#### Maya

After importing the FBX file into Maya you will need to turn off the _Alpha is Luminance_ attribute in the _Color Balance_ section for each texture node. To see the brush colors in the viewport turn on the _Display Colors_ attribute and set _Material Blend_ to Multiply in the _Mesh Component Display_ section on each mesh shape node.

To render with the vertex colors you can use the mentalrayVertexColors shader node to access the stroke color in your material.

#### Sketchfab

To post to Sketchfab you will need to upload the FBX file and the textures.

We are working with Sketchfab to have Tilt Brush import correctly, but if the strokes look wrong you can try opening the 3D Settings Editor in Sketchfab and under the Materials tab set the material properties manually.

#### Unity

We recommend using the Tilt Brush Toolkit and the .glb format. Tilt Brush Toolkit also understands the .fbx format.

#### Command-line Exporting

To export sketches from the command line, use the --export option to specify a file or set of files to export. --export supports wildcards, and multiple files can be specified with a single --export flag. Filenames without a path are assumed to be found in the Tilt Brush Sketches directory.

You can override the destination folder of exports using the --exportPath flag.

We suggest you also specify the -batchmode option if you don’t want the Tilt Brush window to appear.

```text
TiltBrush.exe --export Untitled_15.tilt Untitled_2*.tilt C:\Downloads\downloaded.tilt --exportPath C:\Temp -batchmode
```

## Exporting Video

### Rendering ‘Offline’ videos

When you create a video from inside Tilt Brush using the Camera tool, Tilt Brush will create a Windows batch file alongside the video \(In Documents\Tilt Brush\Videos\) that you can run to re-render the video at a higher resolution. For example:

 _Untitled\_13\_00.mp4_

 _Untitled\_13\_00.HQ\_Render.bat_

Double-clicking the ".bat" batch file will give you several options for re-rendering your video:

![](.gitbook/assets/1%20%281%29.png)

Press the number corresponding to the format you prefer. It will then launch Tilt Brush, which will reload your sketch and render the video. Once it is done, Tilt Brush will exit. As rendering at higher quality tends to affect the framerate, it is suggested that you do not wear your headset until this process completes.

“No Quick Load” option \(\#6\) will forego quick loading of the sketch and will force it to load at normal speed. It is recommended that the time spent recording should exceed the normal loading time of the sketch or else the video may end before the sketch completes loading.

### Video Camera Paths

Rendering offline videos is achieved by saving off the path the camera took when the video was taken, and then re-using that to recreate the video. The camera path is saved off in ASCII USD \([Universal Scene Description](https://graphics.pixar.com/usd/docs/index.html)\) format, so if you have an application that can read and write USD, you may be able to use it to edit camera paths. Camera paths can also be combined with USD exports from Tilt Brush, to exactly recreate how the camera moved through the scene.

If you want to render a camera path from the command line directly, rather than using the batch file detailed above, you can use the following:

```text
Tiltbrush.exe --renderCameraPath <path/to/camerpath.usda> <path/to/sketchfile.tilt>
```

### Changing Eye Scale on ODS 360 videos

When you render an ODS video, you may find things like the floor is missing, or parts of your objects get clipped off.

The reason this happens is that it’s often easier to scale down your sketch to make it easy to move the camera when you take your original video, but when you render out an ODS file, the objects are too close to the camera.

To fix this, you can change a value in the .usda file. Open it up in your favorite text editor and look at around line 30 for:

```text
uniform float eyeScale = 1
```

If you reduce this value, the render will feel bigger, and the camera is less likely to clip with parts of your sketch. A good value to try out is:

```text
uniform float eyeScale = 0.1
```

Then you can just try re-rendering with the batch file.

### Exporting 360 videos / Offline Video Rendering

Videos can be rendered ‘offline’ faster and at a much higher resolution and framerate than using the internal Multicam tool

1. **Editing Tilt Brush cfg file**
2. Go to C:\Documents\Tilt Brush\Tilt Brush cfg
3. Under "Video" add the flag "SaveCameraPath": true,
4. Save Tilt Brush cfg
5. **Camera Setup**
6. Load the sketch you would like to render
7. Find a good spot from which you would like to capture your 360 video
8. Be sure to look around in all directions to make sure no objects are too close to the point of capture
9. Save your sketch
10. Record your video by moving camera or keeping camera stationary
11. After saving, exit Tilt Brush
12. **Rendering** Note: When you create a video from inside Tilt Brush using the Camera tool with configuration "SaveCameraPath" flag set to _true_, Tilt Brush will create a Windows batch file alongside the video \(In Documents\Tilt Brush\Videos\) that you can run to re-render the video at a higher resolution
13. Go to C:\Documents\Tilt Brush\Videos . There should be .usda, .bat and video file which corresponds to the .tilt file
14. Double click on .bat file
15. If you run that batch file a command window will appear giving you several options for re-rendering your video:![](.gitbook/assets/2%20%281%29.png)Press a number to get whichever format you prefer. It will then launch Tilt Brush, which will reload your sketch, and re-render the video. Once it is done, Tilt Brush will exit. As rendering at higher quality tends to affect the framerate, it is suggested that you do not wear your headset while this process completes.
16. Once the render is complete, it will pop open the “VRVideos” folder which should contain an video file with your stereo render.
17.  **Converting into 360 video**
    1. [Download the 360° Video Metadata app](https://support.google.com/youtube/answer/6178631?hl=en) for [Mac](https://github.com/google/spatial-media/releases/download/v2.0/360.Video.Metadata.Tool.mac.zip) or [Windows](https://github.com/google/spatial-media/releases/tag/v2.0). The dialog should look like this:![](.gitbook/assets/3%20%281%29.png)
    2. Un-zip the file, then open the 360 Video Metadata app. If you're on a Mac, you may need to right-click the app and then click Open.
    3. Select the video file.
    4. Select the checkbox for My Video is stereoscopic 3D \(top/bottom layout\)
    5. Click Inject Metadata
    6. Enter a name for the file that will be created.
    7. Save the file. A new file will be created automatically in the same location as the original file.
18. **Uploading to Youtube**
    1. Upload the new “injected” video file to YouTube
    2. Note that it takes YouTube some additional time to process 360 videos, until this process is finished, you may see the raw over/under and the “View in Cardboard” option will not be available.
    3. Once processing is done, you should see this icon when viewing the video on your phone, indicating that it’s ready to be viewed in VR:

![](.gitbook/assets/4%20%281%29.png)

## Tilt Brush Unity Shader Examples

Use these with geometry you export from Tilt Brush and import into Unity. However, you should prefer to use the [Tilt Brush Toolkit](http://github.com/googlevr/tilt-brush-toolkit), which comes with Tilt Brush shaders.

#### Opaque shader

```text
Shader "Brush/Standard"
{
    Properties
    {
        _Color ("Main Color", Color) = (1,1,1,1)
        _SpecColor ("Specular Color", Color) = (0.5, 0.5, 0.5, 0)
        _Shininess ("Shininess", Range (0.01, 1)) = 0.078125
        _MainTex ("Base (RGBA)", 2D) = "white" {}
        _BumpMap ("Normalmap", 2D) = "bump" {}
        _Cutoff ("Alpha cutoff", Range(0,1)) = 0.5
    }
    SubShader
    {
        Tags
        {
            "Queue"="AlphaTest" "IgnoreProjector"="True" "RenderType"="TransparentCutout"
        }
        LOD 400
        CGPROGRAM
        #pragma target 3.0
        #pragma surface surf StandardSpecular vertex:vert alphatest:_Cutoff addshadow
        struct Input
        {
            float2 uv_MainTex;
            float2 uv_BumpMap;
            float4 color : Color;
        };

        sampler2D _MainTex;
        sampler2D _BumpMap;
        fixed4 _Color;
        half _Shininess;

        void vert(inout appdata_full i)
        {
        }

        void surf(Input IN, inout SurfaceOutputStandardSpecular o)
        {
            fixed4 tex = tex2D(_MainTex, IN.uv_MainTex);
            o.Albedo = tex.rgb * _Color.rgb * IN.color.rgb;
            o.Smoothness = _Shininess;
            o.Specular = _SpecColor;
            o.Normal = UnpackNormal(tex2D(_BumpMap, IN.uv_BumpMap));
            o.Alpha = tex.a * IN.color.a;
        }
        ENDCG
    }
    FallBack "Transparent/Cutout/VertexLit"
}
```

#### Additive shader

```text
Shader "Brush/Additive"
{
    Properties
    {
        _MainTex ("Texture", 2D) = "white" {}
    }
    Category
    {
        Tags
        {
            "Queue"="Transparent" "IgnoreProjector"="True" "RenderType"="Transparent"
        }
        Blend SrcAlpha One
        AlphaTest Greater .01
        ColorMask RGB
        Cull Off Lighting Off ZWrite Off Fog
        {
            Color (0,0,0,0)
        }
        SubShader
        {
            Pass
            {
                CGPROGRAM
                #pragma vertex vert
                #pragma fragment frag
                #include "UnityCG.cginc"
                sampler2D _MainTex;

                struct appdata_t
                {
                    float4 vertex : POSITION;
                    fixed4 color : COLOR;
                    float3 normal : NORMAL;
                    float2 texcoord : TEXCOORD0;
                };

                struct v2f
                {
                    float4 vertex : POSITION;
                    fixed4 color : COLOR;
                    float2 texcoord : TEXCOORD0;
                };

                float4 _MainTex_ST;

                v2f vert(appdata_t v)
                {
                    v2f o;
                    o.vertex = mul(UNITY_MATRIX_MVP, v.vertex);
                    o.texcoord = TRANSFORM_TEX(v.texcoord, _MainTex);
                    o.color = v.color;
                    return o;
                }

                fixed4 frag(v2f i) : COLOR
                {
                    half4 c = tex2D(_MainTex, i.texcoord);
                    return i.color * c;
                }
                ENDCG
            }
        }
    }
}
```

## Tilt Brush File Format

The .tilt file format can also be parsed by the [Tilt Brush Toolkit](http://github.com/googlevr/tilt-brush-toolkit).

A .tilt is a zip-format file with a prepended header:

```text
uint32 sentinel ('tilT')
uint16 header_size (currently 16)
uint16 header_version (currently 1)
uint32 reserved
uint32 reserved
```

Inside the zip, the strokes are stored in a custom binary format in a file, "data.sketch":

```text
uint32 sentinel
uint32 version
uint32 reserved (must be 0)
[ uint32 size + <size> bytes of additional header data ]
int32 num_strokes
num_strokes * {
    int32 brush_index
    float32x4 brush_color
    float32 brush_size
    uint32 stroke_extension_mask
    uint32 controlpoint_extension_mask
    [ int32/float32 for each set bit in stroke_extension_mask & ffff ]
    [ uint32 size + <size> bytes for each set bit in stroke_extension_mask & ~ffff ]
    int32 num_control_points
    num_control_points * {
        float32x3 position
        float32x4 orientation (quat)
        [ int32/float32 for each set bit in controlpoint_extension_mask ]
    }
}
```

The orientation is that of the controller. Curve and surface frames must be reconstructed.

Stroke extensions:

| 0 | uint32 bitfield. Bit 0: IsGroupContinue |
| :--- | :--- |


Control point extensions:

| 0 | float pressure, in \[0,1\] |
| :--- | :--- |
| 1 | uint32 timestamp, in milliseconds |

### 

Also inside the zip is "metadata.json", the metadata for the sketch in json format. Here are some of the fields that can be found there:

* "Authors": an array of author names.
* "SceneTransformInRoomSpace": the transform of the scene relative to the room.
* "ThumbnailCameraTransformInRoomSpace": the transform used to generate the sketch as an array of:
  * translation \(array of 3 floats\)
  * rotation quaternion \(array of 4 floats\)
  * scale \(single float\)
* "ModelIndex": an array of models imported into the sketch. Each model can have the following:
  * "FilePath": location of the model
  * "PinStates": an array to indicate whether each instance of the model should initially be pinned.
  * "RawTransforms": an array of transforms for each instance of the model.

## Previous Releases

#### Version 22

* Added Groups to Selection tool.
  * Grouping allows brush strokes and widgets to share selection state. Select part of a group and the whole group is selected with it.
  * Grouping status data is saved with the sketch.
  * When a sketch is exported, each group is written to a separate node in the exported file. This allows easier sketch manipulation in editing tools, post-export.
  * “Group Selection” is one of the buttons available on the new selection tray that pops out next to the selection button when the selection tool is on.
* Added Reference Videos support.
  * New tab added to Media Library Panel for videos.
  * Videos are taken from the **Tilt Brush\Media Library\Videos** directory.
  * Videos, like reference images, are not stored in the .tilt file and are not uploaded to Poly.
  * You can link to an online video by putting its URL into a .txt file inside the videos directory.
  * Audio from videos is supported, but is ‘2D’ only.
  * Known bugs:
    * Reference Videos do not currently work in offline renders.
* Export Improvements.
  * Tilt Brush exports .glb \(glTF 2.0\) instead of .glb1 \(glTF 1.1\). glTF 2.0 is supported by more tools and is slightly more efficient.
  * Export now works on Oculus Quest \(.glb only\)
  * [Tilt Brush Toolkit](https://github.com/googlevr/tilt-brush-toolkit) supports both .glb and .glb1.
  * **glb**: Added timing information to .glb exports.
    * Tilt Brush Toolkit will put timing information into texcoord2.
    * Timestamps are a vec3.
      * x,y = the earliest/latest timestamp in the stroke which contains that vertex.
      * z = the timestamp for that vertex.
    * This can be disabled in the Tilt Brush config Export section with “ExportStrokeTimestamp”: false
    * [How to use the Tilt Brush config file.]()
  * **glb, fbx**: Media Library models are now included in exports.
  * **glb, fbx**: Various quality of life improvements in the exported file.
* New tool tip descriptions.
  * Tool tips have a new cleaner and consistent look.
* Deterministic Geometry Generation.
  * Some stroke behavior is randomized—for example, brush textures and Light Wire light colors. This behavior is now saved into the .tilt, so when you re-load a sketch you will see the same thing as when you drew it.

#### Version 21

* Quest release only.
* Added Labs Panel.
  * Contains Reference Image Panel, Pin Tool, Export, and experimental Cameras.
* Added Reference Image support.
  * Requires connecting your Quest to a PC and side loading images into a Tilt Brush folder. Some restrictions apply.
  * See the [Help Center](https://support.google.com/tiltbrush/answer/9427219?hl=en&ref_topic=7074683) for a more detailed explanation of how to use Reference Images.
* Added Export to .glb1 \(binary glTF\).
  * Updated Tilt Brush Toolkit to support .glb1 import.
  * Previously, Reference Images would appear in the export as as empty transform nodes. They are now included in the export.
* Added Cameras.
  * Experimental version of Snapshot and Gif Capture cameras.
* Tilt Brush files moved to “/sdcard/Tilt Brush” on Quest.
  * This prevents work from being lost when Tilt Brush is uninstalled.

#### 

#### Version 20

* PC release only.
* Add Valve Index support.
  * Update to latest SteamVR plugin to support custom input bindings.
* Added Logitech VR Ink Pilot Edition.
* Drastically decreased the amount of memory allocated during sketch quick-loading.
* Variety of performance optimizations pulled from the Oculus Quest version.

#### 

#### Version 19

* Oculus Quest release only.
* Deviations from PC.
  * Labs Panel has been removed.
    * Export not supported.
    * Spectator Camera not supported.
    * Twitch Chat not supported.
    * YouTube Chat not supported.
    * Local Media Library not supported.
    * Tiltasaurus game not supported.
  * MultiCam has been removed.
    * Photo capture, video capture, and streaming are all supported by the Oculus Dash platform.
  * Select All has been disabled.
  * Invert Selection has been disabled.
  * Flip Selection has been disabled.
  * Autosave has been disabled. Be careful!
* Added Memory Warning Mode.
  * Memory allocation can be viewed in the Settings Panel.
  * After crossing a memory threshold, the app will enter a ‘Memory Warning’ state.
  * Deleting a Sketch will reset allocated memory.
  * Sketches above a certain triangle limit will display a warning in the Showcase and Liked Sketches section of the Sketchbook.
  * Sketches above a certain larger triangle limit will display a more severe warning in the Liked Sketches section of the Sketchbook.

#### 

#### Version 18

* New audio for all brushes.
  * Each brush sound is now unique, and subtly reacts to the way you are painting.
* Flip Selection.
  * Long press on Selection Tool icon in Advanced mode.
* Allow tuning of MultiCam field of view.
  * Requires “Tilt Brush.cfg”, stored in: **Documents/Tilt Brush**
  * Format:

{

 "Video": {

 "FOV": 90,

 },

 "Flags": {

 "FOV": 100,

 },

}

* * [How to use the Tilt Brush config file.]()
* Added a button in the Settings to link to the [Help Center](https://support.google.com/tiltbrush/).
* Import and apply normal maps for .fbx models in Media Library.
* Fix screen tearing bugs with video recording.
* Added a frame counter for offline rendering.
* Fix some Poly models not loading.
  * Visible error was, “No usable geometry found!”.

#### 

#### Version 17

* Added controller support for Windows Mixed Reality headsets on SteamVR

#### 

#### Version 16

* NEW BRUSHES! 12 brand new brushes for your enjoyment:
  * Wet Paint - Glossy, high shine paint
  * Dr Wigglez - Animated sketchy charcoal
  * Cel Vinyl - A flat cartoon brush with a black outline
  * Petal - 3d flower-like brush, also great for hair
  * Icing - A lit tube brush with a light texture
  * Spikes - 3d spikes
  * Lofted - 3d calligraphic brush
  * Comet - A new spin on a 3D animated fire brush
  * Hull brushes - create volumes by sweeping out the brush with a few different shading options:
    * Shiny
    * Matte
    * Unlit
    * Diamond
* Beginner & Advanced modes.
  * New “Beginner” mode with a more limited set of tools, well suited for new users, and when giving demos.
  * Panel layout saved session to session in Advanced mode.
  * New Main Menu Panel design.
* New Pin tool.
  * New dedicated tool for quickly pinning and unpinning models, guides and images.
  * Located on the Labs Panel.
* Select All and Invert Selection.
  * Long press on Select Tool icon in Advanced mode.
* Recall Mirror.
  * Long press on Mirror Tool icon in Advanced mode.
  * Useful for retrieving the mirror when it is out of arm's reach.
* Rapid Undo / Redo.
* Press & hold the Undo or Redo button on the controller to repeat the action repeatedly.
* New UI audio.
* Stroke Simplification Slider.
  * Allows vertex reduction on sketches. Useful for low performance PCs and simplifying geometry before export.
  * Located on the Settings Panel.
* Pixar's Universal Scene Description \(USD\) is now exported when pressing ‘Export’ on the Labs Panel.
  * This new export includes geometry, models, brush curves, and stroke timing.
* Support for [changing eye scale]() when rendering ODS 360 videos.
  * You can now create a camera path with everything scaled down, and then scale the camera back up when doing an offline render.
* General performance improvements.
  * Sped up rendering of UI.
  * Sped up rendering of several brushes.

#### 

#### Version 15

* Support for importing any object uploaded to Poly \(w/ CC-BY license\)
  * The “Poly” panel is located inside Tilt Brush: "Tools" panel -&gt; “More Tools...” -&gt; “Poly”.
  * Any CC-BY Blocks model or .obj you like on Poly will appear on that panel \(assuming you’re signed-in with the same account\).
  * You can remix Blocks models and uploaded .objs in your Tilt Brush sketches, and share remixed sketches back to Poly!
  * Note: you cannot import published Tilt Brush sketches into Tilt Brush sketches at this time.
* New intro flow and updated Sketchbook panel
  * Starting with the second time users open Tilt Brush, we now show a more illustrative “intro” screen.
  * The controllers also default to having the Sketchbook open, highlighting sketches featured from Poly.
* Selection improvements
  * Stamp mode: when gripping a selection with your painting controller, you can now stamp duplicates of your selection in your scene
* New contextual tooltips for actions and features
  * We’ve added contextual tooltips to instruct users how to use certain features.
  * Specifically: grip to grab, toss to dismiss, selection, and sharing sketches to Poly.
* Video Recording
  * 360 videos now render 5x as fast.
  * Added the option to use “h.264” encoder, see user config for details.
  * Videos can now be rendered ‘offline’ at a higher resolution and framerate than feasible from inside Tilt Brush. See [Rendering ‘Offline’ Videos]().

#### 

#### Version 14

* Blocks Library:
  * Accessible on the “Tools” panel, the Blocks Library allows you to add remixable featured and liked [Blocks](https://vr.google.com/blocks/) objects to your Tilt Brush sketches.
  * Tilt Brush sketches using Blocks objects can now be published to vr.google.com/sketches.
  * \*Only\* remixable Blocks objects will appear in the Blocks Library.
* Selection Tool:
  * With the new “Selection Tool”, you can select and duplicate strokes and models in your scene.
  * “Selection” is found next to the “Eraser” button on the Tools panel.
  * Select strokes using the trigger. You can also flip into deselect mode by tapping the thumbpad \(Vive\) or “A/X” button \(Rift\).
  * If you want to move your selection, grab it as you would any other model in your scene. To delete a selected group of strokes, just throw it away.
  * Duplicate selections by holding the thumbpad \(Vive\) or “A/X” button \(Rift\) while intersecting your controller with selected strokes.
* Quick Tool:
  * Holding the “menu” button \(Vive\) or “Y/B” \(Rift\) on the controller now triggers a “Quick Tool” menu, letting you quickly swap tools without reaching back to the palette.
* Palette icon reorganization:
  * Reshuffled icons on the palette, based on common usage patterns
  * Moved the user profile button to the Menu Panel
  * Introduced a new “More…” menu where we’re moving more advanced tools and features.
  * We did not remove any Tools - if you’re looking for something and can’t find it, it is probably either in a “More…” menu or under “Labs.”
* Relaxed limit on model scale:
  * Imported models can be scaled to much smaller and larger sizes.
  * At certain large scales you may find performance hitches -- your fate is in your hands.
* Fixed duplicate upload bug:
  * Now when you upload sketches to vr.google.com/sketches, new drafts of a sketch will overwrite the last draft \(instead of creating a new one\).
  * Doesn’t affect published sketches.
* Tiltasaurus tweaks:
  * Now sketches are saved automatically when a new word is chosen.

#### Version 13

* Internal version that was either too good to release, or the dev team suffered from triskaidekaphobia.

#### Version 12

* Ability to “repaint” stroke colors
  * Allows you to change the color of any strokes in your scene
  * Accessible through the “Labs” panel
* “Featured” sketches in Tilt Brush pull from tiltbrush.com/sketches
  * Share your sketches to the web for a chance to be featured in Tilt Brush!
  * Featured sketches are found in the “Sketchbook” panel in the app
* Ability to view rights reserved sketches liked on tiltbrush.com/sketches
* Added a parameter in "Tilt Brush.cfg" to control camera smoothing for video captures

#### Version 11

* UI polish
  * Refreshed panel form factor \(rounded edges, same sizes, all elements aligned to a grid\)
  * Refreshed the visual style of the icons
* Added lights/backdrop to the undo/redo stack
  * Changes to lights’ color and orientation are on undo stack
  * Changes to skybox \(unlocking, changing color and orientation\) are on undo stack
  * Changes to fog color and density are on undo stack
  * Changing environments is on undo stack
* Camera movement for 360 stereo video export \([example](https://www.youtube.com/watch?v=EUYJSxjUmYg)\)
  * Two sketches can now be specified when rendering with --captureOds
  * Save the same sketch twice: the first with your starting camera angle, and the second with the camera where you want the path to end
  * The camera will move on a path from the first camera location to the second in a single 360 video
  * See “Exporting 360 Videos” below for details
* Faster video encoding
  * The video camera now encodes faster, which enables higher resolution videos and higher frame rates. See “Using the Tilt Brush.cfg file” below for details on how to adjust resolution and frame rate.
* Integrated Google VR [spatial audio](https://developers.google.com/vr/concepts/spatial-audio)
* Sketches exported to FBX include transforms for _Media Library_ assets. This means you can easily rebuild your scenes \(including those _Media Library_ assets\) in another 3D package. Formal support is in place for Unity and Maya.
* **100% Brush Parity** in the [Tilt Brush Toolkit](https://github.com/googlevr/tilt-brush-toolkit) \(including all particles\)
* Linear lighting support in The [Tilt Brush Toolkit](https://github.com/googlevr/tilt-brush-toolkit)
  * Previously, there were issues with color disparity between Linear & Gamma lighting modes.
  * If you export with **Version 10 or above, you should use the new Toolkit.** Otherwise, your colors will look incorrect.

#### Version 10

* Sharing
  * Share sketches to the [online gallery](https://vr.google.com/sketches)!
  * Use the Share button on the Save/Trash Panel to upload the active sketch. Requires logging in with a Google account.
  * Unsaved sketches shared to the online gallery are automatically saved to your Sketchbook.
  * Imported models, images, and guides currently do not upload to the online gallery.
  * Environment models, like the Snowman and Moon, currently do not upload to the online gallery.
* Added ‘Likes’ tab to Sketchbook
  * Sketches ‘Liked’ on the online gallery show up in this tab. Browse [here](https://vr.google.com/sketches)!
  * Sketches flagged as ‘Don’t Allow Remixing’ on the online gallery will _not_ show up in the Likes section of your Sketchbook \(for now\).
* Added Profile to Sketchbook
  * Log in with your Google account to Share sketches to the online gallery and to view Liked sketches from the gallery.
  * Logging in must be done through a web browser, which will open when clicking the Profile button or Share button.
* Lighting Panel
  * Control the color of the ambient lighting.
  * Control the colors, intensities, and directions of one shadow-casting and one non shadow-casting light.
  * Custom lighting is saved with the sketch.
* Backdrop Panel
  * Change the sky to a two-colored gradient.
    * Each of the two colors can be customized.
    * The orientation of the gradient can be customized.
  * Change the color and density of the fog.
  * Custom sky and fog is saved with the sketch.
* Detachable and Customizable UI Panes
  * Grab any Panel with the grip button to adjust its position on the Pane, or to remove it from the Pane.
  * The Save/Trash Panel _cannot_ be removed from the Pane.
  * Panels opened in the ••• Panel selection popup can be attached to a Pane.
  * Panel configuration can be reset by clicking the Refresh button in the ••• Panel selection popup.
* Changed save flow to allow Save and Save New
  * An unsaved sketch must have a thumbnail captured before saving.
  * A previously saved sketch can be saved over with Save, or copied to a new file with Save New.
  * Honestly, it works like every application ever and exactly as you’d expect.
* Added Disaster Recovery functionality
  * Active sketch is periodically backed up to **C:\Users\**&lt;username&gt;**\Documents\Tilt Brush\Sketches\Autosave** folder. [More info](https://docs.google.com/document/d/1UnXLNrIV5z-bfHilWh1--vdN_-MY9BdLg5fcs9xlpDU/edit#heading=h.fti7q68lns72).
* Increased performance of particle brushes.
* Greatly increased performance of Eraser and Brush Picker.
* Fix material leaking bug which caused large hitches after long periods of usage.
* Colors in .fbx exports are now in linear space.
* Fixes to add more compatible brushes in the Unity SDK.
* Color Picker type saved between sessions.
* Custom Color Palette is shared across all color pickers.
* Updated SteamVR plugin to v1.2.0.

#### Version 9

* Oculus Rift support on Oculus Home
* Oculus Rift support on SteamVR
* Added customizable Color Palette to Color Picker.
* Color Palette is saved with sketch.
* Fixed bug allowing false positives when Eraser was at the origin.
* Revised loading overlay to be consistent across multiple platforms.
* Added 'ShowControllers' flag to config for toggling controller visibility. Intended use for performances, galleries, and mixed reality.
* Disabled saving videos under a second in length, as they were confusing YouTube upload.

#### Version 8

* Sharing directly from Tilt Brush to YouTube
  * When you record a video, you now have the option to upload to YouTube.
  * Hold down the thumbpad after a video has finished recording to go into Preview mode.
  * If you like the video you’ve captured, hold down the checkmark to upload.
  * YouTube sharing requires that you sign-into your YouTube account in your default desktop browser.
  * If your video includes audio you may be affected by YouTube’s copyright policies. Read about them [here](https://support.google.com/youtube/topic/2676339).
  * Hint: Want to record audio from your microphone? Go to the _Recording_ tab in Windows Sound properties, select _Properties_ for your microphone then check _Listen to this device_. Make sure the Video Recorder has found audio before beginning a recording!
* Guides for easily constraining strokes to cubes, spheres, and other shapes.
  * Access through Tools -&gt; More… -&gt; Guides.
  * Use the sphere, cube, and pill guides to create perfect shapes.
  * Guides are moved and scaled similar to other widgets, using the Grip buttons.
* Straightedge now shows the final stroke you’re painting.
* Increased size range for a couple dozen brushes.
* “DisableAudio” field added to the Tilt Brush.cfg.
  * [How to use the Tilt Brush config file.]()
* Change to save file naming.
* Fixed bug where Tilt Brush would be unplayable when the Documents folder was moved or inaccessible due to virus detection software.
* Minor improvements to models.
  * Models can now be grabbed while inside them.
  * Model materials support alpha cut-out and transparency.
  * FBX format models are now supported.
* Minor placement fixes to the Mirror tool.
* Added in-app reminder instructions for skipping the intro tutorial.

#### Version 7.5

* Media Library Improvements
  * Support for importing multiple models and images.
  * Added ability to pin models and images, disabling movement.
    * While holding a model or image, pull Trigger to pin and unpin.
  * Models and images save with sketch.
  * Models and images contribute to Tilt Meter.
  * Model and image interactions added to the undo stack.
  * Images support binary alpha.
  * Updated visuals for highlighting objects that can be grabbed with Grip button.
* Improved Snapping
  * While holding a snappable object, hold Trackpad to snap.
    * Snappable objects include: models, images, mirror, Tips ‘N Tricks, and brush strokes, when Straightedge is selected.
    * Removed auto-snap on Mirror and Straightedge.
  * Model, image, and Tips ‘N Tricks snap to cardinal orientations.
  * Mirror snaps to flat horizontal, as well as 15 degree increments where n=\(x, 0, z\).
  * Straightedge snaps to up, down, 45 degrees, and 0 degrees.
  * Models and images can snap to center of environment.
    * In the Pedestal environment, models and images snap to the pedestal.
* Video Recorder Improvements
  * Video capture now records with audio.
  * Ability to customize video resolution, FPS, container type in the Tilt Brush.cfg. [How to use the Tilt Brush config file.]()
* Misc. improvements
  * "Animal Ruler" shows relative size when using the scale feature.
  * Mirror position saved with sketch.
  * Mirror position added to undo stack.
  * Added unsaved work warning before loading a sketch.
  * Added clock to Controller Console.
  * Animate grip and trigger buttons on controller meshes.
  * Added new tips to the Tips ‘N Tricks.
  * Updated SteamVR plugin to v1.1.1.
  * “Author” field added to the Tilt Brush.cfg.
    * When the Author field is set, all sketches created will have the author name embedded in saved .tilt files.
    * [How to use the Tilt Brush config file.]()
  * Support scripts have moved to the [Tilt Brush Toolkit](https://github.com/googlevr/tilt-brush-toolkit).

#### Version 7

* Rotate and Resize
  * Hold both grip buttons at the same time to move, turn, or resize yourself.
  * While resizing, click the trackpad to reset yourself to original size.
  * Any changes to size or rotation are saved with sketches.
* Media Library
  * Added ability for users to import an .obj model into their sketch.
  * Moved reference images and models to “Media Library” panel accessed through the “More…” menu on the Tools panel.
  * Models are pulled from the **Documents/Tilt Brush/Media Library/Models** folder, images are pulled from the **Documents/Tilt Brush/Media Library/Images** folder.
  * See **Tilt Brush/Media Library/MediaLibraryReadme.txt** for details on how to use Media Library.
* Tiltasaurus
  * Added new game to the Labs panel.
  * See the [Help Center](https://support.google.com/tiltbrush#topic=7074683) for instructions how to play.
  * Adding _Tiltasaurus.json_ to the **Documents/Tilt Brush** folder will let you add your own list of words.
  * Format:

```text
{
   "Categories":[
      {
         "Name":"Action",
         "Words":[
            "Applause",
            "Arguing",
            "Ballet"
         ]
      },
      {
         "Name":"Animal",
         "Words":[
            "Butterfly ",
            "Cat",
            "Chicken"
         ]
      }
   ]
}
```

* Controller Swapping
  * Point the controllers away from each other and tap the bottoms to swap the palette and paint brush.
* High resolution snapshot mode
  * Added flag “HighResolutionSnapshots” to the Tilt Brush.cfg. [How to use the Tilt Brush config file.]()
  * Setting the flag to true causes the Camera tool to take snapshots at 6x the default resolution \(11,880 x 6,588px\).
* Exporting to Sketchfab
  * Many important material properties are now preserved when exporting .fbx files and then uploading to Sketchfab. [Posting to Sketchfab.]()
* Misc. improvements
  * More aggressive video camera stabilization.
  * Fire brush bloom effect fixed on “Future Desktop” settings.
  * Cleaned up the progress bar images, added info text during loading.
  * Added new tips to the Tips ‘N Tricks.
  * Changed video file extension to .mp4.
  * Exports binary FBX by default, configurable in Tilt Brush.cfg. [How to use the Tilt Brush config file.]()
  * Pressing the pad no longer activates teleport with Teleport Tool. Trigger only.
  * Teleport Tool boundaries are extended when the sketch has been resized.
  * Changed selection icon for Sketchbook to trash can.
  * References to models are saved with sketches, but the file data is not embedded within the .tilt file. If a sketch is loaded without the referenced model in the Media Library, a missing model icon will be displayed.
  * Added ‘About’ button to Settings for viewing really exciting third party notices.

#### Version 6

* Audio reactive brushes
  * Added new “Audio Reactive” mode for brushes.
    * Toggle Audio Reactive mode on the Brushes panel.
    * Audio Reactive mode scans the computer’s audio out signals and connects to the first found active signal.
    * Audio Reactive mode will respond to _any_ computer audio.
  * Added 15 new brushes and deprecated 3 \(Taffy, Leaves, and Plasma\)
  * Updated many brushes to add audio-reactive behaviour.
* Cameras
  * Renamed from “MultiCam”.
  * Added Video mode to “Cameras”.
  * Added vignetting and depth of field effects to snapshots and videos.
* Interface improvements
  * Streamlined the UI down to 3 panels.
  * Added dedicated Sketchbook panel, below Tools panel.
  * Added toggleable measurements to Straightedge tool.
    * Enable this feature on the Settings panel.
  * Undo/Redo can be used when a panel has focus.
  * Swiping on the brush controller thumbpad scrolls through the pages of the Brushes panel.
  * Added new “More” menu.
  * Changed Teleport tool icon visual from “Pin” to “Feet”.
  * Application button on the brush controller now toggles the last tool.
  * New visual design for the Color and Brush Picker tool.
* Grabbable object improvements
  * Moveable UI panels now move out of each other’s way.
  * Mirror can be reset by dragging it to the target above the center of the floor.
  * Mirror now snaps to vertical and horizontal planes.
* Added Tips ‘N Tricks tutorial section, under “More” menu.
* Export button now generates textured .fbx files. See the [Exporting Tilt Brush Sketches]() section below for more details.
* Improved visual quality at all performance levels.
* Unlit brushes made more efficient by using single-sided geometry.
* Added progress bar when exporting or loading sketches.

#### Version 5

* Switch versioning numbers to be more open-ended.
* Added 5-Second Gif mode to MultiCam.
* Export button now auto-generates .fbx, along with old .json intermediate file.
* Color picker works on reference images.
* Revised controller pad visuals for MultiCam.
* Fix help text on Twitch Chat window.
* Allow controller pad click to teleport.

#### Version 1.4

* Added Teleport Tool.
* Added ability to view YouTube Live chat while streaming. \(see notes below\)
* Replaced IRC support with dedicated Twitch Chat support. \(see notes below\)
* Labs Panel can be dismissed by tossing.
* Improved Undo/Redo trackpad click functionality.
* Reference Image widget resets position when a new image is selected.
* Moved Quick-Load tip to Palette controller so user can teleport during sketch load.

**Labs Panel**

* YouTube Chat
  * Requires “Tilt Brush.cfg”, stored in: **Documents/Tilt Brush**
  * Format:

```text
{
 "YouTube": {
 "ChannelID": "UCabcdefghijklmnopqrstuv",
 },
}
```

* * Note: [How to find your YouTube Channel ID.](https://support.google.com/youtube/answer/3250431)
  * [How to use the Tilt Brush config file.]()
  * Use Grip button to move chat widget.
  * Use both Grip buttons to scale chat widget.
  * Toss the widget to dismiss it.
* Twitch Chat
  * Requires “Tilt Brush.cfg”, stored in: **Documents/Tilt Brush**
  * Format:

```text
{
 "Twitch": {
 "Username": "TiltBrushStreamer",
 "OAuth": "oauth:abcdefghijklmnopqrstuvwxyz0123",
 "Channel": "#tiltbrushchannel",
 },
}
```

* * Note: [How to get an OAuth key for Twitch.](https://twitchapps.com/tokengen/)
  * [How to use the Tilt Brush config file.]()
  * Use Grip button to move chat widget.
  * Use both Grip buttons to scale chat widget.
  * Toss the widget to dismiss it.

#### Version 1.3

* Improved guide for Spectator Camera in Circle Mode.
* Added Mirror snap functionality.
* Added basic Export support.
* Added ability to view .jpgs and .pngs as Reference Images.
* Added visual notification when an important message is on the Controller Console.
* Added a button to Sketch Gallery for easy viewing Sketches on disk.
* Added ability to connect to an IRC channel for assisting live streamers.
* Added a ‘Labs’ button on the Settings panel for advanced and experimental features.
* Skip the intro tutorial by holding down both trigger buttons.

**Labs Panel**

* Reference Images
  * Used for viewing external images while inside Tilt Brush.
  * Loads .png and .jpg images stored in **Documents/Tilt Brush/Reference Images**.
  * Use Grip button to move image widget.
  * Use both Grip buttons to scale image widget.
  * Toss the widget to dismiss it.
  * _Caution!_ Extra large images, such as 4k, may cause performance hitches in Tilt Brush.
* Export
  * Exports current scene's metadata and 3D geometry to a json file in **Documents/Tilt Brush/Exports**.
  * Tilt Brush ships with sample [Python 2.7](https://www.python.org/download/releases/2.7/) scripts to convert the .json to .obj and .fbx formats. These scripts are in the **Support/bin** folder, which is next to TiltBrush.exe. The fbx conversion also requires the [Autodesk FBX Python SDK](http://images.autodesk.com/adsk/files/fbx20151_fbxpythonsdk_win.exe). To find TiltBrush.exe from Steam, right-click "Tilt Brush" → Properties → Local Files → Browse Local Files...
  * Example script usage:

    python convert\_to\_fbx.py "c:\Users\_username_\Documents\Tilt Brush\Exports\Untitled\_1.json"

    Each script has a set of command-line options that fine-tune the generated file.

  * Note that this initial preview **does not export textures or materials**. In addition, the .obj file format does not support vertex colors. We’re looking into solutions to provide users with more of this data, but didn’t want to delay sharing what we have now. The .fbx does support vertex colors, but to see them you will need to apply a shader that uses vertex color information like the two example Unity shaders below.
  * Please [let us know](mailto:tiltbrush@google.com?Subject=I%20used%20export) how you use this functionality!
* IRC
  * Requires “Tilt Brush.cfg”, stored in: **Documents/Tilt Brush**
  * Format:

```text
{
   "IRC":{
      "ServerName":"irc.twitch.tv",
      "ServerPort":6667,
      "Username":"TiltBrushStreamer",
      "OAuth":"oauth:abcdefghijklmnopqrstuvwxyz0123",
      "Channel":"#tiltbrushchannel"
   }
}
```

}

Note: [How to get an OAuth key for Twitch.](http://help.twitch.tv/customer/portal/articles/1302780-twitch-irc)

* * [How to use the Tilt Brush config file.]()
  * Use Grip button to move chat widget.
  * Use both Grip buttons to scale chat widget.
  * Toss the widget to dismiss it.
* Watermark
  * The Tilt Brush logo watermark can be disabled. This also requires a "Tilt Brush.cfg" file, stored in **Documents/Tilt Brush**. The format is

```text
{
 "Flags": {
 "ShowWatermark": false,
 },
}
```



*  * [How to use the Tilt Brush config file.]()

