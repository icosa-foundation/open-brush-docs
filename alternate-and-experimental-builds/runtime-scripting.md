# Feature: Runtime Scripting

#### Status: Very experimental and buggy. 

## Download

* [Oculus Quest](https://nightly.link/IxxyXR/open-brush/workflows/build/experiments%2Fmoonsharp/Oculus%20Quest.zip)
* [Oculus PC VR ](https://nightly.link/IxxyXR/open-brush/workflows/build/experiments%2Fmoonsharp/Windows%20Rift.zip)(Rift, Quest via Link cable...)
* [SteamVR ](https://nightly.link/IxxyXR/open-brush/workflows/build/experiments%2Fmoonsharp/Windows%20OpenXR.zip)(Vive, Index, Reverb...)
* [Other Builds](https://nightly.link/IxxyXR/open-brush/workflows/build/experiments%2Fmoonsharp) (Pico, Pimax etc)
* [Code](https://github.com/IxxyXR/open-brush/tree/features/moonsharp)

### What does it do?

Unlike the existing OpenBrush API, runtime scripting is designed to run small scripts that directly modify
the behaviour of various features while you are actually using them. For example a script might move the
pointer as you are painting or add new strokes in response to your actions.

### What's it good for?

Changing the way Open Brush responds to user actions. Adding new mirror modes or creating a new custom brush tool.

### How do I install it?

Download a build for your headset from the link above and unzip it. You can run the Windows exe directly. To install the Quest apk use SideQuest: [https://uploadvr.com/sideloading-quest-how-to/](https://uploadvr.com/sideloading-quest-how-to/)

### How do I use it?

There are new buttons on the scipts panel that allow you to set
an active runtime script in (currently) one of three categories. All scripts are written in Lua and the type of script is determined by
the filename prefix. Name your scripts using the script type first followed by
the name of your script. Script types are:

1. Pointer Scripts: Changes the pointer position
2. Tool Scripts: draws entire strokes when you release the trigger
3. Symmetry Scripts: Creates and position additional pointers similar to how the mirror works

So here is a simple example of a Pointer Script. You would name the file something
like PointerScript.circles.lua:

    function Main()
        return {
            pointer.position.x + (math.sin(app.time * 15) * .25),
            pointer.position.y + (math.cos(app.time * 15) * .25),
            pointer.position.z
        }
    end


### Known Issues

Lots. It's an early proof of concept. Currently coordinates aren't correctly
converted to canvas space and there are probably many other issues.

## How do I get help

Come over to the [Open Brush Discord](https://discord.com/invite/fS69VdFXpk) and chat to me ( @andybak#5425 ). I'm on UK time (currently UTC+1) but I check in fairly regularly.

### Can I see it in action?

Not yet. 
