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

[How to get an OAuth key for Twitch.](https://twitchapps.com/tokengen/)

[How to find your YouTube Channel ID.](https://support.google.com/youtube/answer/3250431)

### Config file valid values

* PostEffectsOnCapture: true | false
* ShowWatermark: true | false
* ShowHeadset: true | false
* UnlockScale: true | false
* SnapshotWidth: 1 - some reasonably large number
* SnapshotHeight: 1 - some reasonably large number
* FOV: 1 - 179
* DisableAudio: true | false
* ExportBinaryFbx: true | false
* ExportFbxVersion: FBX201600 | FBX201400 | FBX201300 | FBX2012 | FBX201100\
  Unless set in the config file it will default to the 2014 version. If you have older software that has problems importing the FBX file try an older version.
* Encoder: h.264

### Setting config values from the command line

Any of the above settings in the Open Brush.cfg file can also be specified on the command line (not applicable to Quest users). The format is --Section.Setting \<value>. For example:

```
--Flags.ShowWatermark true

--Video.CameraSmoothing 0.99

--User.Author "Captain Tilt Brush"
```
