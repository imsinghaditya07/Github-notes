# ⚡ Git Aliases: Boosting Your Productivity

Git aliases allow you to create shortcuts for long or complex commands. This not only saves typing time but also makes your workflow feel much smoother.

---

## 🛠️ How to Set an Alias
You can set aliases globally using the following syntax:
```bash
git config --global alias.<short-name> <actual-command>
```

---

## 🚀 Recommended Professional Aliases

### 1. The "Status" Shortcut
```bash
git config --global alias.s status
# Usage: git s
```

### 2. The "Beautiful Log"
One of the most useful aliases. It shows a compact, colorful graph of your history.
```bash
git config --global alias.lg "log --color --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit"
# Usage: git lg
```

### 3. The "Undo Last Commit"
Soft reset the last commit while keeping your changes staged.
```bash
git config --global alias.uncommit "reset --soft HEAD~1"
# Usage: git uncommit
```

### 4. The "Amend" Shortcut
Add changes to the last commit without changing the message.
```bash
git config --global alias.amend "commit --amend --no-edit"
# Usage: git amend
```

### 5. The "Clear Staged"
Unstage everything with one command.
```bash
git config --global alias.unstage "reset HEAD --"
# Usage: git unstage
```

---

## 📝 Viewing Your Aliases
To see all the aliases you've set, you can peek into your global config:
```bash
git config --global --get-regexp alias
```

## 💡 Pro Tip
If you want to use a shell command (not just a Git command) as an alias, start the command with an exclamation mark `!`.
```bash
# Open a visual tool for the current repo
git config --global alias.visual "!gitk"
```

---
[⬅️ Back to Home](../README.md)
