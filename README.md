# UNL NSBE Website

Official website for the University of Nebraska–Lincoln chapter of the National Society of Black Engineers.

🌐 **Live site:** [unlnsbe.org](https://unlnsbe.org)

---

## 📁 Project Structure

```
/
├── index.html       ← Main (and only) HTML file — all 5 sections are here
├── CNAME            ← Custom domain config for GitHub Pages
├── css/
│   └── style.css    ← All styles
└── js/
    └── main.js      ← Animations, nav behavior, form handling
```

---

## 🚀 Deploying to GitHub Pages

### Step 1 — Create the GitHub repo
1. Go to [github.com](https://github.com) and create a **new repository**
2. Name it anything (e.g. `unlnsbe-website` or `unlnsbe.github.io`)
3. Set it to **Public**

### Step 2 — Push this code
```bash
git init
git add .
git commit -m "Initial site"
git branch -M main
git remote add origin https://github.com/YOUR-ORG/YOUR-REPO.git
git push -u origin main
```

### Step 3 — Enable GitHub Pages
1. Go to your repo → **Settings** → **Pages**
2. Under **Source**, select **Deploy from a branch**
3. Choose branch: `main`, folder: `/ (root)`
4. Click **Save**

### Step 4 — Configure your custom domain (unlnsbe.org)
GitHub Pages needs a few DNS records at your domain registrar:

**A Records** — point your apex domain to GitHub:
```
A  @  185.199.108.153
A  @  185.199.109.153
A  @  185.199.110.153
A  @  185.199.111.153
```

**CNAME Record** — point www to GitHub Pages:
```
CNAME  www  YOUR-ORG.github.io
```

Then in GitHub → Settings → Pages → Custom domain: enter `unlnsbe.org` and check **Enforce HTTPS**.

DNS changes can take up to 24 hours to propagate.

---

## ✏️ Updating Content

### Change officer names/roles
Edit the **Members section** in `index.html` — search for `member-card` divs.  
To add a photo, replace the `<div class="member-initials">` with:
```html
<img src="images/yourname.jpg" alt="Name" style="width:100%;height:100%;object-fit:cover;">
```

### Update events
Edit the **Events section** in `index.html` — search for `event-card` divs.

### Update contact info
Search for `nsbe@unl.edu` and meeting details in the Contact section.

### Update social links
Search for `Instagram`, `LinkedIn`, `Twitter/X` in the Contact section and replace `href="#"` with real URLs.

---

## 🎨 Colors & Fonts
- **Black:** `#0a0a0a`
- **Gold:** `#C9A84C`
- **Fonts:** Playfair Display (headings) + DM Sans (body) — loaded from Google Fonts
