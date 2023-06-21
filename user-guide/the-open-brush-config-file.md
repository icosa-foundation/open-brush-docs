# The Open Brush config file

The Open Brush config file can be used to tweak various options for advanced users. A blank Open Brush.cfg file will be created in the Open Brush folder on application startup if one does not exist.

Example SteamVR / Rift path: **C:\Users\\**_\<username>_**\Documents\Open Brush\Open Brush.cfg**.

On an Oculus Quest, you can find this file in **/sdcard/Open Brush**. You can use either adb or the SideQuest file viewer to access this file.

Contents of the default _Open Brush.cfg:_

```
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

Sample contents of a _Open Brush.cfg_ with various fields filled in:

```
{
   "User":{
      "Author":"Tiltasaurus"
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

[How to get an OAuth key for Twitch.](https://twitchapps.com/tokengen/)

[How to find your YouTube Channel ID.](https://support.google.com/youtube/answer/3250431)

### Valid Config file Settings

1. **PostEffectsOnCapture:** (true | false) This setting determines whether post-processing effects will be applied to captured images or videos. When set to true, effects will be applied; when set to false, they will not.
2. **ShowWatermark**: (true | false) This setting controls the visibility of the Open Brush watermark on exported images and videos. When set to true, the watermark will be visible; when set to false, it will be hidden.
3. **ShowHeadset**: (true | false) This setting determines whether the user's VR headset will be visible in the final exported images or videos. When set to true, the headset will be shown; when set to false, it will not.
4. **UnlockScale**: (true | false) This setting allows users to scale their artwork beyond the default limits. When set to true, users can scale their artwork to larger sizes; when set to false, scaling will be limited to the default range.
5. **SnapshotWidth**: (1 - some reasonably large number) This setting controls the width (in pixels) of exported images. Users can specify a value between 1 and a reasonably large number to set the desired image width.
6. **SnapshotHeight**: (1 - some reasonably large number) This setting controls the height (in pixels) of exported images. Users can specify a value between 1 and a reasonably large number to set the desired image height.
7. **FOV**: (1 - 179) This setting determines the field of view (FOV) for the camera used during image or video capture. Users can specify a value between 1 and 179 degrees to set the desired FOV.
8. **DisableAudio**: (true | false) This setting allows users to disable audio playback within Open Brush. When set to true, audio playback will be disabled; when set to false, audio playback will function as normal.
9. **ExportBinaryFbx**: (true | false) This setting controls whether exported FBX files will be in binary format. When set to true, binary FBX files will be exported; when set to false, ASCII FBX files will be exported.
10. **ExportFbxVersion**: (FBX201600 | FBX201400 | FBX201300 | FBX2012 | FBX201100) This setting specifies the version of the FBX file format to be used when exporting 3D models. Users can choose from FBX201600, FBX201400, FBX201300, FBX2012, or FBX201100. If not specified in the config file, the default version is FBX201400. If users experience issues importing the FBX file into older software, they may need to select an older version.
11. **Encoder**: (h.264) This setting specifies the video codec used for encoding exported videos. Currently, the only supported codec is h.264.

### Setting config values from the command line

Any of the above settings in the Open Brush.cfg file can also be specified on the command line (not applicable to Quest users). The format is --Section.Setting \<value>. For example:

```
--Flags.ShowWatermark true

--Video.CameraSmoothing 0.99

--User.Author "Captain Open Brush"
```
