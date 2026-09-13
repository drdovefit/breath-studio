# Breath Studio

A configurable inhale / vacuum / exhale breathing timer for guiding a class.

`index.html` is self-contained — no build step, no dependencies. Open it in a browser, or
serve the folder and point a phone at it.

## Structure

A class is built in three levels:

- **Steps** — Inhale, Exhale, Stop, Swallow, Slow vacuum, Open ribs… each with a direction
  (rising / held / falling) and a length in seconds. Cue names are free text.
- **Sets** — a group of steps with a repeat count, e.g. Inhale/Exhale ×3. All the sets
  played through once make **one round** (one vacuum).
- **Positions** — each position has a name, its own number of rounds (vacuums), its own
  seconds to switch, and optionally its own timing that overrides the pattern.

The switch break can be turned off entirely, or skipped for a single position by setting
its switch time to 0.

## Screens

| Screen | What it does |
| --- | --- |
| Session | The live ring: phase cue, position and round readout, pause, hold-behaviour switch, record button |
| Patterns | Presets (4-7-8, Box, Coherent, Vacuum Breath) and the custom class |
| Build | Sets, positions, switch behaviour, and the record-while-it-plays panel |
| Voice | Per-cue takes (up to 10 each) and the whole-session voice-over |
| Settings | Colours and themes, background video, corner timer, countdown, music, the three volumes |

## Countdown, music and volumes

A countdown runs after each position change, before the breathing restarts — a tone per
second with a higher tone on the last. It can be switched off and its length set between 2
and 15 seconds. A background music track is your own uploaded audio file, looped under the
session. Cue/countdown, voice-over and music each have their own volume; music can be
adjusted while a session runs.

## Recording and media

Recording uses the browser's microphone, so the page must be served over `https://` or
opened from `localhost` — and you have to allow microphone access. Audio takes, voice-overs
and the background video are held in the browser session only; they are not uploaded
anywhere and they clear on reload.

## Hosting on GitHub Pages

1. Commit this folder to a repository.
2. Settings → Pages → deploy from the branch, root (or `/docs` if you move it there).
3. Pages serves over HTTPS, so the microphone works.
