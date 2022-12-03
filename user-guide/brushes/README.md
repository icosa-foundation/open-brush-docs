# Brushes

The main release of Open Brush as a wide selection of brushes. The [main experimental build](../../alternate-and-experimental-builds/main-experimental-build.md) has even more but be warned that they may not export correctly. Furthermore a few of the experimental brushes are currently buggy and will be removed soon (Holiday Tree, Candy Cane, Plait and Snowflake).

## Creating your own brushes

There are currently three ways to add and modify brushes:

1. This requires you to learn your way around Unity a little bit: [https://lachlansleight.medium.com/customizing-tilt-brush-6e9a63bd5425](https://steamcommunity.com/linkfilter/?url=https://lachlansleight.medium.com/customizing-tilt-brush-6e9a63bd5425) Brushes created this way won't export to other apps correctly without manual shader editing. Using them in other Unity projects via the [Unity SDK](../open-brush-unity-sdk.md) is possible but requires manual editing of the Unity shaders and materials.
2. Tim Aidley created a feature that allows editing of brushes via config files: [https://github.com/TimAidley/open-brush/blob/features/simple-brushes/Docs/UserBrushes.md](https://steamcommunity.com/linkfilter/?url=https://github.com/TimAidley/open-brush/blob/features/simple-brushes/Docs/UserBrushes.md)
3. Developed on top of Tim's work is a work in progress feature that allows editing brushes directly in VR. However it's experimental, doesn't currently work on the native Quest version of Open Brush and has had only a very small amount of testing so far: [https://docs.openbrush.app/alternate-and-experimental-builds/brush-editing](https://docs.openbrush.app/alternate-and-experimental-builds/brush-editing)&#x20;

This last method will be the recommended method moving forwards and we hope to fully support export and the Unity SDK.&#x20;

{% content-ref url="brush-list.md" %}
[brush-list.md](brush-list.md)
{% endcontent-ref %}
