# The Fairest of All

**Book One of the Mirrorlands. An interactive fairytale LitRPG you play in your browser.**

> *Mirror, mirror, in your hand... who's the bravest in the land?*

<p align="center">
  <img src="docs/screenshot-title-mobile.png" alt="Title screen on a phone" width="260">
  &nbsp;
  <img src="docs/screenshot-fight-mobile.png" alt="A boss fight on a phone" width="260">
</p>

**Play it:** `https://YOUR-USERNAME.github.io/YOUR-REPO/` (replace with your own GitHub Pages address after you turn Pages on; see below).

---

## What it is

A choose-your-path story with real RPG parts: stats, classes, gear, skills, levels, shops, boss fights, achievements and a map. You play a hero in a world built from public-domain fairy tales, guided by the vain, theatrical, never-lying **Magic Mirror**. The Mirror says it wants to make you the Fairest of All. Read the fine print.

- **36 chapters in six acts**, levels 1 to 30, four endings, and an after-credits sequel hook.
- **Written for ages 8 to 12.** Simple words, gentle scares, and a Leave panel that reminds players it is only a story and suggests breaks.
- **A first step into LitRPG** for readers of fairytale-adventure series.
- **Fourth-wall touches:** the screen itself is the mirror. It reacts to your clock, your tab, and how you touch the glass. It never uses the camera or microphone.
- **One file.** The whole game is `index.html`. No server, no accounts, no tracking, no install.

## Contents of the story

| Act | Title | Chapters |
|---|---|---|
| I | The Mirror Wakes | 1 to 6 |
| II | The Briar Wood | 7 to 12 |
| III | The Glass Mountain | 13 to 18 |
| IV | The Gingerbread Reach | 19 to 24 |
| V | The Mirror's Cellar | 25 to 30 |
| VI | The Throne of Glass | 31 to 36 |

See [`docs/CHAPTER_MAP.md`](docs/CHAPTER_MAP.md) for the full chapter list, the seven shards and how the endings work.

---

## Put it on GitHub Pages

1. Create a new repository on GitHub (public, or private on a plan that supports private Pages).
2. Upload everything in this folder. At minimum you need **`index.html`** and **`.nojekyll`** in the **root** of the repository.
3. In the repo go to **Settings > Pages**.
4. Under **Build and deployment**, set **Source** to **Deploy from a branch**, choose your **main** branch and the **/ (root)** folder, then **Save**.
5. Wait a minute or two. GitHub shows your live address at the top of the Pages screen. It looks like `https://YOUR-USERNAME.github.io/YOUR-REPO/`.
6. Open it on your phone and play a few minutes.

To update later, replace `index.html` in the repo and commit. Pages redeploys on its own.

**Custom domain (optional):** in Settings > Pages, add your domain under **Custom domain**, and add the DNS records GitHub lists. Turn on **Enforce HTTPS**.

---

## Works on phones and desktops

- Responsive from 320 px phones to wide desktop monitors. The page never scrolls sideways.
- Large, readable text on phones (about 19 px base, with nothing important under about 13 px), and tap targets of at least 44 px.
- Light and dark themes follow the device automatically, with a manual toggle in Settings.
- **Settings panel:** four text sizes (Smaller to Largest), high contrast, reduced motion (text appears at once, no timed effects), vibration on or off, and a light/dark/match-device theme.
- Respects the device's "reduce motion" setting.
- Tested at 320, 360, 390, 430, 768, 1024 and 1440 px wide, and a landscape phone, in current Chromium. Please also try it on a real iPhone and a real Android phone before you announce it.

## Privacy and safety

- **Nothing leaves the device.** No analytics, no cookies, no accounts, no ads, no network requests except the font stylesheet.
- **Saves stay in the browser.** Progress is kept in `sessionStorage`, and moves to `localStorage` only after the player agrees in Chapter 5. Keys: `fairest.act1.v1` (save) and `fairest.prefs.v1` (settings). Clearing site data erases the save.
- **Fonts** load from Google Fonts (Metamorphous, Nunito, IBM Plex Mono, Caveat). If you want zero third-party requests, download the four families, host them in the repo and change the single `<link rel="stylesheet">` near the top of `index.html`.
- The "Leave the Mirror" panel is always available from the Menu.

---

## Repository layout

```
index.html              The finished game (this is what Pages serves)
.nojekyll               Tells GitHub Pages to serve the file as-is
README.md               This file
docs/                   Screenshots and CHAPTER_MAP.md
src/                    Source files and build script
  data.js               Stats, classes, enemies, achievements, chapter titles, art
  scenes.js ... scenes6.js   The story, one file per act
  polish.css, hero.svg  Visual design layer and title illustration
  base.html             Engine and layout that the build script patches
  build.py              Applies the patches and joins the source files
  build_site.py         Builds ../index.html (run this one)
  tests/                Automated playthrough tests
```

## Editing the story

You only need Python 3.

```bash
cd src
python3 build_site.py     # rebuilds ../index.html
```

Each scene is a small object:

```js
SC.c21_in = {
  ch: 21,
  t: ['N: The girl leads you to a hidden camp.',
      'G: "Oh, that is just gossip."'],
  c: [{ l: 'Help Gretel with her puzzle', go: 'c21_jars' }]
};
```

Line prefixes: `G:` the Mirror, `S:` system message, `W:` a whisper, `P:` Pip, `N:` narration, `A:` an ally, `I:` an item (`name|rarity|stat|flavor`).

The sequel hook lives in `src/scenes6.js` (`SC.c37_hook`).

## Tests (optional)

```bash
cd src && python3 build_site.py   # the tests read the file this build creates
cd tests
npm install
node live.js     # one paced playthrough from the title to the sequel hook
node fuzz.js     # 30 random playthroughs; all should reach the ending
```

---

## Credits and rights

- Story, design and code: **[YOUR NAME OR PEN NAME]**.
- Built on public-domain fairy tales (the Brothers Grimm, Hans Christian Andersen, Charles Perrault). All characters in the game are public-domain figures or original creations.
- **Copyright (c) [YEAR] [YOUR NAME OR PEN NAME]. All rights reserved.** Add a `LICENSE` file if you want to allow others to reuse any part of this project; without one, others may view the page but not copy or redistribute it.

## Coming next

**Book Two: The Sleeping Court.** A hundred years of roses, a spindle that never stops spinning, and a Mirror that does not lie, but never wakes you up.
