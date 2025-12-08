# Elan Barenholtz - Academic Website

A clean, modern single-page website showcasing research on the autoregressive brain framework.

## Files

- `index.html` - Main website file (self-contained with embedded CSS)
- `elan-headshot.jpg` - Headshot image
- `README.md` - This file

### 2. Test Locally

Open `index.html` in your web browser to preview the site locally. All styles are embedded, so it works without a server.

## Deployment Options

### Option 1: GitHub Pages (Recommended)

1. **Create a GitHub repository:**
   ```bash
   cd outputs
   git init
   git add .
   git commit -m "Initial commit: Academic website"
   ```

2. **Push to GitHub:**
   ```bash
   # Create a new repository on GitHub (e.g., elan-barenholtz.github.io)
   git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPO-NAME.git
   git branch -M main
   git push -u origin main
   ```

3. **Enable GitHub Pages:**
   - Go to your repository on GitHub
   - Click Settings → Pages
   - Under "Source", select "main" branch
   - Click Save
   - Your site will be live at `https://YOUR-USERNAME.github.io/YOUR-REPO-NAME/`

4. **Custom Domain (Optional):**
   - In repository Settings → Pages → Custom domain
   - Enter your domain (e.g., `elanbarenholtz.com`)
   - Follow GitHub's instructions to configure DNS

### Option 2: Netlify

1. **Via Netlify Drop (Easiest):**
   - Go to [Netlify Drop](https://app.netlify.com/drop)
   - Drag and drop the `outputs` folder
   - Your site will be live instantly with a random URL
   - You can claim the site and customize the URL or add a custom domain

2. **Via Git (Recommended for updates):**
   - Push your code to GitHub (see GitHub Pages steps above)
   - Log in to [Netlify](https://www.netlify.com/)
   - Click "New site from Git"
   - Connect your GitHub repository
   - Deploy settings:
     - Build command: (leave empty)
     - Publish directory: `.` or `/`
   - Click "Deploy site"
   - Your site will be live at `random-name.netlify.app`
   - You can customize the subdomain or add a custom domain in Site settings

### Option 3: Vercel

1. **Via Vercel CLI:**
   ```bash
   cd outputs
   npm i -g vercel
   vercel
   ```
   Follow the prompts to deploy.

2. **Via Vercel Dashboard:**
   - Push your code to GitHub
   - Log in to [Vercel](https://vercel.com/)
   - Click "New Project"
   - Import your GitHub repository
   - Click "Deploy"
   - Your site will be live at `your-project.vercel.app`

### Option 4: Traditional Web Hosting

Upload all files in the `outputs` directory to your web hosting provider via FTP/SFTP:
- `index.html`
- `elan-headshot.png`

The site will work immediately as a static site.

## Customization

### Colors

The color scheme is defined in CSS variables at the top of `index.html` (around line 17):

```css
:root {
    --primary-color: #1a5f7a;      /* Deep teal - change this for a different accent */
    --secondary-color: #2c3e50;     /* Dark blue-gray */
    --text-dark: #2d3748;           /* Main text color */
    --text-light: #4a5568;          /* Secondary text */
    --bg-light: #f7fafc;            /* Light background */
}
```

### Fonts

The site uses Google Fonts (Inter for body, Merriweather for optional serifs). To change fonts, edit line 9 in `index.html`.

### Content

All content is in the HTML body. Each section is clearly labeled with comments like `<!-- Hero Section -->`.

## Browser Support

- Modern browsers (Chrome, Firefox, Safari, Edge)
- Mobile responsive
- No JavaScript required (pure HTML/CSS)

## License

Content © 2025 Elan Barenholtz. Code structure may be reused with attribution.
