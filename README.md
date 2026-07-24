# Fun Hub — Calculator & Offline Games

A single-page, dependency-free web app: a calculator plus a handful of classic offline games, styled with a claymorphism design system and playable entirely offline (no build step, no backend, no external JS/CSS libraries).

**Live demo:** https://jabanonuevo.github.io/calcu/

## Features

- 🧮 **Calculator** — standard arithmetic, keyboard support, and a confetti burst for fun result numbers (42, 69, 100, 420, 1337, 8008, π).
- 🌐 **Network Tools** — IPv4 subnet calculator: enter an IP with a CIDR prefix or subnet mask to get the network/broadcast address, usable host range, wildcard mask, IP class, public/private/loopback/multicast classification, and binary representation, plus a CIDR-to-subnet-mask quick reference table.
- ❌ **Tic-Tac-Toe** — 2-player mode, plus Vs Computer Easy (random) and Unbeatable (minimax AI) modes.
- 🐍 **Snake** — arrow keys / WASD / on-screen d-pad / swipe controls, speeds up as your score grows.
- 🔢 **2048** — keyboard and swipe controls, win/game-over detection.
- 🧠 **Memory Match** — emoji card-flip game with a move counter.
- ✊ **Rock, Paper, Scissors** — play against the computer with a running win/tie/loss tally.

Shared across every game:
- 🌗 Light/dark theme toggle (persisted)
- 🔊 Synthesized sound effects and 🎉 confetti (no external audio/image assets)
- 🏆 High scores, best times, and tallies saved to `localStorage`
- 📱 Responsive layout with touch support

## Running it

No install or build step required — it's plain HTML/CSS/JS.

- **Open directly:** double-click `index.html` (or `calculator.html`, an identical copy) to open it in your browser.
- **Or serve it locally:**
  ```bash
  python3 -m http.server 8000
  ```
  then visit `http://localhost:8000`.

## Project structure

```
index.html        # the app (calculator + all games)
calculator.html    # identical copy, kept in sync
```

Both files are self-contained — all HTML, CSS, and JavaScript live in one file, so the app works fully offline once loaded (the only external reference is an optional Google Fonts stylesheet, which degrades gracefully without internet access).

## Deployment

Served via GitHub Pages from the `main` branch root. Any push to `main` updates the live site automatically.
