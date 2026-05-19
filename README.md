# Psych Screening Form

A Filipino/Taglish psychiatric screening interview form built for UP-PGH Batch Masikhay 2026. Type into structured fields during the interview, then one-click copy a fully assembled SOAP note in the PGH template format.

**Live:** [your-deployment-url-here]

---

## Why

The standard PGH psych screening template is a paper-format document. During a 20–30 minute interview, a clinician needs to: ask questions, jot notes, and later transcribe into the SOAP format. This form collapses jotting and transcription — fill structured fields while interviewing, then paste the assembled note straight into your EMR or write-up.

## Features

- **Full Filipino/Taglish interview prompts** for every section (ID data → CC → HPI → ROS → PMH → FMH → OB-GYN → Substance → Anamnesis → MSE → Plan)
- **One-click SOAP assembly** matching the PGH 2026 template format
- **Structured MSE** — dropdowns for stature, mood, affect, etc. that compose the standard MSE paragraph for you
- **Auto-grouped ROS negatives** — denied items collapse into "Denies depressive, manic, psychotic, trauma symptoms"; positives listed individually with notes
- **C-SSRS-style SI ladder** with active-SI warning banner that surfaces when intent/plan is marked
- **Symptom checklist tabs** — SIGECAPS, DIGFAST, I CANT REST, Trauma+IANA, SCZ Spectrum
- **Autosave** to browser localStorage — survives accidental tab closes
- **Mobile-friendly** — usable on phone or tablet during bedside interviews
- **Offline-capable** — once loaded, runs without internet (only fonts come from CDN)

## Usage

1. Open the deployed URL in any browser.
2. Read questions from the italic `ASK` blocks as you interview the patient.
3. Type responses into the fields below each prompt.
4. Click **Copy Final Note** in the top bar → the entire SOAP note is on your clipboard, ready to paste.
5. Click **Clear (New Patient)** to wipe the form and start fresh.

Data persists in your browser between sessions until you Clear or wipe browser storage.

## Deploy to Vercel

### Option A — Vercel + GitHub (recommended)

1. Push this repo to GitHub.
2. Go to [vercel.com/new](https://vercel.com/new) and import the repo.
3. Framework preset: **Other** (Vercel auto-detects static HTML).
4. Click **Deploy**. Live in ~30 seconds.

Every push to `main` redeploys automatically.

### Option B — Vercel CLI

```bash
npm i -g vercel
vercel
```

Follow the prompts; pick **Static** when asked.

### Option C — GitHub Pages

In your repo settings → Pages → Source: `main` / `(root)`. Save. Live at `https://<username>.github.io/<repo>/`.

## Stack

Zero dependencies. Single `index.html` with vanilla HTML/CSS/JS. Google Fonts (Fraunces + IBM Plex) loaded from CDN.

## Privacy

No analytics, no telemetry, no server. All patient data stays in the user's browser localStorage. Clearing browser data deletes everything.

## License

MIT — feel free to fork, modify, share with your batch.

## Acknowledgments

Built on top of the official PGH Department of Psychiatry screening template (2026). Interview prompts adapted for natural Taglish flow.
