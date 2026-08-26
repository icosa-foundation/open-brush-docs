# Platform and Device Support

Open Brush supports a wide range of VR headsets and platforms beyond the original Tilt Brush.

## Supported Headsets

Open Brush works on many more devices than Tilt Brush, including:

### PC VR
- HTC Vive / Vive Pro / Vive Cosmos
- Valve Index
- Oculus Rift / Rift S
- Meta Quest (via Link cable or Air Link)
- Windows Mixed Reality headsets
- HP Reverb G2
- Pimax headsets
- Any OpenXR-compatible PC VR headset

### Standalone VR
- Meta Quest 1, 2, 3, and Pro
- Pico Neo 3, 4, and 4 Pro
- Pico 4 Ultra
- Steam Frame
- Zapbox (mixed reality on mobile devices)

## Platform-Specific Features

### Passthrough Hull Brush

On headsets that support passthrough (Meta Quest, Pico), you can use the Passthrough Hull Brush to paint with passthrough effects. This brush shows the real world through your painted strokes, creating mixed reality effects.

To use it:
1. Enable passthrough mode in your headset settings or Open Brush
2. Select the Hull brush or compatible brush
3. Look for passthrough options in the brush settings

This allows you to blend your VR creations with the real world, creating unique mixed reality artwork.

Passthrough can also be used in [multiplayer rooms](multiplayer.md#passthrough-rooms). Each participant sees their own camera view behind the shared Open Brush scene.

### Steam Frame

The Steam Frame build includes a native interaction profile, controller models and button highlighting for the Steam Frame controllers. Open Brush selects this profile automatically; no controller binding setup is normally required.

Web links opened inside Open Brush use the Steam overlay browser on Steam Frame. This includes forwarding for Open Brush's local API and device-login pages. If a link does not open, make sure the Steam overlay is enabled and retry it from Open Brush.

### Oculus MRC Fixes

Mixed Reality Capture (MRC) on Oculus/Meta headsets has been improved with various bug fixes, allowing better quality recordings of yourself interacting with your Open Brush sketches for streaming and content creation.

## Precise Slider Control

On all platforms, you can use the thumbstick for fine control when adjusting sliders:

- **Normal movement**: Swipe or move the thumbstick for regular slider adjustment
- **Precise control**: Hold the thumbstick in position for slower, more precise adjustments
- Works on brush size, color values, and all other slider controls

This is particularly useful for:
- Fine-tuning exact color values
- Setting precise brush sizes
- Adjusting settings that need careful calibration

## See Also

- [Monoscopic Mode](monoscopic-mode.md) - Running Open Brush on non-VR devices
- [Multiplayer](multiplayer.md) - Shared painting, passthrough rooms and colocation
- [Settings Panel](using-the-open-brush-tools-quick-tools-and-menu-panels/the-admin-panel/settings.md)
