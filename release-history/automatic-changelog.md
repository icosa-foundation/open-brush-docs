# Changelog since v2.10

[Full release details](https://github.com/icosa-foundation/open-brush/compare/v2.10...4d8d72da028c5141d68601d41d3cb475107d9146)

## 🚀 Features

- Plugin scripting ([PR #699](https://github.com/icosa-foundation/open-brush/pull/699) by @andybak)

- Enable axis locking for guides ([PR #856](https://github.com/icosa-foundation/open-brush/pull/856) by @andybak)

- Icosa Gallery Integration ([PR #865](https://github.com/icosa-foundation/open-brush/pull/865) by @andybak)

- Increase the default and max complexity for Icosa models ([PR #868](https://github.com/icosa-foundation/open-brush/pull/868) by @andybak)

- UI tweaks ([PR #877](https://github.com/icosa-foundation/open-brush/pull/877) by @andybak)

- Mesh splitting ([PR #880](https://github.com/icosa-foundation/open-brush/pull/880) by @andybak)

- Harmonize panels between PC and mobile ([PR #885](https://github.com/icosa-foundation/open-brush/pull/885) by @andybak)

- Non VR mode improvements ([PR #888](https://github.com/icosa-foundation/open-brush/pull/888) by @andybak)

- Save selected strokes ([PR #711](https://github.com/icosa-foundation/open-brush/pull/711) by @andybak)

- Still frame export ([PR #893](https://github.com/icosa-foundation/open-brush/pull/893) by @andybak)

- Allow symmetry modes to affect Tool Plugin output ([PR #897](https://github.com/icosa-foundation/open-brush/pull/897) by @andybak)

- Better saved strokes ux ([PR #912](https://github.com/icosa-foundation/open-brush/pull/912) by @andybak)


## 🐛 Fixes

- Fix/plugin merge fixes ([PR #848](https://github.com/icosa-foundation/open-brush/pull/848) by @andybak)

- Remove old "not supported" code that sneaked back in with plugin merge ([PR #849](https://github.com/icosa-foundation/open-brush/pull/849) by @andybak)

- Prevent error loading image widgets from old sketches ([PR #853](https://github.com/icosa-foundation/open-brush/pull/853) by @andybak)

- Fix bug where the layers panel doesn't init if it's not open when a sketch is loaded ([PR #854](https://github.com/icosa-foundation/open-brush/pull/854) by @andybak)

- Fix cloning widgets and strokes to multiple symmetry targets ([PR #855](https://github.com/icosa-foundation/open-brush/pull/855) by @andybak)

- Minor plugin scripting fixes ([PR #863](https://github.com/icosa-foundation/open-brush/pull/863) by @andybak)

- Fix bug where the sketch dropdown was empty after viewing a sketch ([PR #867](https://github.com/icosa-foundation/open-brush/pull/867) by @andybak)

- Blocks Icosa obj support ([PR #870](https://github.com/icosa-foundation/open-brush/pull/870) by @andybak)

- Use indices rather than InstanceId to ensure unique names that persist across sessions ([PR #878](https://github.com/icosa-foundation/open-brush/pull/878) by @andybak)

- Split models not model widgets ([PR #881](https://github.com/icosa-foundation/open-brush/pull/881) by @andybak)

- Partial fix for "Smoke" and WIP support for baking more than just vertex position ([PR #883](https://github.com/icosa-foundation/open-brush/pull/883) by @andybak)

- Ignore material instance naming when matching brushes ([PR #884](https://github.com/icosa-foundation/open-brush/pull/884) by @andybak)

- Saved Strokes Quest Bugfixes ([PR #892](https://github.com/icosa-foundation/open-brush/pull/892) by @andybak)

- PR 893 minor fixes ([PR #896](https://github.com/icosa-foundation/open-brush/pull/896) by @andybak)

- Example media files copying issues ([PR #898](https://github.com/icosa-foundation/open-brush/pull/898) by @andybak)

- GLTF files on android have no textures ([PR #899](https://github.com/icosa-foundation/open-brush/pull/899) by @andybak)

- Restore animation behaviour for GLTF imports ([PR #903](https://github.com/icosa-foundation/open-brush/pull/903) by @andybak)

- Fix animations not working due to node renaming for uniqueness ([PR #904](https://github.com/icosa-foundation/open-brush/pull/904) by @andybak)

- Switch to legacy animation mode ([PR #911](https://github.com/icosa-foundation/open-brush/pull/911) by @andybak)

- Fix coordinate space when calculating save icon for selected strokes ([PR #914](https://github.com/icosa-foundation/open-brush/pull/914) by @andybak)

- More Saved Stroke Fixes ([PR #915](https://github.com/icosa-foundation/open-brush/pull/915) by @andybak)


## 🛠️ Infrastructure

- Disable push of the Q1 build to Oculus (finally blocked by them) ([PR #850](https://github.com/icosa-foundation/open-brush/pull/850) by @mikeage)

- Add support for periodically (monthly) rebuilding a PR ([PR #858](https://github.com/icosa-foundation/open-brush/pull/858) by @mikeage)

- Fix broken workflow ([PR #859](https://github.com/icosa-foundation/open-brush/pull/859) by @mikeage)

- Do not save caches from development builds ([PR #866](https://github.com/icosa-foundation/open-brush/pull/866) by @mikeage)

- Only run the periodic rebuilds on the main repo, not on any forks ([PR #869](https://github.com/icosa-foundation/open-brush/pull/869) by @mikeage)

- Add PICO 4 Ultra and PICO 4 Pro ([PR #874](https://github.com/icosa-foundation/open-brush/pull/874) by @mikeage)

- Add gitleaks to pre-commit and update all hooks ([PR #875](https://github.com/icosa-foundation/open-brush/pull/875) by @mikeage)

- Replace --version with --version_id ([PR #879](https://github.com/icosa-foundation/open-brush/pull/879) by @mikeage)

- Remove periodic rebuild since it doesn't work if a workflow was originally run over 30 days ago ([PR #882](https://github.com/icosa-foundation/open-brush/pull/882) by @mikeage)

- Add sleep before setting the release channel version for ArborXR ([PR #886](https://github.com/icosa-foundation/open-brush/pull/886) by @mikeage)

- Add Mac (non-VR) releases to Itch ([PR #890](https://github.com/icosa-foundation/open-brush/pull/890) by @mikeage)

- Disable LFS in wretry (fixes intermittent build failures at the beginning) ([PR #907](https://github.com/icosa-foundation/open-brush/pull/907) by @mikeage)

- Fix ArborXR upload again (use the --wait option) ([PR #908](https://github.com/icosa-foundation/open-brush/pull/908) by @mikeage)

- Fix builds from forks with just main (no tags) ([PR #902](https://github.com/icosa-foundation/open-brush/pull/902) by @mikeage)

- Improve build resiliency ([PR #909](https://github.com/icosa-foundation/open-brush/pull/909) by @mikeage)

- Fix spelling mistake in non-gnu style arg ([PR #910](https://github.com/icosa-foundation/open-brush/pull/910) by @mikeage)


## 📦 Dependencies / Maintenance

- Bump rexml from 3.3.9 to 3.4.2 in the bundler group across 1 directory ([PR #913](https://github.com/icosa-foundation/open-brush/pull/913) by @dependabot[bot])


## 💬 Uncategorized

- Fix various issues related to additive loading ([PR #889](https://github.com/icosa-foundation/open-brush/pull/889) by @andybak)

- Fix GLTF blend shape import ([PR #918](https://github.com/icosa-foundation/open-brush/pull/918) by @andybak)





