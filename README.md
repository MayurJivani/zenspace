<div align="center">

# ZenSpace

**A quiet room in the browser, with a timer, a to-do list and your own music.**

[Open it](https://awt-zenspace.web.app) · [Futile Studio](https://futile.studio)

[![Live](https://img.shields.io/badge/live-awt--zenspace.web.app-c6ff00?style=flat-square&labelColor=0b0b0b)](https://awt-zenspace.web.app)
![React](https://img.shields.io/badge/React-18-0b0b0b?style=flat-square&logo=react)
![Create React App](https://img.shields.io/badge/Create%20React%20App-5-0b0b0b?style=flat-square)
![Last commit](https://img.shields.io/github/last-commit/MayurJivani/zenspace?style=flat-square&labelColor=0b0b0b&color=c6ff00)

</div>

> **Archive** · university project, started 2023 · live at awt-zenspace.web.app

## Overview

ZenSpace is a study room that runs in the browser. Pick a room, start a timer, keep a to-do list beside it, and put a YouTube video or your own music on in the background.

It started as a university project in April 2023 and the live site is still up.

## Features

- **Six spaces.** The window, book, plant, house, car and mountain buttons each play a background video from that space's list. Every press uses the next position in the lists, shared by all six spaces.
- **Customs.** Paste a YouTube link to change the background video, or an audio link to play music. Links without an 11-character video ID are ignored.
- **Music mode.** Submitting an audio link switches to the music track at full volume and mutes the background video. The speaker button switches back to the video's sound.
- **Timer.** Set hours, minutes and seconds, then play, pause or stop. When it runs out it shows "Timer is up!!".
- **To-do list.** Add tasks, tick them off and remove them. The list is not saved, so it clears on reload.

## Stack

- React 18 with Create React App (react-scripts 5.0.1)
- react-youtube for the embedded players
- react-use-todo for the to-do list state
- Boxicons (loaded from unpkg) and react-icons for the icons
- Firebase Hosting for the live site

## Running it locally

```bash
npm install
npm start      # http://localhost:3000
npm run build  # production bundle in build/
```

## Project structure

- `src/App.js` renders the sidebar.
- `src/Sidebar.js` holds the spaces, the Customs panel, the menu and the YouTube players.
- `src/CountDown.jsx` and `src/Timer.jsx` are the timer.
- `src/components/` has the to-do list pieces.
- `src/Backvid.js` and `src/Backaud.js` are older background players. They are commented out in `App.js`.

## Configuration

There are no environment variables. The YouTube video IDs for each space are hardcoded in `src/Sidebar.js`. Customs links are typed into the app and kept only in memory.

## Known gaps

- The Dashboard and Spaces menu items do not do anything yet.
- `npm test` runs the starter test in `src/App.test.js`, which looks for "learn react" text the app does not render. I have not run it, but by reading it, it will fail.
- The timer and to-do list are not saved between visits.
- The repo has no Firebase config file (no `firebase.json`), so the hosting setup is not in the repo.

## Licence

No licence file yet, all rights reserved.

---

<p align="center"><sub>Built by <a href="https://github.com/MayurJivani">Mayur Jivani</a> at <a href="https://futile.studio">Futile Studio</a>. Everything is futile. Do it anyway.</sub></p>
