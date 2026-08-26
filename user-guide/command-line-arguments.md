# Command Line Arguments

\(If you're not sure how to launch an app with command line arguments I found this tutorial via Google: [https://www.digitalcitizen.life/shortcut-arguments-parameters-windows/](https://www.digitalcitizen.life/shortcut-arguments-parameters-windows/) - suggestions for a better link gratefully received\)

Open Brush accepts the following command line arguments:

* --noQuickLoad
* --captureOds
* --outputPath odsOutputPath
* --outputPrefix odsOutputPrefix
* --preview
* --noCorrection
* --turnTable
* --numFrames
* --fps
* --export \(followed by full path to .tilt file\)
* --exportPath \(defaults to \[Open Brush folder\]/Exports
* -batchmode / -nographics
* --renderCameraPath
* --EnableMonoscopicMode
* --DisableXrMode
* --ForceViewOnly
* \(filename of .tilt file in Sketches folder to load automatically\)
* \(Any valid user config setting and value\)

`--DisableXrMode` starts Open Brush without XR. Add `--ForceViewOnly` to keep editing tools hidden and use the flat-screen sketch viewer. `--EnableMonoscopicMode` starts the non-VR painting and debugging interface instead. See [Using Open Brush without a VR headset](monoscopic-mode.md) for the difference between the modes.



