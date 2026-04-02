# ✏️ HeartSpeak Studio — Customization Guide

Everything you need to make this site fully yours.

---

## 1. YOUR NAME & PERSONAL DETAILS

### HeartSpeak Studio (`public/index.html`)

Search for these placeholders and replace:

| Find | Replace with |
|------|-------------|
| `Your Name` | Your actual name |
| `HeartSpeak Studio` | Keep or rename your brand |
| `A brand at the intersection...` | Your own brand statement |
| `Social Psychology` | Your actual background |
| `Founder & Creator` | Your title |
| The `A` initial in the founder portrait | Your initial |

**Founder bio section** — find the `<p class="founder-body">` blocks and rewrite them with your story.

---

## 2. PROFILE PHOTO

The site uses an illustrated placeholder. To add your real photo:

1. Add your image to `src/assets/` (e.g., `founder.jpg`)
2. In `index.html`, find `.founder-portrait-frame` and replace the initials div with:

```html
<img src="../src/assets/founder.jpg" 
     alt="Your Name" 
     style="width:100%;height:100%;object-fit:cover;border-radius:var(--radius-lg);" />
```

---

## 3. PRICING

### HeartSpeak Studio products
Find these in `public/index.html` and update:
- `$27` → HeartMap product price
- `$22`, `$18`, `$15`, `$12`, `$16` → Your product prices
- `Free` → Keep or add a price

### HeartMap App (`public/heartmap.html`)
Find the `plans` object in the `<script>` section:
```javascript
const plans = {
  monthly: { name: 'Monthly Plan', price: '$14/mo' },
  annual:  { name: 'Annual Plan',  price: '$99/yr' },
  couple:  { name: 'Couples Plan', price: '$149/yr' }
};
```
Update prices to match your actual offering.

---

## 4. REAL PAYMENT LINKS

### Option A: Gumroad (Easiest)
1. Create products at [gumroad.com](https://gumroad.com)
2. Replace the `btn-primary` onclick handlers with:
```html
<a href="https://yourname.gumroad.com/l/heartmap" class="btn-primary">Get Access</a>
```

### Option B: Stripe Checkout
1. Create a Stripe account and products
2. Replace checkout modal with a link to your Stripe payment link:
```javascript
function openCheckout(plan) {
  window.location.href = 'https://buy.stripe.com/your_link_here';
}
```

### Option C: Lemon Squeezy
Similar to Stripe — create products and replace links.

---

## 5. CONTACT FORM (REAL EMAIL DELIVERY)

### Formspree (Recommended — free)
1. Sign up at [formspree.io](https://formspree.io)
2. Create a form and get your endpoint
3. In `index.html`, find the contact form and update:
```html
<form action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
  <!-- existing form fields -->
  <button type="submit" class="btn-primary">Send Message</button>
</form>
```

### Netlify Forms (If hosting on Netlify)
Add `netlify` to the form tag:
```html
<form name="contact" netlify>
```
Submissions go straight to your Netlify dashboard.

---

## 6. EMAIL LIST / NEWSLETTER

Replace the opt-in form with your email platform:

### Mailchimp
```html
<form action="https://yourlist.us1.list-manage.com/subscribe/post?u=XXXXX&id=XXXXX" method="post">
  <input type="email" name="EMAIL" class="optin-input" placeholder="your@email.com" />
  <button type="submit" class="btn-primary">Join Us</button>
</form>
```

### ConvertKit / Kit
Use their embeddable form code and style with your existing classes.

---

## 7. PODCAST EPISODES

In `public/index.html`, find the `.episodes-grid` section and update each episode card:

```html
<div class="episode-card" onclick="window.open('YOUR_EPISODE_LINK')">
  <div class="ep-num">Ep. 001</div>
  <div class="ep-title">Your Episode Title Here</div>
  <p class="ep-desc">Episode description...</p>
  <div class="ep-meta">
    <span class="ep-time">45 min</span>
    <span class="ep-cat attach">Category</span>
  </div>
</div>
```

---

## 8. BOOKING / DISCOVERY CALLS

Replace "Book a Discovery Call" buttons with your booking link:

**Calendly:**
```html
<a href="https://calendly.com/yourname/discovery-call" 
   target="_blank" class="btn-primary">Book a Discovery Call</a>
```

**Acuity Scheduling:**
```html
<a href="https://acuityscheduling.com/schedule.php?owner=XXXXXX" 
   target="_blank" class="btn-primary">Book a Discovery Call</a>
```

---

## 9. SOCIAL LINKS

In the footer of `index.html`, find:
```html
<li><a>Instagram</a></li>
<li><a>Newsletter</a></li>
```

Replace with:
```html
<li><a href="https://instagram.com/yourusername" target="_blank">Instagram</a></li>
<li><a href="https://open.spotify.com/show/your-show-id" target="_blank">Podcast</a></li>
```

---

## 10. FAVICON

Replace `public/favicon.svg` with your own logo SVG, or add a `.ico` file.
Update the `<link rel="icon">` in both HTML files if needed.

---

## 11. COLORS

All colors are CSS variables at the top of each HTML file. Find `:root {` and update:

```css
:root {
  --maroon: #8b3a52;        /* Main accent — change to your brand color */
  --maroon-light: #c06b88;  /* Secondary accent */
  --lavender-deep: #9178d8; /* Purple tones */
  --gold: #c9a96e;          /* Gold accent */
}
```

---

## 12. HEARTMAP ACCESS CODES

In `public/heartmap.html`, find:
```javascript
const validCodes = ['HEART2024','LOVE-LOOP','GIFT-ACCESS','BETA-TEST','COUPLE-CODE'];
```

Replace with your own codes. You can also make this dynamic by checking against a backend/database.

---

## 13. LINKING HEARTMAP FROM THE STUDIO SITE

The HeartMap app lives at `/heartmap.html`. To link to it:
```html
<a href="/heartmap.html" class="btn-primary">Open HeartMap App</a>
```

Or if using a subdomain (e.g., `app.heartspeakstudio.com`), host `heartmap.html` separately.

---

## 14. GOOGLE ANALYTICS

Add before `</head>` in both HTML files:
```html
<script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXXXXXXXX"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'G-XXXXXXXXXX');
</script>
```

---

## 15. SEO META TAGS

Add inside `<head>` of `index.html`:
```html
<meta name="description" content="HeartSpeak Studio — Where storytelling meets healing. Relationship coaching, digital wellness tools, and psychology-informed content." />
<meta property="og:title" content="HeartSpeak Studio" />
<meta property="og:description" content="Where storytelling meets healing." />
<meta property="og:image" content="https://yourdomain.com/og-image.jpg" />
<meta property="og:url" content="https://yourdomain.com" />
<meta name="twitter:card" content="summary_large_image" />
```

---

*Questions? Reach out via the contact form on your site.*
