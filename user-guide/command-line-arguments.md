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

`--ForceViewOnly` starts Open Brush with painting and editing tools hidden; it works with or without XR. Add `--DisableXrMode` when you specifically want the flat-screen viewer. `--EnableMonoscopicMode` starts the non-VR painting and debugging interface instead. See [View-only Mode](view-only-mode.md) and [Monoscopic Mode](monoscopic-mode.md) for the difference between the modes.



