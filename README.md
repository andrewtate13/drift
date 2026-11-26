# Drift

Slow, dark, burn-in-safe visuals for whatever is playing on your Spotify account, made for an LG OLED's web browser.

- Four scenes: **Nebula**, **Eclipse**, **Silk**, **Melt** (the album cover itself, liquified). Colours come from the current cover.
- A now-playing card and synced lyrics that drift around the whole screen. Nothing stays still, so it's safe for the OLED.
- Can act as a Spotify speaker (Web Playback SDK): pick **Drift** in Spotify on your phone and the TV plays the music. If the TV's browser can't do that, it just mirrors whatever plays elsewhere.
- Keeps the TV awake with a dark looping video under the visuals. LG only skips its screensaver while a real video plays full screen (tested on a webOS TV with Chromium 87). After 30 minutes of nothing playing, the video stops and the TV may sleep normally.

## Setup

1. **Spotify app**: go to <https://developer.spotify.com/dashboard>, then *Create app*.
   - Name/description: anything (e.g. "Drift").
   - Redirect URI: the exact address of this page, including the trailing slash (e.g. `https://YOURNAME.github.io/drift/`).
   - APIs used: tick **Web API** and **Web Playback SDK**.
   - Save, then copy the **Client ID**, which goes into `CLIENT_ID` at the top of `index.html`.
   - Development mode allows 5 users, and the app owner needs Premium.
2. **TV**: open the Web Browser app, go to the page, press OK on **Connect Spotify**, log in once. Pin the page to the home screen from the browser menu.
3. **Daily use**: open Drift on the TV. In Spotify on your phone, tap the speaker icon and pick **Drift** (or just play anywhere, and Drift mirrors it).

Try it without Spotify: add `?demo` to the address. Log out / reset: add `?reset`.

## Remote

| Button | Does |
|---|---|
| OK (press the wheel) | play / pause |
| ◀ ▶ | change scene |
| ▲ ▼ | brightness |
| RED | hide / show the card |
| GREEN | lyrics on / off |
| YELLOW / BLUE | previous / next track |
| INFO | help |

Lyrics come from [LRCLIB](https://lrclib.net). Single file, no build step, no server.
