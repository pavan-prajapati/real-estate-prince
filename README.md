# Real Estate Portfolio — GitHub Pages Site

## 🚀 Deploy to GitHub Pages (Free)

1. Create a GitHub account at github.com
2. Click **New Repository** → name it `your-username.github.io` (for your main site)
   - OR any name like `realestate` (URL becomes `your-username.github.io/realestate`)
3. Upload all these files to the repo
4. Go to **Settings → Pages → Source: Deploy from branch → main → / (root)**
5. Your site is live in ~2 minutes!

---

## 📁 Folder Structure

```
/
├── index.html          ← Homepage (hero + project grid)
├── contact.html        ← Contact form
├── style.css           ← All styles (one file, all pages)
├── main.js             ← Nav toggle + project filter + scroll reveal
├── projects/
│   ├── sunrise-heights.html    ← Template project page
│   ├── green-valley.html       ← Copy & edit for each project
│   └── ...
└── assets/
    ├── images/         ← Project photos (JPG, <300KB each for speed)
    ├── videos/         ← Project walkthroughs (MP4)
    └── brochures/      ← PDF brochures
```

---

## ✏️ Customize

### Change your name/details
Edit `index.html` and `contact.html`:
- Replace "Rahul Sharma" with your name
- Replace "+91 99000 00000" with your number
- Replace "rahul@example.com" with your email
- Replace RERA number with yours

### Add a new project
1. Copy `projects/sunrise-heights.html` → rename it `projects/project-name.html`
2. Edit: title, description, location, RERA number, price table, map embed
3. Add a card in `index.html` inside the `projects-grid` div:
```html
<a href="projects/project-name.html" class="project-card" data-tags="panvel">
  <div class="card-img-wrap">
    <img src="assets/images/yourimage.jpg" alt="Project Name" />
    <div class="card-badge">New Launch</div>
  </div>
  <div class="card-body">
    <div class="card-meta">
      <span class="card-location">📍 Location</span>
      <span class="card-type">2 BHK</span>
    </div>
    <h3 class="card-title">Project Name</h3>
    <p class="card-price">Starting ₹XX L</p>
  </div>
</a>
```

### Filter tags (data-tags)
Add location tags on cards: `data-tags="panvel"` or `data-tags="panvel navi-mumbai"`
Add matching filter buttons in `index.html`:
```html
<button class="filter-btn" data-filter="kharghar">Kharghar</button>
```

### Add images
Drop `.jpg` files in `assets/images/` and reference them in your HTML:
```html
<img src="assets/images/myproject.jpg" alt="Project Name">
```
**Tip:** Compress images to under 300KB using squoosh.app (free)

### Map embed
1. Go to Google Maps → search your location
2. Click Share → Embed a map → Copy the iframe
3. Paste it inside `<div class="map-embed">` in the project page

### Contact form (no backend needed)
**Option A — Formspree (easiest, free):**
1. Sign up at formspree.io
2. Create a form → get your ID
3. Replace `YOUR_FORMSPREE_ID` in `contact.html`

**Option B — WhatsApp only:**
Change the submit button to a WhatsApp link:
```html
<a href="https://wa.me/91YOURNUMBER?text=Hi+Rahul" class="btn-submit">Chat on WhatsApp</a>
```

---

## 🎨 Color Customization
Edit `style.css` at the top — CSS variables:
```css
--gold: #c9a84c;        /* accent color */
--bg: #0f0e0c;          /* dark background */
--cream: #f2ece0;       /* text color */
```

---

## 💡 Tips
- Keep videos short (30–60 sec) or use YouTube embeds to keep the site fast
- Add `loading="lazy"` on `<img>` tags for faster mobile loading (already done in template)
- Test on mobile using Chrome DevTools (F12 → phone icon)
