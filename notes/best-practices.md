# ✨ Git & GitHub Best Practices for Professionals

Writing code is only half the job. Managing it professionally is what separates a student from a software engineer.

---

## ✍️ 1. Commit Messages (Conventional Commits)
Follow the [Conventional Commits](https://www.conventionalcommits.org/) specification.

**Format:** `<type>(<scope>): <subject>`

*   `feat`: A new feature (e.g., `feat(auth): add google oauth2`)
*   `fix`: A bug fix (e.g., `fix(api): handle null response from database`)
*   `docs`: Documentation changes
*   `style`: Formatting, missing semi colons, etc; no code change
*   `refactor`: Refactoring production code
*   `test`: Adding missing tests, refactoring tests
*   `chore`: Updating build tasks, package manager configs, etc.

**Rule of Thumb:** A commit message should complete the sentence: *"If applied, this commit will..."*

---

## ☢️ 2. Keep Commits Atomic
A commit should be the **smallest possible unit** of a task.
*   **Bad:** "Added login, fixed header, and updated footer colors."
*   **Good:**
    1. `feat(auth): add login form`
    2. `fix(ui): adjust header z-index`
    3. `style(ui): update footer brand color`

---

## 🌿 3. Branch Naming Conventions
Don't name branches `stuff` or `my-fix`. Use categories:
*   `feature/feature-name` or `feat/feature-name`
*   `bugfix/issue-id` or `fix/issue-id`
*   `hotfix/issue-id` (For urgent production fixes)
*   `docs/api-update`

---

## 🔍 4. The Pull Request (PR) Checklist
Before you hit "Create Pull Request":
1.  **Self-Review:** Look at your own diff. Did you leave `console.log` or commented-out code?
2.  **Pass Tests:** Does the code actually run?
3.  **Sync with Main:** Have you rebased or merged the latest `main` into your branch?
4.  **Description:** Explain the *What* and the *Why*. If it's a UI change, add a screenshot or GIF.

---

## 🛡️ 5. Never Force Push to Shared Branches
Commands like `git push --force` overwrite the history for everyone else. Only use it on your own private feature branches. Never on `main` or `develop`.

---

## 🗑️ 6. Use .gitignore Wisely
Never commit:
*   `node_modules/` or vendor folders.
*   `.env` files (Secret keys, API tokens).
*   OS-generated files (`.DS_Store`).
*   Build artifacts (`dist/`, `build/`).

---
[⬅️ Back to Home](../README.md)
