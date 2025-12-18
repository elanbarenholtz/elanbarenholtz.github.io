# Website Development Session Log
**Date:** December 7, 2024

## What We Built

Created a professional single-page academic website for Elan Barenholtz showcasing the Autoregressive Brain research framework.

## Files Created

All files are located in: `/Users/elanbarenholtz/outputs/`

1. **index.html** (27KB)
   - Single-page website with embedded CSS
   - Sections: Hero, Theory, Key Propositions, Research, Evidence, Writing, Affiliations, Contact
   - Mobile responsive, no external dependencies except Google Fonts
   - Color scheme: Deep teal accent (#1a5f7a) on clean academic layout

2. **elan-headshot.jpg** (476KB)
   - Professional headshot displayed as circle in hero section
   - Copied from: `/Users/elanbarenholtz/Desktop/elan_headshot.jpg`

3. **README.md** (3.5KB)
   - Deployment instructions for GitHub Pages, Netlify, Vercel
   - Customization guide

## Deployed To

- **Live Site:** https://elanbarenholtz.github.io/
- **GitHub Repo:** https://github.com/elanbarenholtz/elanbarenholtz.github.io
- **Branches:** Both `main` and `master` (GitHub Pages deploys from `master`)

## Git Configuration

```bash
Repository: https://github.com/elanbarenholtz/elanbarenholtz.github.io.git
Local Path: /Users/elanbarenholtz/outputs/
Initial Commit: 186c865 "New academic website featuring autoregressive brain research"
```

---

## How to Resume This Project Later

### 1. Access Your Local Files

```bash
cd ~/outputs
ls -la
```

Your files are permanently saved at `/Users/elanbarenholtz/outputs/`

### 2. Make Edits to the Website

```bash
cd ~/outputs
# Edit files (use any text editor or IDE)
open index.html  # Opens in default browser to preview
```

### 3. Push Changes to GitHub (Updates Live Site)

```bash
cd ~/outputs
git add .
git commit -m "Description of your changes"
git push origin main
git push origin main:master
```

**Important:** You must push to BOTH `main` and `master` branches. The live site deploys from `master`.

### 4. Or Clone from GitHub (On Any Machine)

```bash
git clone https://github.com/elanbarenholtz/elanbarenholtz.github.io.git
cd elanbarenholtz.github.io
# Make changes, then push as above
```

### 5. Quick Edits via GitHub Web Interface

1. Go to: https://github.com/elanbarenholtz/elanbarenholtz.github.io
2. Click on `index.html`
3. Click the pencil icon (Edit this file)
4. Make changes
5. Commit directly to `master` branch
6. Changes deploy automatically to https://elanbarenholtz.github.io/

---

## Common Tasks

### Preview Changes Locally
```bash
cd ~/outputs
open index.html  # Opens in browser
```

### Update Content
Edit `index.html` in any text editor. All content is in the `<body>` section with clear comments like:
- `<!-- Hero Section -->`
- `<!-- The Autoregressive Brain -->`
- `<!-- Key Propositions -->`
- etc.

### Change Colors
Edit the CSS variables at the top of `index.html` (around line 17):
```css
:root {
    --primary-color: #1a5f7a;  /* Change this for different accent color */
}
```

### Replace Headshot
```bash
cp /path/to/new-image.jpg ~/outputs/elan-headshot.jpg
git add elan-headshot.jpg
git commit -m "Update headshot"
git push origin main
git push origin main:master
```

---

## Troubleshooting

### Site Not Updating After Push
1. Wait 2-5 minutes for GitHub Pages to rebuild
2. Check build status: https://github.com/elanbarenholtz/elanbarenholtz.github.io/actions
3. Hard refresh browser: `Cmd + Shift + R`
4. Try incognito window to bypass cache

### Verify What's Live
```bash
curl -s https://elanbarenholtz.github.io/ | head -20
```

### Check Git Status
```bash
cd ~/outputs
git status
git log --oneline -n 5
git remote -v
```

---

## Website Structure

The site is a single HTML file with embedded CSS. No build process, no dependencies.

**Sections (in order):**
1. Navigation (fixed top bar)
2. Hero (photo + intro)
3. The Autoregressive Brain (theory overview)
4. Key Propositions (4 cards)
5. Current Research (3 items)
6. Empirical Evidence (morphosyntax experiment)
7. Writing & Media (Substack, podcast links)
8. Affiliations (Center for Future Mind, MPCR Lab)
9. Contact
10. Footer

**Technology Stack:**
- Pure HTML5 + CSS3
- Google Fonts: Inter (body), Merriweather (optional serif)
- No JavaScript
- Mobile responsive (breakpoint: 768px)

---

## Contact Info on Site

- Email: ebarenholtz@fau.edu
- Twitter: @ebarenholtz
- Substack: generativebrain
- Theory of Everything Podcast: 2 episodes linked
- Center for Future Mind: https://www.fau.edu/future-mind/
- MPCR Lab: http://mpcrlab.com/

---

## Next Steps (If Needed)

1. **Custom Domain:** Configure in GitHub repo Settings → Pages → Custom domain
2. **Add Analytics:** Insert Google Analytics or similar tracking code
3. **Add More Content:** Edit `index.html` to add publications, CV, etc.
4. **SEO Optimization:** Add meta tags for social sharing (Open Graph, Twitter Cards)

---

## Quick Reference Commands

```bash
# Navigate to project
cd ~/outputs

# View files
ls -lh

# Preview in browser
open index.html

# Check git status
git status

# Make changes and push
git add .
git commit -m "Your message"
git push origin main
git push origin main:master

# View live site
open https://elanbarenholtz.github.io/
```

---

**End of Session Log**
