# Fit Coach

Voice-guided workouts in your browser. Press go, follow the coach — no account, no tracking, no training data leaves your device.

**Live:** https://fit.955827.xyz

## What's inside

9 coached workouts plus a custom Tabata timer and a **Daily Mix** circuit generator — with real-time voice coaching, synced stick-figure demos, haptic cues and a progress ring:

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
- **Daily Mix** — a science-based random bodyweight circuit. Pick a duration (10/15/20 min) and intensity; moves are ordered warm-up → alternating lower/upper/core/cardio → cool-down, following ACSM and the 7-Minute Workout (Klika & Jordan 2013). Reuses the same voice cues, demos and form cues, so there is no new content to maintain. Shuffle for a new circuit.
- **Share & import a plan by QR** — the whole circuit is encoded into a short `?mix=` code, so a QR code carries the plan itself with no backend and no plan database. Scan or paste the link to load the exact same circuit on another device. Uses the same `api.qrserver.com` generator as `rcj-card`.
- **Three tabs** — Train / Technique / Records. Technique is a lookup of evidence-based form cues; Records keeps per-session duration, move, cue count and completion state, with a one-tap clear and a CSV export.
- **Zero backend** — one HTML file. Works offline once loaded. All progress lives in `localStorage`.
- **Private by default** — no account, no analytics on your behavior, no data collection.
- **Deep links** — `/kegel`, `/boxing`, `/7min`, `/tabata`, `/guide`, `/records` … plus `/?mix=<code>` to load a shared circuit.

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
