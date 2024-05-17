# Changelog since v2.7

[Full release details](https://github.com/icosa-foundation/open-brush/compare/v2.7...364b5046d1b7bfae73e9d1ce6db968b44dc9c685)

## 🚀 Features

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


## 🎨 UI / UX

- Fix Advanced Tools panel initial position ([PR #697](https://github.com/icosa-foundation/open-brush/pull/697) by @andybak)

- Damn panel spacing ([PR #702](https://github.com/icosa-foundation/open-brush/pull/702) by @andybak)


## 🐛 Fixes

- Fix broken multimirror options popup. Hide Tiltosaurus button as it d… ([PR #680](https://github.com/icosa-foundation/open-brush/pull/680) by @andybak)

- Workaround for PCVR depth submission ([PR #685](https://github.com/icosa-foundation/open-brush/pull/685) by @mikeskydev)

- De-initialize XR Subsytems properly ([PR #695](https://github.com/icosa-foundation/open-brush/pull/695) by @andybak)

- Background image preview sphere labels ([PR #700](https://github.com/icosa-foundation/open-brush/pull/700) by @andybak)

- Fix stereo pano sphere preview ([PR #701](https://github.com/icosa-foundation/open-brush/pull/701) by @andybak)

- Enable file system watcher on mobile ([PR #704](https://github.com/icosa-foundation/open-brush/pull/704) by @andybak)

- UnityGltf import is meant to default to off ([PR #707](https://github.com/icosa-foundation/open-brush/pull/707) by @andybak)

- Fix issue where transparent brushes were invisible in Quest passthrough mode. ([PR #715](https://github.com/icosa-foundation/open-brush/pull/715) by @andybak)


## 🛠️ Infrastructure

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





