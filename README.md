<div align="center">
  <img src="banner.png" alt="TypeSprint" width="120" />
  <h1>TYPESPRINT<code>.exe</code></h1>
  <p><em>how fast do you type?</em></p>
  <p>
    <img src="https://img.shields.io/badge/vanilla-JS-c8ff00?style=flat-square&labelColor=0e0e0e" />
    <img src="https://img.shields.io/badge/zero-dependencies-c8ff00?style=flat-square&labelColor=0e0e0e" />
    <img src="https://img.shields.io/badge/one-file-c8ff00?style=flat-square&labelColor=0e0e0e" />
  </p>
</div>

---

## what is this

A minimal, zero-dependency speed typing test.
No framework. No npm. No build step.
Just open `index.html` and type.

Built on **[alvakry-theme](../alvakry-theme)** — dark/light, bilingual EN/ID,
and hiding a secret you'll have to find yourself.

---

## features

| | |
|---|---|
| ⏱ **timed modes** | 15s · 30s · 60s · 120s |
| 📊 **live stats** | WPM · accuracy · errors · time left |
| 🌐 **bilingual** | English & Bahasa Indonesia word pools |
| 🎨 **dark / light** | auto-detects system preference, persisted |
| 🔊 **click sounds** | Web Audio API — crisp tick on correct, dull on error |
| 📈 **run history** | last 20 sessions saved locally |
| 🔒 **no going back** | once you space to the next word, you commit |
| 🤫 **secret mode** | `Alt+P` — you'll figure out the rest |

---

## usage

```sh
# no install required
open index.html
```

---

## controls

| key | action |
|-----|--------|
| `Space` | confirm word, advance |
| `Backspace` | delete within current word only |
| `Tab` / `Esc` | restart test |
| `Alt+P` | open secret code prompt |

---

## scoring

```
WPM      = (correct_chars ÷ 5) ÷ elapsed_minutes
Raw WPM  = (all_chars_typed ÷ 5) ÷ elapsed_minutes
Accuracy = (correct_chars ÷ total_chars) × 100
```

Every 5 characters = 1 word. Industry standard formula.

---

## secret mode

Press `Alt+P`. Enter the code. 

The words will mean something.

*(no spoilers here)*

---

## stack

```
HTML  CSS  Vanilla JS
─────────────────────────────────
Web Audio API        click sounds
localStorage         settings + history
requestAnimationFrame  custom cursor
IntersectionObserver   scroll fade-in
```

---

## design tokens

```css
--bg        #f8f7f5 / #0e0e0e
--fg        #0d0d0d / #f0ede8
--accent    #c8ff00   /* neon lime */
--correct   #22c55e
--wrong     #ef4444
--sans      Space Grotesk
--mono      Space Mono
```

---

## file structure

```
speed typing website/
├── index.html   ← the whole app. one file.
├── banner.png   ← icon (replace with your own)
└── README.md    ← you are here
```

> To replace the favicon: add your `favicon.png` to the folder.
> The `<link>` tag in `index.html` already points to it.

---

<div align="center">
  <sub>built with alvakry-theme · no frameworks were harmed in the making of this project</sub>
</div>
