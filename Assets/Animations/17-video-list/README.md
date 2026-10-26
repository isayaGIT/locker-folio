# Video List / 视频列表入场与悬浮

- **Group:** 17
- **Motion type:** CSS keyframes + transitions
- **Trigger / behavior:** 影像列表错位入场，卡片悬浮和选中反馈。
- **Live demo:** https://locker.zezn.dev/
- **Fork:** https://github.com/zhushan-wubi/locker-folio
- **Upstream implementation:** https://github.com/qzz0518/locker-folio/tree/main
- **Original implementation revision audited:** `9f5891f4a7512ec71340a2f2f3fdffaa23bc1335`
- **Original file paths:** listed below; copies under `Source/` preserve the original `src/...` layout.
- **Capture provenance:** `preview.gif` is a locally recorded preview from the live demo, not an upstream-supplied GIF. See `CAPTURE.md` at the archive root for capture method and known limits.

## Source files copied into this group

- `src/components/work/BackToFolders.tsx`
- `src/components/work/VideoList.tsx`
- `src/components/work/frameLoop.ts`
- `src/components/work/imageSources.ts`
- `src/components/work/transition.css`
- `src/components/work/video.css`
- `src/components/work/workTransition.ts`
- `src/data/content.ts`
- `src/experience/experienceMachine.ts`
- `src/store.ts`
- `src/styles/global.css`

## Animation identifiers

`vlIn`

## Dependencies and reuse notes

- `Source/` contains the recursive closure of local imports found from this group’s entry files, plus the shared global stylesheet where CSS tokens and reduced-motion rules are defined.
- Third-party runtime packages are not vendored; consult the root `package.json` for exact package declarations.
- The copies are reference/archive source, not a separately built package. Relative imports remain in their original `src/...` layout.
- Static media referenced by URL may remain in `public/assets/` in the original project; this archive is focused on motion implementation source, not a full site snapshot.
- Preserve original author credit and source links when redistributing. Code is under the repository’s MIT license; the design concept and individual replacement assets have separate rights as described in the upstream README.

## Preview fidelity note

真实视频列表页面状态与进入过程。
