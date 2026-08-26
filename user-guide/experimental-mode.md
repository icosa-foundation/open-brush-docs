# Experimental Brushes

## Turning on Experimental Brushes

![](<../.gitbook/assets/image-061.png>)

Open the [Settings Panel](using-the-open-brush-tools-quick-tools-and-menu-panels/the-admin-panel/settings.md) and select **Experimental Mode**. The extra brushes appear immediately; you do not need to restart Open Brush. Select the button again to hide them.

The switch only controls which brushes appear in the Brushes panel. Open Brush keeps every brush definition loaded, so a sketch or multiplayer stroke that uses an experimental brush still displays when Experimental Mode is off.

See the [list of Experimental Brushes](brushes/experimental-brushes.md). Some duplicate existing brushes for technical reasons, and some may not export correctly, which is why they remain experimental.

### Compatibility Issues

Any sketch you save that contains these new brushes may not look correct when you export it to other Unity projects using the [Open Brush SDK](open-brush-unity-sdk.md)

We are currently working on a new Unity Toolkit that has support for all the experimental brushes in conjunction with the [new glb export format](exporting-open-brush-sketches-to-other-apps/configuring-export.md#choosing-between-the-new-and-old-gltf-formats)

## What was Experimental Mode?

{% hint style="info" %}
Some features that used to require experimental mode have been made part of normal mode. The only remaining difference in experimental mode is the brushes. There is also no longer a separate build for experimental mode but we do have some [experimental feature builds](../alternate-and-experimental-builds/) you can download.
{% endhint %}

Google had various stages for a new feature to make its way into Tilt Brush. It would start off available only to a closed group of testers and developers. After that it might be added to the [Labs panel](check-out-labs-or-experimental-features.md) in the official release. Finally, it would be released as an officially supported feature.

We have merged all those features into the main version now - so there's no need for a separate experimental mode aside from activating the extra set of brushes.
