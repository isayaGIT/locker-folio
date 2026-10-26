# Hotspot Rings / 热点扩散反馈

- **Group:** 06
- **Motion type:** Frame-driven + interaction
- **Trigger / behavior:** 场景热点的环形反馈与命中按钮响应。
- **Live demo:** https://locker.zezn.dev/
- **Fork:** https://github.com/zhushan-wubi/locker-folio
- **Upstream implementation:** https://github.com/qzz0518/locker-folio/tree/main
- **Original implementation revision audited:** `9f5891f4a7512ec71340a2f2f3fdffaa23bc1335`
- **Original file paths:** listed below; copies under `Source/` preserve the original `src/...` layout.
- **Capture provenance:** `preview.gif` is a locally recorded preview from the live demo, not an upstream-supplied GIF. See `CAPTURE.md` at the archive root for capture method and known limits.

## Source files copied into this group

- `src/experience/experienceMachine.ts`
- `src/experience/experienceTimeline.ts`
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

展示真实内容浮层与场景之间的交互过渡；环形反馈本身很短，本轮没有把它独立隔离为微距片段。
