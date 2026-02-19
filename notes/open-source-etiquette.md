# 🤝 Open Source Etiquette: Be a Good Citizen

Contributing to open source is about more than code; it's about communication and respect. Follow these unwritten rules to get your PRs merged.

---

## 🧹 1. Before You Code
-   **Read CONTRIBUTING.md:** Most large repos have one. It tells you how to set up the dev environment and run tests.
-   **Search First:** Don't open a new issue without searching if it already exists. Duplicate issues are noise.
-   **Ask Before You Build:** If you want to add a *huge* new feature, open an issue/discussion first. Don't spend 2 weeks coding something the maintainers might not want.

---

## 📝 2. Writing Good Issues
-   **Be Reproducible:** "It doesn't work" is unhelpful. Provide steps to reproduce the bug.
-   **Environment:** What OS? What browser? What version of the library?
-   **Screenshots/Logs:** A picture is worth 1000 words. A stack trace is worth 1000 hours.

---

## 🔄 3. The Pull Request (PR)
-   **Descriptive Title:** Not "fix bug". Use "fix(auth): handle null token in login".
-   **Link the Issue:** Type `Fixes #123` in the description. GitHub will auto-close the issue validation when merged.
-   **Small is Beautiful:** Reviewers hate 5000-line PRs. Break it down.
-   **Pass CI:** If the redness (tests failing) is showing, don't ask for review yet.

---

## 💬 4. Handling Feedback
-   **Don't Take it Personally:** Code review is about the code, not you.
-   **Be Patient:** Maintainers often do this in their free time. Don't ping them every 2 hours.
-   **Squash Your Commits:** If asked, combine your "wip", "typo", "fix" commits into one clean commit before merging.

---
[⬅️ Back to Home](../README.md)
