# Brushes

Open Brush comes with a wide selection of brushes and there are even more if you switch on [Experimental Mode](../experimental-mode.md). But be warned that the experimental brushes can be more problemmatic if you need to export to other apps. See the docs on the [Unity Toolkit/SDK](../open-brush-unity-sdk.md) and on [Exporting ](../exporting-open-brush-sketches-to-other-apps/)for more information. We plan to move many of the experimental brushes into normal mode when we're satisfied that they work everywhere the regular brushes work.

## Customizing Brushes

There are currently three ways to add and modify brushes:

1. This requires you to learn your way around Unity a little bit: [https://lachlansleight.medium.com/customizing-tilt-brush-6e9a63bd5425](https://steamcommunity.com/linkfilter/?url=https://lachlansleight.medium.com/customizing-tilt-brush-6e9a63bd5425) Brushes created this way won't export to other apps correctly without manual shader editing. Using them in other Unity projects via the [Unity SDK](../open-brush-unity-sdk.md) is possible but requires manual editing of the Unity shaders and materials.
2. Tim Aidley has created a feature that allows editing of brushes via config files: [https://github.com/TimAidley/open-brush/blob/features/simple-brushes/Docs/UserBrushes.md](https://steamcommunity.com/linkfilter/?url=https://github.com/TimAidley/open-brush/blob/features/simple-brushes/Docs/UserBrushes.md)
3. Developed on top of Tim's work is a work-in-progress feature that allows editing brushes directly in VR. However it's experimental, doesn't currently work on the native Quest version of Open Brush and has had only a very small amount of testing so far: [Brush Editing](../../alternate-and-experimental-builds/brush-editing.md)

This last method will eventually be the recommended method moving forwards and we hope to fully support these custom brushes in the Unity SDK and for exporting..

{% content-ref url="brush-list.md" %}
[brush-list.md](brush-list.md)
{% endcontent-ref %}
