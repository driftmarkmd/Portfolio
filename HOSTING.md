# Hosting this portfolio for free

The site is plain static files (`index.html`, `styles.css`, `assets/`, `CREDITS.md`), so there's no build step. Upload the whole `portfolio/` folder as is. `preview.png` and `preview-mobile.png` are screenshots for review and don't need to be uploaded.

Size check: the three videos are web-compressed copies (~4 MB each, ~13 MB total), well under GitHub's 100 MB per-file limit. Nothing has been published yet.

## Option A: GitHub Pages (free)
1. Create a free GitHub account and a new **public** repository, e.g. `portfolio` (Pages on private repos requires a paid plan).
2. Upload the contents of this folder to the repo root: on GitHub, use **Add file → Upload files**, or run:
   ```bash
   cd portfolio
   git init && git add . && git commit -m "Portfolio site"
   git branch -M main
   git remote add origin https://github.com/<your-username>/portfolio.git
   git push -u origin main
   ```
3. In the repo, go to **Settings → Pages → Build and deployment**, set Source to **Deploy from a branch**, choose branch `main` and folder `/ (root)`, then click **Save**.
4. After a minute or two the site is live at `https://<your-username>.github.io/portfolio/`. All paths are relative, so the subfolder URL works.
5. Optional: if you name the repo `<your-username>.github.io`, the site is served at `https://<your-username>.github.io/`.
6. Optional custom domain: enter it under **Settings → Pages → Custom domain**, add the DNS records GitHub shows you, and then tick **Enforce HTTPS**.

## Option B: Vercel (free Hobby plan)
- **Drag and drop / CLI:** install the CLI with `npm i -g vercel`, then run `cd portfolio && vercel` and accept the defaults. Framework: "Other". There's no build command, and the output directory is `.`. Run `vercel --prod` to publish to production. You'll get a `https://<project>.vercel.app` URL.
- **From GitHub:** push the folder to a GitHub repo (as above). In Vercel, choose **Add New → Project → Import** the repo, set Framework Preset to **Other** and leave the build command empty, then click **Deploy**. Every push to `main` redeploys.
- Custom domain: go to **Project → Settings → Domains** and follow the DNS instructions.
- Note: Vercel's Hobby plan is for personal, non-commercial use. A portfolio is generally fine, but check Vercel's current fair-use terms. If in doubt, use GitHub Pages.

## Before you publish
- Replace the placeholders in the Contact section: `[your email]`, `[your Fiverr profile link]`, `[your Upwork profile link]`, `[your phone]`, `[your city / time zone]`. The mailto link also has a placeholder (`mailto:[your-email]`).
- Keep the "fictional business" and AI-voiceover disclosures and the credits link.
- The local starter pack prices are marked as drafts. Update them once you've set them.
