# 🌿 Branching & Merging: Mastering the Flow

Branches allow you to work on different features or fixes simultaneously without breaking the "production-ready" code on `main`.

---

## 🏗️ Managing Branches

```bash
# List all local branches
git branch

# Create a new branch (but stay on current)
git branch <branch-name>

# Switch to a branch
git checkout <branch-name>
# OR (modern way)
git switch <branch-name>

# Create AND switch to a new branch (Common Workflow)
git checkout -b <branch-name>
# OR (modern way)
git switch -c <branch-name>

# Delete a branch (must be merged)
git branch -d <branch-name>

# Force delete a branch (unmerged changes will be lost)
git branch -D <branch-name>
```

## 🤝 Integrating Changes

### 1. Merging (Traditional)
Creates a "merge commit" that ties two histories together.

```bash
# First, switch to the destination branch (e.g., main)
git switch main

# Merge the feature branch into main
git merge <feature-branch>
```

### 2. Rebasing (Professional/Clean History)
Rewrites project history by placing your commits on top of another branch. Result: A perfectly linear history.

```bash
# Switch to your feature branch
git switch <feature-branch>

# Rebase onto the latest main
git rebase main
```

## 📦 Stashing
"I'm not ready to commit, but I need to switch branches."

```bash
# Save your uncommitted changes to a temporary stack
git stash

# List your stashes
git stash list

# Re-apply the last stashed changes
git stash pop

# Remove the last stash without applying
git stash drop
```

---

## ⚡ Real-World Pro Workflow
1. `git switch -c feat/login-page` (Start feature)
2. *Work work work*
3. `git add .` & `git commit -m "feat: add login validation"`
4. `git switch main` & `git pull origin main` (Update local main)
5. `git switch feat/login-page`
6. `git rebase main` (Sync feature branch with latest main)
7. `git push origin feat/login-page`

---
[⬅️ Back to Home](../README.md)
