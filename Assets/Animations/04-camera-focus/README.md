# Camera Focus / 镜头聚焦与返回

- **Group:** 04
- **Motion type:** Interaction-triggered timeline
- **Trigger / behavior:** 点击热点或实体物件，镜头飞向目标；返回时恢复稳定机位。
- **Live demo:** https://locker.zezn.dev/
- **Fork:** https://github.com/zhushan-wubi/locker-folio
- **Upstream implementation:** https://github.com/qzz0518/locker-folio/tree/main
- **Original implementation revision audited:** `9f5891f4a7512ec71340a2f2f3fdffaa23bc1335`
- **Original file paths:** listed below; copies under `Source/` preserve the original `src/...` layout.
- **Capture provenance:** `preview.gif` is a locally recorded preview from the live demo, not an upstream-supplied GIF. See `CAPTURE.md` at the archive root for capture method and known limits.

## Source files copied into this group

- `src/experience/experienceClock.ts`
- `src/experience/experienceMachine.ts`
- `src/experience/experienceTimeline.ts`
- `src/scene/CameraRig.tsx`
- `src/scene/Hotspots.tsx`
- `src/scene/cameraDirector.ts`
- `src/scene/cameraPath.ts`
- `src/scene/hotspotActions.ts`
- `src/scene/hotspotSpecs.ts`
- `src/scene/sceneConfig.ts`
- `src/scene/userZoom.ts`
- `src/store.ts`

## Animation identifiers

This group is primarily driven by TypeScript/Three.js/GSAP or CSS transitions; see the source files above.

## Dependencies and reuse notes

- `Source/` contains the recursive closure of local imports found from this group’s entry files, plus the shared global stylesheet where CSS tokens and reduced-motion rules are defined.
- Third-party runtime packages are not vendored; consult the root `package.json` for exact package declarations.
- The copies are reference/archive source, not a separately built package. Relative imports remain in their original `src/...` layout.
- Static media referenced by URL may remain in `public/assets/` in the original project; this archive is focused on motion implementation source, not a full site snapshot.
- Preserve original author credit and source links when redistributing. Code is under the repository’s MIT license; the design concept and individual replacement assets have separate rights as described in the upstream README.

## Preview fidelity note

展示从内容浮层回到 3D 场景的镜头/场景过渡；单独聚焦曲线的精确机位轨迹未完全隔离。
