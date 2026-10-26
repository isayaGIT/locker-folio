# Fallback / 降级页面与控件反馈

- **Group:** 21
- **Motion type:** CSS transitions
- **Trigger / behavior:** WebGL/性能降级路径中的静态首屏与控件反馈。
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
- `src/data/content.ts`
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

显示真实 3D 场景与返回过渡；由于当前浏览器支持 WebGL，本轮没有进入 WebGL 降级分支，因此不是 fallback 分支的直接录屏。
