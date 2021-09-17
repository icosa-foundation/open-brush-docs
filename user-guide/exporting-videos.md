# Exporting Videos

### Rendering ‘Offline’ videos

When you create a video from inside Tilt Brush using the Camera tool, Tilt Brush will create a Windows batch file alongside the video \(In Documents\Tilt Brush\Videos\) that you can run to re-render the video at a higher resolution. For example:

 _Untitled\_13\_00.mp4_

 _Untitled\_13\_00.HQ\_Render.bat_

Double-clicking the ".bat" batch file will give you several options for re-rendering your video:

![](../.gitbook/assets/1%20%281%29.png)

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
15. If you run that batch file a command window will appear giving you several options for re-rendering your video:![](../.gitbook/assets/2%20%281%29.png)Press a number to get whichever format you prefer. It will then launch Tilt Brush, which will reload your sketch, and re-render the video. Once it is done, Tilt Brush will exit. As rendering at higher quality tends to affect the framerate, it is suggested that you do not wear your headset while this process completes.
16. Once the render is complete, it will pop open the “VRVideos” folder which should contain an video file with your stereo render.
17.  **Converting into 360 video**
    1. [Download the 360° Video Metadata app](https://support.google.com/youtube/answer/6178631?hl=en) for [Mac](https://github.com/google/spatial-media/releases/download/v2.0/360.Video.Metadata.Tool.mac.zip) or [Windows](https://github.com/google/spatial-media/releases/tag/v2.0). The dialog should look like this:![](../.gitbook/assets/3%20%281%29.png)
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

