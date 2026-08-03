# A Long-expected Party

A complete, self-contained Three.js scene that procedurally renders and animates
the opening paragraph of *The Lord of the Rings* as a short "movie" in the browser:

> When Mr. Bilbo Baggins of Bag End announced that he would shortly be
> celebrating his eleventy-first birthday with a party of special magnificence,
> there was much talk and excitement in Hobbiton.

Everything on screen is generated in code at load time — no textures, models,
or other assets. One HTML file, one CDN import of Three.js.

## What's in the scene

- **Bag End** — the Hill with its round green door, round windows, chimney smoke
- **Hobbiton** — cottages with windows that light up at dusk, smaller smials, gardens
- **The party field** — striped marquees, long tables, an eleventy-first birthday
  cake with candles, the great Party Tree, lanterns and string lights
- **~30 hobbits** — Bilbo waving at his door, gossip clusters, strollers on the
  path, excited children circling the field; everyone looks up for the fireworks
- **A full day→dusk→night cycle** across seven shots, ending with a
  deterministic fireworks finale (rockets, sphere/ring/willow bursts)
- **Synthesized audio** (WebAudio, no files): wind, birdsong, crowd murmur,
  rocket whistles and booms

## The player

Modeled on a film player: letterbox bars, vignette, dips to black between shots,
verbatim captions, and a transport with play/pause, previous/next shot, a
scrubber with shot markers, timecode, CC / Sound / Fullscreen toggles.

| Key | Action |
| --- | ------ |
| `space` | play / pause |
| `[` / `]` | previous / next shot |
| `c` | captions on/off |
| `m` | sound on/off |
| `f` | fullscreen |

Deep links: `?t=<seconds>` seeks to a moment, `&autoplay` starts without the
title card (e.g. `index.html?autoplay&t=72` goes straight to the fireworks).

## Run it

Open `index.html` in a browser (internet access needed once, for the Three.js
CDN module), or serve it locally:

```sh
python3 -m http.server 8123
open http://127.0.0.1:8123/
```

## Credits

Structure and player chrome inspired by
[karpathy.ai/lotr-movie](https://karpathy.ai/lotr-movie/).
Scene, animation, and audio are original code. Text captions quote the opening
paragraph of J. R. R. Tolkien's *The Fellowship of the Ring*.
