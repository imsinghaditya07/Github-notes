#  Daily Git Tips

Here are some useful git commands for daily use.


## 1. Clean Untracked Files
git clean -fd: Removes untracked files and directories.


## 2. Switch to Previous Branch
git checkout -: Quickly switch back to the previous branch you were on.


## 3. Modify Last Commit
git commit --amend: Add staged changes to the previous commit or edit its message.


## 4. View Reference Log
git reflog: Shows a log of all reference updates (e.g., checkout, reset, commit). Great for recovering lost commits.


## 5. Stash Changes
git stash: Temporarily shelves (stashes) changes so you can work on something else.


## 6. Apply Specific Commit
git cherry-pick <commit>: Apply the changes introduced by some existing commit.


## 7. Undo Last Commit (Keep Changes)
git reset --soft HEAD~1: Undoes the last commit but keeps changes staged.


## 8. View Staged Changes
git diff --staged: Show changes between the index and your last commit.


## 9. Visual Log
git log --oneline --graph --all: Show a graphical representation of the commit history.


## 10. Delete Branch
git branch -d <branch>: Deletes the specified branch. Use -D simply to force delete.

