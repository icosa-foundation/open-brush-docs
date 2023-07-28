# Feature: Improved GLTF Importer

#### Status: Very nearly ready with a few remaining bugs

## Download

This feature has now been merged into the [beta release](open-brush-beta-docs.md)

### What does it do?

The current GLTF import in Open Brush fails to open many valid GLTF files. This feature build replaces it with a much more up to date library [GLTFast](https://github.com/atteneder/glTFast)

### What's it good for?

Importing a wide range of GLTF files into Open Brush including animated models.

### How do I install it?

Download a build for your headset from the link above and unzip it. You can run the Windows exe directly. To install the Quest apk use SideQuest: [https://uploadvr.com/sideloading-quest-how-to/](https://uploadvr.com/sideloading-quest-how-to/)

### How do I use it?

Just import gltf models as you normally would.

### Known Issues

* When you load a sketch containing GLTF models, the models do not appear. The workaround is to open the sketch a second time.
* Some models are improperly sized in the 3D model panel and obscure other models.
* There's no way to control the animation for animated models and selecting them can sometimes be tricky.

## How do I get help

Come over to the [Open Brush Discord](https://discord.com/invite/fS69VdFXpk) and chat to me ( @andybak#5425 ). I'm on UK time (currently UTC+1) but I check in fairly regularly.

### Can I see it in action?

Not yet.
