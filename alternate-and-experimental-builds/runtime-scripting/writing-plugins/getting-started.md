# Getting Started

## Choosing an Editor

In theory you could use any text editor to write and edit your plugin scripts: Notepad on Windows or TextEdit on MacOS.

However an editor that is designed for writing code has many useful features to make your life easier. You might already have a favourite editor. However one thing to consider it whether it supports Lua properly - and also if allows you to use the autocomplete hints that we automatically provide.

These hints will allow your editor to suggest method names, offer tooltips for parameters and even spot errors in the types you're using in your code.

If you're not sure then the simplest thing to do is just use Visual Studio Code:

{% embed url="https://code.visualstudio.com/download" %}

## Autocomplete and Intellisense for Lua scripts&#x20;

If you look in your Plugins folder there is a subfolder called LuaModules and in there are a few commonly used libraries, that will provide some useful features.&#x20;

However one file is different. It contains empty definitions for all available API methods and properties along with special comments that can be used by the EmmyLua plugin to give you working autocomplete, intellisense and tooltips. This makes writing scripts and finding bugs much easier.

If you're using Visual Studio Code then follow these steps:\
\
1\. Launch the Plugins build of Open Brush at least once to create the correct plugins folder.

2. Launch Visual Studio Code and open this folder: Documents\Open Brush\Plugins
3. Click on the button on the left that shows the Extensions sidebar: \
   ![](<../../../.gitbook/assets/image (1).png>)
4. Search for "Lua" and look for the sumneko extension:

<div align="left">

<figure><img src="../../../.gitbook/assets/image (1) (1).png" alt="" width="343"><figcaption></figcaption></figure>

</div>

5. Click to install it and wait for it to finish installing
6. Click the small cog icon and then open the Extension Settings:\
   ![](<../../../.gitbook/assets/image (2).png>)
7. Optionally you can hide a lot of spurious warnings by disabling "lowercase-global" warnings under **Lua> Diagnostics: Disable:** \
   ![](../../../.gitbook/assets/image.png)\
   (In our plugins we're using upper and lower case initial letters to distinguish your stuff from the API supplied-things but standard lua style is to use it to differentiate local from global. Don't worry for now...)
8. Scroll down to **Lua> Workspace: Library** and add "LuaModules"\
   ![](<../../../.gitbook/assets/image (3).png>)



If you create a new file called PointerScript.Test.lua and start typing:

```lua
function Start()
    print (App.
```

As soon as you type the period you should see a list of suggestions that match the "App" part:

![](<../../../.gitbook/assets/image (4).png>)

If not - check you've followed all the steps above.\
If it worked then we can move on...\


## Next Steps

Now you've got a code editor installed and a plugin to help make things easier, you can move on to tweaking the example plugins and maybe even writing your own plugins from scratch.
