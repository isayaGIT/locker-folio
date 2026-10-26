# Locker Folio — Animation Archive

**Interactive browser:** open [`animation-gallery.html`](../../animation-gallery.html) from the repository root to search, preview, and inspect all archived animation groups.

A source-oriented inventory of the animation and interaction systems in the forked Locker Folio project.

- **Target fork:** https://github.com/isayaGIT/locker-folio
- **Upstream:** https://github.com/qzz0518/locker-folio
- **Live demo:** https://locker.zezn.dev/
- **Audited revision:** `9f5891f4a7512ec71340a2f2f3fdffaa23bc1335`
- **Archive rule:** each numbered group contains a `README.md`, a `Source/` tree preserving original `src/...` paths, and a `preview.gif` when a valid live capture is available.

## Animation groups

| Group | Motion model | Copied source files | Keyframe identifiers found in copied CSS |
|---|---|---:|---|
| [01 Loading / 背景文字漂移](./01-loading/README.md) | Timeline choreography | 9 | ghostDrift |
| [02 Mosaic Reveal / 马赛克揭幕](./02-mosaic-reveal/README.md) | Timeline choreography | 7 | cellOut |
| [03 3D Scene Intro / 柜体场景入场](./03-scene-intro/README.md) | Timeline choreography + 3D frame loop | 24 | TS/3D/interaction logic |
| [04 Camera Focus / 镜头聚焦与返回](./04-camera-focus/README.md) | Interaction-triggered timeline | 12 | TS/3D/interaction logic |
| [05 Surface Drag / 3D 物件拖动与悬浮](./05-surface-drag/README.md) | Interaction-driven + frame loop | 17 | TS/3D/interaction logic |
| [06 Hotspot Rings / 热点扩散反馈](./06-hotspot-rings/README.md) | Frame-driven + interaction | 10 | TS/3D/interaction logic |
| [07 Poster Intro / 海报 3D 入场编排](./07-poster-intro/README.md) | GSAP timeline + 3D scene | 12 | TS/3D/interaction logic |
| [08 Poster Deck / 海报拖动与惯性](./08-poster-deck/README.md) | Interaction-driven + frame loop | 12 | TS/3D/interaction logic |
| [09 Work Folders / 文件夹与纸张层次](./09-work-folders/README.md) | Timeline + hover interactions | 8 | starIn, starSpinA, starSpinB, foldIn |
| [10 Overlay Lifecycle / 浮层进入与退出](./10-overlay-lifecycle/README.md) | Timeline choreography | 11 | ovhOut, ovIn, closeIn, wvIn |
| [11 Work Transition / 圆形遮罩与波纹转场](./11-work-transition/README.md) | Web Animations API + frame loop | 7 | TS/3D/interaction logic |
| [12 Navigation / 导航下划线与菜单](./12-navigation/README.md) | CSS transitions + keyframes | 7 | ruleSwipe, navMenuIn |
| [13 Credit Entry / 来源署名入场](./13-credit-entry/README.md) | CSS keyframes + transitions | 4 | crIn |
| [14 About Card / 信息卡片弹入](./14-about-card/README.md) | CSS keyframes | 9 | idcDrop |
| [15 Skills Deck / 技能内容分层入场](./15-skills-deck/README.md) | CSS keyframes + state-driven transitions | 10 | skModeIn, skIn, skFade |
| [16 Contact Board / 联系纸条与纸张展开](./16-contact-board/README.md) | CSS keyframes + interaction | 18 | cbIn, noteFly, paperIn |
| [17 Video List / 视频列表入场与悬浮](./17-video-list/README.md) | CSS keyframes + transitions | 11 | vlIn |
| [18 Design View / 设计作品与书刊展开](./18-design-view/README.md) | CSS keyframes + transitions | 21 | dvIn, pdHead, ipIn |
| [19 Photograph Wall / 照片墙拖动与切换](./19-photo-wall/README.md) | Interaction-driven + transitions | 13 | TS/3D/interaction logic |
| [20 Website Carousel / 网站预览卡片轮播](./20-website-carousel/README.md) | CSS transitions + keyframes | 11 | wscFade |
| [21 Fallback / 降级页面与控件反馈](./21-fallback-transitions/README.md) | CSS transitions | 5 | TS/3D/interaction logic |

## Inventory methodology

The source scan includes CSS `@keyframes`, CSS `transition`/`animation` declarations, Web Animations API calls, `requestAnimationFrame`, GSAP timelines, and React Three Fiber `useFrame` loops. A visual effect can span multiple mechanisms; the 21 groups are organized around user-visible behavior rather than mechanically splitting individual keyframe declarations.

## Attribution and licensing

The repository code is MIT-licensed according to the upstream project. The original Locker visual concept and page/interaction design are attributed by the upstream README to Xiaohongshu creator momo; this code archive does not claim ownership of that concept. Replacement imagery and fonts can have separate licenses. Keep the upstream README, source credit and asset-specific rights notices intact.

## Preview status

See `CAPTURE.md` for capture provenance, generation commands and per-group GIF validation. Do not describe a missing or failed capture as an upstream-provided animation asset.
