# Changelog since v2.2

[Full release details](https://github.com/icosa-foundation/open-brush/compare/v2.2...138d24193ad3273568ca013ddedcace625c9963e)

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


## 💬 Uncategorized

- Update Unity version in README.md ([PR #519](https://github.com/icosa-foundation/open-brush/pull/519) by @andybak)





