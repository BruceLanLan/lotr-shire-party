# Prompt

后来的模型只读这一份也可以交卷。中文与英文是同一条题，要求一致。

不要覆盖根目录 `index.html`，也不要覆盖 `models/` 下已有目录。
写到 `models/<your-model-id>/index.html`，并在 `README.md` 的 Live Demo 表加一行。

---

## 中文

做一部能在浏览器里播放的短片，不是幻灯片，也不是用视频模型生成的成片。

**硬约束**

- 一个 HTML 文件；只允许从 CDN 引入一次 Three.js。
- 画面与声音全部在加载时用代码生成。禁止贴图、模型、音频文件、以及任何外部素材。
- 禁止 MiniMax / Runway / 静帧 Ken Burns / 实拍剪辑。
- 不要复制本仓库里任何已有的 `index.html`。

**故事**

把《魔戒同盟》开篇这一段演成约 90–120 秒的短片。字幕必须逐字引用，只允许在短语边界切开分到不同镜头：

> When Mr. Bilbo Baggins of Bag End announced that he would shortly be
> celebrating his eleventy-first birthday with a party of special
> magnificence, there was much talk and excitement in Hobbiton.

**工艺门槛（前几版单文件交卷最常倒在这里）**

1. **同一套世界。** 袋底洞、下山小路、霍比屯的斯密奥/村舍、水面或水车、宴会场、大宴会树，是同一个地方。每个镜头只是把摄像机放进这个世界，不是另搭一座布景。
2. **它得读得像村子，不像公园。** 多座能分辨的圆门斯密奥；小路真正从绿门连到宴会场；字幕提到大树时镜头里要看得到那棵树；远景里袋底洞的绿门必须能认出来。圆窗是窗，不要排成一张脸。
3. **霍比特人是角色。** 要有走/停，面向行进方向，脚在地面高度上。比尔博在门口挥手；路上的人是走过来的，不是原地晃；孩子会跑；聚谈的人朝向彼此；烟花升起时全体抬头。禁止只会上下弹的圆球人。
4. **要导演，不要推镜。** 至少 8 个镜头。推、升、持、切都要有理由。禁止一个大远景用两三个关键帧插值晃十四秒。镜头不要钻进山体或树干。镜头之间淡入淡出。
5. **白天 → 黄昏 → 夜晚是连续的天光**，不是换一张背景色。灯是因为天黑了才亮。烟花是山丘上方的绽放，不是稀稀落落的几个点。
6. **声音是画面的一部分。** 在 Play 的用户手势里启动 AudioContext。风、鸟、人群、火箭哨音、爆炸——第一秒就要听得见，并且跟影片时间绑定，拖进度条时声画仍对齐。

**播放器**

电影播放器：上下黑边、暗角、原文字幕、控制栏（播放/暂停、上一镜/下一镜、带镜头刻度的进度条、时间码、CC / Sound / Full）。

按键：`空格` `[` `]` `c` `m` `f`  
深链：`?t=<秒>`、`&autoplay`

参考 [karpathy.ai/lotr-movie](https://karpathy.ai/lotr-movie/) 的世界复用、走位和镜头走廊，不要抄它的文件结构，也不要引入旁白音轨。

---

## English

Make a short movie that plays in the browser. Not a slideshow. Not a video-model reel.

**Hard constraints**

- One HTML file. One CDN import of Three.js.
- Everything on screen and in the speakers is generated in code at load time. No textures, models, audio files, or other assets.
- No MiniMax / Runway / Ken Burns stills / live-action edit.
- Do not copy any existing `index.html` in this repo.

**Story**

Animate the opening paragraph of *The Fellowship of the Ring* as a ~90–120s short. Captions must quote this text verbatim; you may split it across shots only at phrase boundaries:

> When Mr. Bilbo Baggins of Bag End announced that he would shortly be
> celebrating his eleventy-first birthday with a party of special
> magnificence, there was much talk and excitement in Hobbiton.

**Craft bar** (where earlier one-file runs fell short)

1. **One shared world.** Bag End, the lane, Hobbiton smials/cottages, water or a mill, the party field, and the Party Tree are the same place. Every shot is a camera in that world, not a new diorama.
2. **It must read as a village, not a park.** Several distinct round-door smials; a path that actually connects the green door to the field; the Party Tree on screen when the caption names it; Bag End’s green door readable in the establishing shot. Windows are windows, not a face.
3. **Hobbits are characters.** Walk and idle, face the direction of travel, stand on the ground. Bilbo waves at his door. Strollers walk the lane. Children run. Gossipers face each other. Everyone looks up for the fireworks. No bobbing blobs.
4. **Direct it.** At least eight shots. Dolly, crane, hold, and cut for a reason. Do not Ken-Burns a wide shot for fourteen seconds with two lerp keys. Keep the lens out of hillsides and trunks. Dip to black between shots.
5. **Day → dusk → night is one continuous sky**, not a background swap. Lights come on because evening fell. Fireworks burst over the Hill; they are not a handful of dots.
6. **Sound is part of the picture.** Start the AudioContext on the Play gesture. Wind, birds, crowd, rocket whistles, booms — audible from the first second, driven by film time so the scrubber stays in sync.

**Player**

Letterbox, vignette, verbatim captions, transport (play/pause, prev/next shot, scrubber with shot marks, timecode, CC / Sound / Full).

Keys: `space` `[` `]` `c` `m` `f`  
Deep links: `?t=<seconds>`, `&autoplay`

Study [karpathy.ai/lotr-movie](https://karpathy.ai/lotr-movie/) for world reuse, locomotion, and camera corridors. Do not copy its file layout, and do not add a narration track.
