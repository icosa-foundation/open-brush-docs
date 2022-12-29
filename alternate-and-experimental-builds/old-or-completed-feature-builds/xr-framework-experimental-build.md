---
description: The future of Open Brush begins here!
cover: https://www.khronos.org/assets/uploads/apis/OpenXR-After_3.png
coverY: 23.641703377386197
---

# XR Framework Beta

**Status: Merged! Find this on the main** [**beta release**](../open-brush-beta-docs.md)**!**

We have been hard at work updating Open Brush to the latest version of Unity and it's new XR Framework. This will enable us to keep up to date with new features that are only available with modern VR SDKs such as hand tracking and passthrough. In addition it will make it much easier to support new platforms and devices moving forward.

As this is a big fundamental change in how Open Brush interacts with devices, we need your help testing our new builds before we release it generally.

### I want to help test! Where do I get the new build?

Thank you very much! Please join our [Discord ](https://discord.gg/W7NCEYnEfy)and give yourself the 'Beta Testers' role from our `#welcome-rules` channel (click the button!) to receive important updates about new builds. We're discussing this huge change in a dedicated channel, called `#unity-xr`. Come and say hi!\


:warning: Remember that this is a beta release, so if you do any important work with Open Brush, please back up your files! :warning:&#x20;

\
This section is very detailed per platform, so here's some quick links to your preferred version:\
\
[Windows via SteamVR (OpenXR)](xr-framework-experimental-build.md#windows-via-steamvr-openxr)\
[Oculus Quest](xr-framework-experimental-build.md#oculus-quest)\
[Oculus Desktop](xr-framework-experimental-build.md#oculus-desktop)\
\
Already set up? Jump to:\
[What should I be testing?](xr-framework-experimental-build.md#what-should-i-be-testing)\
[How do I report bugs?](xr-framework-experimental-build.md#how-do-i-report-bugs)

### Windows via SteamVR (OpenXR)

Our desktop build is now powered by OpenXR! To make it easy to access, we have added a new beta channel on Steam.

![Accessing Open Brush properties via Steam.](<../../.gitbook/assets/image (13) (1) (1) (1).png>)

First, grab Open Brush from the Steam store. Once you have added it to your library, right click on the listing and choose 'Properties...'

![The beta unlocks!](<../../.gitbook/assets/image (15) (1).png>)

Select 'Betas' from the sidebar. In the text box, add the access code: **`openbrushxrbeta` ** and click 'Check Code'. A blue banner will appear below, confirming your access!

![Selecting the beta branch after opting in.](<../../.gitbook/assets/image (17) (1).png>)

You can now access the openxr and openxr-experimental betas. select your desired beta from the dropdown and Steam will automatically install that version! The name of the game in your Steam library will be appended with \[openxr].

![Selecting the OpenXR Mode when launching Open Brush.](<../../.gitbook/assets/image (12) (1).png>)

When you click Launch from within Steam, make sure to select 'Launch Open Brush in OpenXR Mode'!

### Oculus Quest

We have created a special [SideQuest](https://side.quest) page for installation of the Quest beta. If you are already know what you're doing with SideQuest, proceed onwards! If you haven't used SideQuest before, please take some time to follow their [excellent guide](https://side.quest/setup-howto) on setting up your Quest for development builds.

{% embed url="https://sidequestvr.com/app/9538/beta-open-brush" %}
SideQuest page link for those that know what to do!
{% endembed %}

#### Easy Installer (Beta)

SideQuest have just released a new in-headset installer which you can find on the guide above! If you're using this method, simply search for 'Open Brush Beta' from within the SideQuest app to install the beta. From your app drawer, in the top right, there is a dropdown to filter types of apps. Select it, scroll to the bottom, and select 'Unknown Sources'. You will see an app called 'Open Brush (`feature_xr_v2`). Click it to begin testing!

![Open Brush (feature-xr-v2) in the Unknown sources section of the Quest app drawer.](<../../.gitbook/assets/image (13) (1).png>)

#### Advanced Installer

Make sure your Quest is connected to your device. In the SideQuest app on your computer, search for 'Open Brush Beta'. On the app page, click 'DOWNLOAD APP (SIDELOAD)'. The app will install!

![Searching for Open Brush Beta in SideQuest](<../../.gitbook/assets/image (16) (1).png>)

![Open Brush Beta page, highlighting the download app button.](<../../.gitbook/assets/image (12).png>)

In your headset, open the app drawer. In the top right, there is a dropdown to filter types of apps. Select it, scroll to the bottom, and select 'Unknown Sources'. You will see an app called 'Open Brush (`feature_xr_v2`). Click it to begin testing!

### Oculus Desktop

Due to the way the Oculus Desktop store versioning works, we can't automate builds without disrupting the main build! Instead, you can access a manual build from [Nightly Link](https://nightly.link/icosa-gallery/open-brush/workflows/build/feature%2Fxr\_v2).&#x20;

{% embed url="https://nightly.link/icosa-gallery/open-brush/workflows/build/feature%2Fxr_v2" %}

![nightly.link showing the various builds for xr\_v2](<../../.gitbook/assets/image (14) (1).png>)

Click the long link beside the name of the build you wish to use (i.e. Windows Rift). A quick reminder that Windows Rift is the build you want if you're using Quest linked to your PC!

#### Rift (Oculus Desktop)

![Setting Oculus as active XR Runtime](<../../.gitbook/assets/image (17).png>)

**Note: before you begin, you may need to set Oculus as your active XR Runtime.** this may appear as a banner on the Oculus Desktop app. Go to Settings, General and under 'OpenXR Runtime', click 'Set Oculus as Active'. You may need to restart your PC afterwards.\
\
Double click the downloaded zip file. Press the Extract all button, and unzip the folder to a known location. You may want to use your Desktop or Documents folder. Once unzipped, open the StandaloneWindows64-Oculus folder, and double click  'OpenBrush-featurexrvr2.exe' to run the program!\
\
Windows may scan the folder for viruses as it's an unknown folder, which will prevent the program launching until complete. This is perfectly normal, and the program will launch by itself once finished.

### What should I be testing?

In short, everything you can! The previous SDKs were woven throughout the fabric of the app, so our changes impacted a lot of features. We have [prepared a list](https://github.com/icosa-gallery/open-brush/issues/249) over on our GitHub with suggestions of things to test (anything already ticked is assumed to be working).

### How do I report bugs?

If you are a GitHub user, please feel free to add a comment to our [Issue #249](https://github.com/icosa-gallery/open-brush/issues/249) where we are keeping track of validation.\
\
Otherwise, please join our [Discord ](https://discord.gg/W7NCEYnEfy)if you haven't already and post a message in the `#unity-xr` channel, we'll log it on your behalf!

