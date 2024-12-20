# Previous Github Wiki

This wiki contains various information about [Tilt Brush](https://www.tiltbrush.com), and [Open Brush](https://github.com/icosa-foundation/open-brush). It is collated from discussions with the TB dev team and delving into the source code. If you would like to contribute information please add an issue to this project.

## Index

* About [Brushes](brushes.md). [Comparisons](comparison.md).
* [Building OpenBrush](buildingopenbrush.md).
* [Monoscopic Mode](monoscopicmode.md)
* [Pseudo Code](pseudocode.md).
* [GUI](userinterface.md).
* Unity [Burst Compiler](burstcompiler.md) info.
* Unity [XR Input](https://docs.unity3d.com/Manual/xr_input.html) manual.
  * [XR interaction toolkit](https://docs.unity3d.com/Packages/com.unity.xr.interaction.toolkit@1.0/manual/index.html) overview.

## Glossary

* **Canvas** is a local space coordinate system workspace for brushes. See "Room". Suffix "`_CS`" may be applied.
* **GeometryPool** stores mesh in C#-convenient format prior to being batched.
* **Knot** is a control point with some more data glommed on; it's a term that `GeometryBrush` invented.
* **Pressure** is user controlled adjustment to painting, e.g. trigger pull amount. Brush specific result.
* **Room** is global space coordinate system workspace for pointers. See "Canvas". Suffix "`_PS`" may be applied.

## Useful

* [Geometry3Sharp](https://github.com/gradientspace/geometry3Sharp) project.
* [Platform dependent compilation in Unity](https://docs.unity.cn/2019.4/Documentation/Manual/PlatformDependentCompilation.html).
* [Unity Burst compiler info](https://docs.unity3d.com/Packages/com.unity.burst@1.4/manual/docs/QuickStart.html).

## Interesting

* [Buckminster](https://github.com/pearswj/buckminster).
* [Gradient Space](https://www.gradientspace.com) - home of Geometry3Sharp.
* [HE\_Mesh](https://github.com/wblut/HE_Mesh) a Java library for creating and manipulating polygonal meshes. Aimed primarily at Processing.
* [Human pose tracking from single camera](https://github.com/XinArkh/VNect).
* [keijiro's effects](https://github.com/keijiro).
* [Soundstage VR](https://github.com/googlearchive/soundstagevr) music composition. [Demo](https://www.youtube.com/watch?v=q0nibydjajQ).
* [WebVR directory](https://webvr.directory) - lots of interesting web VR projects.
