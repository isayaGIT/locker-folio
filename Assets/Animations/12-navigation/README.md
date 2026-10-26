# Navigation / 导航下划线与菜单

- **Group:** 12
- **Motion type:** CSS transitions + keyframes
- **Trigger / behavior:** 导航下划线扫过、菜单滑入、导航文字位置反馈。
- **Live demo:** https://locker.zezn.dev/
- **Fork:** https://github.com/zhushan-wubi/locker-folio
- **Upstream implementation:** https://github.com/qzz0518/locker-folio/tree/main
- **Original implementation revision audited:** `9f5891f4a7512ec71340a2f2f3fdffaa23bc1335`
- **Original file paths:** listed below; copies under `Source/` preserve the original `src/...` layout.
- **Capture provenance:** `preview.gif` is a locally recorded preview from the live demo, not an upstream-supplied GIF. See `CAPTURE.md` at the archive root for capture method and known limits.

## Source files copied into this group

- `src/components/Nav.tsx`
- `src/components/nav.css`
- `src/data/content.ts`
- `src/experience/experienceMachine.ts`
- `src/hooks/useMediaQuery.ts`
- `src/store.ts`
- `src/styles/global.css`

## Animation identifiers

`ruleSwipe`, `navMenuIn`

## Dependencies and reuse notes

- `Source/` contains the recursive closure of local imports found from this group’s entry files, plus the shared global stylesheet where CSS tokens and reduced-motion rules are defined.
- Third-party runtime packages are not vendored; consult the root `package.json` for exact package declarations.
- The copies are reference/archive source, not a separately built package. Relative imports remain in their original `src/...` layout.
- Static media referenced by URL may remain in `public/assets/` in the original project; this archive is focused on motion implementation source, not a full site snapshot.
- Preserve original author credit and source links when redistributing. Code is under the repository’s MIT license; the design concept and individual replacement assets have separate rights as described in the upstream README.

## Preview fidelity note

展示导航/内容切换时的页面过渡；导航下划线本身不是独立录制的专项微距预览。
