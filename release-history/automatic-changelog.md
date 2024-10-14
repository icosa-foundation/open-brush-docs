# Changelog since v2.2

[Full release details](https://github.com/icosa-foundation/open-brush/compare/v2.2...321325470e64ada8c362bc193277c904f0b16f9b)

## 🚀 Features

- Reset eye texture scale to 1 ([PR #430](https://github.com/icosa-foundation/open-brush/pull/430) by @mikeskydev)

- Feat: Internationalization (i18n) ([PR #419](https://github.com/icosa-foundation/open-brush/pull/419) by @mikeskydev)

- Add websocket support to the API server ([PR #336](https://github.com/icosa-foundation/open-brush/pull/336) by @andybak)

- Backport a simplified version of model import from EditableModels ([PR #446](https://github.com/icosa-foundation/open-brush/pull/446) by @andybak)

- Feature/xr keyboard ([PR #406](https://github.com/icosa-foundation/open-brush/pull/406) by @andybak)

- Grab widgets snap to guides where appropriate ([PR #450](https://github.com/icosa-foundation/open-brush/pull/450) by @andybak)

- Simple 2D viewing mode when no headset is present ([PR #421](https://github.com/icosa-foundation/open-brush/pull/421) by @andybak)

- Feature/repaint selected ([PR #409](https://github.com/icosa-foundation/open-brush/pull/409) by @andybak)

- Add Quest support to the pure Android XR build ([PR #469](https://github.com/icosa-foundation/open-brush/pull/469) by @mikeskydev)

- Use GLTFast as the primary load; fall back to the old code if it fails ([PR #278](https://github.com/icosa-foundation/open-brush/pull/278) by @andybak)

- Snap improvements and Transform panel ([PR #303](https://github.com/icosa-foundation/open-brush/pull/303) by @andybak)

- Feature/multi mirrors ([PR #345](https://github.com/icosa-foundation/open-brush/pull/345) by @andybak)

- Webcam (or other streaming video source) panel ([PR #477](https://github.com/icosa-foundation/open-brush/pull/477) by @andybak)

- Updated translations ([PR #483](https://github.com/icosa-foundation/open-brush/pull/483) by @andybak)

- Replace geometry intersection shader on Quest 1 ([PR #475](https://github.com/icosa-foundation/open-brush/pull/475) by @andybak)

- Opt-in large mesh support ([PR #492](https://github.com/icosa-foundation/open-brush/pull/492) by @andybak)

- Thumbstick changes AdvancedSlider value + visual feedback on controller model ([PR #494](https://github.com/icosa-foundation/open-brush/pull/494) by @andybak)

- Custom skybox ([PR #495](https://github.com/icosa-foundation/open-brush/pull/495) by @andybak)

- Layer Renaming via XR Keyboard ([PR #502](https://github.com/icosa-foundation/open-brush/pull/502) by @andybak)

- Support SVG for reference images ([PR #496](https://github.com/icosa-foundation/open-brush/pull/496) by @andybak)

- Add i18n for WMR, Pico 3, 4, Valve Index, and Vive ([PR #522](https://github.com/icosa-foundation/open-brush/pull/522) by @mikeskydev)

- Move selection to current layer ([PR #508](https://github.com/icosa-foundation/open-brush/pull/508) by @andybak)

- JSON exports also include the sketch metadata ([PR #528](https://github.com/icosa-foundation/open-brush/pull/528) by @andybak)

- [Pico] Add Chinese build, disable accounts ([PR #535](https://github.com/icosa-foundation/open-brush/pull/535) by @mikeskydev)

- feat: Language Selector ([PR #537](https://github.com/icosa-foundation/open-brush/pull/537) by @mikeskydev)

- Move from GVR Audio to Unity Audio ([PR #551](https://github.com/icosa-foundation/open-brush/pull/551) by @mikeskydev)

- Camera path workflow improvements ([PR #544](https://github.com/icosa-foundation/open-brush/pull/544) by @andybak)

- Allow distinct Quest vs Experimental panel config ([PR #549](https://github.com/icosa-foundation/open-brush/pull/549) by @andybak)

- Update Android SDK Target to v32 (Android 12); request MANAGE_EXTERNAL_STORAGE ([PR #563](https://github.com/icosa-foundation/open-brush/pull/563) by @mikeage)

- Base Multiplayer implementation ([PR #578](https://github.com/icosa-foundation/open-brush/pull/578) by @mikeskydev)

- Initial iOS Support ([PR #556](https://github.com/icosa-foundation/open-brush/pull/556) by @mikeskydev)

- Remove "Export all" shortcut ([PR #610](https://github.com/icosa-foundation/open-brush/pull/610) by @andybak)

- Feature/sketchfab improvements ([PR #611](https://github.com/icosa-foundation/open-brush/pull/611) by @andybak)

- UI for passthrough-related scene locking and resetting ([PR #612](https://github.com/icosa-foundation/open-brush/pull/612) by @andybak)

- Compliance with Meta Age Group API requirements ([PR #659](https://github.com/icosa-foundation/open-brush/pull/659) by @mikeskydev)

- Remove almost all uses of Experimental Mode, and combine Monoscopic into the main releases ([PR #674](https://github.com/icosa-foundation/open-brush/pull/674) by @andybak)

- Skip intro tutorial on Zapbox ([PR #681](https://github.com/icosa-foundation/open-brush/pull/681) by @mikeskydev)

- Allow generation of sphere with gesture on mobile ([PR #678](https://github.com/icosa-foundation/open-brush/pull/678) by @mikeskydev)

- Update lots of shaders to singlepass ([PR #677](https://github.com/icosa-foundation/open-brush/pull/677) by @mikeskydev)

- Preview spheres for 360 images ([PR #687](https://github.com/icosa-foundation/open-brush/pull/687) by @andybak)

- Pagination for layers UI ([PR #698](https://github.com/icosa-foundation/open-brush/pull/698) by @andybak)

- Folder navigation UI ([PR #689](https://github.com/icosa-foundation/open-brush/pull/689) by @andybak)

- Import/export improvements ([PR #573](https://github.com/icosa-foundation/open-brush/pull/573) by @andybak)

- Passthrough Hull Brush ([PR #613](https://github.com/icosa-foundation/open-brush/pull/613) by @andybak)

- UnityGLTF Shader Variants ([PR #714](https://github.com/icosa-foundation/open-brush/pull/714) by @andybak)

- Add Pico support to the generic OpenXR build ([PR #719](https://github.com/icosa-foundation/open-brush/pull/719) by @mikeskydev)

- Disable boundary when passthrough is active ([PR #735](https://github.com/icosa-foundation/open-brush/pull/735) by @andybak)

- Logitech MK Ink Integration ([PR #768](https://github.com/icosa-foundation/open-brush/pull/768) by @andybak)

- Allow profiler to use bundled sketches ([PR #769](https://github.com/icosa-foundation/open-brush/pull/769) by @andybak)


## 🎨 UI / UX

- Branding Refresh ([PR #662](https://github.com/icosa-foundation/open-brush/pull/662) by @mikeskydev)

- Fix Advanced Tools panel initial position ([PR #697](https://github.com/icosa-foundation/open-brush/pull/697) by @andybak)

- Damn panel spacing ([PR #702](https://github.com/icosa-foundation/open-brush/pull/702) by @andybak)


## 🐛 Fixes

- Temporarily disable snap grab icon ([PR #427](https://github.com/icosa-foundation/open-brush/pull/427) by @mikeskydev)

- Add a timeout to HttpListener to avoid loading for very long time when using China mobile hotspot ([PR #432](https://github.com/icosa-foundation/open-brush/pull/432) by @chengnay)

- Revert "Add a HttpListener timeout" ([PR #438](https://github.com/icosa-foundation/open-brush/pull/438) by @andybak)

- Temp remove system locale selector ([PR #436](https://github.com/icosa-foundation/open-brush/pull/436) by @mikeskydev)

- Quick fix for bug with images on layers sometimes breaking script loading ([PR #445](https://github.com/icosa-foundation/open-brush/pull/445) by @andybak)

- Add missing swipe hint to Multicam tool ([PR #455](https://github.com/icosa-foundation/open-brush/pull/455) by @andybak)

- Hotfix/widget layers offby1 ([PR #457](https://github.com/icosa-foundation/open-brush/pull/457) by @andybak)

- Multicam recording fix ([PR #464](https://github.com/icosa-foundation/open-brush/pull/464) by @andybak)

- Keyboard code improvements and bug fixes ([PR #467](https://github.com/icosa-foundation/open-brush/pull/467) by @andybak)

- Fix missing localization for a few promo popups ([PR #468](https://github.com/icosa-foundation/open-brush/pull/468) by @mikeskydev)

- Fix: Can't switch back to brush if selection tool picked immediately on launch ([PR #472](https://github.com/icosa-foundation/open-brush/pull/472) by @andybak)

- Fix bug with snap rotation on rotated canvas. ([PR #301](https://github.com/icosa-foundation/open-brush/pull/301) by @andybak)

- Load HttpListener in a background thread; fixes delay on China mobile hotspots ([PR #442](https://github.com/icosa-foundation/open-brush/pull/442) by @chengnay)

- Hotfix/selection snapping bugs ([PR #480](https://github.com/icosa-foundation/open-brush/pull/480) by @andybak)

- Update ReferenceImage.shader ([PR #481](https://github.com/icosa-foundation/open-brush/pull/481) by @andybak)

- Fix webcam breaking Oculus builds ([PR #484](https://github.com/icosa-foundation/open-brush/pull/484) by @andybak)

- Fix an NRE when hitting stop in editor ([PR #488](https://github.com/icosa-foundation/open-brush/pull/488) by @andybak)

- Fix issue where undo didn't respect symmetry mode ([PR #485](https://github.com/icosa-foundation/open-brush/pull/485) by @andybak)

- Fix wallpaper symmetry visualisations; they were offset +15 by mistake ([PR #490](https://github.com/icosa-foundation/open-brush/pull/490) by @andybak)

- Fix selection bug after cloning to multimirrors ([PR #487](https://github.com/icosa-foundation/open-brush/pull/487) by @andybak)

- Support per widget setting for two sided and set it to true when duplicating to multimirror ([PR #486](https://github.com/icosa-foundation/open-brush/pull/486) by @andybak)

- Use total pixels instead of max(width, height) for determining the maximum image size ([PR #500](https://github.com/icosa-foundation/open-brush/pull/500) by @andybak)

- fix selection tray collider ([PR #504](https://github.com/icosa-foundation/open-brush/pull/504) by @mikeskydev)

- Fix index truncation when exporting large glbs ([PR #517](https://github.com/icosa-foundation/open-brush/pull/517) by @andybak)

- Fixes 3D models being omitted from GLTF export since switch to GLTFast ([PR #526](https://github.com/icosa-foundation/open-brush/pull/526) by @andybak)

- Don't overwrite user colour unless we're in multimirror mode ([PR #529](https://github.com/icosa-foundation/open-brush/pull/529) by @andybak)

- Show state of Experimental Mode in the settings panel ([PR #532](https://github.com/icosa-foundation/open-brush/pull/532) by @andybak)

- hotfix experimental mode toggle ([PR #536](https://github.com/icosa-foundation/open-brush/pull/536) by @mikeskydev)

- Fix admin panel promo scale ([PR #533](https://github.com/icosa-foundation/open-brush/pull/533) by @mikeskydev)

- Minimal changes to fix editor on MacOS with Apple Silicon ([PR #530](https://github.com/icosa-foundation/open-brush/pull/530) by @andybak)

- Switch main scene sdk mode back to OpenXR ([PR #540](https://github.com/icosa-foundation/open-brush/pull/540) by @andybak)

- Remove passthrough prefab if not supported ([PR #538](https://github.com/icosa-foundation/open-brush/pull/538) by @mikeskydev)

- fix typo ([PR #542](https://github.com/icosa-foundation/open-brush/pull/542) by @andybak)

- Fix sketchbook context menu button being disabled for first button ([PR #543](https://github.com/icosa-foundation/open-brush/pull/543) by @andybak)

- Add in the changes that Unity autogenerates ([PR #553](https://github.com/icosa-foundation/open-brush/pull/553) by @andybak)

- Disable mobile bloom for camera snapshots ([PR #554](https://github.com/icosa-foundation/open-brush/pull/554) by @andybak)

- This seems to fix most bugs with duplicating to multimirror. ([PR #562](https://github.com/icosa-foundation/open-brush/pull/562) by @andybak)

- Fix exception when mirror-duplicating 3d Models or other non-flat widgets ([PR #564](https://github.com/icosa-foundation/open-brush/pull/564) by @andybak)

- Video batch file fix ([PR #565](https://github.com/icosa-foundation/open-brush/pull/565) by @andybak)

- Quest panel UI fixes ([PR #569](https://github.com/icosa-foundation/open-brush/pull/569) by @andybak)

- i18n Tidy up ([PR #576](https://github.com/icosa-foundation/open-brush/pull/576) by @mikeskydev)

- Fixes for Quest Accounts Panel showing Desktop version ([PR #575](https://github.com/icosa-foundation/open-brush/pull/575) by @andybak)

- Fix OAuth sign in on Android ([PR #577](https://github.com/icosa-foundation/open-brush/pull/577) by @mikeskydev)

- Fix Keijiro Tube and mark Race and Digital as "broken" (hidden by default) ([PR #579](https://github.com/icosa-foundation/open-brush/pull/579) by @andybak)

- Small i18n fixes ([PR #580](https://github.com/icosa-foundation/open-brush/pull/580) by @mikeskydev)

- Fix colours not being calculated when toggling multimirror. Cleanup some dead code ([PR #582](https://github.com/icosa-foundation/open-brush/pull/582) by @andybak)

- Fixes for Sketchbook and popup ([PR #587](https://github.com/icosa-foundation/open-brush/pull/587) by @andybak)

- Set TrackingOrigin to Stage ([PR #590](https://github.com/icosa-foundation/open-brush/pull/590) by @andybak)

- Update LeakyPen.shader ([PR #591](https://github.com/icosa-foundation/open-brush/pull/591) by @andybak)

- Correctly set model layer when loading a sketch ([PR #601](https://github.com/icosa-foundation/open-brush/pull/601) by @andybak)

- Fix positioning of layer rename keyboard ([PR #602](https://github.com/icosa-foundation/open-brush/pull/602) by @andybak)

- Don't allow selection of media widgets if not on the active layer ([PR #606](https://github.com/icosa-foundation/open-brush/pull/606) by @andybak)

- Reset orientation settings ([PR #609](https://github.com/icosa-foundation/open-brush/pull/609) by @mikeskydev)

- Fix Mobile advanced tools panel ([PR #617](https://github.com/icosa-foundation/open-brush/pull/617) by @andybak)

- Rename icon had vanished. Made a better one. ([PR #619](https://github.com/icosa-foundation/open-brush/pull/619) by @andybak)

- Fix select all and invert selection for non-main layers ([PR #628](https://github.com/icosa-foundation/open-brush/pull/628) by @andybak)

- Zapbox: Set to iPhone only for now ([PR #638](https://github.com/icosa-foundation/open-brush/pull/638) by @mikeskydev)

- [Zapbox] Temp set portrait orientation ([PR #642](https://github.com/icosa-foundation/open-brush/pull/642) by @mikeskydev)

- Correctly set the androidVersionCode on a build rerun ([PR #645](https://github.com/icosa-foundation/open-brush/pull/645) by @mikeage)

- Fix a few issues around layers and selections ([PR #646](https://github.com/icosa-foundation/open-brush/pull/646) by @andybak)

- Zapbox set up everything else ([PR #652](https://github.com/icosa-foundation/open-brush/pull/652) by @mikeskydev)

- Localization Fixes ([PR #655](https://github.com/icosa-foundation/open-brush/pull/655) by @mikeskydev)

- Remove broken custom drawer and fix corrupted value ([PR #653](https://github.com/icosa-foundation/open-brush/pull/653) by @andybak)

- Turn off MSAA for Zapbox ([PR #657](https://github.com/icosa-foundation/open-brush/pull/657) by @mikeskydev)

- Reset default environment. Passthrough only for Zapbox ([PR #660](https://github.com/icosa-foundation/open-brush/pull/660) by @mikeskydev)

- Reset default brush to Light ([PR #664](https://github.com/icosa-foundation/open-brush/pull/664) by @mikeskydev)

- Fix for broken camera preview due to logo change ([PR #667](https://github.com/icosa-foundation/open-brush/pull/667) by @andybak)

- Fix broken multimirror options popup. Hide Tiltosaurus button as it d… ([PR #680](https://github.com/icosa-foundation/open-brush/pull/680) by @andybak)

- Workaround for PCVR depth submission ([PR #685](https://github.com/icosa-foundation/open-brush/pull/685) by @mikeskydev)

- De-initialize XR Subsytems properly ([PR #695](https://github.com/icosa-foundation/open-brush/pull/695) by @andybak)

- Background image preview sphere labels ([PR #700](https://github.com/icosa-foundation/open-brush/pull/700) by @andybak)

- Fix stereo pano sphere preview ([PR #701](https://github.com/icosa-foundation/open-brush/pull/701) by @andybak)

- Enable file system watcher on mobile ([PR #704](https://github.com/icosa-foundation/open-brush/pull/704) by @andybak)

- UnityGltf import is meant to default to off ([PR #707](https://github.com/icosa-foundation/open-brush/pull/707) by @andybak)

- Fix issue where transparent brushes were invisible in Quest passthrough mode. ([PR #715](https://github.com/icosa-foundation/open-brush/pull/715) by @andybak)

- m_ColorSaturationMax had accidentally been set to 0 breaking color picker ([PR #724](https://github.com/icosa-foundation/open-brush/pull/724) by @andybak)

- Fix issue where images that are too large fail to load without any in… ([PR #722](https://github.com/icosa-foundation/open-brush/pull/722) by @eeropomell)

- Fix/improve image loading ([PR #729](https://github.com/icosa-foundation/open-brush/pull/729) by @eeropomell)

- Fix/quest sdk no boundary ([PR #737](https://github.com/icosa-foundation/open-brush/pull/737) by @andybak)

- Rename Quest Boundary Property ([PR #739](https://github.com/icosa-foundation/open-brush/pull/739) by @andybak)

- Fix input system errors when running in the editor ([PR #745](https://github.com/icosa-foundation/open-brush/pull/745) by @andybak)

- Shift the preview down so it doesn't overlap the hint ([PR #750](https://github.com/icosa-foundation/open-brush/pull/750) by @andybak)

- Fix background image seams by bypassing cache for now ([PR #749](https://github.com/icosa-foundation/open-brush/pull/749) by @andybak)

- Fix contextual boundary ([PR #761](https://github.com/icosa-foundation/open-brush/pull/761) by @andybak)

- Disable ENABLE_CONTEXTUAL_BOUNDARYLESS_APP as it's still experimental ([PR #762](https://github.com/icosa-foundation/open-brush/pull/762) by @andybak)


## 🛠️ Infrastructure

- (Re-enable) Free disk space before starting the Android build ([PR #454](https://github.com/icosa-foundation/open-brush/pull/454) by @mikeage)

- Merge v2.3 hotfix branch ([PR #459](https://github.com/icosa-foundation/open-brush/pull/459) by @mikeage)

- Correctly calculate changelogs commensurate on commencement of correctional commit ([PR #460](https://github.com/icosa-foundation/open-brush/pull/460) by @mikeage)

- Update steam deployment to remove superflous parameters ([PR #470](https://github.com/icosa-foundation/open-brush/pull/470) by @mikeage)

- Replace all references to icosa-gallery with icosa-foundation ([PR #506](https://github.com/icosa-foundation/open-brush/pull/506) by @mikeage)

- Save steam's config.vdf after each login to prevent logout ([PR #509](https://github.com/icosa-foundation/open-brush/pull/509) by @mikeage)

- Separate Rift and Quest upload ([PR #520](https://github.com/icosa-foundation/open-brush/pull/520) by @mikeage)

- Temporarily disable Mac CI builds because we don't have room for the cache it creates ([PR #523](https://github.com/icosa-foundation/open-brush/pull/523) by @mikeage)

- Remove some il2cpp files from Library before saving the cache ([PR #525](https://github.com/icosa-foundation/open-brush/pull/525) by @mikeage)

- Optimize package caching ([PR #527](https://github.com/icosa-foundation/open-brush/pull/527) by @mikeage)

- Fix Android cleanup job ([PR #541](https://github.com/icosa-foundation/open-brush/pull/541) by @mikeage)

- Enable the 'free extra space' step on Windows (and update the comments) ([PR #548](https://github.com/icosa-foundation/open-brush/pull/548) by @mikeage)

- Update game-ci build to v4 ([PR #557](https://github.com/icosa-foundation/open-brush/pull/557) by @mikeage)

- Only save a cache if it doesn't exist (overwrite doesn't work) ([PR #559](https://github.com/icosa-foundation/open-brush/pull/559) by @mikeage)

- Update license used for PRs from forks ([PR #560](https://github.com/icosa-foundation/open-brush/pull/560) by @mikeage)

- Enable masking of UNITY_PASSWORD ([PR #566](https://github.com/icosa-foundation/open-brush/pull/566) by @mikeage)

- [TEMP] Use a forked version of unity-builder that doesn't randomize UUIDs ([PR #570](https://github.com/icosa-foundation/open-brush/pull/570) by @mikeage)

- Update pre-commit with plugins that are compatible with python 3.12 ([PR #572](https://github.com/icosa-foundation/open-brush/pull/572) by @mikeage)

- Speed up the Disk Cleanup step ([PR #574](https://github.com/icosa-foundation/open-brush/pull/574) by @mikeage)

- Retry build on license acquisition failure ([PR #571](https://github.com/icosa-foundation/open-brush/pull/571) by @mikeage)

- Create a distinct Quest 1 build ([PR #585](https://github.com/icosa-foundation/open-brush/pull/585) by @mikeage)

- Separate Publishing Quest 1 and Quest 2+ into two jobs ([PR #586](https://github.com/icosa-foundation/open-brush/pull/586) by @mikeage)

- Change build directories to align with the unity-builder standard directories ([PR #593](https://github.com/icosa-foundation/open-brush/pull/593) by @mikeage)

- Catch exceptions in DoBuild() and print them in a way that Github will highlight ([PR #592](https://github.com/icosa-foundation/open-brush/pull/592) by @mikeage)

- Automatically create a new cache whenever the dependencies change ([PR #594](https://github.com/icosa-foundation/open-brush/pull/594) by @mikeage)

- Only save PackageCache if it's based on the unmodified packages-lock.json ([PR #595](https://github.com/icosa-foundation/open-brush/pull/595) by @mikeage)

- Don't include the _BackUpThisFolder_ButDontShipItWithYourGame folder in the artifacts ([PR #588](https://github.com/icosa-foundation/open-brush/pull/588) by @mikeage)

- Upload Pico builds automatically ([PR #597](https://github.com/icosa-foundation/open-brush/pull/597) by @mikeage)

- Update actions from Pico CI PR to v4 ([PR #603](https://github.com/icosa-foundation/open-brush/pull/603) by @mikeage)

- Don't include the changelog as notes for Pico (limit 1000 characters) ([PR #604](https://github.com/icosa-foundation/open-brush/pull/604) by @mikeage)

- Update the Steam release procedure ([PR #607](https://github.com/icosa-foundation/open-brush/pull/607) by @mikeage)

- Update pre-commit with python 3.12 fixes ([PR #624](https://github.com/icosa-foundation/open-brush/pull/624) by @mikeage)

- Improve pre-commit (dotnet, and remove a python warning) ([PR #627](https://github.com/icosa-foundation/open-brush/pull/627) by @mikeage)

- Create a DMG for Mac Monoscopic ([PR #625](https://github.com/icosa-foundation/open-brush/pull/625) by @mikeage)

- Upload Zapbox build to the App Store ([PR #629](https://github.com/icosa-foundation/open-brush/pull/629) by @mikeskydev)

- Fix (and tweak) fastlane issues ([PR #632](https://github.com/icosa-foundation/open-brush/pull/632) by @mikeage)

- Fix (again) the fastlane upload to the app store ([PR #635](https://github.com/icosa-foundation/open-brush/pull/635) by @mikeage)

- Add yamlfmt and enforce via pre-commit ([PR #636](https://github.com/icosa-foundation/open-brush/pull/636) by @mikeage)

- Use Mac OS 13 instead of latest (currently 12) when pushing iOS builds ([PR #637](https://github.com/icosa-foundation/open-brush/pull/637) by @mikeage)

- Select the fastlane lane based on whether it's a beta (testflight) or formal (app store) ([PR #634](https://github.com/icosa-foundation/open-brush/pull/634) by @mikeage)

- Add a workflow to export (encrypted) secrets  ([PR #639](https://github.com/icosa-foundation/open-brush/pull/639) by @mikeage)

- Move non-secret information from Github secrets to variables and rename ([PR #640](https://github.com/icosa-foundation/open-brush/pull/640) by @mikeage)

- Fix broken Dependabot PRs ([PR #650](https://github.com/icosa-foundation/open-brush/pull/650) by @mikeage)

- DMG Issues ([PR #658](https://github.com/icosa-foundation/open-brush/pull/658) by @mikeage)

- Don't push iOS Zapbox builds to the Apple Store; just to testflight (even for formal builds) ([PR #665](https://github.com/icosa-foundation/open-brush/pull/665) by @mikeage)

- Add Mac OS Monoscopic build to Steam ([PR #669](https://github.com/icosa-foundation/open-brush/pull/669) by @mikeage)

- Always specify --age-group for Oculus ([PR #670](https://github.com/icosa-foundation/open-brush/pull/670) by @mikeage)

- Update pre-commit, fix two pylint warnings ([PR #671](https://github.com/icosa-foundation/open-brush/pull/671) by @mikeage)

- Update GeneratedThirdPartyNotices.txt and make sure it stays in sync ([PR #673](https://github.com/icosa-foundation/open-brush/pull/673) by @mikeage)

- Fix automatic changelog page in the docs; update to the new (as of Jan 26th) path ([PR #675](https://github.com/icosa-foundation/open-brush/pull/675) by @mikeage)

- Merge the contents of the release-history directory instead of overwriting ([PR #676](https://github.com/icosa-foundation/open-brush/pull/676) by @mikeage)

- Minor formatting improvements ([PR #682](https://github.com/icosa-foundation/open-brush/pull/682) by @andybak)

- Release Linux Viewer/Standalone on Steam and Github ([PR #683](https://github.com/icosa-foundation/open-brush/pull/683) by @mikeage)

- Fix github release (typo in directory name) ([PR #684](https://github.com/icosa-foundation/open-brush/pull/684) by @mikeage)

- MacOS: sign all bundles, rather than listing them explicitly ([PR #706](https://github.com/icosa-foundation/open-brush/pull/706) by @mikeage)

- Add a section in the changelog for UI/UX PRs ([PR #703](https://github.com/icosa-foundation/open-brush/pull/703) by @mikeage)

- Add support for a [xCI BUILD DEV] (without the x) to build Development builds ([PR #712](https://github.com/icosa-foundation/open-brush/pull/712) by @mikeage)

- Fix artifact upload of development builds ([PR #713](https://github.com/icosa-foundation/open-brush/pull/713) by @mikeage)

- Update the (very rarely used) Unity License Test action ([PR #718](https://github.com/icosa-foundation/open-brush/pull/718) by @mikeage)

- Retry build on license failure; retry pre-commit on dotnet-format failure ([PR #716](https://github.com/icosa-foundation/open-brush/pull/716) by @mikeage)

- Run ovr-platform-util on Linux instead of Mac ([PR #727](https://github.com/icosa-foundation/open-brush/pull/727) by @mikeage)

- Fix Q1 upload ([PR #732](https://github.com/icosa-foundation/open-brush/pull/732) by @mikeage)

- Fix iOS builds after the unity upgrade ([PR #733](https://github.com/icosa-foundation/open-brush/pull/733) by @mikeage)

- Always run "Free Disk Space" on all platforms ([PR #734](https://github.com/icosa-foundation/open-brush/pull/734) by @mikeage)

- Revert "Run ovr-platform-util on Linux instead of Mac (#727)" ([PR #738](https://github.com/icosa-foundation/open-brush/pull/738) by @mikeage)

- Move the config.vdf secret (for Steam) to an Organization level secret ([PR #741](https://github.com/icosa-foundation/open-brush/pull/741) by @mikeage)

- Remove more unneeded files to free more disk space ([PR #753](https://github.com/icosa-foundation/open-brush/pull/753) by @mikeage)

- Run the build on 'main' periodically to keep the caches alive ([PR #754](https://github.com/icosa-foundation/open-brush/pull/754) by @mikeage)

- Fix missing version in DMG, Signed .app, and Steam upload ([PR #755](https://github.com/icosa-foundation/open-brush/pull/755) by @mikeage)

- gzip config.vdf before storing as a secret ([PR #771](https://github.com/icosa-foundation/open-brush/pull/771) by @mikeage)


## 📦 Dependencies / Maintenance

- Bump mikepenz/release-changelog-builder-action from 3.7.0 to 3.7.1 ([PR #428](https://github.com/icosa-foundation/open-brush/pull/428) by @dependabot[bot])

- Bump actions/setup-python from 4.5.0 to 4.6.0 ([PR #433](https://github.com/icosa-foundation/open-brush/pull/433) by @dependabot[bot])

- Bump mikepenz/release-changelog-builder-action from 3.7.1 to 3.7.2 ([PR #441](https://github.com/icosa-foundation/open-brush/pull/441) by @dependabot[bot])

- Bump actions/setup-python from 4.6.0 to 4.6.1 ([PR #448](https://github.com/icosa-foundation/open-brush/pull/448) by @dependabot[bot])

- Bump actions/setup-dotnet from 3.0.3 to 3.2.0 ([PR #451](https://github.com/icosa-foundation/open-brush/pull/451) by @dependabot[bot])

- Move user folder to Application.persistentDataPath ([PR #462](https://github.com/icosa-foundation/open-brush/pull/462) by @andybak)

- Bump actions/setup-python from 4.6.1 to 4.7.0 ([PR #466](https://github.com/icosa-foundation/open-brush/pull/466) by @dependabot[bot])

- Restore Steam password; it seems to be needed ([PR #471](https://github.com/icosa-foundation/open-brush/pull/471) by @mikeage)

- Revert "Move user folder to Application.persistentDataPath" ([PR #474](https://github.com/icosa-foundation/open-brush/pull/474) by @mikeskydev)

- Update mikepenz/release-changelog-builder-action to v4 ([PR #478](https://github.com/icosa-foundation/open-brush/pull/478) by @mikeage)

- Remove old vscode package ([PR #507](https://github.com/icosa-foundation/open-brush/pull/507) by @mikeskydev)

- Bump actions/checkout from 3 to 4 ([PR #518](https://github.com/icosa-foundation/open-brush/pull/518) by @dependabot[bot])

- Bump game-ci/unity-builder from 2 to 3 ([PR #505](https://github.com/icosa-foundation/open-brush/pull/505) by @dependabot[bot])

- Bump actions/setup-python from 4.7.0 to 4.7.1 ([PR #545](https://github.com/icosa-foundation/open-brush/pull/545) by @dependabot[bot])

- Fix corruption with Quest screenshots ([PR #552](https://github.com/icosa-foundation/open-brush/pull/552) by @andybak)

- Temp revert controller i18n ([PR #567](https://github.com/icosa-foundation/open-brush/pull/567) by @mikeskydev)

- Bump actions/setup-dotnet from 3.2.0 to 4.0.0 ([PR #581](https://github.com/icosa-foundation/open-brush/pull/581) by @dependabot[bot])

- Bump actions/setup-python from 4.7.1 to 4.8.0 ([PR #584](https://github.com/icosa-foundation/open-brush/pull/584) by @dependabot[bot])

- Bump actions/setup-python from 4.8.0 to 5.0.0 ([PR #589](https://github.com/icosa-foundation/open-brush/pull/589) by @dependabot[bot])

- Update artifact actions from v3 to v4 ([PR #600](https://github.com/icosa-foundation/open-brush/pull/600) by @mikeage)

- Bump actions/cache from 3 to 4 ([PR #614](https://github.com/icosa-foundation/open-brush/pull/614) by @dependabot[bot])

- Bump pre-commit/action from 3.0.0 to 3.0.1 ([PR #623](https://github.com/icosa-foundation/open-brush/pull/623) by @dependabot[bot])

- Bump CyberAndrii/setup-steamcmd from 1.1.5 to 1.2.0 ([PR #626](https://github.com/icosa-foundation/open-brush/pull/626) by @dependabot[bot])

- Bump softprops/action-gh-release from 1 to 2 ([PR #649](https://github.com/icosa-foundation/open-brush/pull/649) by @dependabot[bot])

- Bump actions/setup-python from 5.0.0 to 5.1.0 ([PR #668](https://github.com/icosa-foundation/open-brush/pull/668) by @dependabot[bot])

- Bump rexml from 3.2.6 to 3.2.8 ([PR #717](https://github.com/icosa-foundation/open-brush/pull/717) by @dependabot[bot])

- Unity 2022 LTS ([PR #708](https://github.com/icosa-foundation/open-brush/pull/708) by @mikeskydev)

- Bump actions/setup-dotnet from 4.0.0 to 4.0.1 ([PR #740](https://github.com/icosa-foundation/open-brush/pull/740) by @dependabot[bot])

- Bump actions/setup-python from 5.1.0 to 5.1.1 ([PR #742](https://github.com/icosa-foundation/open-brush/pull/742) by @dependabot[bot])

- Bump rexml from 3.2.9 to 3.3.2 and update fastlane ([PR #748](https://github.com/icosa-foundation/open-brush/pull/748) by @dependabot[bot])

- Bump mikepenz/release-changelog-builder-action from 4 to 5 ([PR #747](https://github.com/icosa-foundation/open-brush/pull/747) by @dependabot[bot])

- Bump rexml from 3.3.2 to 3.3.3 in the bundler group across 1 directory ([PR #752](https://github.com/icosa-foundation/open-brush/pull/752) by @dependabot[bot])

- Bump rexml from 3.3.3 to 3.3.6 in the bundler group across 1 directory ([PR #758](https://github.com/icosa-foundation/open-brush/pull/758) by @dependabot[bot])

- Bump actions/setup-python from 5.1.1 to 5.2.0 ([PR #759](https://github.com/icosa-foundation/open-brush/pull/759) by @dependabot[bot])

- Update some UPM packages ([PR #765](https://github.com/icosa-foundation/open-brush/pull/765) by @andybak)

- Update Zapbox SDK ([PR #770](https://github.com/icosa-foundation/open-brush/pull/770) by @andybak)


## 💬 Uncategorized

- Update Unity version in README.md ([PR #519](https://github.com/icosa-foundation/open-brush/pull/519) by @andybak)

- Update info on setting up Google API ([PR #618](https://github.com/icosa-foundation/open-brush/pull/618) by @andybak)

- Update README.md ([PR #760](https://github.com/icosa-foundation/open-brush/pull/760) by @mikeskydev)

- Fix fastlane build by freeing extra space ([PR #764](https://github.com/icosa-foundation/open-brush/pull/764) by @mikeage)





