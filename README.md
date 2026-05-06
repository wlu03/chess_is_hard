# Chess is Hard

A static research-style writeup of the EXPTIME-completeness of generalized $n \times n$ chess.

## Files

- `index.html` — single-page article
- `style.css` — typography & layout
- `images/` — figures (FL81 architecture, gadget diagrams)
- `vercel.json` — caching & header config

Math is rendered client-side with MathJax 3 via CDN.

## Local preview

```sh
python3 -m http.server 8000
# open http://localhost:8000
```

## Deploying to Vercel

### Option A — Vercel CLI (fastest)

```sh
npm i -g vercel        # one-time
vercel                 # preview deploy, follow prompts
vercel --prod          # production deploy
```

When prompted:
- *Set up and deploy?* → **Y**
- *Which scope?* → your account
- *Link to existing project?* → **N** (first time)
- *Project name* → `chess-is-hard` (or whatever you want)
- *Directory* → `./` (default)
- *Override settings?* → **N**

Vercel auto-detects this as a static site — no build step required.

### Option B — GitHub + Vercel dashboard

1. `git add . && git commit -m "site" && git push`
2. Go to <https://vercel.com/new>, import the repo
3. Framework preset: **Other** · Build command: *(blank)* · Output directory: `./`
4. Click **Deploy**

Subsequent pushes to the default branch auto-deploy.
