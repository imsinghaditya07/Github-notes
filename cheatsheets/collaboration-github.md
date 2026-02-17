# 🤝 Collaboration & GitHub: working with a Team

GitHub adds the "social" and "remote" layer to Git. This cheat sheet focuses on pushing, pulling, and professional workflows like PRs.

---

## ☁️ Remote Repositories

```bash
# View existing remotes
git remote -v

# Link your local repo to a GitHub repo
git remote add origin <url>

# Rename a remote
git remote rename <old-name> <new-name>

# Remove a remote
git remote remove <name>
```

## 🚀 Syncing Code

```bash
# Push your branch to GitHub
git push origin <branch-name>

# Push and set upstream (so you can just say 'git push' next time)
git push -u origin <branch-name>

# Download changes from GitHub (and merge them automatically)
git pull origin <branch-name>

# Download changes from GitHub (WITHOUT merging)
git fetch origin
```

## 🔱 Forks & Pull Requests (The Professional Way)

1.  **Fork** the project on GitHub (creates your own copy).
2.  **Clone** your fork locally.
3.  **Add Upstream** (the original repo you forked from):
    ```bash
    git remote add upstream <original-repo-url>
    ```
4.  **Stay Synced** with the original project:
    ```bash
    git fetch upstream
    git merge upstream/main
    ```
5.  **Submit PR:** Push your branch to *your* fork and click "Compare & pull request" on GitHub.

## 🔑 SSH Setup (Pro Level)
Tired of typing passwords? Use SSH keys.

1.  Generate key: `ssh-keygen -t ed25519 -C "your_email@example.com"`
2.  Add to agent: `ssh-add ~/.ssh/id_ed25519`
3.  Copy public key: `cat ~/.ssh/id_ed25519.pub`
4.  Paste in **GitHub Settings -> SSH and GPG keys**.

---

## 🛡️ Tagging & Releases

```bash
# List tags
git tag

# Create a version tag
git tag -a v1.0.0 -m "First stable release"

# Push tags to GitHub
git push origin --tags
```

---
[⬅️ Back to Home](../README.md)
