# 🛡️ GitHub Security: Defending Your Code

Security isn't just for the Ops team. GitHub provides built-in tools to secure your code, dependencies, and secrets.

---

## 🔍 1. Dependabot
Dependabot keeps your dependencies up-to-date and secure. It monitors your `package.json`, `requirements.txt`, etc., for known vulnerabilities.

-   **Alerts:** Notifies you if you're using a library with a known CVE (Common Vulnerabilities and Exposures).
-   **Security Updates:** Automatically opens Pull Requests to upgrade vulnerable dependencies to a patched version.
-   **Version Updates:** (Optional) Automatically opens PRs to keep *all* dependencies on the latest version, not just the vulnerable ones.

**How to Enable:**
`Settings > Security & analysis > Dependabot alerts & security updates`

---

## 🕵️ 2. Secret Scanning (Push Protection)
One of the most common hacks is developers accidentally committing API keys (AWS, Stripe, OpenAI) to a public repo.

-   **Secret Scanning:** Scans your entire history for known secret patterns.
-   **Push Protection:** (Crucial) **Blocks** you from pushing commits that contain secrets *before* they even leave your computer.

**Best Practice:**
Enable "Push protection" for your personal account:
`Settings > Code security and analysis > Secret scanning > Push protection`

---

## 🔬 3. CodeQL (Code Scanning)
CodeQL is a semantic code analysis engine. It queries your code as if it were data to find logical vulnerabilities (e.g., SQL injection, XSS) that simple linters miss.

-   Runs as a GitHub Action.
-   Free for public repositories.
-   Available for private repos with Advanced Security (Enterprise).

---

## 🚧 4. Branch Protection Rules
Prevent disaster by enforcing rules on your `main` branch.

**Go to:** `Settings > Branches > Add rule` for `main`:

1.  **Require a pull request before merging:** No one (including you) can push directly to main.
2.  **Require status checks to pass:** Tests *must* pass before the "Merge" button turns green.
3.  **Require linear history:** Enforces a clean history (no merge commits on main) if you prefer rebase workflows.
4.  **Include administrators:** Enforce these rules even on repo owners (prevents "oops" moments).

---
[⬅️ Back to Home](../README.md)
