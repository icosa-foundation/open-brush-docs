# Feature: Plugin Scripting

#### Status: Mostly working and lots of fun to play with.

## Download

* [Oculus Quest 1](https://nightly.link/IxxyXR/open-brush/workflows/build/experiments%2Fmoonsharp/Oculus%20Quest%20%281%29.zip)
* [Oculus Quest 2 or 3](https://nightly.link/IxxyXR/open-brush/workflows/build/experiments%2Fmoonsharp/Oculus%20Quest%20%281%29.zip)
* [Oculus PC VR ](https://nightly.link/IxxyXR/open-brush/workflows/build/experiments%2Fmoonsharp/Windows%20Rift.zip)(Rift, Quest via Link cable...)
* [SteamVR and other PC VR](https://nightly.link/IxxyXR/open-brush/workflows/build/experiments%2Fmoonsharp/Windows%20OpenXR.zip)(Vive, Index, Reverb...)
* [Other Builds](https://nightly.link/IxxyXR/open-brush/workflows/build/experiments%2Fmoonsharp) (Pico, Pimax etc)
* [Code](https://github.com/IxxyXR/open-brush/tree/experiments/moonsharp)

### What does it do?

Unlike the existing [OpenBrush API](../../user-guide/open-brush-api/), plugin scripting is designed to run small scripts that directly modify the behaviour of various features while you are actually using them. For example a script might move the pointer as you are painting or add new strokes in response to your actions.

### What's it good for?

Changing the way Open Brush responds to user actions. Adding new mirror modes or creating a new custom brush tool.

### How do I install it?

[Download](./#download) a build for your headset from the link above and unzip it. You can run the Windows exe directly. To install the Quest apk use SideQuest: [https://uploadvr.com/sideloading-quest-how-to/](https://uploadvr.com/sideloading-quest-how-to/)

### How do I use it?

See [Using Plugins](using-plugins.md)

### How do I write my own plugin scripts?

See [Writing Plugins](writing-plugins/)

### Known Issues

Some API commands are untested. Please report bugs on the plugins and scripting channel on Discord. There's lots more I want to do with this including scripted 3d object creation, better UI for parameters (different input widgets etc).

## How do I get help

Come over to the [Open Brush Discord](https://discord.com/invite/fS69VdFXpk) and chat to me ( @andybak#5425 ). I'm on UK time but I check in fairly regularly.

### Can I see it in action?

{% embed url="https://www.youtube.com/watch?v=7YxjNvCY8ak" %}
