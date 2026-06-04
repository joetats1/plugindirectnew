# PluginDirect.co.uk

The UK's first plug-in solar comparison site. Fully static HTML — no build tools, no server, no dependencies.

## Deploy in 60 seconds

### Option A — GitHub Pages (free, recommended)
1. Push this repository to GitHub
2. Go to **Settings → Pages**
3. Set **Source** to `main` branch, `/ (root)` folder
4. Click **Save**
5. Your site is live at `https://yourusername.github.io/plugindirect`
6. Point your custom domain `plugindirect.co.uk` to GitHub Pages:
   - Add a `CNAME` file containing `plugindirect.co.uk` (already included)
   - In your domain registrar (GoDaddy/Namecheap etc), add these DNS records:
     ```
     A     @     185.199.108.153
     A     @     185.199.109.153
     A     @     185.199.110.153
     A     @     185.199.111.153
     CNAME www   yourusername.github.io
     ```

### Option B — Netlify (free, even faster)
1. Go to [netlify.com/drop](https://netlify.com/drop)
2. Drag the entire folder onto the deploy zone
3. Live in 30 seconds — then add your custom domain in Settings → Domain

### Option C — Bluehost (existing hosting)
1. Log in to Bluehost → Advanced → File Manager
2. Navigate to `public_html`
3. Upload `index.html`
4. Done

## File structure

```
plugindirect/
├── index.html          ← The entire site (single file)
├── README.md           ← This file
├── CNAME               ← Custom domain for GitHub Pages
├── .gitignore          ← Excludes OS clutter
└── LICENSE             ← MIT licence
```

## Before you launch — checklist

- [ ] Sign EcoFlow affiliate programme (Awin merchant 51797) — eu.affiliate@ecoflow.com
- [ ] Sign Anker affiliate programme (Webgains prog 289655) — ankersolix.com/uk/become-an-affiliate
- [ ] Replace product card URLs with tracked affiliate links
- [ ] Create Trustpilot business account at trustpilot.com/business
- [ ] Submit to Google Search Console — search.google.com/search-console
- [ ] Set up Google Analytics 4 — analytics.google.com
- [ ] Update `og:image` meta tag to a real hosted image URL
- [ ] Update canonical URL in `<head>` if domain changes
- [ ] Test all 6 product "View Deal" buttons link correctly
- [ ] Read the LEGAL.md file and action every item

## Tech stack

No framework. No build step. No npm install.

- **HTML/CSS/JS** — single `index.html`, ~4,800 lines
- **Fonts** — Syne + DM Sans via Google Fonts (non-blocking)
- **Charts** — Chart.js loaded from CDN only when savings dashboard scrolls into view
- **AI features** — Anthropic API (DNO certificate email, photo analysis) — requires API key
- **Images** — Unsplash hotlinks (replace with self-hosted for production)

## Updating the site

Every update is a new `index.html`. Workflow:
1. Request changes from Claude in your conversation
2. Download the updated file
3. Rename to `index.html`
4. `git add index.html && git commit -m "Update site" && git push`
5. GitHub Pages deploys automatically within 60 seconds

## Affiliate links

All product links currently point to brand homepages. Once your affiliate accounts are approved:

| Brand | Replace `window.open('URL')` with |
|-------|-----------------------------------|
| EcoFlow | Your Awin tracked link |
| Anker | Your Webgains tracked link |
| Zendure | Your Zendure direct link |
| Marstek | Your Marstek direct link |
| Hoymiles | Your Hoymiles direct link |
| Thunder Energy | Your Thunder Energy direct link |
