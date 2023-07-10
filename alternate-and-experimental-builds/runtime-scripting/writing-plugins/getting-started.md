# Getting Started

## Choosing an Editor

In theory you could use any text editor to write and edit your plugin scripts: Notepad on Windows or TextEdit on MacOS.

However an editor that is designed for writing code has many useful features to make your life easier. You might already have a favourite editor. However one thing to consider it whether it supports Lua properly - and also if allows you to use the autocomplete hints that we automatically provide.

These hints will allow your editor to suggest method names, offer tooltips for paramters and even spot errors in the type of parameters you're passing to methods or functions.

## Autocomplete and Intellisense Using EmmyLua&#x20;

If you look in your Plugins folder there is a subfolder called LuaModules and in there are a few commonly used libraries. However one file is different. It contains empty stubs for all available API methods and properties along with special comments that can be used by the EmmyLua plugin to give you working autocomplete, intellisense and tooltips. This makes writing scripts and finding bugs much easier.

EmmyLua has been tested in Visual Studio Code, WebStorm (and other Jetbrains editors) but it also claims to support any editor that uses the language server protocol (LSP) standard. If you don't already have a passionate attachment to a particular editor then you should probably start with [Visual Studio Code](https://code.visualstudio.com/)

[EmmyLua for Visual Studio Code](https://marketplace.visualstudio.com/items?itemName=tangzx.emmylua)

[EmmyLua for Jetbrains](https://plugins.jetbrains.com/plugin/9768-emmylua)

[EmmyLua Docs](https://emmylua.github.io/)
