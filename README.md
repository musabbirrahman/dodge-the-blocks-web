# 🟩 Dodge the Blocks — Living Worlds

A browser game: dodge falling hazards across 11 biomes, each with its own weather, mechanics, wildlife and recorded ambience.

**Play:** `https://musabbirrahman.github.io/dodge-the-blocks/` (after enabling GitHub Pages)

## Features
- 11 biomes: slippery Ice, windy Forest, Desert sandstorms, Ocean currents, Rainforest lightning, Volcano geysers, low-gravity Galaxy, Mushroom spore clouds, Jungle coconut drops, Savanna stampedes, Cherry Blossom
- Modes: Classic, Speed Rush, Zen, Hardcore, Score Attack, Journey (new world every 45s)
- Dash (Shift / Z / X / ⚡ button / gamepad A), power-ups, combo meter, boss waves
- Coins, cube skins, achievements, day/night cycle, wildlife
- Keyboard, touch, and gamepad support; fullscreen; installable as an offline web app

## Run locally
Serve the folder (audio and the service worker need http, not file://):
```bash
python3 -m http.server 8080   # then open http://localhost:8080
```
(Opening `index.html` directly also works for gameplay and audio; installable/offline features need a server.)

## Controls
← → / A D move · Shift, Z or X dash · Space pause · Gamepad: stick/d-pad, A dash, Start pause · Touch: drag, or on-screen buttons

## Android APK (Capacitor)
```bash
mkdir www && cp -r index.html manifest.webmanifest sw.js icons sounds www/
npm init -y && npm i @capacitor/core @capacitor/cli @capacitor/android
npx cap init "Dodge the Blocks" com.yourname.dodgeblocks --web-dir=www
npx cap add android && npx cap sync && npx cap open android
```
Then in Android Studio: **Build → Build APK(s)**. (`android/` is git-ignored.)

## Audio credits
Ambience recordings in `sounds/` come from Freesound / Pixabay-style sources (file names keep the author prefix). **Verify each file's license and add required attribution here before publishing or releasing on an app store.** Files were compressed to mono 72 kbps.

| File | Author prefix |
|---|---|
| dragon-studio-freezing-winter-wind | dragon-studio |
| alex_jauk-dreamy-land | alex_jauk |
| soul_serenity_sounds-distant-breeze | soul_serenity_sounds |
| audiopapkin-beautiful-birdsong-3 | audiopapkin |
| tanweraman-desert-wind-2 | tanweraman |
| enternalrainsounds-calm-rain-ambience | enternalrainsounds |
| 49656682-steady-rain-with-rolling-thunder | 49656682 |
| freesound_community-* (6 files) | freesound_community |

Game code: add your own license (e.g. MIT) as `LICENSE`.


## Mobile
Touch controls live inside the game area (work in fullscreen): hold ◀ ▶ or drag anywhere on the playfield to move, ⚡ to dash, ⏸ / ⛶ in the top bar. Long-press text selection and context menus are disabled. Worlds, modes and audio are below the game (use "Worlds & Modes").

Portrait phones now get a taller playfield (more reaction time) with controls in a band under it; landscape keeps the wide view. A rotate hint shows on the start screen in portrait.
