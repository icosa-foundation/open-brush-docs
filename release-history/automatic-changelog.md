# Changelog since v2.9

[Full release details](https://github.com/icosa-foundation/open-brush/compare/v2.9...a0ef47cf81371232e86a1e0ad6f807f33ee3b0af)

## 🚀 Features

- Logitech MK Ink Integration ([PR #768](https://github.com/icosa-foundation/open-brush/pull/768) by @andybak)

- Allow profiler to use bundled sketches ([PR #769](https://github.com/icosa-foundation/open-brush/pull/769) by @andybak)

- Multiplayer Beta ([PR #774](https://github.com/icosa-foundation/open-brush/pull/774) by @andybak)

- Runtime switching of experimental mode ([PR #802](https://github.com/icosa-foundation/open-brush/pull/802) by @andybak)

- Allow the erase tool to also "erase" media widgets ([PR #818](https://github.com/icosa-foundation/open-brush/pull/818) by @andybak)


## 🐛 Fixes

- Settings tidyup ([PR #788](https://github.com/icosa-foundation/open-brush/pull/788) by @mikeskydev)

- Catch wmic exceptions so they don't mess up device initialization ([PR #805](https://github.com/icosa-foundation/open-brush/pull/805) by @andybak)

- Fix quality level bugs ([PR #806](https://github.com/icosa-foundation/open-brush/pull/806) by @andybak)

- Guard against tracking glitches that effect painting ([PR #808](https://github.com/icosa-foundation/open-brush/pull/808) by @andybak)

- Fix MX Stylus Regression ([PR #811](https://github.com/icosa-foundation/open-brush/pull/811) by @andybak)

- Fix editor issues with localization ([PR #825](https://github.com/icosa-foundation/open-brush/pull/825) by @andybak)

- The eraser tool should not erase pinned widgets ([PR #819](https://github.com/icosa-foundation/open-brush/pull/819) by @andybak)


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


## 📦 Dependencies / Maintenance

- Update some UPM packages ([PR #765](https://github.com/icosa-foundation/open-brush/pull/765) by @andybak)

- Update Zapbox SDK ([PR #770](https://github.com/icosa-foundation/open-brush/pull/770) by @andybak)

- Bump the all-actions-updates group with 2 updates ([PR #781](https://github.com/icosa-foundation/open-brush/pull/781) by @dependabot[bot])

- Force photon to the previous, working, version ([PR #783](https://github.com/icosa-foundation/open-brush/pull/783) by @mikeage)

- Bump rexml from 3.3.6 to 3.3.9 in the bundler group across 1 directory ([PR #784](https://github.com/icosa-foundation/open-brush/pull/784) by @dependabot[bot])


## 💬 Uncategorized

- Enable incremental garbage collector ([PR #807](https://github.com/icosa-foundation/open-brush/pull/807) by @andybak)

- Update Zapbox SDK to 0.4.0 ([PR #834](https://github.com/icosa-foundation/open-brush/pull/834) by @tangobravo)





