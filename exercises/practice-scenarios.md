# 🎯 Real-World Practice Scenarios

The best way to learn Git is to break things (safely). Try to complete these scenarios in a test repository.

---

### 🔥 Scenario 1: The "Duh" Moment
**Goal:** Fix a typo in a commit that you already made.
1.  Create a file `test.txt`.
2.  Add and commit it with the message: `feat: adding test fileee` (note the typo).
3.  Use the correct command to fix that message to `feat: add test file`.

### 🌿 Scenario 2: The Parallel Developer
**Goal:** Understand how branches work.
1.  On `main`, create a file `shared.txt` with content "Line 1". Commit it.
2.  Create a branch `feature-a`.
3.  On `feature-a`, change `shared.txt` to "Line 1 - Updated by A". Commit it.
4.  Switch back to `main`.
5.  On `main`, change `shared.txt` to "Line 1 - Updated by Main". Commit it.
6.  **Challenge:** Merge `feature-a` into `main`. You WILL get a conflict. Resolve it manually.

### 🍒 Scenario 3: The Picky Boss
**Goal:** Use Cherry-picking.
1.  Create a branch `experimental`.
2.  Make 3 different commits on `experimental` (add 3 different files).
3.  Switch back to `main`.
4.  **Challenge:** Only bring the **second** commit from `experimental` into `main` without merging the whole branch.

### 🧹 Scenario 4: The Clean Freak
**Goal:** Use Rebasing.
1.  Create a branch `messy-feature`.
2.  Make a commit on `messy-feature`.
3.  Go to `main`, make a commit there (simulating another dev pushing code).
4.  Go back to `messy-feature`.
5.  **Challenge:** Use `rebase` to put your feature commit on top of the new `main` commit. Check `git log` to see the linear history.

---

## 🏆 Checklist for Completion
- [ ] I have used `git status` at every step.
- [ ] I understand the difference between `merge` and `rebase`.
- [ ] I can resolve a conflict without panicking.
- [ ] I know how to use `git reflog` to save my life.

---
[⬅️ Back to Home](../README.md)
