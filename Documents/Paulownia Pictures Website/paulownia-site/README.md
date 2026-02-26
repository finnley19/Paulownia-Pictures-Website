# Paulownia Pictures Website
## Replacement site for paulowniapictures.com

---

## 📁 Files in this folder

```
paulownia-site/
├── index.html        ← Home page
├── about.html        ← About the film, cast, crew & reviews
├── screenings.html   ← Screenings & film festivals
├── gallery.html      ← Photo gallery
├── contact.html      ← Contact page
├── style.css         ← All styling (shared across pages)
├── images/           ← PUT ALL YOUR PHOTOS HERE
│   ├── home-hero.jpg        ← Main home page image
│   ├── gallery-01.jpg
│   ├── gallery-02.jpg
│   ... (up to gallery-10.jpg)
└── README.md         ← This file
```

---

## 🖼️ IMPORTANT: Adding your images

You need to place your saved photos into the `images/` folder.

### Home page image
- Name it `home-hero.jpg` (or edit `index.html` line 24 to match your filename)

### Gallery images
- Name them `gallery-01.jpg` through `gallery-10.jpg`
- OR edit the `src` values in `gallery.html` to match whatever filenames you used

---

## 🚀 Hosting on GitHub Pages (free)

1. Go to **github.com** and create a free account
2. Click **"New repository"**
   - Name it: `paulowniapictures`
   - Set it to **Public**
   - Click "Create repository"
3. On the next screen, click **"uploading an existing file"**
4. Drag and drop ALL files from this folder (including the `images/` folder)
5. Click **"Commit changes"**
6. Go to **Settings → Pages**
7. Under "Source", select **"Deploy from a branch"** → `main` → `/ (root)`
8. Click Save. After a minute, the site will be live at:
   `https://YOUR-USERNAME.github.io/paulowniapictures/`

---

## 🌐 Pointing paulowniapictures.com to GitHub Pages

### Step 1: Transfer domain from GoDaddy to Cloudflare
1. Go to **cloudflare.com** and create a free account
2. Click **"Add a site"** → enter `paulowniapictures.com`
3. Select the **Free plan**
4. Cloudflare will show you new nameservers (e.g. `aria.ns.cloudflare.com`)
5. Log into **GoDaddy**, go to your domain settings, and change the nameservers to the ones Cloudflare gave you
6. Wait up to 24 hours for it to take effect

### Step 2: Add DNS records in Cloudflare
In Cloudflare, go to DNS and add these records:

| Type  | Name | Value                    |
|-------|------|--------------------------|
| A     | @    | 185.199.108.153          |
| A     | @    | 185.199.109.153          |
| A     | @    | 185.199.110.153          |
| A     | @    | 185.199.111.153          |
| CNAME | www  | YOUR-USERNAME.github.io  |

### Step 3: Configure GitHub Pages custom domain
1. In your GitHub repository, go to **Settings → Pages**
2. Under "Custom domain", type `paulowniapictures.com`
3. Tick **"Enforce HTTPS"**
4. Add a file called `CNAME` to your repo containing just: `paulowniapictures.com`

Once DNS propagates, the site will be live at **www.paulowniapictures.com** — for free.

---

## 💰 Cost summary
- GitHub Pages hosting: **FREE**
- Cloudflare DNS: **FREE**  
- Domain renewal (transfer to Cloudflare Registrar): **~£8-10/year**
- **Saving: ~£170/year vs. current Wix + GoDaddy setup**

---

## ✏️ Updating the site in future
To make changes, just edit the HTML files and re-upload them to GitHub.
The site updates automatically within a minute or two.
