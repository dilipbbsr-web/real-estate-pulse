# 🏙️ Real Estate Pulse — Setup Guide

## Step 1 — Set Up Formspree (Email Enquiries)

1. Go to **https://formspree.io** → Sign Up Free
2. Click **+ New Form** → Name it "Real Estate Enquiry"
3. Copy your **Form ID** (looks like: `xpzgkwlb`)
4. Open `index.html` → Find this line:
   ```
   action="https://formspree.io/f/YOUR_FORM_ID"
   ```
5. Replace `YOUR_FORM_ID` with your actual ID
6. Every enquiry will now arrive at your registered email ✅

---

## Step 2 — Upload to GitHub

1. Go to **github.com** → Sign in → **New Repository**
2. Name it: `real-estate-pulse`
3. Set to **Public** → Click **Create Repository**
4. Click **uploading an existing file**
5. Drag and drop **all files including the `.github` folder**
6. Click **Commit changes**

---

## Step 3 — Deploy Free on Netlify

1. Go to **netlify.com** → Sign Up (use GitHub account)
2. Click **Add new site → Import from Git**
3. Choose **GitHub** → Select `real-estate-pulse` repo
4. Build settings: leave all blank (it's pure HTML)
5. Click **Deploy site**
6. Your site is live at: `https://yourname.netlify.app` 🎉

### Custom domain name (free on Netlify):
- Netlify dashboard → **Site settings → Domain management**
- Click **Edit site name** → set to `realestatepulse`
- Your URL becomes: `https://realestatepulse.netlify.app`

---

## Step 4 — Daily Auto-Updates (GitHub Actions)

The `.github/workflows/daily-refresh.yml` file runs **every day at 6 AM IST** automatically.
- It updates `daily.json` with today's date
- Netlify detects the commit and auto-rebuilds the site
- The "Tip of the Day" rotates daily via JavaScript — no manual work needed

**To enable:** In GitHub repo → **Settings → Actions → General → Allow all actions** ✅

---

## Updating Content

To add new posts or tips: open `index.html` in GitHub's web editor, find the `posts` or `dailyTips` arrays in the `<script>` section, add your content, and commit. Netlify redeploys in ~30 seconds.
