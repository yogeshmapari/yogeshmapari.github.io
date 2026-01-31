# 🚀 GitHub Connection Setup Guide

## Prerequisites: Install Git

### Step 1: Download & Install Git

1. **Go to**: https://git-scm.com/download/win
2. **Download** the latest Git for Windows installer
3. **Run** the installer and follow the installation wizard:
   - Choose default options for most settings
   - Select "Use Git from Command Line" option
   - Use "OpenSSL library" for HTTPS
   - Default line ending conversion

### Step 2: Verify Git Installation

After installation, open Command Prompt and run:
```bash
git --version
```

You should see something like: `git version 2.42.0.windows.1`

---

## Setup Steps (After Installing Git)

### Step 1: Configure Git User

```bash
git config --global user.name "Yogesh Mapari"
git config --global user.email "patilmapari@gmail.com"
```

### Step 2: Initialize Git Repository (if not already done)

Navigate to your portfolio directory:
```bash
cd C:\Users\patil\OneDrive\Desktop\projects\git\yogeshmapari.github.io
```

Check if git is initialized:
```bash
git status
```

If it shows `.git` folder exists, you're ready. If not, initialize:
```bash
git init
```

### Step 3: Create GitHub Repository

1. Go to https://github.com/new
2. Create a new repository with the name: `yogeshmapari.github.io`
3. **Do NOT** initialize with README, gitignore, or license
4. Click **Create Repository**

### Step 4: Add Remote URL

Copy the HTTPS URL from GitHub (looks like):
```
https://github.com/YOUR_USERNAME/yogeshmapari.github.io.git
```

Then add it to your local repository:
```bash
git remote add origin https://github.com/YOUR_USERNAME/yogeshmapari.github.io.git
```

### Step 5: Add Files to Git

Stage all files:
```bash
git add .
```

### Step 6: Create Initial Commit

```bash
git commit -m "Initial commit: Enhanced portfolio with modern design and functionality"
```

### Step 7: Push to GitHub

```bash
git branch -M main
git push -u origin main
```

**Note**: On first push, you may be asked for GitHub credentials. Enter your GitHub username and password (or personal access token).

---

## Alternative: Using SSH (More Secure)

### Generate SSH Key

```bash
ssh-keygen -t ed25519 -C "patilmapari@gmail.com"
```

Follow the prompts:
- Press Enter for default file location
- Enter a secure passphrase (or press Enter for none)

### Add SSH Key to GitHub

1. Go to https://github.com/settings/keys
2. Click "New SSH key"
3. Get your public key from:
   ```bash
   cat ~/.ssh/id_ed25519.pub
   ```
4. Paste it in GitHub and save

### Use SSH Remote

Instead of HTTPS, use:
```bash
git remote add origin git@github.com:YOUR_USERNAME/yogeshmapari.github.io.git
```

---

## Quick Reference Commands

```bash
# Check git status
git status

# Add all files
git add .

# Commit changes
git commit -m "Your message here"

# Push to GitHub
git push

# Pull from GitHub
git pull

# Check remote URL
git remote -v

# View commit history
git log

# Create a new branch
git checkout -b feature-branch

# Switch branch
git checkout main

# Merge branch
git merge feature-branch
```

---

## GitHub Pages Setup

Since your repository is `yogeshmapari.github.io`, GitHub automatically treats it as a GitHub Pages site.

### Steps to Enable:

1. Go to your repository on GitHub
2. Click **Settings** → **Pages**
3. Select **Deploy from a branch**
4. Choose branch: `main`
5. Choose folder: `/ (root)`
6. Click **Save**

Your portfolio will be live at: `https://yogeshmapari.github.io`

---

## Troubleshooting

### "fatal: not a git repository"
**Solution**: Run `git init` in your portfolio directory first

### "fatal: 'origin' does not appear to be a 'git' repository"
**Solution**: Add the remote URL:
```bash
git remote add origin https://github.com/YOUR_USERNAME/yogeshmapari.github.io.git
```

### Authentication Failed
**Solution**: 
- Use personal access token instead of password
- Or set up SSH key authentication
- Or use GitHub CLI: `gh auth login`

### Files not showing on GitHub
**Make sure to**:
1. Run `git add .`
2. Run `git commit -m "message"`
3. Run `git push`

---

## What Gets Pushed

The following files will be pushed to GitHub:
- ✅ index.html - Your portfolio page
- ✅ assets/ folder - CSS, JS, and images
- ✅ All documentation files (MD files)
- ✅ Resume PDFs
- ✅ _config.yml
- ⚠️ May want to exclude with .gitignore:
  - node_modules/
  - .env files
  - IDE settings
  - OS files (.DS_Store, Thumbs.db)

### Sample .gitignore

Create a `.gitignore` file with:
```
# IDE
.vscode/
.idea/
*.swp
*.swo

# OS
.DS_Store
Thumbs.db
*.log

# Node
node_modules/

# Env
.env
.env.local
```

---

## Next Steps

1. **Install Git** from https://git-scm.com/download/win
2. **Follow the setup steps** above
3. **Verify** your portfolio is on GitHub:
   - Visit: https://github.com/YOUR_USERNAME/yogeshmapari.github.io
4. **Check GitHub Pages** is deployed:
   - Visit: https://yogeshmapari.github.io

---

## Quick Setup Script

After installing Git, you can run this in Command Prompt (one command at a time):

```bash
cd C:\Users\patil\OneDrive\Desktop\projects\git\yogeshmapari.github.io

git config --global user.name "Yogesh Mapari"
git config --global user.email "patilmapari@gmail.com"

git init

git add .

git commit -m "Initial commit: Enhanced portfolio with modern design and functionality"

git remote add origin https://github.com/YOUR_USERNAME/yogeshmapari.github.io.git

git branch -M main

git push -u origin main
```

**Replace `YOUR_USERNAME` with your actual GitHub username!**

---

## Support Resources

- **Git Documentation**: https://git-scm.com/doc
- **GitHub Help**: https://docs.github.com
- **GitHub Pages**: https://docs.github.com/en/pages
- **Personal Access Token**: https://github.com/settings/tokens
- **SSH Keys**: https://github.com/settings/keys

---

## Status Checklist

After setup, you should have:
- [x] Git installed on your computer
- [x] Git user configured globally
- [x] Local .git folder initialized
- [x] GitHub repository created
- [x] Remote origin added
- [x] Files staged and committed
- [x] Portfolio pushed to GitHub
- [x] GitHub Pages enabled
- [x] Portfolio live at yourname.github.io

---

**Need Help?** 
- Check git status: `git status`
- View remote: `git remote -v`
- View logs: `git log`
- Check configuration: `git config --list`

Your portfolio is ready to go live! 🚀
