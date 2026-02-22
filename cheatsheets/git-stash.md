# 🗃️ Git Stash Cheat Sheet

> *"I was halfway through a complex feature when an urgent bug came in. I couldn't commit half-written code. So, I stashed it."*

Git Stash temporarily shelves (or stashes) changes you've made to your working directory, leaving you with a clean slate to switch branches, pull updates, or fix a bug without having to make a messy "WIP" (Work In Progress) commit.

---

## 🚀 1. The Core Commands

If you only learn two stash commands, learn these:

### `git stash` 
Takes all your modified tracked files and staged changes, saves them on a temporary clipboard (the stash), and resets your working directory to match the `HEAD` commit.

### `git stash pop`
Takes the most recent stash, applies it back to your working directory, and **deletes** the stash from the clipboard.

---

## 🛠️ 2. Advanced Stashing

### Stashing with a Message
If you use stash frequently, you will forget what is in them. Give your stashes a name!
```bash
git stash push -m "half-finished login UI"
```

### Stashing Untracked Files
By default, `git stash` **does not** save newly created files that haven't been `git add`ed yet. To stash everything, including new files:
```bash
git stash -u   # -u means "include untracked"
```
*(To include ignored files too, use `git stash -a`)*

### Viewing Your Stashes
You can have multiple stashes saved at once. They are stored in an array interface, indexed from 0.
```bash
git stash list
```
*Output looks like:*
`stash@{0}: On main: half-finished login UI`
`stash@{1}: WIP on feature/auth: 8ebd92a fix typo`

### Applying without Deleting
Unlike `pop`, `apply` puts the stashed changes back into your working directory but **keeps** the stash on your clipboard (useful if you want to apply the same stash to multiple branches).
```bash
git stash apply          # Applies the most recent stash (stash@{0})
git stash apply stash@{1} # Applies a specific older stash
```

---

## 🗑️ 3. Cleaning Up

### Deleting a specific stash
If you realize you don't need a stashed chunk of code anymore:
```bash
git stash drop stash@{1}
```

### Deleting ALL stashes
Clear your entire stash clipboard (Cannot be undone easily!):
```bash
git stash clear
```

---

## 🎯 Typical Workflow Scenario

1. You are modifying `index.html` on branch `feature-ui`.
2. Boss says: *Fix the production bug on main right now!*
3. `git stash -u -m "ui changes"` (Your working directory is now clean).
4. `git checkout main`
5. Fix bug, commit, push.
6. `git checkout feature-ui`
7. `git stash pop` (Your half-finished `index.html` modifications are right back where you left them).
