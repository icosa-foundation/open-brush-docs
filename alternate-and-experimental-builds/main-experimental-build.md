# "Experimental Mode" Builds

## What are Experimental Mode Builds?

Google had various stages for a new feature to make it's way into Tilt Brush. It would start off available only to a closed group of testers and developers. After that it might be added to the [Labs panel ](../user-guide/check-out-labs-or-experimental-features.md)in the official release. And finally it would be released as an officially supported feature.

When Tilt Brush was released as open source, we discovered all the features that had been previously available to a select few and we made a build available for everyone to try. We call this the "Experimental Build" although other people are also working on new features so there's now actually several experimental builds - but if you see a mention of THE Experimental Build then it's most likely referring to this one.

Other builds may be "experimental mode" and add their own features on top of these. Or they may offer you the choice of a build with and without "Experimental Mode" enabled.

### Compatibility Issues

The main thing to be aware of with "Experimental Mode" builds is the new brushes. Any sketch you save that contains these new brushes might have problems when you export it to another piece of software or load it in a non-experimental version of Open Brush.

We are testing a fix for exporting sketches that use experimental brushes. The brush strokes won't look correct but at least the export will work. Try it out by downloading the versions below and please come and tell us if it works or doesn't for you:

#### Test Builds to fix export for experimental brushes:

* [Quest](https://nightly.link/IxxyXR/open-brush/workflows/build/features%2Fexperimental-brushes-export/Oculus%20Quest%20Experimental.zip)
* [Rift](https://nightly.link/IxxyXR/open-brush/workflows/build/features%2Fexperimental-brushes-export/Windows%20Rift%20Experimental.zip)
* [SteamVR](https://nightly.link/IxxyXR/open-brush/workflows/build/features%2Fexperimental-brushes-export/Windows%20SteamVR%20Experimental.zip)

We also have a special version of [Open Brush Unity SDK](../user-guide/open-brush-unity-sdk.md) with support for most of the experimental brushes: [https://github.com/IxxyXR/open-brush-toolkit/tree/experimental-brushes](https://github.com/IxxyXR/open-brush-toolkit/tree/experimental-brushes)

### Bugs and Incomplete Features

There are four brushes in experimental mode that are interesting but very buggy. The main problem is that you can't use "Undo" after drawing with them. They are: Brain, Snowflake, Tree and Candy Cane.

### Downloading and installing the main Experimental Build

This build is the pre-release version of Open Brush and may contain untested new features. See the [release ](../release-history.md)history for more information on new and upcoming features.

In addition it has "Experimental Mode" enabled. See below for a list of features that are enabled in this mode. If you want a pre-release build without "experimental mode" enabled then see [Pre-release builds](broken-reference)

#### Steam

1. Install Open Brush normally in Steam and open the Open Brush properties in your Steam Library:

![](<../.gitbook/assets/image (10).png>)

2\. Choose the pre-release experimental branch from the "beta" tab:

![](<../.gitbook/assets/image (12) (1) (1) (1) (1).png>)

#### Itch.io

You can also download the main Experimental Build on [Itch.io](https://openbrush.itch.io/openbrush)

To launch it on a PC just download, unzip, and run the main executable file.

If you want to install it to a standalone Oculus Quest then you'll need to [sideload it](https://sidequestvr.com/setup-howto).

## What Features are there that are only in this build?

### Experimental Brushes

There are [50 new brushes](main-experimental-build.md#experimental-brushes) - although some are buggy and some actually duplicate existing brushes and were included for technical reasons. That still leaves plenty of cool new brushes to play with. But be warned - they don't work properly when you export your sketches. Which is why they are still in "experimental mode" only.

### 3D Model Import

This is for PC only (not Quest). As well as importing still images and videos you can import 3D models (fbx/obj/gltf). The importer is rather fussy and doesn't work reliably. We'd like to improve this and move it to the main release.

### Drafting

Combined with the new Drafting Brush, this gives an easy way to sketch out guides and construction lines for yourself. This button quickly toggles them on and off so you can see them while you paint and then quickly see how your sketch will appear to others when you export it without the drafting lines.

### Double Mirror

If the mirror tool is great, then a double mirror is twice as great. Instant 4-way symmetry. ( If you're interested in painting with more complex symmetry then you can also check out the experimental [Polyhedra and Symmetry build](broken-reference) )

### Rebrush Tool

A more powerful version of the Recolor Tool. This enables you to replace the brush used on existing strokes with any other brush of your choice.

### Save Selected Strokes

This will save the currently selected strokes to your Local Media Library so you can use them in other sketches like you can imported 3d models.

### Profiling

Not as interesting as it sounds. Mainly useful for developers testing changes or new hardware.
