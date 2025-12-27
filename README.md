# Excel to Semicolon Converter

A simple web app to convert Excel column data to semicolon-separated format.

![Version](https://img.shields.io/badge/version-1.0.0-blue)
![License](https://img.shields.io/badge/license-MIT-green)

## Features

- **`;` Mode**: Join items with semicolons → `Part1;Part2;Part3`
- **`;=` Mode**: Prepend `;=` to each item → `;=Part1;=Part2;=Part3`
- Auto-convert on paste
- One-click copy to clipboard
- Works offline (no server needed)

## 🚀 Quick Start

### Option 1: Use Online (GitHub Pages)
Visit: `https://YOUR-USERNAME.github.io/clipboard-converter`

### Option 2: Run Locally
Just open `index.html` in your browser!

---

## 📦 Setup Guide

### Step 1: Create GitHub Repository

1. Go to [github.com](https://github.com) and sign in
2. Click **"New repository"** (green button)
3. Name it: `clipboard-converter`
4. Make it **Public** (required for free GitHub Pages)
5. Click **"Create repository"**

### Step 2: Upload Your Code

**Option A: GitHub Web Interface (Easiest)**
1. Click "uploading an existing file"
2. Drag and drop `index.html`
3. Click "Commit changes"

**Option B: Git Command Line**
```bash
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/clipboard-converter.git
git push -u origin main
```

### Step 3: Enable GitHub Pages (Free Hosting)

1. Go to your repository on GitHub
2. Click **Settings** → **Pages** (left sidebar)
3. Under "Source", select **"Deploy from a branch"**
4. Choose **"main"** branch and **"/ (root)"** folder
5. Click **Save**
6. Wait 1-2 minutes, then visit: `https://YOUR-USERNAME.github.io/clipboard-converter`

---

## 🖥️ Create Windows Executable

### Option 1: Electron (Recommended)

Install Node.js first from [nodejs.org](https://nodejs.org)

```bash
# Install Electron packager globally
npm install -g electron electron-packager

# In your project folder, create package.json (see below)
# Then run:
electron-packager . ClipboardConverter --platform=win32 --arch=x64 --icon=icon.ico
```

### Option 2: Use Tauri (Smaller file size)

See [tauri.app](https://tauri.app) for setup instructions.

---

## 📁 Project Structure

```
clipboard-converter/
├── index.html          # Main app (everything in one file)
├── README.md           # This file
├── package.json        # For Electron build
├── main.js             # Electron main process
└── icon.ico            # App icon (optional)
```

---

## 🔄 Version Control & Updates

### Making Updates

1. Edit your files locally
2. Commit and push:
```bash
git add .
git commit -m "Added new feature"
git push
```
3. GitHub Pages auto-updates in 1-2 minutes

### Version Numbering

Update version in `index.html`:
- **1.0.0** → **1.0.1** for bug fixes
- **1.0.0** → **1.1.0** for new features
- **1.0.0** → **2.0.0** for major changes

---

## 🛠️ Future Features Ideas

- [ ] Custom separator input
- [ ] Save/load presets
- [ ] Dark/light theme toggle
- [ ] Batch file processing
- [ ] History of conversions

---

## 📄 License

MIT License - feel free to use and modify!
