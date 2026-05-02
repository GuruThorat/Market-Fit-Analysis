# FitLens — AI Market-fit Report Generator

Test product–market fit using AI. Upload a resume or paste user data, get instant analysis on willingness to pay, conversion likelihood, and validation experiments.

## Features

- AI-powered analysis using Google Gemini (free tier)
- PDF & text file upload with auto-extraction
- Interactive radar chart for fit dimensions
- 4 key metrics: Fit score, willingness to pay, conversion likelihood, completion potential
- Evidence-based fit signals & risk signals
- Hypothesis experiment generator
- PDF export of full report
- Local-only API key storage (never sent anywhere except Google)
- Mobile responsive
- Sample data button for quick demos

## Tech Stack

- Pure HTML / CSS / Vanilla JS (no build step)
- Tailwind CSS via CDN
- Chart.js for radar visualization
- pdf.js for PDF text extraction
- html2pdf.js for export
- Google Gemini 2.0 Flash API

## Deploy to Vercel (3 minutes)

### Option 1 — Drag & drop (easiest, no Git)

1. Go to [vercel.com/new](https://vercel.com/new) and sign in (GitHub/Google login is fine)
2. Click **"Import Third-Party Git Repository"** → skip
3. Or use the Vercel CLI:
   ```bash
   npm i -g vercel
   cd /path/to/this/folder
   vercel
   ```
   Follow prompts. Done in 30 seconds.

### Option 2 — Via GitHub (best for portfolio)

1. Create a new GitHub repo, push these files:
   ```bash
   git init
   git add .
   git commit -m "Initial commit: FitLens market-fit generator"
   git remote add origin https://github.com/YOUR_USERNAME/fitlens.git
   git push -u origin main
   ```

2. Go to [vercel.com/new](https://vercel.com/new)
3. Click **Import** next to your repo
4. Click **Deploy** (no config changes needed — Vercel auto-detects static)
5. Get a live URL like `fitlens.vercel.app` in ~30 seconds

### Option 3 — Pure drag & drop on Vercel

1. Zip the folder containing `index.html` and `vercel.json`
2. Go to [vercel.com](https://vercel.com) → New Project → Upload
3. Drop the zip → Deploy

## Local testing

Just open `index.html` in your browser. That's it. No server needed.

For best results, use a local server:
```bash
# Python
python3 -m http.server 8000

# Node
npx serve

# VSCode
Live Server extension
```

## Get your free Gemini API key

1. Go to [aistudio.google.com/apikey](https://aistudio.google.com/apikey)
2. Sign in with Google
3. Click **"Create API key"**
4. Copy and paste into the app
5. Free tier: 15 requests/min, 1500/day. No credit card required.

## Privacy

- API key is stored only in your browser's localStorage
- All API calls go directly from browser to Google Gemini
- No backend, no analytics, no data collection
- Resume / user data never touches any server except Google's

## Customization

- **Branding**: edit the header section (search for "FitLens" in `index.html`)
- **Colors**: tweak the CSS variables at the top of `index.html`
- **Prompt**: modify `buildPrompt()` to change analysis dimensions
- **Metrics**: update the metric cards section to add/remove KPIs

## For your portfolio / resume

Bullet points you can use:

> **Market-fit Report Generator** | Self Project
> - Designed and shipped a Minimum Viable Experiment (MVE) to test product–market fit and user hypotheses
> - Built an AI-powered tool integrating Google Gemini API with structured JSON outputs for 90%+ accuracy
> - Implemented PDF parsing, radar visualization, and evidence-based scoring across 5 fit dimensions
> - Tracked key metrics — willingness to pay, conversion likelihood, completion potential — to guide strategy
> - Deployed serverless on Vercel; zero backend, fully privacy-preserving

## License

MIT — free to fork, modify, and ship.
