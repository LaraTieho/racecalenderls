# Lesotho Race Calendar 2026

Made to track running dates for 2026 within Lesotho — a single-page static site listing 2026 road races in Lesotho and nearby South African border towns, searchable and filterable by month and distance, with entry fees and registration deadlines.

Source data: `Running Calender.xlsx` (kept in this repo for reference/updates). The race list is embedded directly in [index.html](index.html) as a JS array — there's no build step or backend.

## Updating race data

1. Edit `Running Calender.xlsx`, or edit the `races` array near the top of the `<script>` block in `index.html` directly.
2. Commit and push — Vercel redeploys automatically on push to `main`.

## Deploying to Vercel

This is a static site (one `index.html`, no framework, no build command), so Vercel's zero-config static detection handles it — no `vercel.json` needed.

**Option A — Git integration (recommended, auto-deploys on push):**
1. Go to https://vercel.com/new
2. Import the `racecalenderls` GitHub repository
3. Framework Preset: **Other** (static)
4. Build Command: *(leave empty)*
5. Output Directory: *(leave empty / root)*
6. Click **Deploy**

Every push to `main` will auto-deploy.

**Option B — Vercel CLI:**
```bash
npm i -g vercel
vercel        # preview deploy
vercel --prod # production deploy
```

## Local preview

Just open `index.html` in a browser, or serve it:
```bash
npx serve .
```
