# Stack vs Heap — Java Memory Inspector

An interactive, single-file explainer for how Java uses the **stack** and the
**heap**: primitives vs. references, aliasing, call frames, pass-by-value
(for both primitives and objects), and garbage collection with transitive
reachability. Step through curated snippets and watch memory update live, with
animated reference arrows.

Everything lives in `index.html` — no build step, no dependencies (fonts load
from Google Fonts over the network).

## Deploy to Vercel

### Option A — drag & drop (no CLI)
1. Go to https://vercel.com/new
2. Drag this whole folder onto the page (or zip it and upload).
3. Framework preset: **Other**. Build command: leave empty. Output dir: `./`
4. Click **Deploy**.

### Option B — Vercel CLI
```bash
npm i -g vercel      # if you don't have it
cd stack-heap-site
vercel               # follow the prompts (accept defaults)
vercel --prod        # promote to production
```

### Option C — Git
Push this folder to a GitHub/GitLab/Bitbucket repo, then "Import Project" in
Vercel and deploy. No settings needed — it's detected as a static site.

## Run locally
Just open `index.html` in a browser, or serve it:
```bash
python3 -m http.server 3000   # then visit http://localhost:3000
```

## Files
- `index.html` — the entire app
- `vercel.json` — static hosting config (clean URLs + basic security headers)
