# 🚀 Deploy Guide — Step by Step

## Option 1: GitHub Pages (Free, 5 minutes)

### Step 1: Create a GitHub Account
Go to [github.com](https://github.com) and sign up if you don't have an account.

### Step 2: Create a New Repository
1. Click the **+** icon → **New repository**
2. Name it: `heartspeakstudio` (or any name you want)
3. Set to **Public** (required for free GitHub Pages)
4. Click **Create repository**

### Step 3: Upload Your Files
**Easy method (no coding required):**
1. On your new repo page, click **uploading an existing file**
2. Drag and drop ALL the files from this zip
3. Scroll down, click **Commit changes**

**Or use GitHub Desktop:**
1. Download [GitHub Desktop](https://desktop.github.com)
2. Clone your new repo
3. Copy all files from this zip into the repo folder
4. Commit and push

### Step 4: Enable GitHub Pages
1. Go to your repo → **Settings** tab
2. Scroll to **Pages** in the left sidebar
3. Under **Source**, select **Deploy from a branch**
4. Branch: `main`, Folder: `/public`
5. Click **Save**

### Step 5: Your Site is Live!
After ~2 minutes, your site will be at:
`https://YOUR-USERNAME.github.io/heartspeakstudio`

---

## Option 2: Netlify (Recommended — Custom Domain + Auto-Deploy)

### Step 1: Push to GitHub first (see above)

### Step 2: Connect to Netlify
1. Go to [netlify.com](https://netlify.com) → Sign up free
2. Click **Add new site** → **Import an existing project**
3. Connect GitHub → Select your `heartspeakstudio` repo
4. Build settings:
   - Build command: *(leave empty)*
   - Publish directory: `public`
5. Click **Deploy site**

### Step 3: Your site is live instantly!
Netlify gives you a random URL like `amazing-name-123.netlify.app`

### Step 4: Add Your Custom Domain
1. In Netlify → **Domain settings**
2. Click **Add custom domain**
3. Enter `heartspeakstudio.com` (or your domain)
4. Follow the DNS instructions to point your domain

---

## Option 3: Vercel (Super Fast CDN)

1. Go to [vercel.com](https://vercel.com) → Sign up with GitHub
2. Click **New Project** → Import your repo
3. Framework preset: **Other**
4. Output directory: `public`
5. Deploy!

---

## 🌐 Custom Domain Setup

### If you bought your domain from:

**GoDaddy:**
1. Login → My Products → DNS
2. Add CNAME record: `www` → `your-netlify-url.netlify.app`
3. Add A record: `@` → `75.2.60.5` (Netlify's IP)

**Squarespace Domains:**
1. Domains → Manage → DNS Settings
2. Add CNAME: `www` → your Netlify/Vercel URL

**Namecheap:**
1. Domain List → Manage → Advanced DNS
2. Add CNAME record pointing to your deployment URL

**Google Domains / Squarespace:**
Same process — add CNAME for `www` pointing to your host

---

## 📱 Testing Your Site

After deploying, test on:
- Desktop browser (Chrome, Safari, Firefox)
- Mobile (iPhone Safari, Android Chrome)
- Check both pages: `/` and `/heartmap.html`

---

## 🔄 Making Updates

After initial deploy, to update your site:
1. Edit the HTML files
2. Commit and push to GitHub
3. **Netlify/Vercel auto-deploys** within ~30 seconds
4. **GitHub Pages** updates within ~2 minutes

---

## 💬 Need Help?

Common issues:
- **Site shows 404**: Make sure files are in the `/public` folder
- **Styles not loading**: All CSS is inline — should work automatically  
- **Fonts not loading**: Requires internet connection (Google Fonts)
- **Form not sending**: See CUSTOMIZATION.md → Contact Form section

