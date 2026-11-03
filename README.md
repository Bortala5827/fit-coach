# Fit Coach

Voice-guided workouts in your browser. Press go, follow the coach — no account, no tracking, no training data leaves your device.

**Live:** https://fit.955827.xyz

## What's inside

9 entries — 8 coached workouts plus a custom Tabata timer — with real-time voice coaching, synced stick-figure demos, haptic cues and a progress ring:

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
| ⏲️ | **Tabata Timer** | Custom work / rest / rounds |

Every workout has three intensity levels (Light / Standard / Hard). Rest screens always tell you what's next, and a form cue stays on screen for the whole set. Finishing a session logs its duration, move and cue count.

## Highlights

- **Audio-first** — built with the Web Speech API, so you can train without watching the screen. Toggle voice off anytime.
- **Synced demos** — an animated stick figure mirrors every cue, so form is never a guess.
- **Three tabs** — Train / Technique / Records. Technique is a lookup of evidence-based form cues; Records keeps per-session duration, move, cue count and completion state, with a one-tap clear.
- **Optional background music** — the playlist is fetched from `voice.955827.xyz/products.json`, which points at the same self-hosted `cdn.955827.xyz/music/*.m4a` tracks the blog uses. It plays at low volume and ducks automatically whenever the coach speaks. Off by default; offline or an unreachable playlist silently falls back to no music and never blocks a workout.
- **Zero backend** — one HTML file. Works offline once loaded. All progress lives in `localStorage`.
- **Private by default** — no account, no analytics on your behavior, no data collection.
- **Deep links** — `/kegel`, `/boxing`, `/7min`, `/tabata`, `/guide`, `/records` … each is its own landing path.

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
