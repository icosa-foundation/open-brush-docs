# Exporting video

{% hint style="info" %}
Quest and other Standalone Headset Users - exporting video directly from within Open Brush is currently only supported for PC VR only. See the [section below](exporting-videos.md#quest-and-other-non-pc-devices)
{% endhint %}

### The Camera Tool

The standard way to export video is using the [Camera Tool](using-the-open-brush-tools-quick-tools-and-menu-panels/#cameras) within Open Brush itself.

### Settings that affect video render

There are several useful settings you can change in the [config file](exporting-videos.md#the-camera-tool).

### Rendering ‘Offline’ videos

When you create a video from inside Open Brush using the Camera tool and you've set "SaveCameraPath" to True in the [Open Brush config file](the-open-brush-config-file.md) - Open Brush will create a Windows batch file alongside the video (In Documents\Open Brush\Videos) that you can run to re-render the video at a higher resolution. For example:

_Untitled\_13\_00.mp4_

_Untitled\_13\_00.HQ\_Render.bat_

Double-clicking the ".bat" batch file will give you several options for re-rendering your video:

![](<../.gitbook/assets/1 (1).png>)

Press the number corresponding to the format you prefer. It will then launch Open Brush, which will reload your sketch and render the video. Once it is done, Open Brush will exit. As rendering at higher quality tends to affect the framerate, it is suggested that you do not wear your headset until this process completes.

“No Quick Load” option (#6) will forego quick loading of the sketch and will force it to load at normal speed. It is recommended that the time spent recording should exceed the normal loading time of the sketch or else the video may end before the sketch completes loading.

### Video Camera Paths

Rendering offline videos is achieved by saving off the path the camera took when the video was taken, and then re-using that to recreate the video. The camera path is saved off in ASCII USD ([Universal Scene Description](https://graphics.pixar.com/usd/docs/index.html)) format, so if you have an application that can read and write USD, you may be able to use it to edit camera paths. Camera paths can also be combined with USD exports from Open Brush, to exactly recreate how the camera moved through the scene.

If you want to render a camera path from the command line directly, rather than using the batch file detailed above, you can use the following:

```
Openbrush.exe --renderCameraPath <path/to/camerpath.usda> <path/to/sketchfile.tilt>
```

### Changing Eye Scale on ODS 360 videos

When you render an ODS video, you may find things like the floor is missing, or parts of your objects get clipped off.

The reason this happens is that it’s often easier to scale down your sketch to make it easy to move the camera when you take your original video, but when you render out an ODS file, the objects are too close to the camera.

To fix this, you can change a value in the .usda file. Open it up in your favorite text editor and look at around line 30 for:

```
uniform float eyeScale = 1
```

If you reduce this value, the render will feel bigger, and the camera is less likely to clip with parts of your sketch. A good value to try out is:

```
uniform float eyeScale = 0.1
```

Then you can just try re-rendering with the batch file.

{% hint style="info" %}
If you're rendering stereoscopic video then reducing eyeScale will reduce the strength of the stereo effect as well. It's often better to scale your scene in this case.
{% endhint %}

### Exporting 360 videos / Offline Video Rendering

Videos can be rendered ‘offline’ faster and at a much higher resolution and framerate than using the internal Multicam tool

1. **Editing Open Brush cfg file**
2. Go to C:\Documents\Open Brush\Open Brush.cfg
3. Under "Video" add the flag "SaveCameraPath": true,
4. Save Open Brush.cfg
5. **Camera Setup**
6. Load the sketch you would like to render
7. Find a good spot from which you would like to capture your 360 video
8. Be sure to look around in all directions to make sure no objects are too close to the point of capture
9. Save your sketch
10. Record your video by moving camera or keeping camera stationary
11. After saving, exit Open Brush
12. **Rendering**\
    \*\*\*\*Note: When you create a video from inside Open Brush using the Camera tool with configuration "SaveCameraPath" flag set to _true_, Tilt Brush will create a Windows batch file alongside the video (In Documents\Open Brush\Videos) that you can run to re-render the video at a higher resolution
13. Go to C:\Documents\Open Brush\Videos . There should be .usda, .bat and video file which corresponds to the .tilt file
14. Double click on .bat file
15. If you run that batch file a command window will appear giving you several options for re-rendering your video:\
    \
    ![](<../.gitbook/assets/2 (1).png>)\
    \
    Press a number to get whichever format you prefer. It will then launch Open Brush, which will reload your sketch, and re-render the video. Once it is done, Open Brush will exit. As rendering at higher quality tends to affect the framerate, it is suggested that you do not wear your headset while this process completes.
16. Once the render is complete, it will pop open the “VRVideos” folder which should contain an video file with your stereo render.
17. **Converting into 360 video** \
    \
    1\. [Download the 360° Video Metadata app](https://support.google.com/youtube/answer/6178631?hl=en) for [Mac](https://github.com/google/spatial-media/releases/download/v2.0/360.Video.Metadata.Tool.mac.zip) or [Windows](https://github.com/google/spatial-media/releases/tag/v2.0). The dialog should look like this:\
    \
    ![](<../.gitbook/assets/3 (1).png>) \
    \
    2\. Un-zip the file, then open the 360 Video Metadata app. If you're on a Mac, you may need to right-click the app and then click Open. \
    3\. Select the video file. \
    4\. Select the checkbox for My Video is stereoscopic 3D (top/bottom layout) \
    5\. Click Inject Metadata \
    6\. Enter a name for the file that will be created. \
    7\. Save the file. A new file will be created automatically in the same location as the original file.
18. **Uploading to Youtube**
    1. Upload the new “injected” video file to YouTube
    2. Note that it takes YouTube some additional time to process 360 videos, until this process is finished, you may see the raw over/under and the “View in Cardboard” option will not be available.
    3. Once processing is done, you should see an icon when viewing the video on your phone, indicating that it’s ready to be viewed in VR.

## Quest and Other Non-PC Devices

Currently Open Brush doesn't support recording video directly on the headset. There are two main ways to work around this limitation.

### Option 1: Draw a Camera Path in the headset and render on a computer

Standalone headsets like the Quest have the same Camera Path Tool as PC VR - the difference is that the record button is currently disabled. However any paths you create are saved with your sketch and can be copied to a PC or Mac and rendered there. The PC doesn't need to be a VR-capable PC - you can run Open Brush in a mode that doesn't require a VR headset.

There is an example script you can use to help you generate the video.&#x20;

1. Launch Open Brush at least once to ensure the correct folders are created in your Documents folder.
2. Copy the sketch from your headset to the Open Brush/Sketches folder on your PC
3. Ensure Open Brush is running and then switch to your web browser and enter this url: [http://localhost:40074/help/](http://localhost:40074/help/)

<figure><img src="../.gitbook/assets/image (48).png" alt=""><figcaption></figcaption></figure>

4.  Click on the Example Scripts link and then click on **/examplescripts/record\_camera\_path.html**\


    <figure><img src="../.gitbook/assets/image (49).png" alt=""><figcaption></figcaption></figure>
5. Click browse and select the sketch you copied from the Quest earlier
6. Click "Go"
7. This will generate the video as if you'd recorded the path inside the headset

### Option 2: Use native Quest video recording feature

This allows you to record what you can see and record by moving through the scene. The quality will be lower than the above method and you may need to ensure that UI elements are hidden (The [Spectator script ](open-brush-api/)can help with this)
