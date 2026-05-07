# MediCore Hospital Management System — Deployment Guide

## What's Included
- `hospital-management-system.html` — single self-contained file, no dependencies to install

---

## Option 1 — GitHub Pages (Free, Recommended)

### Step 1 — Create a GitHub account
Go to https://github.com and sign up (free).

### Step 2 — Create a new repository
1. Click **New** → Repository
2. Name it: `hospital-management-system`
3. Set to **Public**
4. Click **Create repository**

### Step 3 — Upload the file
1. Click **Add file → Upload files**
2. Drag `hospital-management-system.html` into the box
3. **Important:** Rename the file to `index.html` before uploading (GitHub Pages serves `index.html` as the homepage)
4. Click **Commit changes**

### Step 4 — Enable GitHub Pages
1. Go to **Settings → Pages** (left sidebar)
2. Under **Source**, select `Deploy from a branch`
3. Branch: `main` / folder: `/ (root)`
4. Click **Save**

### Step 5 — Access your site
After 1–2 minutes, your app will be live at:
```
https://YOUR_USERNAME.github.io/hospital-management-system/
```

---

## Option 2 — Netlify (Free, Easiest)

### Step 1
Go to https://netlify.com and sign up (free).

### Step 2
On the dashboard, find the box that says **"Drag and drop your site folder here"**.

### Step 3
Rename your file to `index.html`, then drag and drop it directly onto that box.

### Step 4
Netlify will instantly deploy it and give you a URL like:
```
https://random-name-123.netlify.app
```
You can customize this URL in site settings.

---

## Option 3 — Vercel (Free)

### Step 1
Go to https://vercel.com and sign up with GitHub.

### Step 2
Create a folder on your computer called `hms-app` and place `index.html` inside it.

### Step 3
Install Vercel CLI (requires Node.js):
```bash
npm install -g vercel
```

### Step 4
In terminal, navigate to the folder and run:
```bash
cd hms-app
vercel
```
Follow the prompts. Your app will be live at:
```
https://hms-app.vercel.app
```

---

## Option 4 — Open Locally (No Server Needed)

Just double-click `hospital-management-system.html` in your file explorer — it opens directly in any browser (Chrome, Firefox, Edge).

No internet, no server, no installation required.

---

## File Structure

```
hospital-management-system.html   ← entire app in one file
```

Everything is self-contained: HTML + CSS + JavaScript in a single file.
All fonts load from Google Fonts (requires internet for styling).

---

## How to Customize

### Change hospital name
Open the file in any text editor (Notepad, VS Code) and find:
```html
<span class="logo-name">MediCore
```
Replace `MediCore` with your hospital name.

### Change currency
Find all instances of `₹` and replace with your currency symbol (`$`, `€`, `£`, etc.).

### Add more doctors to the default list
Find `let doctors = [` in the `<script>` section and add entries following the same format.

### Change the color theme (primary blue)
Find `:root {` near the top and change:
```css
--primary: #1a56db;
```
to any hex color of your choice.

---

## Features Summary

| Module             | Features                                                    |
|--------------------|-------------------------------------------------------------|
| Dashboard          | Stats overview, bed occupancy, recent appointments          |
| Patient Registration | Add, search, toggle status, delete patient records        |
| Doctors & Staff    | Add, search, toggle availability, delete staff records      |
| Appointments       | Book, confirm, cancel appointments with status tracking     |
| Billing & Payments | Generate invoices, mark paid, track outstanding balances    |

---

## Browser Compatibility

| Browser | Support |
|---------|---------|
| Chrome 90+ | ✅ Full |
| Firefox 88+ | ✅ Full |
| Edge 90+ | ✅ Full |
| Safari 14+ | ✅ Full |
| Mobile browsers | ✅ Responsive |

---

## Notes

- **Data is not saved between sessions** — refreshing the page resets to default demo data. To add persistent storage, integrate a backend (Node.js + MongoDB) or use localStorage.
- This is a frontend-only prototype — suitable for demos, presentations, and learning.
- For production hospital use, add authentication and a backend database.

---

*MediCore HMS — Built with HTML, CSS & JavaScript | No frameworks required*
