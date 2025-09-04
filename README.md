# Deep Learning Portfolio  

This repository contains my **Deep Learning Portfolio**, built with [Jupyter Book](https://jupyterbook.org/).  
It compiles my course notebooks, exercises, labs, and projects into a professional, interactive portfolio hosted on **GitHub Pages**.  

🔗 **Live site:** [https://kardcy.github.io/Deep-Learning-Portfolio/](https://kardcy.github.io/Deep-Learning-Portfolio/)  

---

## 📂 Repository Structure  

```bash
Deep-Learning-Portfolio/
│
├── mybook/ # Jupyter Book project
│ ├── _config.yml # Book configuration
│ ├── _toc.yml # Table of contents
│ ├── intro.md # Introduction / landing page
│ ├── labs/ # Laboratory notebooks
│ ├── exercises/ # Exercise notebooks
│ ├── projects/ # Project notebooks
│ └── images/ # Logos, figures, etc.
│
└── README.md # Documentation (this file)
```

## How to Build and Publish the Book  

### 1. Update Content  
- Add or edit your notebooks (`.ipynb`) and Markdown files (`.md`).  
- Place them into the correct section: **labs**, **exercises**, or **projects**.  

### 2. Save to GitHub (main branch)  
Commit your changes so the source files are tracked:  

```bash
git add .
git commit -m "Update labs/exercises/projects"
git push origin main
```

### 3. Build the Book Locally  
Run this inside the `mybook/` folder:  

```bash
jupyter-book build .
```

Or run it on the `Deep-Learning-Portfolio/` folder:

```bash
jupyter-book build mybook/
```

### 4. Deploy to GitHub Pages
Publish the built book with:

```bash
ghp-import -n -p -f _build/html # inside mybook/ folder
ghp-import -n -p -f mybook/_build/html # inside Deep-Learning-Portfolio/ folder
```

## Notes
- You don’t need to `git push` the `_build/html` folder manually.
- The `ghp-import` tool handles publishing the site to `gh-pages`.
- Make sure GitHub Pages is enabled in your repo settings:
    - Go to **Settings** → **Pages**
    - Under **Branch**, select `gh-pages` → **Save**
