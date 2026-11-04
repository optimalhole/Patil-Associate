# Patil Associate — simple website

Plain HTML, CSS and JavaScript. No React, no build step, no install.
Bilingual (मराठी / English), responsive for phones, tablets and desktops.

## Run on your computer

Just double-click `index.html`, or serve the folder:

```bash
python3 -m http.server 8000     # then open http://localhost:8000
```

## Publish on GitHub Pages

1. Create a new repository on GitHub (e.g. `patil-associate`).
2. Upload all files in this folder (drag & drop on GitHub, or use git):
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin https://github.com/<your-username>/patil-associate.git
   git push -u origin main
   ```
3. Repo **Settings → Pages → Build and deployment**: Source = **Deploy from a branch**, Branch = **main**, folder = **/ (root)** → Save.
4. After about a minute the site is live at `https://<your-username>.github.io/patil-associate/`.

## Files

| File | Purpose |
|---|---|
| `index.html` | Home |
| `properties.html` | All properties with search and filters |
| `property.html?id=1` | Property detail |
| `about.html`, `videos.html`, `contact.html` | Other pages |
| `login.html`, `admin.html` | Sign in and simple admin panel |
| `404.html` | Page not found |
| `css/style.css` | All styling |
| `js/data.js` | Text (मराठी/English) and sample properties |
| `js/app.js` | Header, footer, language switch, page logic |

## Edit content

- Change wording: `js/data.js` (`translations`).
- Change sample properties and videos: `js/data.js` (`initialProperties`, `initialVideos`).
- Phone / email: `js/app.js` (footer) and `contact.html`.

## Before going live

- Demo admin login: `admin@patilassociate.in` / `Patil@123` (in `js/app.js`). It runs only in the browser — replace with real authentication (e.g. Firebase Auth).
- Admin changes are saved in the visitor's own browser only (localStorage). Use Firebase/Supabase to share them with everyone.
- The enquiry form shows a thank-you message only. Connect a service such as Formspree or Firebase in `js/app.js` (`pages.contact`).
