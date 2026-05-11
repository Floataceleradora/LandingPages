# Float — Brazil Week NYC

Static one-page site for Brazil Week NYC 2026.

## Deploy to Vercel

### Option A — GitHub + Vercel (recommended, auto-deploys on push)

1. Create a new GitHub repo (private if you want to keep it under wraps).
2. Push everything in this folder to that repo:
   ```bash
   cd "deploy"
   git init
   git add .
   git commit -m "Initial deploy"
   git branch -M main
   git remote add origin git@github.com:YOUR_USER/float-brazilweek-nyc.git
   git push -u origin main
   ```
3. Go to https://vercel.com/new
4. Import the GitHub repo. Framework preset: **Other** (it's just static files).
5. Click Deploy. You'll get a URL like `float-brazilweek-nyc-xxxx.vercel.app`.
6. (Optional) In Vercel project settings, add a custom domain — e.g. `nyc.floatbrasil.com` if you want it as a subdomain on your main site.

### Option B — Vercel CLI (fastest one-off)

```bash
npm install -g vercel
cd "deploy"
vercel
```

Follow the prompts. First time will ask to log in.

### Option C — Drag and drop

Go to https://vercel.com/new and drag the `deploy` folder onto the page. Done.

## What's in here

- `index.html` — the page
- `og.png` — 1200×630 preview that appears when the link is shared on WhatsApp, LinkedIn, Twitter
- `favicon-*.png` — browser tab icon at multiple resolutions

## Updating later

Edit the source file at `../Float-BrazilWeek-NYC.html`, then re-run the prep script to copy it back into this `deploy/` folder. If you're using Option A (GitHub), `git push` and Vercel re-deploys automatically.
