# Importing Images, Videos and 3D Models

eIf you want to see an image or 3D model while you paint in Open Brush, you can add it to your scene. You can move, change, or delete reference images.

1. Make sure you are in Advanced Mode.
2. Below your palette, go to the Menu panel and select "**More Options...**".
3. On your paint palette, swipe to the Tools panel and select More.
4. Select **Labs** to open the [Labs Panel](using-the-open-brush-tools-quick-tools-and-menu-panels/the-admin-panel/labs-panel.md)

![](<../.gitbook/assets/image-098.png>)

Click this icon to open the Media Library:

### <img src="../.gitbook/assets/image (8) (1) (1).png" alt="" data-size="original">

#### **Add an image or video clip**

1. Copy a PNG or JPG file to Documents/Open Brush/Media Library/Images or a video file to Documents/Open Brush/Media Library/Videos
2. In Open Brush, make sure you are in [Advanced Mode](using-the-open-brush-tools-quick-tools-and-menu-panels/tool-panels.md).
3. Go to the Menu panel (below your palette) and select **"More Options..."** **>** **Labs > Local Media Library > Local Images**.
4. Switch between selecting images and models using the icons in the top left.

You can organize your media files into folders. See [Folder Navigation](folder-navigation.md) for more information.

#### **Add a 3D model**

1. Copy any [supported](importing-images-videos-3d-models.md#supported-file-formats) 3d file to Documents/Open Brush/Media Library/Models.
2. In Open Brush, make sure you are in Advanced Mode. On the Quest you also need to switch Experimental Mode on in the settings.
3. Go to the Menu panel (below your palette) and select **"More Options..."** **> Labs > Local Media Library > Local Models**.
4. Switch between selecting images and models using the icons in the top left.
5. See "Supported Formats" below to see which file types you can use.

You can organize your media files into folders. See [Folder Navigation](folder-navigation.md) for more information.

### Supported File Formats

<table><thead><tr><th width="140">Type</th><th>Format</th><th>Notes</th></tr></thead><tbody><tr><td>Images</td><td>PNG</td><td></td></tr><tr><td></td><td>JPEG</td><td></td></tr><tr><td></td><td>SVG</td><td>(SVGs can be imported either as images or as a mesh)</td></tr><tr><td></td><td>HDR</td><td></td></tr><tr><td>Video</td><td>MP4</td><td>See notes below.</td></tr><tr><td></td><td>MKV</td><td>See notes below.</td></tr><tr><td></td><td>MOV</td><td>See notes below.</td></tr><tr><td></td><td>WEBM</td><td>See notes below. Must use VP8 codec. Supports transparency on Windows only.</td></tr><tr><td>3d Models</td><td>GLTF/GLB</td><td></td></tr><tr><td></td><td>OBJ</td><td></td></tr><tr><td></td><td>FBX</td><td>PC/Mac only.</td></tr><tr><td></td><td>USD</td><td>PC/Mac only. Support is rather outdated and experimental</td></tr><tr><td></td><td>PLY</td><td>Point clouds only. Binary little-endian format.</td></tr><tr><td></td><td>SVG</td><td>(SVGs can be imported either as images or as a mesh)</td></tr><tr><td></td><td>VOX</td><td>Magicavoxel format for voxel models</td></tr></tbody></table>

## WebM Video Import

WebM is a video format that supports transparency (alpha channel), allowing you to import videos with transparent backgrounds. This is particularly useful for effects, animated sprites, or reference footage.

**Requirements:**
- Must use VP8 codec
- Transparency is currently only supported on Windows
- Place .webm files in Documents/Open Brush/Media Library/Videos

## Point Cloud Import

You can import point cloud data in PLY format (binary little-endian). Point clouds are useful for:
- Importing 3D scanned data
- Working with photogrammetry outputs
- Creating particle-like effects
- Reference data from LiDAR scans

Place .ply files in Documents/Open Brush/Media Library/Models and they will appear in the model browser.

{% hint style="info" %}
Video support varies across OS and hardware versions. See:\
\
[https://learn.microsoft.com/en-us/windows/win32/medfound/supported-media-formats-in-media-foundation#video-codecs](https://learn.microsoft.com/en-us/windows/win32/medfound/supported-media-formats-in-media-foundation#video-codecs)\
\
[https://learn.microsoft.com/en-us/windows/win32/medfound/supported-media-formats-in-media-foundation#video-codecs](https://learn.microsoft.com/en-us/windows/win32/medfound/supported-media-formats-in-media-foundation#video-codecs)\
\
for more detailed information.
{% endhint %}

### **Interacting with Imported Objects**

**Move an image or model:** Position your controller on the image, press and hold a grip button on the side of your controller. Then, drag the image to the new location and release the grip button.

**Resize an image or model:** With your controllers near the image or model, press and hold both grip buttons. Then, move the controllers farther apart or closer together.

**Pin an image or model:** While holding your selection with the grip, pull the trigger to pin. Alternatively, you can use the Pin tool to pin images, models, or guides.

**Remove an image or model:** With your controller near the reference image, press and hold a grip button. Then, flick the controller away from your body and release the grip button. You can also use the [eraser tool](using-the-open-brush-tools-quick-tools-and-menu-panels/tools-panel/).
