# 📍 Git Basics: The Essential Toolkit

This cheat sheet covers the foundational commands you need to manage a local repository and start tracking your work.

---

## ⚙️ Configuration
Set up your identity before your first commit.

```bash
# Set global username
git config --global user.name "Your Name"

# Set global email
git config --global user.email "your.email@example.com"

# Check your settings
git config --list
```

## 🏗️ Starting a Repository
Every project starts here.

```bash
# Initialize a new local repository
git init

# Clone an existing repository from GitHub
git clone <url>
```

## 📝 The Staging Area & Committing
The "Save" mechanism of Git.

```bash
# Check the status of your files
git status

# Add a specific file to staging
git add <filename>

# Add ALL changed files to staging
git add .

# Record your changes with a message (Atomic Commit)
git commit -m "feat: initial project setup"

# Amend the last commit (if you forgot a file or typo)
git commit --amend -m "new message"
```

## 🔍 Inspection & History
Knowing what happened and when.

```bash
# View commit history (basic)
git log

# View commit history (professional one-liner)
git log --oneline --graph --decorate --all

# See changes in your working directory (not yet staged)
git diff

# See changes in your staged area
git diff --staged
```

## 🧹 Undoing Changes
Because we all make mistakes.

```bash
# Unstage a file (keep the changes in the file)
git restore --staged <file>

# Discard changes in a file (revert to last commit)
git restore <file>

# Undo the last commit BUT keep the changes in your files
git reset --soft HEAD~1

# DELETE the last commit and all changes (USE WITH CAUTION)
git reset --hard HEAD~1
```

---
[⬅️ Back to Home](../README.md)
