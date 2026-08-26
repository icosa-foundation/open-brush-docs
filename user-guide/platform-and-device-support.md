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
- Meta Quest 1, 2, 3, 3S, and Pro
- Pico Neo 3, 4, and 4 Pro
- Pico 4 Ultra
- Steam Frame
- Zapbox (mixed reality on mobile devices)

## Platform-Specific Features

### Meta Quest

The dedicated Quest build is the usual choice because it includes Meta-specific features such as passthrough. The generic Android OpenXR APK can also run on Quest through the standard OpenXR loader, but it does not include every feature provided by the dedicated Quest build.

### Passthrough Hull Brush

On supported Meta Quest and Zapbox builds, the experimental Passthrough Hull brush reveals the device's camera view through the area covered by a stroke.

1. Turn on [Experimental Brushes](experimental-mode.md).
2. Select the **Passthrough** environment in Open Brush.
3. Choose **Passthrough Hull** from the Brushes panel.
4. Paint the areas where you want the camera view to show through.

The brush only works in the Passthrough environment. Its depth interaction is limited: it can reveal passthrough through other brush geometry behind the stroke and may not compose as expected with transparent strokes.

Passthrough can also be used in [multiplayer rooms](multiplayer.md#passthrough-rooms). Each participant sees their own camera view behind the shared Open Brush scene.

#### Passthrough scene alignment

Open Brush locks scene movement by default when you enter the Passthrough environment so an accidental world-grab does not move the sketch away from the physical surroundings.

Open the Environment popup while Passthrough is selected to use its scene controls:

1. **Lock Scene Transform** prevents or allows world-grab movement.
2. **Reset Scene Transform** restores the scene's original position, rotation and scale.

Locking the transform only prevents movement inside Open Brush. Headset tracking and room setup still determine how accurately virtual content remains aligned with the physical space.

#### Passthrough boundary behaviour

On supported Meta Quest builds, Open Brush asks the headset to suppress its boundary display while the Passthrough environment is active and restores the normal boundary behaviour after leaving that environment. Passthrough does not remove the need to keep the physical play area clear.

### Pico

Open Brush is available from the [Pico Store](https://store-global.picoxr.com/global/detail/1/7246792261630050310). Formal GitHub releases also provide a Pico APK and a generic Android OpenXR APK; the generic OpenXR build can run on Pico without installing a custom OpenXR loader.

The separate Chinese Pico build omits cloud-account sign-in services that are unavailable in that region.

### Logitech MX Ink

Open Brush supports the [Logitech MX Ink](logitech-mx-ink.md) stylus on Meta Quest 2, 3 and 3S. It provides pressure-sensitive painting and can be used alongside the regular Touch controllers.

### Zapbox

The Zapbox build uses tracked Zapbox controller models and laser pointers for interacting with the Open Brush interface. Its first-use tutorial includes the Zapbox controls.

### Steam Frame

The Steam Frame build includes a native interaction profile, controller models and button highlighting for the Steam Frame controllers. Open Brush selects this profile automatically; no controller binding setup is normally required.

Web links opened inside Open Brush use the Steam overlay browser on Steam Frame. This includes forwarding for Open Brush's local API and device-login pages. If a link does not open, make sure the Steam overlay is enabled and retry it from Open Brush.

### Oculus MRC Fixes

Mixed Reality Capture (MRC) on Oculus/Meta headsets has been improved with various bug fixes, allowing better quality recordings of yourself interacting with your Open Brush sketches for streaming and content creation.

## Precise Slider Control

Supported advanced sliders can be adjusted without trying to hit an exact point on the slider:

1. Point at the slider so it has focus.
2. Move the painting controller's thumbstick left or right to decrease or increase the value in small steps.
3. Read the temporary value indicator on the controller model, then return the stick to its centre.

This is used by advanced option panels such as Multi Mirror and plugin parameters. It does not replace the normal pointing and trigger-drag interaction on sliders that do not support thumbstick adjustment.

## See Also

- [Monoscopic Mode](monoscopic-mode.md) - Running Open Brush on non-VR devices
- [Multiplayer](multiplayer.md) - Shared painting, passthrough rooms and colocation
- [Settings Panel](using-the-open-brush-tools-quick-tools-and-menu-panels/the-admin-panel/settings.md)
