# GitHub Pages Deployment Guide

## Prerequisites

- GitHub account
- Git installed locally (optional, can use GitHub Desktop or web interface)
- VS Code (recommended)

---

## Quick Deployment (Browser-Only Method)

No need to install Git! Do everything from GitHub:

### Step 1: Create GitHub Repository
1. Go to [github.com/new](https://github.com/new)
2. Repository name: `wedding-expense-app`
3. Description: "Wedding Budget Tracker with Real-Time Sync"
4. Choose Public (required for GitHub Pages free tier)
5. Click "Create Repository"

### Step 2: Upload Files
1. In your new repository, click "Add file" → "Upload files"
2. Drag and drop these files:
   - `index.html` (main app file)
   - `README.md` (documentation)
   - `.gitignore` (optional, but recommended)
3. Click "Commit changes"

### Step 3: Enable GitHub Pages
1. Go to repository Settings
2. Scroll to "Pages" section (left sidebar)
3. Under "Source", select:
   - Branch: `main`
   - Folder: `/ (root)`
4. Click "Save"
5. Wait 1-2 minutes for deployment
6. Your site will be live at: `https://YOUR-USERNAME.github.io/wedding-expense-app/`

---

## Local Git Method (Recommended)

### Step 1: Install Git
- **Windows**: Download from [git-scm.com](https://git-scm.com)
- **Mac**: `brew install git`
- **Linux**: `sudo apt-get install git`

### Step 2: Clone & Setup
```bash
# Create a local folder
mkdir wedding-expense-app
cd wedding-expense-app

# Initialize git
git init

# Add files (copy index.html, README.md, .gitignore here first)

# Stage files
git add .

# Initial commit
git commit -m "Initial commit: Wedding expense app"
```

### Step 3: Connect to GitHub
1. Create new repo on GitHub (as shown above)
2. Copy the repository URL (HTTPS or SSH)
3. Add remote:
```bash
git remote add origin https://github.com/YOUR-USERNAME/wedding-expense-app.git
git branch -M main
git push -u origin main
```

### Step 4: Enable Pages
Follow Step 3 from "Quick Deployment" section above

---

## Using GitHub Desktop (GUI)

### Step 1: Install GitHub Desktop
Download from [desktop.github.com](https://desktop.github.com)

### Step 2: Create Local Repository
1. File → New Repository
2. Name: `wedding-expense-app`
3. Local Path: Choose a folder
4. Click "Create Repository"

### Step 3: Add Your Files
1. Copy `index.html`, `README.md`, `.gitignore` to the repo folder
2. GitHub Desktop will detect changes
3. Enter commit message: "Initial commit: Wedding expense app"
4. Click "Commit to main"

### Step 4: Publish to GitHub
1. Click "Publish Repository"
2. Ensure "Keep this code private" is UNCHECKED (for free Pages)
3. Click "Publish Repository"

### Step 5: Enable Pages
Same as Step 3 in "Quick Deployment" section

---

## Access Your Live App

After deployment completes (1-2 minutes):
```
https://USERNAME.github.io/wedding-expense-app/
```

### Example
If your GitHub username is `kritikush26`:
```
https://kritikush26.github.io/wedding-expense-app/
```

---

## Firebase Configuration

⚠️ **Important Security Note**: This app uses hardcoded Firebase credentials for email: `kritikush26@gmail.com`

To use with your own Firebase project:

1. Create Firebase project at [firebase.google.com](https://firebase.google.com)
2. Get your config from Project Settings
3. In `index.html`, find this section (around line 407):
```javascript
const firebaseConfig = {
  apiKey: "YOUR_API_KEY",
  authDomain: "YOUR_AUTH_DOMAIN",
  projectId: "YOUR_PROJECT_ID",
  storageBucket: "YOUR_STORAGE_BUCKET",
  messagingSenderId: "YOUR_MESSAGING_SENDER_ID",
  appId: "YOUR_APP_ID"
};
```

4. Replace with your credentials
5. Create Firestore collections:
   - `masters` (budget/vendors)
   - `expenses` (transactions)
6. Update auth credentials in line 416:
```javascript
// Old (example):
await signInWithEmailAndPassword(auth, "kritikush26@gmail.com", "KritiKush26");

// New (your credentials):
await signInWithEmailAndPassword(auth, "your.email@gmail.com", "your-password");
```

---

## Troubleshooting

### App not loading?
- ✓ Check HTTPS in URL (GitHub Pages requires HTTPS)
- ✓ Clear browser cache (Ctrl+Shift+Del)
- ✓ Verify `index.html` is in root folder
- ✓ Check Firebase credentials are correct

### 404 on custom domain?
- Check repository Settings → Pages
- Verify branch is set to `main`
- Ensure `index.html` exists in root

### Repository not finding files?
- Ensure files are in root directory, not a subfolder
- Commit and push were successful
- GitHub Pages source is set correctly

---

## Updates & Maintenance

### Push changes:
```bash
git add .
git commit -m "Update: Your change description"
git push origin main
```

Site updates automatically after push (1-2 min delay)

### Continuous Deployment
The app syncs in real-time with Firebase, so:
- New budgets appear instantly
- Expenses update live
- No need to redeploy for data changes

---

## Performance Tips

- ✓ GitHub Pages caches files - hard refresh (Ctrl+Shift+R) to see updates
- ✓ Tailwind CSS loads via CDN - ensure internet connection
- ✓ Firebase SDK loads from jsDelivr - check broadband speed
- ✓ Chart.js caches in browser - clear cache if charts don't update

---

## Alternative Hosting Options

| Platform | Cost | Setup |
|----------|------|-------|
| **GitHub Pages** | Free | Easy |
| **Firebase Hosting** | Free tier | Medium |
| **Netlify** | Free tier | Easy |
| **Vercel** | Free tier | Easy |

For this app, GitHub Pages is recommended (no server needed, static HTML)

---

## Need Help?

1. Check File → Preferences → Settings for VS Code extensions
2. Enable "GitHub Repositories" extension for easy management
3. Visit GitHub Status page if pages fail
4. Check Firebase console for data sync issues

---

**Deploy Status**: Ready for GitHub Pages ✅
**Required Files**: index.html, README.md (optional), .gitignore (optional)
**Deploy Time**: 2-5 minutes from first push

