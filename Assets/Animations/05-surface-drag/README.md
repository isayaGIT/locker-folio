# Surface Drag / 3D 物件拖动与悬浮

- **Group:** 05
- **Motion type:** Interaction-driven + frame loop
- **Trigger / behavior:** 拖动物件时通过射线与承载面求交并限制边界，松手后反馈/回弹。
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
- `src/scene/PhysicalProps.tsx`
- `src/scene/PropDecal.tsx`
- `src/scene/Props.tsx`
- `src/scene/SurfaceDraggable.tsx`
- `src/scene/cameraDirector.ts`
- `src/scene/cameraPath.ts`
- `src/scene/decalSpecs.ts`
- `src/scene/hotspotActions.ts`
- `src/scene/hotspotSpecs.ts`
- `src/scene/lockerSpec.ts`
- `src/scene/propSpecs.ts`
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

展示真实 3D 场景状态；本轮浏览器录制未能可靠捕获一次完整的实体物件指针拖拽，不能把此 GIF 当作拖拽行为的完整验收证据。
