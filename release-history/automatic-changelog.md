# Changelog since v2.32

[Full release details](https://github.com/icosa-foundation/open-brush/compare/v2.32...bd6f6b3536e2e96e54977c0bb7e3ede4e37475fb)

## 🚀 Features

- Unity 6 Kitchen Sink ([PR #1069](https://github.com/icosa-foundation/open-brush/pull/1069) by @andybak)

- Default media files improvements ([PR #1155](https://github.com/icosa-foundation/open-brush/pull/1155) by @andybak)

- Crop strokes ([PR #984](https://github.com/icosa-foundation/open-brush/pull/984) by @andybak)

- Tool plugin stroke preview ([PR #1022](https://github.com/icosa-foundation/open-brush/pull/1022) by @andybak)

- Simple straight edge snapping ([PR #1151](https://github.com/icosa-foundation/open-brush/pull/1151) by @andybak)

- Http api tests ([PR #1148](https://github.com/icosa-foundation/open-brush/pull/1148) by @andybak)

- EXR import and better hdr image handling ([PR #1130](https://github.com/icosa-foundation/open-brush/pull/1130) by @andybak)

- Splat capture camera path ([PR #1166](https://github.com/icosa-foundation/open-brush/pull/1166) by @andybak)

- Add pinch dolly navigation for touchscreen viewer ([PR #1171](https://github.com/icosa-foundation/open-brush/pull/1171) by @andybak)

- Build and publish non-XR Apple viewer apps ([PR #1169](https://github.com/icosa-foundation/open-brush/pull/1169) by @andybak)

- Expose bloom amount and threshold in user config ([PR #1177](https://github.com/icosa-foundation/open-brush/pull/1177) by @andybak)

- 3D stroke filling ([PR #1174](https://github.com/icosa-foundation/open-brush/pull/1174) by @andybak)

- Darken brush ([PR #1021](https://github.com/icosa-foundation/open-brush/pull/1021) by @andybak)

- Membrane brush variant with outlines ([PR #1184](https://github.com/icosa-foundation/open-brush/pull/1184) by @andybak)

- Symmetry plugin versions of old parent brushes ([PR #1183](https://github.com/icosa-foundation/open-brush/pull/1183) by @andybak)

- Better video rendering quality and configurability ([PR #1185](https://github.com/icosa-foundation/open-brush/pull/1185) by @andybak)

- Integrate handtracking and Android Direct Storage SAF ([PR #1191](https://github.com/icosa-foundation/open-brush/pull/1191) by @andybak)


## 🐛 Fixes

- Unity6 post merge fixes ([PR #1154](https://github.com/icosa-foundation/open-brush/pull/1154) by @andybak)

- Unity 6 post-merge fixes 2 ([PR #1157](https://github.com/icosa-foundation/open-brush/pull/1157) by @andybak)

- Fix guide settings panel ([PR #1161](https://github.com/icosa-foundation/open-brush/pull/1161) by @andybak)

- Fix export exceptions ([PR #1162](https://github.com/icosa-foundation/open-brush/pull/1162) by @andybak)

- Fix tools affecting other layers ([PR #1163](https://github.com/icosa-foundation/open-brush/pull/1163) by @andybak)

- Reject invalid ToolScript preview scales ([PR #1165](https://github.com/icosa-foundation/open-brush/pull/1165) by @andybak)

- Fix non-vr black screen ([PR #1170](https://github.com/icosa-foundation/open-brush/pull/1170) by @andybak)

- Upstream catalog fixes from SAF branch ([PR #1168](https://github.com/icosa-foundation/open-brush/pull/1168) by @andybak)

- Fix macOS plugin bundle identifiers before signing ([PR #1176](https://github.com/icosa-foundation/open-brush/pull/1176) by @andybak)

- Fix atlas issues ([PR #1178](https://github.com/icosa-foundation/open-brush/pull/1178) by @andybak)

- Shader passthrough fixes ([PR #1180](https://github.com/icosa-foundation/open-brush/pull/1180) by @andybak)

- Revert explicit sample coverage in UnlitA2CVertexColor shader ([PR #1182](https://github.com/icosa-foundation/open-brush/pull/1182) by @andybak)

- Fix some MSAA and A2C issues ([PR #1181](https://github.com/icosa-foundation/open-brush/pull/1181) by @andybak)

- Restore OpenGL ES 3 on Pico, whose Vulkan driver crashes ([PR #1188](https://github.com/icosa-foundation/open-brush/pull/1188) by @ThorstenHackbarth)

- Fix gltf shader stripping again ([PR #1187](https://github.com/icosa-foundation/open-brush/pull/1187) by @andybak)

- Fix offline render unicode bugs ([PR #1186](https://github.com/icosa-foundation/open-brush/pull/1186) by @andybak)

- Restore missing post-processing ([PR #1189](https://github.com/icosa-foundation/open-brush/pull/1189) by @andybak)

- Various beta fixes ([PR #1194](https://github.com/icosa-foundation/open-brush/pull/1194) by @andybak)

- Remove unnecessary Play device requirements for AndroidXR builds ([PR #1195](https://github.com/icosa-foundation/open-brush/pull/1195) by @andybak)

- Handtracking bugfix round 1 ([PR #1198](https://github.com/icosa-foundation/open-brush/pull/1198) by @andybak)

- Update Unity Tools package lock for brush fog fixes ([PR #1203](https://github.com/icosa-foundation/open-brush/pull/1203) by @andybak)

- Fix compositor quality switching bugs ([PR #1214](https://github.com/icosa-foundation/open-brush/pull/1214) by @andybak)

- Fix passthrough selection bug on Quest ([PR #1216](https://github.com/icosa-foundation/open-brush/pull/1216) by @andybak)

- Android launcher icon ([PR #1218](https://github.com/icosa-foundation/open-brush/pull/1218) by @andybak)

- Fix mobile widget selection highlights ([PR #1217](https://github.com/icosa-foundation/open-brush/pull/1217) by @andybak)

- Fix Android page size ([PR #1219](https://github.com/icosa-foundation/open-brush/pull/1219) by @andybak)


## 🛠️ Infrastructure

- Fix builds after caches are available in Unity 6+ ([PR #1153](https://github.com/icosa-foundation/open-brush/pull/1153) by @mikeage)

- Fix publish jobs and some general build cleanup ([PR #1156](https://github.com/icosa-foundation/open-brush/pull/1156) by @mikeage)

- Separate 2d builds for Android Viewer ([PR #1220](https://github.com/icosa-foundation/open-brush/pull/1220) by @andybak)


## 📦 Dependencies / Maintenance

- Update imm plugin ([PR #1167](https://github.com/icosa-foundation/open-brush/pull/1167) by @andybak)


## 💬 Uncategorized

- Put UNITY_LIBRARY_CACHE_PATHS in the proper step ([PR #1160](https://github.com/icosa-foundation/open-brush/pull/1160) by @mikeage)

- Integration branch for the PRs that will be merged soon ([PR #1212](https://github.com/icosa-foundation/open-brush/pull/1212) by @andybak)





