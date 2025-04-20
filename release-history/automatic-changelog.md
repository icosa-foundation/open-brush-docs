# Changelog since v2.9

[Full release details](https://github.com/icosa-foundation/open-brush/compare/v2.9...1c9386b72e331a2853a157a812952de28efe47b1)

## 🚀 Features

- Logitech MK Ink Integration ([PR #768](https://github.com/icosa-foundation/open-brush/pull/768) by @andybak)

- Allow profiler to use bundled sketches ([PR #769](https://github.com/icosa-foundation/open-brush/pull/769) by @andybak)

- Multiplayer Beta ([PR #774](https://github.com/icosa-foundation/open-brush/pull/774) by @andybak)

- Runtime switching of experimental mode ([PR #802](https://github.com/icosa-foundation/open-brush/pull/802) by @andybak)

- Allow the erase tool to also "erase" media widgets ([PR #818](https://github.com/icosa-foundation/open-brush/pull/818) by @andybak)

- Zapbox fixes: tutorial, controller materials, and laser pointer ([PR #832](https://github.com/icosa-foundation/open-brush/pull/832) by @apzap)

- Multiplayer fixes and Improvements  ([PR #809](https://github.com/icosa-foundation/open-brush/pull/809) by @sbanca)


## 🐛 Fixes

- Settings tidyup ([PR #788](https://github.com/icosa-foundation/open-brush/pull/788) by @mikeskydev)

- Catch wmic exceptions so they don't mess up device initialization ([PR #805](https://github.com/icosa-foundation/open-brush/pull/805) by @andybak)

- Fix quality level bugs ([PR #806](https://github.com/icosa-foundation/open-brush/pull/806) by @andybak)

- Guard against tracking glitches that effect painting ([PR #808](https://github.com/icosa-foundation/open-brush/pull/808) by @andybak)

- Fix MX Stylus Regression ([PR #811](https://github.com/icosa-foundation/open-brush/pull/811) by @andybak)

- Fix editor issues with localization ([PR #825](https://github.com/icosa-foundation/open-brush/pull/825) by @andybak)

- The eraser tool should not erase pinned widgets ([PR #819](https://github.com/icosa-foundation/open-brush/pull/819) by @andybak)

- Update permission strings ([PR #835](https://github.com/icosa-foundation/open-brush/pull/835) by @tangobravo)

- Revert accidental change to Unity splash screen setting ([PR #840](https://github.com/icosa-foundation/open-brush/pull/840) by @andybak)

- Fix builds on forks; move defines from ProjectSettings to build.yml on a per-platform basis ([PR #842](https://github.com/icosa-foundation/open-brush/pull/842) by @mikeage)


## 🛠️ Infrastructure

- gzip config.vdf before storing as a secret ([PR #771](https://github.com/icosa-foundation/open-brush/pull/771) by @mikeage)

- Combine all dependabot PRs into one ([PR #780](https://github.com/icosa-foundation/open-brush/pull/780) by @mikeage)

- Use PAT to create releases and tags ([PR #782](https://github.com/icosa-foundation/open-brush/pull/782) by @mikeage)

- Do not use # in PR build names ([PR #796](https://github.com/icosa-foundation/open-brush/pull/796) by @mikeage)

- Improve Windows development experience ([PR #797](https://github.com/icosa-foundation/open-brush/pull/797) by @mikeage)

- Support new ubuntu-24 images ([PR #799](https://github.com/icosa-foundation/open-brush/pull/799) by @mikeage)

- Fix chown error in newer Alpine images [affects new builds without caches] ([PR #804](https://github.com/icosa-foundation/open-brush/pull/804) by @mikeage)

- Publish Q1 and Q2 builds to ArborXR ([PR #824](https://github.com/icosa-foundation/open-brush/pull/824) by @mikeage)

- Upload Pico to ArborXR ([PR #826](https://github.com/icosa-foundation/open-brush/pull/826) by @mikeage)

- Add arm64 to cert generation ([PR #829](https://github.com/icosa-foundation/open-brush/pull/829) by @mikeage)

- Switch scoped registries to OpenUPM ([PR #787](https://github.com/icosa-foundation/open-brush/pull/787) by @sbanca)

- Use Xcode 16.2 to build Zapbox ([PR #830](https://github.com/icosa-foundation/open-brush/pull/830) by @mikeage)

- Update packages-lock.json so that we can recreate the cache ([PR #831](https://github.com/icosa-foundation/open-brush/pull/831) by @mikeage)

- Switch to ArborXR v2 CLI ([PR #836](https://github.com/icosa-foundation/open-brush/pull/836) by @mikeage)

- Fix Arbor XR release channel updates which use a version ID instead of a version (despite calling the parameter --version) ([PR #837](https://github.com/icosa-foundation/open-brush/pull/837) by @mikeage)

- Use JSON format for abxr-cli ([PR #838](https://github.com/icosa-foundation/open-brush/pull/838) by @mikeage)

- Faster cleanup step (saves about 1 minute in the slow case) ([PR #839](https://github.com/icosa-foundation/open-brush/pull/839) by @mikeage)

- Add a github action to automatically comment if/when Packages or Project Settings are changed ([PR #841](https://github.com/icosa-foundation/open-brush/pull/841) by @mikeage)

- Fix missing line that caused duplicate comments ([PR #843](https://github.com/icosa-foundation/open-brush/pull/843) by @mikeage)

- Disable package cache ([PR #844](https://github.com/icosa-foundation/open-brush/pull/844) by @mikeage)

- Fix builds on forks; move defines from ProjectSettings to build.yml on a per-platform basis ([PR #842](https://github.com/icosa-foundation/open-brush/pull/842) by @mikeage)


## 📦 Dependencies / Maintenance

- Update some UPM packages ([PR #765](https://github.com/icosa-foundation/open-brush/pull/765) by @andybak)

- Update Zapbox SDK ([PR #770](https://github.com/icosa-foundation/open-brush/pull/770) by @andybak)

- Bump the all-actions-updates group with 2 updates ([PR #781](https://github.com/icosa-foundation/open-brush/pull/781) by @dependabot[bot])

- Force photon to the previous, working, version ([PR #783](https://github.com/icosa-foundation/open-brush/pull/783) by @mikeage)

- Bump rexml from 3.3.6 to 3.3.9 in the bundler group across 1 directory ([PR #784](https://github.com/icosa-foundation/open-brush/pull/784) by @dependabot[bot])

- Update Zapbox SDK to 0.4.0 ([PR #834](https://github.com/icosa-foundation/open-brush/pull/834) by @tangobravo)


## 💬 Uncategorized

- Enable incremental garbage collector ([PR #807](https://github.com/icosa-foundation/open-brush/pull/807) by @andybak)





