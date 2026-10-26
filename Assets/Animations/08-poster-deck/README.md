# Poster Deck / 海报拖动与惯性

- **Group:** 08
- **Motion type:** Interaction-driven + frame loop
- **Trigger / behavior:** 左右拖动海报，释放后惯性滑动，循环切换并按速度倾斜。
- **Live demo:** https://locker.zezn.dev/
- **Fork:** https://github.com/zhushan-wubi/locker-folio
- **Upstream implementation:** https://github.com/qzz0518/locker-folio/tree/main
- **Original implementation revision audited:** `9f5891f4a7512ec71340a2f2f3fdffaa23bc1335`
- **Original file paths:** listed below; copies under `Source/` preserve the original `src/...` layout.
- **Capture provenance:** `preview.gif` is a locally recorded preview from the live demo, not an upstream-supplied GIF. See `CAPTURE.md` at the archive root for capture method and known limits.

## Source files copied into this group

- `src/components/fallback/StaticFallback.tsx`
- `src/components/fallback/capabilities.ts`
- `src/components/fallback/fallback.css`
- `src/components/fallback/index.ts`
- `src/components/work/PostersDeck.tsx`
- `src/components/work/PostersThreeScene.tsx`
- `src/components/work/frameLoop.ts`
- `src/components/work/imageSources.ts`
- `src/data/content.ts`
- `src/hooks/useMediaQuery.ts`
- `src/hooks/useReducedMotion.ts`
- `src/styles/global.css`

## Animation identifiers

This group is primarily driven by TypeScript/Three.js/GSAP or CSS transitions; see the source files above.

## Dependencies and reuse notes

- `Source/` contains the recursive closure of local imports found from this group’s entry files, plus the shared global stylesheet where CSS tokens and reduced-motion rules are defined.
- Third-party runtime packages are not vendored; consult the root `package.json` for exact package declarations.
- The copies are reference/archive source, not a separately built package. Relative imports remain in their original `src/...` layout.
- Static media referenced by URL may remain in `public/assets/` in the original project; this archive is focused on motion implementation source, not a full site snapshot.
- Preserve original author credit and source links when redistributing. Code is under the repository’s MIT license; the design concept and individual replacement assets have separate rights as described in the upstream README.

## Preview fidelity note

展示海报段真实状态；本轮录制没有可靠捕获连续拖动后的惯性滑动，需后续补录专项交互。
