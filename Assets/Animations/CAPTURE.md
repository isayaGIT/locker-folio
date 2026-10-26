# Preview GIF capture log

The preview GIFs were generated from real browser screencast recordings of https://locker.zezn.dev/ using Chrome DevTools MCP and FFmpeg. They are locally recorded previews, not GIF files supplied by the upstream repository.

## Capture sessions

- `fresh-load`: opened a clean `about:blank` page, started screencast, then navigated to the live demo. Used for loading, reveal, scene entry, and credit-area previews.
- `interaction-run-1`: recorded the live demo while visiting work content and returning to the 3D scene. Used for scene/focus and video-list previews.
- `interaction-run-2`: recorded the live demo while navigating ABOUT, SKILLS, CONTACT, SELECTED WORK folders, and work subviews.

## Per-group source segments

| Group | Recording | Start (s) | Requested segment (s) | Notes |
|---|---|---:|---:|---|
| [01](./01-loading/preview.gif) | fresh-load | 7.0 | 1.8 | 真实加载页片段；该页加载初期包含空白帧，预览保留了进入 WELCOME 加载态的过程。 |
| [02](./02-mosaic-reveal/preview.gif) | fresh-load | 9.0 | 1.6 | 真实加载完成到场景出现的转场片段；这是在线演示的录屏，不是上游提供的 GIF。 |
| [03](./03-scene-intro/preview.gif) | fresh-load | 10.0 | 2.4 | 真实 3D 场景入场片段。 |
| [04](./04-camera-focus/preview.gif) | interaction-run-1 | 18.0 | 2.2 | 展示从内容浮层回到 3D 场景的镜头/场景过渡；单独聚焦曲线的精确机位轨迹未完全隔离。 |
| [05](./05-surface-drag/preview.gif) | interaction-run-1 | 20.0 | 2.0 | 展示真实 3D 场景状态；本轮浏览器录制未能可靠捕获一次完整的实体物件指针拖拽，不能把此 GIF 当作拖拽行为的完整验收证据。 |
| [06](./06-hotspot-rings/preview.gif) | interaction-run-2 | 2.6 | 2.0 | 展示真实内容浮层与场景之间的交互过渡；环形反馈未单独隔离。 |
| [07](./07-poster-intro/preview.gif) | interaction-run-2 | 9.8 | 2.2 | 真实设计页海报段入场预览。 |
| [08](./08-poster-deck/preview.gif) | interaction-run-2 | 10.0 | 2.2 | 展示海报段真实状态；本轮录制没有可靠捕获连续拖动后的惯性滑动，需后续补录专项交互。 |
| [09](./09-work-folders/preview.gif) | interaction-run-2 | 8.4 | 1.8 | 真实作品文件夹/内容层切换片段。 |
| [10](./10-overlay-lifecycle/preview.gif) | interaction-run-2 | 2.6 | 5.8 | 连续记录 ABOUT、SKILLS、CONTACT 浮层的进入/退出状态。 |
| [11](./11-work-transition/preview.gif) | interaction-run-2 | 7.8 | 2.0 | 真实内容浮层返回文件夹/子视图切换片段。 |
| [12](./12-navigation/preview.gif) | interaction-run-2 | 8.5 | 2.0 | 展示导航/内容切换时的页面过渡；导航下划线本身不是独立录制的专项微距预览。 |
| [13](./13-credit-entry/preview.gif) | fresh-load | 11.5 | 2.0 | 真实场景页面与来源署名区域；署名的短入场时间较早，未能单独隔离为仅含署名的片段。 |
| [14](./14-about-card/preview.gif) | interaction-run-2 | 3.0 | 2.0 | ABOUT 卡片真实入场片段。 |
| [15](./15-skills-deck/preview.gif) | interaction-run-2 | 4.5 | 2.0 | SKILLS 浮层真实入场片段。 |
| [16](./16-contact-board/preview.gif) | interaction-run-2 | 6.5 | 2.0 | CONTACT 浮层真实入场片段。 |
| [17](./17-video-list/preview.gif) | interaction-run-1 | 0.0 | 2.0 | 真实视频列表页面状态与进入过程。 |
| [18](./18-design-view/preview.gif) | interaction-run-1 | 15.0 | 2.0 | 真实设计类作品内容片段；未完整隔离三段式切换全部关键帧。 |
| [19](./19-photo-wall/preview.gif) | interaction-run-2 | 11.4 | 2.0 | 展示真实作品子视图切换；本轮录制未可靠捕获照片墙的完整拖动/布局切换手势。 |
| [20](./20-website-carousel/preview.gif) | interaction-run-2 | 12.5 | 2.0 | 真实网站预览轮播页片段。 |
| [21](./21-fallback-transitions/preview.gif) | interaction-run-1 | 22.0 | 2.0 | 显示真实 3D 场景与返回过渡；当前浏览器支持 WebGL，未进入 fallback 分支。 |

## Encoding and validation

- Each source MP4 segment was trimmed to a temporary clip, scaled to 420 px wide, encoded at approximately 8 fps, palette-optimized, and written as `preview.gif`.
- Each GIF was probed with `ffprobe` for dimensions, frame count, and duration; the final validation pass checks all 21 GIFs for non-zero size, multiple frames, and adequate duration.
- This is a reference archive, not a claim that every micro-interaction was individually isolated. Specifically, the exact drag/inertia motions for groups 05, 08, and 19 and the WebGL fallback branch for group 21 remain candidates for a second, pointer-precise capture pass.
- Browser recording timestamps are affected by page loading and sparse frames during static intervals; each group README records the known capture limitation rather than overstating fidelity.

## Reproduce the GIF encoding

For a new capture, first trim the MP4 segment, then generate a palette and GIF:

```bash
ffmpeg -ss START -i capture.mp4 -t DURATION -an -vf "scale=420:-1:flags=lanczos" -c:v libx264 -preset ultrafast -crf 22 clip.mp4
ffmpeg -i clip.mp4 -vf "fps=8,palettegen=stats_mode=full" -frames:v 1 palette.png
ffmpeg -i clip.mp4 -i palette.png -lavfi "fps=8[x];[x][1:v]paletteuse=dither=bayer:bayer_scale=3" -loop 0 preview.gif
```

## Attribution reminder

The live demo is a study reference. Preserve the original repository credit. The upstream README distinguishes MIT-licensed repository code from the original Locker visual concept and separately licensed replacement assets.
