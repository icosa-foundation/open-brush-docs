# Differences between Open Brush and Tilt Brush

## Features Added to Open Brush

This section only lists features currently in the main release. There is also a [beta version ](alternate-and-experimental-builds/open-brush-beta-docs.md)with new features. There's also plenty more stuff in [experimental and alternate builds](alternate-and-experimental-builds/).

### Scripting & Extensibility

* [Plugin Scripting](user-guide/using-plugins/) - Create custom tools and modify painting behavior with Lua scripts
* [Scripting API](user-guide/open-brush-api/) - WebSocket and HTTP API support

### Import & Export

* [VOX File Import](release-history/v2.13.md#vox-file-import) - Import Magicavoxel .vox format files
* [Open Blocks Model Import](release-history/v2.13.md#import-open-blocks-models) - Import models from the sibling app Open Blocks
* [New GLTF Importer](user-guide/importing-images-videos-3d-models.md) - Based on GLTFast with support for animated 3D models
* [SVG Import](user-guide/importing-images-videos-3d-models.md) - Import SVG files as images or 3D meshes
* [Point Cloud Import](user-guide/importing-images-videos-3d-models.md#point-cloud-import)
* [360 Panorama Backgrounds](release-history/v2.4-prismatic.md#360-panorama-background-import) - Import jpeg, png, and HDR panoramas (including stereoscopic)
* [WebM Video Import](user-guide/importing-images-videos-3d-models.md#webm-video-import)
* [LATK export](https://lightningartist.org)
* [Folder Navigation UI](user-guide/folder-navigation.md) - Better organization of imported media
* [Splitting 3D Models](release-history/v2.13.md#splitting-3d-models) - Break apart imported models into separate components

### Painting & Drawing Tools

* [Lazy Input](user-guide/lazy-input.md)
* [Jitter](user-guide/repaint-tool.md#jitter)
* [Repaint Tool](user-guide/repaint-tool.md) - Change brush type, color, or size of existing strokes
* [Repaint Selection](user-guide/repaint-tool.md#repaint-selection) - Apply repaint tools to all selected strokes
* [Multi-Mirror](user-guide/multimirror.md) - Dozens of symmetry types with color variance control
* [Bimanual Input](user-guide/bimanual-input-and-revolver.md#bimanual-input)
* [The Revolver](user-guide/bimanual-input-and-revolver.md#revolver)
* [Passthrough Hull Brush](user-guide/platform-and-device-support.md#passthrough-hull-brush) - Paint with passthrough effects
* [Experimental Brushes](user-guide/experimental-mode.md)
* [Logitech MX Ink Integration](user-guide/logitech-mx-ink.md) - Support for Logitech MX Ink stylus

### Guides & Snapping

* [Grid and Angle Snapping](user-guide/grid-and-angle-snapping.md)
* [Enhanced Snap Settings](user-guide/using-the-open-brush-tools-quick-tools-and-menu-panels/extras-panel/snap-settings-panel.md#enhanced-snap-settings) - Snap axis toggles, snap to guides, snap selected objects
* [Guide Settings & Snapping to Guides](user-guide/using-the-open-brush-tools-quick-tools-and-menu-panels/extras-panel/snap-settings-panel.md#snap-to-guides)
* [Plane Guide](user-guide/using-the-open-brush-tools-quick-tools-and-menu-panels/extras-panel/guides-panel.md#plane-guide)
* [View Axis Unlocking](user-guide/world-axis-unlock.md)

### Selection & Transformation

* [Transform Panel](user-guide/using-the-open-brush-tools-quick-tools-and-menu-panels/extras-panel/transform-panel.md) - Axis locks, alignment tools, and precise positioning
* [Selection/Erase Filter](user-guide/selection-erase-filter.md)
* [Full Selection Tools on Quest/Standalone VR](user-guide/using-the-open-brush-tools-quick-tools-and-menu-panels/tools-panel/selection-options.md#selection-tools-on-queststandalone-vr) - "Select All" and "Invert Selection" now available
* [Erase Media Widgets](user-guide/using-the-open-brush-tools-quick-tools-and-menu-panels/tools-panel/selection-options.md#erase-media-widgets) - Use the erase tool on images, videos, and 3D models
* [Snip/Join Strokes](alternate-and-experimental-builds/old-or-completed-feature-builds/snip-tool.md)

### Organization & File Management

* [Layers](alternate-and-experimental-builds/old-or-completed-feature-builds/layers.md)
* [Saved Stroke Gallery](user-guide/importing-images-videos-3d-models.md) - Save and reuse selections of brush strokes
* [Merging Sketches](user-guide/merging-sketches.md)
* [Hiding Brushes with Brush Tags](user-guide/brushes/hiding-brushes-with-brush-tags.md)
* [Move selection to current layer](user-guide/using-the-open-brush-tools-quick-tools-and-menu-panels/tools-panel/selection-options.md#move-selection-to-layer)

### Video & Camera

* [Advanced Camera Tool](user-guide/exporting-videos/camera-tool-gifs-snapshots-video.md)
* [Camera Paths on All Headsets](user-guide/exporting-videos/camera-paths-tool.md) - Create and edit camera paths on standalone devices
* [Camera Path Rendering on All Devices](release-history/v2.13.md#camera-path-rendering-on-all-devices) - Render video frames on standalone headsets
* [Render Video on Any Computer](release-history/v2.4-prismatic.md#render-video-on-any-computer) - Use ffmpeg on Mac and PC to render videos
* [Webcam Viewer](release-history/v2.4-prismatic.md#webcam-viewer) - View webcam feed while working (PC VR only)

### Sharing & Publishing

* [Publish to Viverse](release-history/v2.13.md#publish-worlds-to-viverse) - Share sketches directly to Viverse 3D worlds
* [Icosa Gallery uploads](https://icosa.gallery)
* [Icosa Gallery Integration](user-guide/saving-and-sharing-your-open-brush-sketches.md#icosa-gallery-integration) - Browse and load sample sketches directly from Icosa Gallery

### User Interface

* [XR Keyboard](user-guide/xr-keyboard.md) - Built-in virtual keyboard for naming sketches and layers
* [Multiple Language Support](release-history/v2.4-prismatic.md#multiple-language-support) - French, Spanish, German, Chinese, Japanese, Korean
* [Switching hands](user-guide/switching-hands.md)
* [Reset to "First Time"](user-guide/using-the-open-brush-tools-quick-tools-and-menu-panels/the-admin-panel/settings.md#reset-to-first-time)

### Platform & Device Support

* [Support for More Headsets](user-guide/platform-and-device-support.md#supported-headsets) - Pico, Zapbox, and other OpenXR devices
* [Quest 1 Support](release-history/v2.4-prismatic.md#quest-1-support-is-back) - Full selection tool support restored
* [Audio Reactive Mode for Quest](release-history/v2.4-prismatic.md#audio-reactive-mode-for-quest) - Brushes animate to imported audio
* [Monoscopic Mode](user-guide/monoscopic-mode.md) - Run on non-VR devices
* [Flatscreen View Mode](release-history/v2.4-prismatic.md#flatscreen-view-mode) - Navigate sketches with keyboard, touch, or gamepad
* [Enhanced View-only Mode](release-history/v2.13.md#view-only-mode-improvements) - Improved navigation on non-VR devices with gamepad and touch support
* [Passthrough Mode with Room Scale](release-history/v2.4-prismatic.md#passthrough-room-scale) - Stable scene orientation relative to real space

### Multiplayer & Collaboration

* [Multiplayer Support](alternate-and-experimental-builds/multiplayer.md) - Collaborative sketching with multiple users

### Other Features & Improvements

* [LIV Support](https://www.liv.tv)
* [Oculus MRC fixes](user-guide/platform-and-device-support.md#oculus-mrc-fixes)
* [Fly Tool](user-guide/using-the-open-brush-tools-quick-tools-and-menu-panels/tools-panel/#fly-tool)
* [JSON exports include sketch metadata](user-guide/exporting-open-brush-sketches-to-other-apps/configuring-export.md#json-exports-include-sketch-metadata)
* [Precise slider control using thumb stick](user-guide/platform-and-device-support.md#precise-slider-control)

Bear in mind this gives a misleading impression of the amount of work that has been put in. There's been a ton of effort on things that don't result in user-visible features but will help ease future development. Special props to [@mikeage](https://github.com/mikeage) for the amazing automated build system.

