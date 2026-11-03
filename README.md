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
- **Daily Mix** — a science-based bodyweight circuit, either auto-built or picked à la carte. Choose a duration (10/15/20 min) and intensity for the auto circuit, or tap any of the 12 moves to order your own; hand-picked moves are still ordered cardio first, core last, never the same muscle group back to back. Follows ACSM and the 7-Minute Workout (Klika & Jordan 2013), and reuses the same voice cues, demos and form cues, so there is no new content to maintain.
- **Mid-set coaching** — long holds are not silent: a short form reminder and a pace nudge land at roughly 35% and 80% of every 20s+ interval, so the voice reacts while you work instead of only announcing the move.
- **Plan receipt with QR** — the circuit is printed on Records as a paper-style receipt (dashed cut lines, torn edge, `Ctrl+P` prints just the slip). The whole plan is encoded into a short `?mix=` code, so the QR carries the circuit itself with no backend and no plan database. Scan or paste the link to load the exact same circuit on another device — same `api.qrserver.com` generator as `rcj-card`.
- **Three tabs** — Train / Technique / Records. Technique is a lookup of evidence-based form cues; Records keeps per-session duration, move, cue count and completion state, plus the plan receipt, a one-tap clear and a CSV export.
- **English / 繁體中文** — the coach speaks both, preferring natural system voices (Samantha-class for English, Taiwan Mandarin for Chinese), with a 🎵 shortcut to the voice studio.
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
