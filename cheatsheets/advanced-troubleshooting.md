# 🛠️ Advanced & Troubleshooting: Fixing the Mess

Git is a time machine. If you broke it, you can almost always fix it.

---

## 🍒 Cherry-Picking
"I committed something on Branch A, but I need it on Branch B."

```bash
# Get the commit ID from 'git log'
git checkout <branch-b>
git cherry-pick <commit-hash>
```

## 🔍 The "I'm Lost" Command (Reflog)
Reflog tracks every single movement of HEAD. Even if you deleted a branch or did a hard reset, the commits are still there for ~30 days.

```bash
git reflog
# Find the hash where things were still okay
git reset --hard <hash>
```

## 🚨 Common Scenarios & Fixes

### Scenario 1: I committed to the wrong branch (e.g., main instead of feature)
```bash
# 1. Undo the commit but keep the changes
git reset --soft HEAD~1
# 2. Stash those changes
git stash
# 3. Switch to the correct branch
git switch <feature-branch>
# 4. Apply the changes
git stash pop
```

### Scenario 2: I have a typo in my last commit message
```bash
git commit --amend -m "Corrected message"
```

### Scenario 3: I need to delete a file from Git history (Sensitive data!)
Note: Use `bfg-repo-cleaner` for big jobs, but for small ones:
```bash
git rm --cached <sensitive-file>
git commit --amend
git push origin <branch> --force
```
*Avoid `--force` on `main` unless you are the only one working on it!*

### Scenario 4: Resolving Merge Conflicts
1. Open the file. Look for `<<<<<<<`, `=======`, and `>>>>>>>`.
2. Choose which code to keep.
3. Remove the markers.
4. `git add <file>`
5. `git commit -m "chore: resolve merge conflict"`

---

## 🏗️ Partial Commits (Interactive Staging)
"I changed 5 things in one file, but I want to make 2 separate commits."

```bash
git add -p <file>
# Git will ask you (y/n) for each "hunk" of code.
```

---
[⬅️ Back to Home](../README.md)
