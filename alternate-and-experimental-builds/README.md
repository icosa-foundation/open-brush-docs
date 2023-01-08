# Pre-release, Alternate, and Experimental Builds

## Beta Release

Whenever any new change is added to Open Brush, before it's released to the various stores and sites, there is an engineering "pre-release" version available. If you'd like to help beta test new versions, you can get these builds as soon as the new code is added (generally within 20 minutes!). Windows (SteamVR) and Quest/Quest 2 versions are built automatically which you can get from the [Github releases page](https://github.com/icosa-gallery/open-brush/releases). Versions of the form "vX.Y.0" are official releases, whereas versions that do not end in .0 are made available for testing purposes only, with no guarantees as to their quality.

These builds share a save location with the official Open Brush release, but can be installed alongside the formal version. The Oculus build, like all sideloaded content, will be listed in "Unknown Sources", and will have the word "Github" appended to the name (with a different package name as well) to differentiate it from the official release). These builds are available for both the "regular" and the "experimental mode" described below.

Because of a big change currently in progress there are actually two beta versions at the moment. The regular one:

{% content-ref url="open-brush-beta-docs.md" %}
[open-brush-beta-docs.md](open-brush-beta-docs.md)
{% endcontent-ref %}

The original VR framework in Unity is deprecated and all new apps are built using the Unity XR Plugin framework. We intend to switch to this going forward and we need to to support newer Oculus features and other headsets such as the Vive Focus:

{% content-ref url="old-or-completed-feature-builds/xr-framework-experimental-build.md" %}
[xr-framework-experimental-build.md](old-or-completed-feature-builds/xr-framework-experimental-build.md)
{% endcontent-ref %}

## "Experimental Mode" Build

Whilst Open Brush was still Tilt Brush, the original team had a bunch of features and brushes they felt weren't quite ready to be released in the official app. As soon as Tilt Brush was made open source, everyone immediately leapt on these features with great excitement.

{% content-ref url="main-experimental-build.md" %}
[main-experimental-build.md](main-experimental-build.md)
{% endcontent-ref %}

## Feature Builds

Generally - when someone is working on a new feature, they create a new build to work on until the features is ready to merge back into the main release.

You can download these builds to try out new features. Sometimes the sketches you create with these builds won't open correctly in the main release (but not always) and like all pre-release versions these builds might contain bugs or incomplete features.

{% content-ref url="3d-shapes.md" %}
[3d-shapes.md](3d-shapes.md)
{% endcontent-ref %}

{% content-ref url="brush-editing.md" %}
[brush-editing.md](brush-editing.md)
{% endcontent-ref %}

{% content-ref url="new-monoscopic-mode.md" %}
[new-monoscopic-mode.md](new-monoscopic-mode.md)
{% endcontent-ref %}

{% content-ref url="old-or-completed-feature-builds/" %}
[old-or-completed-feature-builds](old-or-completed-feature-builds/)
{% endcontent-ref %}



## Multibrush (Tilt Brush fork)

Multibrush is mostly an [experimental mode build](main-experimental-build.md) with two extra features:

1\. Post-processing effects that change the appearance of your entire scene.\
2\. Multiuser support: multiple people can paint at the same time and use voice chat in realtime.

Multibrush does not currently include most of the features that we have added to Open Brush since release.

{% embed url="https://blog.rendever.com/2021/02/04/news-multibrush-by-rendever-now-available-on-sidequest-providing-artists-with-a-collaborative-tool-in-virtual-reality" %}

## Silk Brush (Tilt Brush Fork)

{% embed url="https://msub2.github.io/silk-brush/" %}

Tilt Brush. Running in a browser!

### TutoriVR

{% embed url="https://www.tkbala.com/tutorivr" %}

A VR-embedded tutorial system that supplements video tutorials with 3D and contextual aids directly in the user's VR environment.

