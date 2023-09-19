# BuildingOpenBrush

## Android

### Audio

* TiltBrush uses GoogleVR audio regardless of platform, and if the platform SDK supplies audio.
  * `AudioManager` uses `GvrAudioSource`.
  * \(GoogleVR is deprecated\)\[[http://docs.unity3d.com/Packages/com.unity.xr.googlevr.android@2.0/changelog/CHANGELOG.html](http://docs.unity3d.com/Packages/com.unity.xr.googlevr.android@2.0/changelog/CHANGELOG.html)\] to be removed in 2020.1.
  * WORK: Investigate replacement. See [Issue 148](https://github.com/icosa-foundation/open-brush/issues/148).

## XR

The `UnityEditor.XR.Management` plugin offers to remove legacy packages. See `class XRLegacyUninstaller`.

```text
private static List<string> k_PackagesToBeRemoved = new List<string>(){
            "com.unity.xr.googlevr.android",
            "com.unity.xr.googlevr.ios",
            "com.unity.xr.oculus.android",
            "com.unity.xr.oculus.standalone",
            "com.unity.xr.openvr.standalone",
            "com.unity.xr.windowsmr.metro",
        };
```

