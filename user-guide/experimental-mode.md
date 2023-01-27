# Experimental Mode

## What is Experimental Mode?

Google had various stages for a new feature to make it's way into Tilt Brush. It would start off available only to a closed group of testers and developers. After that it might be added to the [Labs panel ](check-out-labs-or-experimental-features.md)in the official release. And finally it would be released as an officially supported feature.

When Tilt Brush was released as open source, we discovered all the features that had been previously available to a select few and we made these available for everyone to try.

Note that using experimental mode used to require running a separate build of Open Brush (prior to 2.0). This is no longer the case - all versions can switch to experimental mode by going in to settings, hitting the toggle button and restarting the app.

### Turning on Experimental Mode

![](../.gitbook/assets/image.png)

Simply open up the Settings Panel, click the button and restart Open Brush.

### Compatibility Issues

The main thing to be aware of with "Experimental Mode" builds is the new brushes. Any sketch you save that contains these new brushes may not look correct when you export it to another piece of software or load it in a non-experimental version of Open Brush.

We also have a special version of [Open Brush Unity SDK](open-brush-unity-sdk.md) with support for most of the experimental brushes. See [the notes for the latest release](https://github.com/icosa-gallery/open-brush-toolkit/releases/latest).

## What Features are there that are only in this build?

### Experimental Brushes

There are [50 new brushes](experimental-mode.md#experimental-brushes) - although some duplicate existing brushes and were included for technical reasons. That still leaves plenty of cool new brushes to play with. But be warned - they might not look correct when you export your sketches. Which is why they are still in "experimental mode" only.

### 3D Model Import

This is for PC only (not Quest). As well as importing still images and videos you can import 3D models (fbx/obj/gltf). The importer is rather fussy and doesn't work reliably. We'd like to improve this and move it to the main release.

### Drafting

Combined with the new Drafting Brush, this gives an easy way to sketch out guides and construction lines for yourself. This button quickly toggles them on and off so you can see them while you paint and then quickly see how your sketch will appear to others when you export it without the drafting lines.

### Double Mirror

If the mirror tool is great, then a double mirror is twice as great. Instant 4-way symmetry. ( If you're interested in painting with more complex symmetry then you can also check out the [Multi-Mirror Feature build](../alternate-and-experimental-builds/multi-mirror.md))

### Save Selected Strokes

This will save the currently selected strokes to your Local Media Library so you can use them in other sketches like you can imported 3d models.

### Profiling

Not as interesting as it sounds. Mainly useful for developers testing changes or new hardware.
