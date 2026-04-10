# Snap & Sell — Setup Guide (15 minutes)

You'll create a website link you can share in your WhatsApp group. Everyone who taps it can photograph items and get instant sale listings.

---

## Step 1: Get an Anthropic API Key (5 min)

1. Go to **https://console.anthropic.com**
2. Click **Sign Up** and create an account (use Google or email)
3. Once logged in, click **API Keys** in the left menu
4. Click **Create Key**, give it a name like "snap-and-sell"
5. **Copy the key** — it looks like `sk-ant-api03-xxxxx...` — save it somewhere safe
6. Go to **Settings → Billing** and add a payment method
7. Go to **Settings → Limits** and set a **monthly spending limit** (e.g. $5 = ~₪18). This guarantees you'll never be charged more than this.

---

## Step 2: Create a Vercel Account (2 min)

1. Go to **https://vercel.com**
2. Click **Sign Up**
3. Sign up with **Google** or **GitHub** (Google is easiest)

---

## Step 3: Deploy the App (5 min)

### Option A — Using GitHub (recommended)

1. Go to **https://github.com** and sign in (or create an account)
2. Click the **+** icon → **New repository**
3. Name it `snap-and-sell`, keep it **Public**, click **Create repository**
4. Click **"uploading an existing file"** link
5. Unzip the `snap-and-sell.zip` file on your computer
6. Drag ALL the files and folders into GitHub's upload area:
   - `api/` folder (contains `analyze.js`)
   - `public/` folder (contains `index.html`)
   - `vercel.json`
7. Click **Commit changes**
8. Go back to **https://vercel.com/dashboard**
9. Click **Add New → Project**
10. Select your `snap-and-sell` repository
11. Click **Deploy** — don't change any settings

### Option B — Direct Upload

1. Go to **https://vercel.com/dashboard**
2. Click **Add New → Project**
3. Choose **"Import from folder"** or drag-and-drop the unzipped folder
4. Click **Deploy**

---

## Step 4: Add Your API Key (2 min)

1. After deploying, go to your project on Vercel
2. Click **Settings** → **Environment Variables**
3. Add a new variable:
   - **Name:** `ANTHROPIC_API_KEY`
   - **Value:** paste your API key from Step 1
4. Click **Save**
5. Go to **Deployments** tab → click the **⋯** menu on the latest deployment → **Redeploy**

---

## Step 5: Share the Link! (1 min)

1. Go to your Vercel dashboard
2. Your site URL is shown at the top — something like `snap-and-sell.vercel.app`
3. Copy it and share in your WhatsApp group!

You can write something like:

> 📸 מוכרים משהו? לחצו על הלינק, צלמו את הפריט, וקבלו מודעת מכירה מוכנה תוך שניות!
> https://snap-and-sell.vercel.app

---

## Managing Costs

- **Check usage:** https://console.anthropic.com → Usage
- **Change spending limit:** Settings → Limits
- **Shut it down instantly:** Delete the API key at console.anthropic.com, or delete the project on Vercel
- **Expected cost:** ~$0.01 per photo (~₪0.03). 500 photos ≈ $5 (₪18)

---

## Troubleshooting

**"API key not configured" error:**
→ Make sure you added the environment variable in Vercel (Step 4) and redeployed.

**"Analysis failed" error:**
→ Check that your Anthropic account has billing set up and the API key is correct.

**Site not loading:**
→ Wait 1-2 minutes after deploying. Try refreshing.

**Want to update the app?**
→ Edit the files on GitHub and Vercel will automatically redeploy.
