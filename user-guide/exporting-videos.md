# Cameras and Exporting Video

{% hint style="info" %}
Quest and other Standalone Headset Users - exporting video directly from within Open Brush is currently only supported for PC VR only. See the [section below](exporting-videos.md#quest-and-other-non-pc-devices)
{% endhint %}

If you are using Open Brush on PC VR / SteamVR, there are three types of cameras available to you. If you are using a version of the software that is run directly on a stand-alone headset such as the Oculus Quest 2 or 3 headsets, then there are limitations on some video functions because standalone headsets cannot process the video without being tethered to a PC. Steam VR allows the PC’s processors to handle the heavy lifting that is required to record Video in VR. This can be done with either a wired or wireless connection between the PC and the headset.

The types of cameras available are:

·       [Cameras Tools](exporting-videos.md#the-cameras-tool-s)

·       [Spectator Camera](exporting-videos.md#the-spectator-camera)

·       [Camera Paths](exporting-videos.md#camera-paths)

### The Cameras Tool(s)

The Cameras Tool is a set of camera tools options that are available in both the Beginners and Advanced Palates.

<figure><img src="../.gitbook/assets/Carmeras Tool.png" alt=""><figcaption><p>The Cameras tool as seen from Beginner's Mode</p></figcaption></figure>

In the Beginner’s mode, the camera icon is a single function tool, opening the Cameras tool on your brush controller. The Cameras tool has these options:&#x20;

1\.       Auto-Gif

2\.       5 Second Gif

3\.       Snapshot

4\.       Video (not present in some versions of Open Brush)

The Cameras tools are all handheld and controlled with the brush controller where you will find the viewfinder and the record function. Using the thumbpad left and right shuffles through the four camera options. Clicking with the trigger initiates the process of recording in all options.&#x20;

The 5 Second Gif requires you to hold down the trigger for the 5 seconds.  You can release the trigger and repull it to stop and start from the same place in the 5 second timeline. The video function begins when you pull the trigger and continues until you pull it again to stop the recording.

The video function allows for a lot of control because you can move with 6 Degrees of Freedom through the scene limited only by your ability to control the direction, speed and orientation of the camera with your brush controller. This results in a handheld video, and the strengths and weaknesses of that approach are the same as real world handheld videography. It is hard to steady a camera being supported by your body.

Any videos created with any of the Cameras options will show up in the /Documents/Open Brush/Videos folder.

When switching to the Advanced Palate, the Cameras icon changes to be a multi-function button.  This is visually shown by a triangle on the lower right corner of the icon.&#x20;

<figure><img src="../.gitbook/assets/Cameras Icon in advanced mode with triangle.png" alt=""><figcaption><p>The Cameras Icon in the Advanced mode also has a sub-menu as indicated by the triangle in the lower right corner of the icon.</p></figcaption></figure>

To access the Cameras sub-menu do a click and hold.&#x20;

In the sub menu you have the option to go into a Camera Options menu.

<figure><img src="../.gitbook/assets/Camera Options.png" alt=""><figcaption><p>The Camera Options tool is available in the Cameras Sub-menu</p></figcaption></figure>

Within the Camera Options menu you can:

·       Turn the Open Brush Watermark on or off,

·       Adjust field of view and smoothing variables, and

·       Toggle Post Effects.

<figure><img src="../.gitbook/assets/Camera Options tools.png" alt=""><figcaption></figcaption></figure>

&#x20;

The series of images below demonstrates the differences in the captures with Field of View set to 140, 70 and 10.  The first image shows the capture with the Watermark turned on, in the rest it has been toggle off. Understanding how this affects the image the camera captures allows you to better control the way you capture the scene.

<figure><img src="../.gitbook/assets/FOV 140 Watermark On.jpg" alt=""><figcaption><p>Field of View set to 140 (wide angle), Watermark Toggled On</p></figcaption></figure>

<figure><img src="../.gitbook/assets/FOV 140 Watermark Off.jpg" alt=""><figcaption><p>Field of view set to 140, Watermark Off.</p></figcaption></figure>

<figure><img src="../.gitbook/assets/FOV 70.jpg" alt=""><figcaption><p>Field of View 70</p></figcaption></figure>

<figure><img src="../.gitbook/assets/FOV 10.jpg" alt=""><figcaption><p>Field of View 10</p></figcaption></figure>

The video below is a demonstration of the tools mentioned above. It was recorded as a screen capture utilizing the Spectator Camera.

{% embed url="https://youtu.be/C1mUcv5fl9k?si=0mbO3RxIDmGgfzD8" %}

### The Spectator Camera

The Spectator Camera does not record images or videos. Instead, it is used to send an image to a monitor. To capture images or videos, a screen capture function is required to record the video that is sent to the monitor. But the Spectator Camera is the only camera that shows the whole environment, including tools and camera paths.

There are four options with the spectator Camera:

Headset: Sends the video from the view of the headset. This is a view that moves along with your head, focusing on what is directly in front of your face as you wear the headset. This is a relatively jerky method of video capture because it moves every time your head moves.

Stationary: This allows you to place a camera inside the scene and it captures either the stationary image in front of the camera, or you can use this as a handheld camera by grabbing and using the tool as you would a tangible camera.

Figure 8:  This is the same camera as the stationary, but it makes a continuous figure 8 moving around a fixed point which is established by where you place the spectator camera.

Circle: Again, this is the same camera, but it revolves around the scene in a horizontal circle on a fixed path through or around the scene.

Because the Spectator Camera does not record, recording of video lies outside of the scope of this document in that it becomes a discussion of a hundred separate toolboxes. You will need screen capture software that allows system audio to be captured along with the video (if you want to include audio in the recording).&#x20;

Note: You may not be able to capture audio from some sources because of DMCA rules in place that allow listening but not recording. Recording of your microphone does not have this limitation. Recording a music video in Spectator Mode can present some challenges that were intentionally put in place to protect copyright. Understanding that there are protections in place to prevent recording of some audio sources is an important part of the planning and production process. You will not be able to record audio from platforms such as Spotify.  You can feed the audio into a scene and the audio responsive brushes will react, but there are digital blocks that prevent you from recording.

A strength of the spectator camera is that it is easy to establish your camera path because it is limited to the preprogrammed options (Stationary, Figure 8, and Circle). You can also use the stationary option as a handheld option and move the camera around the scene. &#x20;

Another strength of the spectator camera is that it shows the environment including tools, controls, headset and controllers. It can also provide the opportunity to record the scene as it is rendered, providing a stroke-by-stroke perspective of how the scene is created.

The weakness of the Spectator Camera is that it is limited to the preprogrammed options, and because recording with the Spectator Camera Option requires screen capture software that is not part of Open Brush.

The Field of View setting in the /Cameras/Camera Options tool does not affect the Spectator Camera. Rather, when establishing the Spectator Camera shot, you can visibly see lines that illustrate the capture field for all of the spectator Camera settings except headset.

### Camera Paths Tools

Camera Paths is an extremely important set of tools for Recording Video, or Virtual Cinematography in Open Brush. The tools are pretty basic, but learning to use them effectively and efficiently is the key to turning out high quality videos where you are in total control of how you capture the scene.

Camera Paths is a set of tools that allow you to control the way that a camera captures the scene as the camera travels along a path you create through the scene. This method gives you a great deal of control and flexibility in your approach to filming the scene. But, once you click the record button, all other functions are locked until it has completed filming the path. There is an option to stop the recording while it is in process, but you will lose the video that was in process if it does not complete the defined path.

<figure><img src="../.gitbook/assets/The Camera Paths tools.png" alt=""><figcaption><p>The Camera Paths Tool opens a separate Panel that contains the tools</p></figcaption></figure>

The tools you can use to manipulate the path include:

Add New Path Tool

<figure><img src="../.gitbook/assets/CP New Path Tool.png" alt=""><figcaption><p>You Must First Create a New Path before you can access the other Camera Paths Tools.</p></figcaption></figure>

This is the only option when you enter the Camera Paths Tools if there are not already established camera paths. To establish a path, you need to click the Add Anchor Point tool and then create a path consisting of 2 or more points. Once you have a path, additional tools become available to you.\


<figure><img src="../.gitbook/assets/Camera Paths Palate and tools.png" alt=""><figcaption><p>The Camera Paths Panel and tools once a path has been established.</p></figcaption></figure>

·       Select Path: allows you to choose which of the existing paths you want to work with.                     &#x20;

<figure><img src="../.gitbook/assets/CP Select Path.png" alt=""><figcaption><p>Select Path Tool</p></figcaption></figure>

·       Show Paths: Makes Paths Visible in the Sketch so they can be manipulated.

<figure><img src="../.gitbook/assets/CP Show paths.png" alt=""><figcaption><p>Show Paths Tool</p></figcaption></figure>

·       Delete Path: Allows you to delete an entire path.

<figure><img src="../.gitbook/assets/CP Delete Path tool.png" alt=""><figcaption><p>Delete Path Tool</p></figcaption></figure>

·       Record Path: After you have created and edited your path, this tool will launch the video recorder that will go through the entire path making a video record.  Videos will show up in the /Documents/Open Brush/Videos folder. Recording cannot be paused. Recording can be cancelled by clicking the X on the bush controller while it is in the recording process.

<figure><img src="../.gitbook/assets/CP record path tool.png" alt=""><figcaption><p>Record Path Tool</p></figcaption></figure>

·       New Anchor Point: Adds an additional anchor point to the path. If the anchor point is added at either end of a path, it will stay activated allowing you to add additional points to the path.&#x20;

<figure><img src="../.gitbook/assets/CP New Anchor Point.png" alt=""><figcaption><p>New Anchor Point Tool</p></figcaption></figure>

·       Delete Anchor Point: Deletes any controls form the timeline.  This includes anchor, direction, speed, and zoom points.&#x20;

<figure><img src="../.gitbook/assets/CP Delete Point tool.png" alt=""><figcaption><p>Delete Point Tool</p></figcaption></figure>

·       Camera Direction Point: Controls the Direction the camera is pointed at the point in the timeline where it is placed. This type of point interacts with previous direction pointsand the path to determine the transition between camera direction points creating a flowing camera direction instead of a jumping camera direction.

<figure><img src="../.gitbook/assets/CP Camera Direction Point.png" alt=""><figcaption><p>Camera Direction Point Tool</p></figcaption></figure>

·       Camera Speed Point: Provides values from .1 to 100 to control the speed the camera moves down the path at a given point. This type of point interacts with previous speed points and the path to determine the transitional speed between points.

<figure><img src="../.gitbook/assets/CP Camera Speed Points.png" alt=""><figcaption><p>Camera Speed Point Tool</p></figcaption></figure>

·       Camera Zoom Point: Provides values from 10 to 140 to control the Field of View as the camera moves down the path at a given point. This type of point interacts with previous zoom points and the path to determine the transitional zoom between points.

<figure><img src="../.gitbook/assets/CP Camera Zoom Point.png" alt=""><figcaption><p>Camera Zoom Point Tool </p></figcaption></figure>

The strength of the Camera Path is its flexibility. The weakness is that you are locked into the defined path once recording has started. The camera paths tool is not accessible until a sketch is fully rendered, and once the recording has started, all other tools are locked until the recording has completed. That means it cannot capture the rendering of a scene, so all videos start with a fully rendered scene.

Creating a camera path can be quite time consuming. In addition to the various tools, you need to work with the way that adding a point to the timeline can affect the elements ahead of and behind it on the path.  Effective use of the Camera Paths requires the use of a lot of control points (each tool creates a control point when it is attached to a location on the camera path).  The flexibility you can achieve comes at the cost of spending time learning each of the tools and how they interact with other points on the timeline.

### Settings that affect video render

There are several useful settings you can change in the [config file](exporting-videos.md#the-camera-tool).

Below is a sample Open Brush.cfg file showing the fields related to Video that can be used to control the video capture / render.

{

&#x20; "User": {

"Author":"Kevin W. Tharp, LLC"

&#x20; },

&#x20; "Video": {

&#x20;     "Resolution":1920,

&#x20;     "OfflineResolution":1920,

&#x20;     "FPS":30,

&#x20;     "OfflineFPS":30,

&#x20;     "ContainerType":"mp4",

&#x20;     "CameraSmoothing":0.98,

&#x20;     "Encoder":"h.264",

&#x20;     "SaveCameraPath":true,

&#x20;     "FOV":129

&#x20; },

&#x20; "Flags": {

&#x20;     "PostEffectsOnCapture":true,

&#x20;     "ShowWatermark":false,

&#x20;     "ShowHeadset":false,

&#x20;     "ShowControllers":true,

&#x20;     "DisableAudio":false

&#x20; },

&#x20;One of the Key variables is the number of frames you see per second (FPS).  In virtual reality itself, this is the refresh rate.  The refresh rate is important to the Virtual Reality experience but does not affect the virtual cinematography because videos of the scene are rendered at a fixed FPS rate.  The number of frames per second affects the memory as each frame is processed in the memory. Using a lower FPS for recording impacts the memory by requiring less memory.&#x20;

When you are recording live, this can be a significant impact because the system renders the scene twice, once for each eye, so that you can see it in VR. Then you add the recording on top of that and you are really taxing the memory available for your display/recording function. If you run out of memory, the VR experience gets glitchy or fails completely.  A glitchy VR experience is a bad thing, because it can lead rapidly to VR sickness and poor quality or failed recording.

To minimize this impact, [offline rendering](exporting-videos.md#rendering-offline-videos) allows your system to redirect some of those memory resources to the function of recording the video.  It does this by running a batch process. While the batch process requires the sketch to load in the headset, it disables all the interaction and dedicates all the memory to rendering and recording the scene.  As such, it is recommended that you not wear the headset while batch rendering is going on, as the display may be glitchy or inconsistent as it is not prioritized during the offline recording process.



### Rendering ‘Offline’ videos

When you create a video from inside Open Brush using the Camera tool and you've set "SaveCameraPath" to True in the [Open Brush config file](the-open-brush-config-file.md) - Open Brush will create a Windows batch file alongside the video (In Documents\Open Brush\Videos) that you can run to re-render the video at a higher resolution. For example:

_Untitled\_13\_00.mp4_

_Untitled\_13\_00.HQ\_Render.bat_

Double-clicking the ".bat" batch file will give you several options for re-rendering your video:

![](<../.gitbook/assets/1 (1).png>)

Press the number corresponding to the format you prefer. It will then launch Open Brush, which will reload your sketch and render the video. Once it is done, Open Brush will exit. As rendering at higher quality tends to affect the framerate, it is suggested that you do not wear your headset until this process completes.

“No Quick Load” option (#6) will forego quick loading of the sketch and will force it to load at normal speed. It is recommended that the time spent recording should exceed the normal loading time of the sketch or else the video may end before the sketch completes loading.

### Video Camera Paths

Note: Video Camera Paths is not the same thing as the [Camera Paths Tools](exporting-videos.md#camera-paths). Video Camera Paths track a camera through a scene and save the spatial data for offline rendering, whereas the Camera Paths Tools create a path that a video will take through a scene while recording.

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
2. Copy the sketch from your headset to the Open Brush/Sketches folder on your PC or Mac
3. If your sketch contains any images, videos or 3d models that appear in your video then copy those from the Quest's Media Library folder to the equivalent location on your PC or Mac.
4. Ensure you have got Open Brush running on the PC or Mac. Switch to your web browser and enter this address: [http://localhost:40074/help/](http://localhost:40074/help/)

<figure><img src="../.gitbook/assets/image (48).png" alt=""><figcaption></figcaption></figure>

4.  Click on the Example Scripts link and then click on **/examplescripts/record\_camera\_path.html**\


    <figure><img src="../.gitbook/assets/image (49).png" alt=""><figcaption></figcaption></figure>
5. Click browse and select the sketch you copied from the Quest earlier
6. Click "Go"
7. This will generate the video as if you'd recorded the path inside the headset

### Option 2: Use native Quest video recording feature

This allows you to record what you can see and record by moving through the scene. The quality will be lower than the above method and you may need to ensure that UI elements are hidden (The [Spectator script ](open-brush-api/)can help with this)
