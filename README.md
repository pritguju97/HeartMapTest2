# 💜 HeartSpeak Studio

**Where storytelling meets healing.**

A premium relationship wellness brand platform including:
- **HeartSpeak Studio** — Main brand website (coaching, products, podcast, about)
- **HeartMap** — Relationship check-in app with paywall, radar chart, guided conversations

---

## 🚀 Quick Deploy Options

### Option 1: GitHub Pages (Free, Instant)
1. Push this repo to GitHub
2. Go to **Settings → Pages**
3. Set source to `main` branch, `/public` folder
4. Your site is live at `https://yourusername.github.io/heartspeakstudio`

### Option 2: Netlify (Free, Custom Domain)
1. Connect your GitHub repo at [netlify.com](https://netlify.com)
2. Set **Publish directory** to `public`
3. Deploy — done in 30 seconds
4. Add your custom domain in Netlify settings

### Option 3: Vercel (Free, Fast CDN)
1. Import repo at [vercel.com](https://vercel.com)
2. Framework: **Other**
3. Output directory: `public`
4. Deploy

### Option 4: Manual Upload
- Upload the contents of `/public` to any web host (Squarespace, Hostinger, GoDaddy, etc.)

---

## 📁 Project Structure

```
heartspeakstudio/
├── public/
│   ├── index.html          ← HeartSpeak Studio main brand site
│   ├── heartmap.html       ← HeartMap relationship app
│   └── favicon.svg         ← Brand favicon
├── src/
│   ├── pages/              ← Individual page notes/docs
│   ├── components/         ← Component reference files
│   └── assets/             ← Fonts, images, icons (add yours here)
├── .github/
│   └── workflows/
│       └── deploy.yml      ← Auto-deploy to GitHub Pages on push
├── netlify.toml            ← Netlify config
├── vercel.json             ← Vercel config
├── CUSTOMIZATION.md        ← How to edit copy, colors, prices
└── README.md               ← This file
```

---

## ✏️ Customizing Your Site

See **CUSTOMIZATION.md** for a full guide on:
- Changing your name, bio, and photos
- Updating pricing
- Adding real payment links (Stripe, Gumroad, etc.)
- Connecting a real email form
- Adding your podcast RSS feed
- Custom domain setup

---

## 🎨 Brand Colors

| Name | Hex |
|------|-----|
| Lavender Deep | `#9178d8` |
| Maroon Light | `#c06b88` |
| Gold | `#c9a96e` |
| Blush | `#f4e0ec` |
| Cream | `#faf7f2` |

---

## 💳 Payment Integration (HeartMap)

The app currently uses a demo checkout. To add real payments:

1. **Stripe** — Replace checkout form with [Stripe Checkout](https://stripe.com/docs/payments/checkout)
2. **Gumroad** — Embed a Gumroad product overlay
3. **Lemon Squeezy** — Drop-in billing for digital products

See `CUSTOMIZATION.md` → Payment section for step-by-step.

---

## 📬 Contact Form Integration

Replace the demo form with:
- [Formspree](https://formspree.io) — Free, no backend needed
- [EmailJS](https://emailjs.com) — Send emails directly from the form
- [Netlify Forms](https://docs.netlify.com/forms/setup/) — If hosted on Netlify, just add `netlify` attribute

---

## 🔗 HeartMap App Access

HeartMap lives at `/heartmap.html`. Link to it from your studio site or host it as a subdomain.

Valid demo access codes (for testing):
- `HEART2024`
- `LOVE-LOOP`  
- `BETA-TEST`
- Any code 8+ characters

---

## 📄 License

© HeartSpeak Studio. All rights reserved.
