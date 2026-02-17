# 📖 Git & GitHub Glossary: Speak Like a Pro

Understanding the terminology is half the battle. This glossary defines the most critical terms in the Git ecosystem.

---

### 📍 General Terms

*   **Repository (Repo):** A folder managed by Git that contains your project files and their entire history.
*   **Commit:** A "snapshot" of your project at a specific point in time. Each commit has a unique ID (SHA-1 hash).
*   **HEAD:** A pointer to the current branch or commit you are working on.
*   **Clone:** Copying an existing repository from a remote server (like GitHub) to your local machine.
*   **Remote:** A version of your repository hosted on the internet or another network (e.g., `origin`).

---

### 🌿 Branching Terms

*   **Branch:** An independent line of development. The default branch is usually named `main`.
*   **Merge:** Combining changes from one branch into another.
*   **Rebase:** Moving or combining a sequence of commits to a new base commit (rewriting history for a linear look).
*   **Conflict:** When Git cannot automatically merge changes (usually because two people changed the same line).
*   **Checkout:** Switching between branches or restoring working tree files.
*   **Detached HEAD:** A state where HEAD points to a specific commit rather than a branch.

---

### ☁️ Collaboration Terms

*   **Fork:** A personal copy of someone else's project on your GitHub account.
*   **Pull Request (PR):** A way to propose changes you've made to a repository so others can review and merge them.
*   **Upstream:** The original repository from which a fork was created.
*   **Push:** Sending your local commits to a remote repository.
*   **Pull:** Fetching changes from a remote and immediately merging them into your local branch.
*   **Fetch:** Downloading changes from a remote WITHOUT merging them.

---

### 🧠 Advanced Concept Terms

*   **SHA-1:** The 40-character unique identifier for every object in Git (commits, files, trees).
*   **Staging Area (Index):** The middle ground where you prepare files before committing them.
*   **Cherry-pick:** Applying the changes introduced by some existing commits to your current branch.
*   **Reflog:** A local log that records every time the HEAD of a branch is updated (the ultimate "undo" tool).
*   **Git Hooks:** Scripts that Git executes before or after events like commit, push, and receive.

---
[⬅️ Back to Home](../README.md)
