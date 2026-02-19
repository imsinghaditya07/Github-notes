# 💻 GitHub CLI (`gh`): The Terminal Powerhouse

Stop context-switching between your terminal and the browser. The GitHub CLI (`gh`) brings pull requests, issues, and more directly to your command line.

---

## 🚀 1. Installation & Auth
**Install:** `winget install GitHub.cli` (Windows) or `brew install gh` (macOS).
**Login:** `gh auth login` (Choose "GitHub.com" and "HTTPS").

---

## 🛠️ 2. Core Commands

### Repositories
-   `gh repo create <name>`: Create a new repo (public/private) and clone it.
-   `gh repo clone <owner>/<repo>`: Clone a repo.
-   `gh repo view --web`: Open the current repo in the browser.

### Pull Requests (The Game Changer)
-   `gh pr create`: Create a PR. Interactive prompts for title/body.
-   `gh pr list`: See all open PRs.
-   `gh pr checkout <number>`: **Best feature.** Fetches a PR branch and switches to it. No more finding remote branch names.
-   `gh pr merge`: Merge the PR (merge/squash/rebase) and delete the branch locally & remotely.

### Issues
-   `gh issue create`: Create an issue.
-   `gh issue list`: View open issues.

### Actions
-   `gh run list`: Check the status of recent CI runs.
-   `gh run watch`: Watch a running workflow in real-time in the terminal.

---

## ⚡ 3. Productivity Aliases
You can define aliases for commands you use often.

`gh alias set prc 'pr create'`
`gh alias set prl 'pr list'`
`gh alias set co 'pr checkout'`

Usage: `gh co 123` (Checks out PR #123)

---

## 🧠 4. Scripting with `--json`
The CLI outputs JSON, making it amazing for automation.

**Example:** List all open PR URLs
```bash
gh pr list --json url --jq '.[].url'
```

**Example:** Check CI status in a script
```bash
gh run list --limit 1 --json conclusion --jq '.[0].conclusion'
# Output: "success" or "failure"
```

---
[⬅️ Back to Home](../README.md)
