# Thread Works Studios — Website

A clean, minimal multi-page website for Thread Works Studios.

## Pages
- `index.html` — Home / Landing
- `services.html` — Services
- `gallery.html` — Gallery / Portfolio
- `about.html` — About Us
- `contact.html` — Contact / Quote Request

## Files
| File | Purpose |
|---|---|
| `style.css` | All styles |
| `nav.js` | Mobile hamburger menu |
| `logo-symbol.png` | Small logo used in nav & footer |
| `logo-full.png` | Full logo used on home & about |
| `vercel.json` | Clean URL config for Vercel |

---

## Deploying to GitHub + Vercel

### Step 1 — Push to GitHub
1. Create a new repository at github.com (e.g. `threadworks-studios`)
2. In your terminal, from this folder:
```bash
git init
git add .
git commit -m "Initial site"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/threadworks-studios.git
git push -u origin main
```

### Step 2 — Deploy on Vercel
1. Go to [vercel.com](https://vercel.com) and sign in with GitHub
2. Click **Add New → Project**
3. Import your `threadworks-studios` repo
4. Leave all settings as default — Vercel detects it as a static site automatically
5. Click **Deploy**

Your site will be live at `https://threadworks-studios.vercel.app` (or your custom domain).

### Step 3 — Custom Domain (optional)
In Vercel → Project Settings → Domains, add your domain (e.g. `threadworksstudios.com`) and follow the DNS instructions.

---

## Contact Form
The contact form uses `data-netlify="true"` by default. To use it:

**Option A — Netlify (if hosting on Netlify instead of Vercel):**
No changes needed, forms work automatically.

**Option B — Formspree (works with Vercel):**
1. Create a free account at [formspree.io](https://formspree.io)
2. Create a new form and copy your form ID
3. In `contact.html`, replace:
   ```html
   data-netlify="true" action="/thank-you.html"
   ```
   with:
   ```html
   action="https://formspree.io/f/YOUR_FORM_ID" method="POST"
   ```
4. Remove the `<input type="hidden" name="form-name" ...>` line

---

## Customization Checklist
- [ ] Replace `logo-symbol.png` and `logo-full.png` with your final logo files
- [ ] Replace all "Add photo here" placeholder boxes with real photos
- [ ] Update address, phone, email, and hours in `about.html` and `contact.html`
- [ ] Update Instagram handle in `contact.html`
- [ ] Set up contact form (Formspree recommended for Vercel)
- [ ] Update page `<title>` tags if needed
- [ ] Add Google Analytics or other tracking (optional)
