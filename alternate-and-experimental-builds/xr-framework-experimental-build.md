---
description: The future of Open Brush begins here!
cover: https://www.khronos.org/assets/uploads/apis/OpenXR-After_3.png
coverY: 23.641703377386197
---

# 🚀 XR Framework Beta

We have been hard at work updating Open Brush to the latest version of Unity and it's new XR Framework. This will enable us to keep up to date with new features that are only available with modern VR SDKs such as hand tracking and passthrough. In addition it will make it much easier to support new platforms and devices moving forward.

As this is a big fundamental change in how Open Brush interacts with devices, we need your help testing our new builds before we release it generally.

### I want to help test! Where do I get the new build?

Thank you very much! Please join our [Discord ](https://discord.gg/W7NCEYnEfy)and give yourself the 'Beta Testers' role from our `#welcome-rules` channel (click the button!) to receive important updates about new builds. We're discussing this huge change in a dedicated channel, called `#unity-xr`. Come and say hi!\


:warning: Remember that this is a beta release, so if you do any important work with Open Brush, please back up your files! :warning:&#x20;

\
This section is very detailed per platform, so here's some quick links to your preferred version:\
\
[Windows via SteamVR (OpenXR)](xr-framework-experimental-build.md#windows-via-steamvr-openxr)\
[Oculus (Desktop and Quest)](xr-framework-experimental-build.md#oculus-desktop-and-quest)\
\
Already set up? Jump to:\
[What should I be testing?](xr-framework-experimental-build.md#what-should-i-be-testing)\
[How do I report bugs?](xr-framework-experimental-build.md#how-do-i-report-bugs)

### Windows via SteamVR (OpenXR)

Our desktop build is now powered by OpenXR! To make it easy to access, we have added a new beta channel on Steam.

![Accessing Open Brush properties via Steam.](<../.gitbook/assets/image (13) (1).png>)

First, grab Open Brush from the Steam store. Once you have added it to your library, right click on the listing and choose 'Properties...'

![The beta unlocks!](<../.gitbook/assets/image (15).png>)

Select 'Betas' from the sidebar. In the text box, add the access code: **`openbrushxrbeta` ** and click 'Check Code'. A blue banner will appear below, confirming your access!

![Selecting the beta branch after opting in.](<../.gitbook/assets/image (18).png>)

You can now access the openxr and openxr-experimental betas. select your desired beta from the dropdown and Steam will automatically install that version! The name of the game in your Steam library will be appended with \[openxr].

![Selecting the OpenXR Mode when launching Open Brush.](<../.gitbook/assets/image (12).png>)

When you click Launch from within Steam, make sure to select 'Launch Open Brush in OpenXR Mode'!

### Oculus (Desktop and Quest)

Due to the way the Oculus Desktop and Quest store versioning works, we can't automate builds without disrupting the main build! Instead, you can access a manual build from [Nightly Link](https://nightly.link/icosa-gallery/open-brush/workflows/build/feature%2Fxr\_v2).&#x20;

{% embed url="https://nightly.link/icosa-gallery/open-brush/workflows/build/feature%2Fxr_v2" %}

![nightly.link showing the various builds for xr\_v2](<../.gitbook/assets/image (14).png>)

Click the long link beside the name of the build you wish to use (i.e. Oculus Quest, Windows Rift). A quick reminder that Windows Rift is the build you want if you're using Quest linked to your PC!

#### Rift (Oculus Desktop)

![Setting Oculus as active XR Runtime](<../.gitbook/assets/image (17).png>)

**Note: before you begin, you may need to set Oculus as your active XR Runtime.** this may appear as a banner on the Oculus Desktop app. Go to Settings, General and under 'OpenXR Runtime', click 'Set Oculus as Active'. You may need to restart your PC afterwards.\
\
Double click the downloaded zip file. Press the Extract all button, and unzip the folder to a known location. You may want to use your Desktop or Documents folder. Once unzipped, open the StandaloneWindows64-Oculus folder, and double click  'OpenBrush-featurexrvr2.exe' to run the program!\
\
Windows may scan the folder for viruses as it's an unknown folder, which will prevent the program launching until complete. This is perfectly normal, and the program will launch by itself once finished.

#### Quest

We recommend using [SideQuest](https://side.quest) for installing our test builds. If you are already know what you're doing, proceed onwards! If you haven't used SideQuest before, please take some time to follow their [excellent guide](https://side.quest/setup-howto) (Advanced Installer) on setting up your Quest for development builds .

Double click the downloaded zip file. Press the Extract all button, and unzip the folder to a known location. You may want to use your Desktop or Documents folder.

**Sideloading the Quest build with SideQuest**

![](<../.gitbook/assets/image (13).png>)

Plug your Quest into your computer, and enable debugging ([Step 5 of SideQuest's guide](https://side.quest/setup-howto)). With SideQuest open, click the icon of a box with an arrow on it. This will open a windows prompt. Navigate to where you extracted your zip earlier. inside the 'Android-Oculus' folder, select and open the file called `com.Icosa.OpenBrush-featurexrv2.apk`. A banner will appear at the bottom of SideQuest, if it eventually says 'All tasks completed', you're good to go!\
\
In your headset, open the app drawer. In the top right, there is a dropdown to filter types of apps. Select it, scroll to the bottom, and select 'Unknown Sources'. You will see an app called 'Open Brush (`feature_xr_v2`)

### What should I be testing?

In short, everything you can! The previous SDKs were woven throughout the fabric of the app, so our changes impacted a lot of features. We have [prepared a list](https://github.com/icosa-gallery/open-brush/issues/249) over on our GitHub with suggestions of things to test (anything already ticked is assumed to be working).

### How do I report bugs?

If you are a GitHub user, please feel free to add a comment to our [Issue #249](https://github.com/icosa-gallery/open-brush/issues/249) where we are keeping track of validation.\
\
Otherwise, please join our [Discord ](https://discord.gg/W7NCEYnEfy)if you haven't already and post a message in the `#unity-xr` channel, we'll log it on your behalf!

