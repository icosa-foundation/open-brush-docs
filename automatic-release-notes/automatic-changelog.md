# Changelog since v2.2

[Full release details](https://github.com/icosa-foundation/open-brush/compare/v2.2...418ae6b636881cbdfe95a5055a5fba81bca66173)

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


## 🛠️ Infrastructure

- (Re-enable) Free disk space before starting the Android build ([PR #454](https://github.com/icosa-foundation/open-brush/pull/454) by @mikeage)

- Merge v2.3 hotfix branch ([PR #459](https://github.com/icosa-foundation/open-brush/pull/459) by @mikeage)

- Correctly calculate changelogs commensurate on commencement of correctional commit ([PR #460](https://github.com/icosa-foundation/open-brush/pull/460) by @mikeage)

- Update steam deployment to remove superflous parameters ([PR #470](https://github.com/icosa-foundation/open-brush/pull/470) by @mikeage)

- Replace all references to icosa-gallery with icosa-foundation ([PR #506](https://github.com/icosa-foundation/open-brush/pull/506) by @mikeage)

- Save steam's config.vdf after each login to prevent logout ([PR #509](https://github.com/icosa-foundation/open-brush/pull/509) by @mikeage)

- Separate Rift and Quest upload ([PR #520](https://github.com/icosa-foundation/open-brush/pull/520) by @mikeage)


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


## 💬 Uncategorized

- Update Unity version in README.md ([PR #519](https://github.com/icosa-foundation/open-brush/pull/519) by @andybak)





