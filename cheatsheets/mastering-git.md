# 🔴 Mastering Git: The Expert Workflow

Once you understand the basics and collaboration, it's time to master the tools that make you a "Git Ninja." This section covers advanced workflows, automation, and deep-dive features.

---

## 🛠️ Interactive Rebase (`git rebase -i`)
Clean up your local history before pushing. Combine, rename, or delete commits.

```bash
# Rebase the last 5 commits
git rebase -i HEAD~5
```

**Common commands in the editor:**
- `pick`: Use the commit as is.
- `reword`: Use the commit but change the message.
- `edit`: Stop and edit the commit.
- `squash`: Combine this commit with the previous one.
- `fixup`: Like squash, but discard this message.
- `drop`: Remove this commit entirely.

---

## 🕵️ Git Bisect
Binary search through your history to find exactly which commit introduced a bug.

```bash
git bisect start
git bisect bad                 # Current version is broken
git bisect good <commit-hash>  # This hash was definitely working
# Git will checkout mid-points. Test it.
git bisect good                # If it works
git bisect bad                 # If it's broken
# ... Repeat until Git finds the culprit
git bisect reset               # Go back to your original state
```

---

## 🔗 Git Hooks
Automate tasks (like linting or running tests) before a commit or push.
Hooks are scripts located in `.git/hooks/`.

**Common Hooks:**
- `pre-commit`: Run linting/tests before the commit is created.
- `commit-msg`: Validate the format of the commit message.
- `pre-push`: Run heavy tests before pushing to remote.

*Pro-tip: Use tools like **Husky** (for JS) to manage these easily.*

---

## 📦 Git Submodules
Keep another Git repository as a subdirectory of your own.

```bash
# Add a submodule
git submodule add <repo-url> <folder-name>

# When cloning a repo with submodules:
git clone --recursive <repo-url>
# OR
git submodule update --init --recursive
```

---

## ⚙️ Advanced Configuration
Customize Git to your liking.

```bash
# Global identity
git config --global user.name "Your Name"
git config --global user.email "email@example.com"

# Set default editor (e.g., VS Code)
git config --global core.editor "code --wait"

# Turn on colorful output
git config --global color.ui auto

# List all configs
git config --list --show-origin
```

---

## 📂 Git Garbage Collection
Git usually manages itself, but sometimes you need to clean up manualy to save space.

```bash
# Cleanup unnecessary files and optimize the local repo
git gc --prune=now --aggressive
```

---

[⬅️ Back to Home](../README.md)
