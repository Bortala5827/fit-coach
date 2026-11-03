# Fit Coach

Voice-guided workouts in your browser. Press go, follow the coach — no account, no tracking, nothing leaves your device.

**Live:** https://fit-coach.pages.dev

## What's inside

8 guided workouts with real-time voice coaching, synced stick-figure demos, haptic cues and a progress ring:

| | Workout | Format |
|---|---|---|
| 🧘 | **Kegel** | Pelvic floor · hold/release cycles |
| 💪 | **Push-ups** | Paced reps with voice count |
| 🏋️ | **Squats** | Slow tempo, knees-out cues |
| 🔥 | **Sit-ups** | Core pacing, neck-safe cues |
| 🥊 | **Boxing** | Random combo callouts, 3–4 rounds |
| ⏱️ | **Plank** | 30/45/60s hold ladder |
| ⚡ | **7-Minute Workout** | 12 moves × 30s, science-backed circuit |
| 🦵 | **Calf Raises** | Full range, 3 × 20 |

Every workout has three intensity levels (Light / Standard / Hard). Rest screens always tell you what's next. Finishing a session earns your daily dot and streak.

## Highlights

- **Audio-first** — built with the Web Speech API, so you can train without watching the screen. Toggle voice off anytime.
- **Synced demos** — an animated stick figure mirrors every cue, so form is never a guess.
- **Zero backend** — one HTML file. Works offline once loaded. Progress (streak, 7-day history, level) lives in `localStorage`.
- **Private by default** — no account, no analytics on your behavior, no data collection.
- **Deep links** — `fit-coach.pages.dev/kegel`, `/boxing`, `/7min` … each workout is its own landing path.

## Run locally

```bash
npx http-server -p 8080
# open http://localhost:8080
```

Or just open `index.html` in a browser.

## Deploy

Static hosting ready — e.g. Cloudflare Pages:

```bash
wrangler pages deploy . --project-name fit-coach
```

## Tech

Vanilla HTML/CSS/JS, single file, zero dependencies, zero build step. MIT licensed.

## Disclaimer

Fit Coach offers fitness guidance, not medical advice. If you have pelvic pain, are recovering from surgery, or have any health concerns, consult a doctor first.
