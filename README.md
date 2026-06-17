# aiseoa — Professional SEO Portfolio Website

A complete, multi-page SEO specialist website for Omar Salah / aiseoa.

## 📁 File Structure

```
aiseoa/
├── index.html          ← Homepage (Hero, Services, AI SEO, Results, Booking System)
├── about.html          ← About Omar Salah (Timeline, Skills, Certifications)
├── portfolio.html      ← SEO Case Studies with filter + modal
├── blog.html           ← Blog (ready for content, email subscribe)
├── css/
│   └── style.css       ← Shared styles for all pages
├── js/
│   ├── aiseoa.js       ← Shared JS (lang switcher, animations, hours)
│   └── components.js   ← Nav + Footer injected on every page
└── README.md
```

## 🚀 Deploy to GitHub Pages

1. Push all files to a GitHub repo (e.g. `aiseoa-website`)
2. Go to **Settings → Pages**
3. Set Source: **Deploy from branch → main → / (root)**
4. Your site will be live at `https://yourusername.github.io/aiseoa-website/`

## 🌐 Custom Domain (aiseoa.com)

1. In repo root, create a file named `CNAME` containing just: `aiseoa.com`
2. In your domain registrar DNS settings, add:
   - `A` record → `185.199.108.153`
   - `A` record → `185.199.109.153`
   - `A` record → `185.199.110.153`
   - `A` record → `185.199.111.153`
   - `CNAME` → `www` → `yourusername.github.io`

## 📧 Enable Contact Form (Formspree — Free)

1. Go to [formspree.io](https://formspree.io) and create a free account
2. Create a new form → copy your Form ID (e.g. `xabcdefg`)
3. In `index.html`, find the `submitBooking()` function and replace:
```javascript
// TODO: Replace with Formspree/EmailJS endpoint
fetch('https://formspree.io/f/YOUR_ID', {
  method: 'POST',
  headers: {'Content-Type': 'application/json'},
  body: JSON.stringify({ name, email, website, service: selectedService.name })
});
```

## 🌍 Languages

- English / Arabic toggle built-in (click EN/AR button in nav)
- Language preference saved in localStorage
- Add more translations in `js/aiseoa.js` inside the `i18n` object

## ⚙️ Customization Checklist

- [ ] Replace emoji avatar in `about.html` with your real photo
- [ ] Update LinkedIn / Twitter links in `js/components.js` footer
- [ ] Update `hello@aiseoa.com` with your real email
- [ ] Set up Formspree form ID in `index.html`
- [ ] Update working hours in `js/aiseoa.js` → `HOURS` object
- [ ] Add real client data to case studies in `portfolio.html`
- [ ] Add `CNAME` file for custom domain

## 🛠️ Tech Stack

- Pure HTML5 + CSS3 + Vanilla JavaScript
- Zero dependencies (no npm, no build step needed)
- Google Fonts (Inter + Space Grotesk + Cairo for Arabic)
- Fully responsive (mobile, tablet, desktop)
- RTL support for Arabic
- Intersection Observer for scroll animations
