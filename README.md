# Wall of Shame — UNO Leaderboard

A single static page (`index.html`), no build step, no dependencies. Photos are
embedded directly in the HTML as base64, so there's nothing else to configure.

## Deploy to Vercel

**Option A — Vercel CLI (fastest)**
1. Install the CLI if you don't have it: `npm i -g vercel`
2. From inside this folder, run:
   ```
   vercel
   ```
3. Answer the prompts (link to a new project, accept defaults). Vercel will
   detect it as a static site automatically since there's an `index.html` at
   the root.
4. Run `vercel --prod` to push it to your production URL.

**Option B — GitHub + Vercel dashboard**
1. Push this folder to a new GitHub repo:
   ```
   git init
   git add .
   git commit -m "Wall of Shame leaderboard"
   git branch -M main
   git remote add origin <your-repo-url>
   git push -u origin main
   ```
2. Go to [vercel.com/new](https://vercel.com/new), import the repo.
3. Leave Framework Preset as **Other** — no build command, no output
   directory needed. Click Deploy.

## Updating scores or adding players

Open `index.html` and edit the card blocks directly — each player's name,
photo, and loss count live in plain view inside the `<div class="grid">`
section (and the top `<div class="card hero">` block for whoever's in 1st).
No rebuild step required; just save and redeploy.
