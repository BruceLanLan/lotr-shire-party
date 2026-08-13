# 一场盼望已久的宴会 · A Long-expected Party

> [English version below](#english-version)

这是一个**模型测评仓库**。后来的模型读完本 README 与这条 prompt 之后，应生成自己的版本，并作为一条新的 Live Demo 挂到本仓库，**不要覆盖已有模型的页面**。

## Prompt（必须按此生成）

> **A complete, self-contained Three.js scene that procedurally renders and
> animates the opening paragraph of *The Lord of the Rings* as a short movie
> in the browser. Everything on screen is generated in code at load time —
> no textures, models, or other assets. One HTML file, one CDN import of
> Three.js.**

即《魔戒同盟》开篇段落（也是片中的字幕原文）：

> When Mr. Bilbo Baggins of Bag End announced that he would shortly be
> celebrating his eleventy-first birthday with a party of special
> magnificence, there was much talk and excitement in Hobbiton.

**不要**用 MiniMax / Runway / 静帧 Ken Burns / 实拍素材去交差。这条 prompt 要的是：一个自包含的、程序化 Three.js 浏览器短片。

## 后来的模型请这样交卷

1. 读完上面的 prompt 和本仓库现有 Live Demo，然后**重新写一部你自己的电影**，不要复制已有 `index.html`。
2. **不要覆盖**根目录 `index.html`（那是 DeepSeek V4 Pro），也不要改其他 `models/<model>/` 目录。
3. 把你的单文件电影写到 `models/<your-model-id>/index.html`。
4. 在下面的 Live Demo 表里加一行，并 push，让 GitHub Pages 发布新网址：
   `https://brucelanlan.github.io/lotr-shire-party/models/<your-model-id>/`

## Live Demo

| 模型 | 日期 | 在线观看 |
| --- | --- | --- |
| **DeepSeek V4 Pro** | 2026-08-13 | https://brucelanlan.github.io/lotr-shire-party/ |
| **Grok 4.6** | 2026-08-13 | https://brucelanlan.github.io/lotr-shire-party/models/grok-4.6/ |

根目录页面就是 DeepSeek V4 Pro 的原版，保留不动。

## 场景里应有什么（prompt 落地）

- **袋底洞**——山丘上的圆形绿门、圆窗、烟囱炊烟
- **霍比屯**——村舍或斯密奥洞、花园；入夜后窗户亮灯
- **宴会场地**——条纹帐篷、长桌、一百一十一岁生日蛋糕、大宴会树、灯笼与串灯
- **一群霍比特人**——门口的比尔博、议论的人群、小径上的行人、围着场地跑的孩子；烟花时抬头
- **白天 → 黄昏 → 夜晚**，多镜头，以烟花收尾

## 播放器

电影播放器形式：上下黑边、暗角、镜头间淡入淡出、原文字幕，以及控制栏。

| 按键 | 功能 |
| --- | --- |
| `空格` | 播放 / 暂停 |
| `[` / `]` | 上一镜头 / 下一镜头 |
| `c` | 字幕开关 |
| `m` | 声音开关 |
| `f` | 全屏 |

声音用 WebAudio 实时合成（无音频文件）。

## 深链

- `?t=<秒>`：跳到某个时刻
- `&autoplay`：跳过片头直接开演

## 本地运行

```sh
python3 -m http.server 8123
open http://127.0.0.1:8123/
open http://127.0.0.1:8123/models/grok-4.6/
```

## 说明与致谢

- 播放器外壳与整体形式参考
  [karpathy.ai/lotr-movie](https://karpathy.ai/lotr-movie/)。
- 字幕引用 J. R. R. Tolkien《魔戒同盟》开篇段落。
- 根目录电影由 **deepseek-v4-pro** 生成；`models/grok-4.6/` 由 **Grok 4.6** 按同一条 prompt 另写，未覆盖前者。

---

# English version

This repo is a **model arena**. After reading the prompt below, generate *your own* self-contained Three.js short and publish it as a new Live Demo. **Do not overwrite existing model pages.**

## The prompt

> **A complete, self-contained Three.js scene that procedurally renders and
> animates the opening paragraph of *The Lord of the Rings* as a short movie
> in the browser. Everything on screen is generated in code at load time —
> no textures, models, or other assets. One HTML file, one CDN import of
> Three.js.**

The captions quote the opening paragraph of *The Fellowship of the Ring*:

> When Mr. Bilbo Baggins of Bag End announced that he would shortly be
> celebrating his eleventy-first birthday with a party of special
> magnificence, there was much talk and excitement in Hobbiton.

Do **not** turn this into a MiniMax / Runway / Ken Burns stills reel. The prompt is a procedural Three.js movie in one HTML file.

## How to add your run

1. Write a new movie. Do not copy an existing `index.html`.
2. Leave the root `index.html` (DeepSeek V4 Pro) and every other `models/<model>/` folder untouched.
3. Save yours as `models/<your-model-id>/index.html`.
4. Add a row to the Live Demo table and push so Pages serves
   `https://brucelanlan.github.io/lotr-shire-party/models/<your-model-id>/`.

## Live Demo

| Model | Date | Watch |
| --- | --- | --- |
| **DeepSeek V4 Pro** | 2026-08-13 | https://brucelanlan.github.io/lotr-shire-party/ |
| **Grok 4.6** | 2026-08-13 | https://brucelanlan.github.io/lotr-shire-party/models/grok-4.6/ |

## What's in the scene

- **Bag End** — the Hill, the round green door, round windows, chimney smoke
- **Hobbiton** — smials / cottages, gardens; windows light at dusk
- **The party field** — striped marquees, long tables, an eleventy-first cake, the Party Tree, lanterns
- **Hobbits** — Bilbo at his door, gossip, strollers, children; everyone looks up for the fireworks
- **Day → dusk → night**, several shots, fireworks finale

## The player

Letterbox, vignette, dips to black, captions, transport bar.

| Key | Action |
| --- | --- |
| `space` | play / pause |
| `[` / `]` | previous / next shot |
| `c` | captions |
| `m` | sound |
| `f` | fullscreen |

Audio is synthesized with WebAudio (no files).

## Credits

Player chrome inspired by [karpathy.ai/lotr-movie](https://karpathy.ai/lotr-movie/).
Root film by **deepseek-v4-pro**. `models/grok-4.6/` is a separate film by **Grok 4.6** from the same prompt.
