# Photography Portfolio — GitHub Pages

A dark, editorial-style photography portfolio. Drop in your images, configure two services, and you're live.

---

## File structure

```
photography-portfolio/
├── index.html              ← Home page
├── css/
│   └── style.css
├── js/
│   └── main.js
├── images/
│   ├── hero-1.jpg          ← Hero grid images (4 total)
│   ├── hero-2.jpg
│   ├── hero-3.jpg
│   ├── hero-4.jpg
│   ├── cat-landscape.jpg   ← Category thumbnail images
│   ├── cat-portrait.jpg
│   ├── cat-concert.jpg
│   ├── cat-stylistic.jpg
│   ├── featured-1.jpg      ← Featured section images
│   ├── featured-2.jpg
│   ├── featured-3.jpg
│   ├── landscape/          ← Gallery images per category
│   │   ├── photo-01.jpg
│   │   ├── photo-01-full.jpg   ← Full-res for lightbox
│   │   └── ...
│   ├── portrait/
│   ├── concert/
│   └── stylistic/
└── pages/
    ├── landscape.html
    ├── portrait.html
    ├── concert.html
    ├── stylistic.html
    └── contact.html
```

---

## 1. Add your photos

Replace placeholder `src` attributes with your actual image paths.

**Tip on image sizes:**
- Thumbnails (gallery): 800–1200px wide, compressed JPEG (~200–400KB)
- Full-res (lightbox): up to 2000px wide (~500KB–1.5MB)
- Hero/category images: 1200px wide minimum

---

## 2. Set up the contact form (Formspree — free)

1. Go to **https://formspree.io** and sign up for free
2. Click **New Form**, give it a name
3. Copy your form endpoint — it looks like `https://formspree.io/f/xyzabcde`
4. In `pages/contact.html`, replace `YOUR_FORM_ID` with your ID:
   ```html
   <form action="https://formspree.io/f/xyzabcde" method="POST">
   ```
5. Also update the `_next` redirect URL to your GitHub Pages URL:
   ```html
   <input type="hidden" name="_next" value="https://YOURUSERNAME.github.io/REPO/pages/contact.html?sent=true">
   ```

Free tier: **50 submissions/month**. Upgrade at formspree.io for more.

**Alternative:** Web3Forms (https://web3forms.com) — free, unlimited submissions.

---

## 3. Add analytics & heatmaps

### Google Analytics 4 (page views, click tracking, demographics)
1. Go to https://analytics.google.com → create a Property
2. Get your **Measurement ID** (format: `G-XXXXXXXXXX`)
3. Uncomment and update the GA4 snippet in the `<head>` of **every HTML file**

### Microsoft Clarity (FREE heatmaps + session recordings)
1. Go to https://clarity.microsoft.com → create a Project
2. Copy the snippet with your **Project ID**
3. Uncomment and paste into the `<head>` of **every HTML file**

Clarity is completely free with no limits — it shows you heatmaps of exactly which photos and areas users click, and session recordings of real visits.

---

## 4. Deploy to GitHub Pages

1. Push this folder to a GitHub repository
2. Go to your repo → **Settings → Pages**
3. Set Source to **Deploy from a branch**, select `main` (or `master`), folder `/` (root)
4. Your site will be live at `https://YOURUSERNAME.github.io/REPO-NAME/`

---

## 5. Customise

- **Your name:** Search and replace `Your Name` / `Your.Name` across all HTML files
- **Your email:** Update `hello@yourname.com` in `contact.html`
- **Your location:** Update "Your City, Country" in `contact.html`
- **Social links:** Update Instagram/VSCO/500px handles in `contact.html`
- **Add a category:** Duplicate a gallery page, update the title/description/images, and add a card to `index.html`
- **Custom domain:** Add a `CNAME` file with your domain name to the repo root, then configure DNS

---

## Fonts

Uses Google Fonts:
- **Cormorant Garamond** — display/headings (serif, elegant)
- **Instrument Sans** — body/UI (clean, geometric)

Both load from `fonts.googleapis.com` — works automatically if you have an internet connection.
