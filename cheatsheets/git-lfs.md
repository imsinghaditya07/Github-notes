# 🐘 Git Large File Storage (LFS) Cheat Sheet

> *Git was designed for code, not massive 3D models, videos, or datasets. Git LFS solves this problem.*

Git Large File Storage (LFS) replaces large files such as audio samples, videos, datasets, and graphics with tiny text "pointers" inside Git, while storing the actual file contents on a remote server like GitHub.

---

## 🛑 The Problem: GitHub's File Size Limit

- **Soft Limit:** GitHub warns you when pushing files larger than **50 MB**.
- **Hard Limit:** GitHub strictly **blocks** pushes containing files larger than **100 MB**.

If you try to push a 120MB dataset, your push will fail. Worse, even if you delete the file later, it will still exist in the Git history and continue to block pushes until you rewrite history. 

**Solution:** Use Git LFS *before* you commit the large file.

---

## ⚙️ 1. Installation and Setup

**Step 1:** Download and install Git LFS (if not already installed with Git).
*   Mac: `brew install git-lfs`
*   Windows: Download installer from `git-lfs.github.com` or use Git for Windows.

**Step 2:** Set up Git LFS for your user account (run once per machine).
```bash
git lfs install
```

---

## 🎯 2. Tracking Large Files

You need to tell Git LFS which files it should manage. You do this using patterns, just like `.gitignore`.

**Track specific file types (e.g., all MP4 videos and PSD files):**
```bash
git lfs track "*.mp4"
git lfs track "*.psd"
```

**Track a specific file or folder:**
```bash
git lfs track "assets/huge-database.sql"
git lfs track "models/**"
```

**Important:** Running `git lfs track` generates or updates a `.gitattributes` file. You **must** commit this file along with your large files!

---

## 🔄 3. Normal Git Workflow

Once you've told LFS to track specific files, you just use Git normally. LFS works invisibly in the background.

```bash
# Add the newly created .gitattributes file AND your large file
git add .gitattributes
git add my-huge-video.mp4

# Commit normally
git commit -m "Add promotional video"

# Push normally (LFS intercepts and uploads the large file separately)
git push origin main
```

---

## 🛠️ 4. Useful LFS Commands

| Command | Description |
| :--- | :--- |
| `git lfs ls-files` | List all files currently tracked by Git LFS in your repo. |
| `git lfs untrack "*.mp4"` | Stop tracking a specific file format with LFS. |
| `git lfs status` | View the status of LFS files pending upload. |
| `git lfs pull` | Explicitly download LFS files (usually done automatically by `git pull`). |

---

## ⚠️ Pro Tips

1. **GitHub Limits:** Every free GitHub account gets **1 GB of free LFS storage** and 1 GB of bandwidth per month. If you exceed this, you must buy a data pack.
2. **Commit `.gitattributes` First:** A common mistake is committing the large file *before* configuring LFS. Always run `git lfs track` and commit `.gitattributes` alongside your large files.
3. **Removing Accidentally Pushed Files:** If you accidentally committed a large file to standard Git instead of LFS, use the [BFG Repo-Cleaner](https://rtyley.github.io/bfg-repo-cleaner/) to purge the large file from your history before trying to push again.
