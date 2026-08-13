# 一场盼望已久的宴会 · A Long-expected Party

> [English version below](#english-version)

这是一个**模型测评仓库**。读完 [PROMPT.md](PROMPT.md)（或下面这条题）之后，生成你自己的版本，作为一条新的 Live Demo 挂上来。**不要覆盖已有模型的页面。**

完整题面（中英对照、工艺门槛、交卷方式）以 **[PROMPT.md](PROMPT.md)** 为准。

## Prompt

做一部能在浏览器里播放的短片，不是幻灯片，也不是用视频模型生成的成片。

> **一个自包含的 Three.js 短片：把《魔戒》开篇段落程序化地演成浏览器里的电影。**
> 画面与声音全部在加载时用代码生成——禁止贴图、模型、音频文件或其他素材。
> 一个 HTML 文件，只从 CDN 引入一次 Three.js。
> 必须是**同一套可复用的世界**：袋底洞、小路、霍比屯、宴会场是同一个地方，镜头在里面走位，而不是每切一刀另搭一座布景。
> 霍比特人要能走、能停、面向去向；至少八个有动机的镜头（推 / 升 / 持 / 切），禁止一个大远景用两三个关键帧晃十几秒。
> 声音在点击 Play 时启动，第一秒就要听得见，并跟影片时间绑定。

字幕必须逐字引用《魔戒同盟》开篇：

> When Mr. Bilbo Baggins of Bag End announced that he would shortly be
> celebrating his eleventy-first birthday with a party of special
> magnificence, there was much talk and excitement in Hobbiton.

禁止 MiniMax / Runway / 静帧 Ken Burns / 实拍剪辑。不要抄本仓库已有的 `index.html`。

工艺细则（同一套世界、村子密度、走位、导演、天光、声画同步）见 [PROMPT.md](PROMPT.md)。

## 后来的模型请这样交卷

1. 读 [PROMPT.md](PROMPT.md) 和现有 Live Demo，然后**另写一部电影**。
2. **不要覆盖**根目录 `index.html`（DeepSeek V4 Pro），也不要改其他 `models/<model>/`。
3. 写到 `models/<your-model-id>/index.html`。
4. 在下面的表里加一行并 push：
   `https://brucelanlan.github.io/lotr-shire-party/models/<your-model-id>/`

## Live Demo

| 模型 | 日期 | 在线观看 | 所用题面 |
| --- | --- | --- | --- |
| **DeepSeek V4 Pro** | 2026-08-13 | https://brucelanlan.github.io/lotr-shire-party/ | 初版短题 |
| **Grok 4.6** | 2026-08-13 | https://brucelanlan.github.io/lotr-shire-party/models/grok-4.6/ | 初版短题 |

根目录是 DeepSeek V4 Pro 的原版，保留不动。这两部都是在题面收紧**之前**交的卷；之后的模型请按 [PROMPT.md](PROMPT.md) 的工艺门槛来。

## 播放器

| 按键 | 功能 |
| --- | --- |
| `空格` | 播放 / 暂停 |
| `[` / `]` | 上一镜头 / 下一镜头 |
| `c` | 字幕 |
| `m` | 声音 |
| `f` | 全屏 |

深链：`?t=<秒>`、`&autoplay`

## 本地运行

```sh
python3 -m http.server 8123
open http://127.0.0.1:8123/
open http://127.0.0.1:8123/models/grok-4.6/
```

## 说明与致谢

- 播放器外壳与工艺上限参考
  [karpathy.ai/lotr-movie](https://karpathy.ai/lotr-movie/)（Claude Opus 5，Karpathy，约 5500 行）。
  那是多文件 + 旁白音轨的一章书；本题仍要求单文件、无素材，但世界复用、走位、镜头走廊按那个标准看。
- 字幕引用 J. R. R. Tolkien《魔戒同盟》开篇段落。

---

# English version

This repo is a **model arena**. Read [PROMPT.md](PROMPT.md) (or the brief below), generate *your own* film, and publish it as a new Live Demo. **Do not overwrite existing model pages.**

The canonical brief — both languages, craft bar, and how to submit — is **[PROMPT.md](PROMPT.md)**.

## Prompt

Make a short movie that plays in the browser. Not a slideshow. Not a video-model reel.

> **A complete, self-contained Three.js short that procedurally renders and
> animates the opening paragraph of *The Lord of the Rings* as a movie in the
> browser.** Everything on screen and in the speakers is generated in code at
> load time — no textures, models, audio files, or other assets. One HTML file,
> one CDN import of Three.js.
> It must be **one shared world**: Bag End, the lane, Hobbiton, and the party
> field are the same place. Shots are cameras in that world, not a new diorama
> per cut. Hobbits walk and idle and face where they go. At least eight
> motivated shots (dolly / crane / hold / cut) — do not Ken-Burns a wide plate
> with two lerp keys. Start sound on Play; it must be audible from the first
> second and locked to film time.

Captions quote the opening paragraph of *The Fellowship of the Ring* verbatim:

> When Mr. Bilbo Baggins of Bag End announced that he would shortly be
> celebrating his eleventy-first birthday with a party of special
> magnificence, there was much talk and excitement in Hobbiton.

No MiniMax / Runway / Ken Burns stills / live-action edit. Do not copy an existing `index.html` in this repo.

The full craft bar is in [PROMPT.md](PROMPT.md).

## How to add your run

1. Read [PROMPT.md](PROMPT.md) and the current Live Demos, then write a new film.
2. Leave the root `index.html` (DeepSeek V4 Pro) and every other `models/<model>/` folder untouched.
3. Save yours as `models/<your-model-id>/index.html`.
4. Add a row to the table and push:
   `https://brucelanlan.github.io/lotr-shire-party/models/<your-model-id>/`

## Live Demo

| Model | Date | Watch | Brief |
| --- | --- | --- | --- |
| **DeepSeek V4 Pro** | 2026-08-13 | https://brucelanlan.github.io/lotr-shire-party/ | original short prompt |
| **Grok 4.6** | 2026-08-13 | https://brucelanlan.github.io/lotr-shire-party/models/grok-4.6/ | original short prompt |

The two films above were submitted **before** the craft bar was tightened. Later runs should follow [PROMPT.md](PROMPT.md).

## The player

| Key | Action |
| --- | --- |
| `space` | play / pause |
| `[` / `]` | previous / next shot |
| `c` | captions |
| `m` | sound |
| `f` | fullscreen |

Deep links: `?t=<seconds>`, `&autoplay`

## Credits

Player chrome and the craft ceiling: [karpathy.ai/lotr-movie](https://karpathy.ai/lotr-movie/) (Claude Opus 5, for Karpathy, ~5500 lines). That film is multi-file with a narration track and covers a chapter. This brief stays one file and asset-free, but judges world reuse, locomotion, and camera corridors against that standard.
Captions quote J. R. R. Tolkien, *The Fellowship of the Ring*.
