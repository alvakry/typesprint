# ⌨ TYPESPRINT.exe

> *how fast do you type?*

A minimal, zero-dependency speed typing test built on the **alvakry-theme** — dark/light, bilingual, and hiding a secret you'll have to find yourself.

---

## features

```
⏱  timed modes       15s / 30s / 60s / 120s
📊  live stats        WPM · accuracy · errors · time left
🌐  bilingual         English & Bahasa Indonesia word pools
🎨  dark / light      auto-detects system preference
🔊  click sounds      Web Audio API — crisp ticks, dull errors
📈  run history       last 20 sessions saved in localStorage
🔒  no backspace      once you move to the next word, you commit
🤫  secret mode       ...try Alt+P
```

---

## usage

No build step. No dependencies. No npm install.

```
open index.html
```

That's it.

---

## controls

| key | action |
|-----|--------|
| `Tab` / `Esc` | restart current test |
| `Space` | advance to next word |
| `Alt+P` | open secret code input |

---

## how WPM is calculated

Standard formula — every 5 characters = 1 word.

```
WPM     = (correct_chars / 5) / elapsed_minutes
Raw WPM = (all_chars_typed / 5) / elapsed_minutes
Accuracy = (correct_chars / total_chars) × 100
```

Backspacing to a previous word is **not allowed** once confirmed with space — by design.

---

## secret mode

Press `Alt+P` anywhere on the page. A code input will appear.

Enter the right code to unlock an alternate word pool.

The words will mean something.

---

## stack

```
HTML · CSS · Vanilla JS
Web Audio API      (click sounds)
localStorage       (theme, language, run history)
IntersectionObserver  (scroll fade)
requestAnimationFrame  (custom cursor)
```

Zero frameworks. Zero libraries. One file.

---

## theme

Built on [alvakry-theme](../alvakry-theme) —
a personal design system using **Space Grotesk** + **Space Mono**
with a neon lime accent (`#c8ff00`).

Design tokens:

```css
--bg        page background
--fg        primary text
--muted     secondary / labels
--border    subtle dividers
--accent    #c8ff00  (the lime)
--correct   #22c55e
--wrong     #ef4444
```

---

## file structure

```
speed typing website/
└── index.html    ← everything. one file.
└── README.md     ← you are here
```

---

<div align="center">
  <sub>built with alvakry-theme · no frameworks were harmed</sub>
</div>
