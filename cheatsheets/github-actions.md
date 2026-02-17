# 🤖 GitHub Actions & CI/CD: Automate Everything

Mastering GitHub isn't just about Git commands; it's about the ecosystem. GitHub Actions allows you to automate your workflow directly in your repository.

---

## 🏗️ What is a Workflow?
A workflow is a configurable automated process. You define them in `.github/workflows/` using YAML files.

### Basic Structure of a `.yml` workflow:
```yaml
name: CI
on: [push, pull_request] # When to run

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3 # Pull the code
      - name: Run a script
        run: echo "Hello, World!"
```

---

## 🧪 Common Master Workflows

### 1. Automated Testing (CI)
Run your tests every time someone creates a PR. This ensures no breaking changes are merged.

```yaml
name: Node.js CI
on: [push, pull_request]
jobs:
  test:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - name: Use Node.js
        uses: actions/setup-node@v3
        with:
          node-version: '18'
      - run: npm install
      - run: npm test
```

### 2. Auto-Publishing (CD)
Automatically deploy your code to Vercel, Netlify, or AWS when you merge to `main`.

### 3. Linting & Formatting
Ensure everyone follows the same code style before they can even merge.

---

## 🔑 Secrets Management
Never hardcode API keys. Use **GitHub Secrets**:
1. Go to Settings > Secrets and variables > Actions.
2. Add your secret (e.g., `CLOUDFLARE_TOKEN`).
3. Use it in your workflow:
   ```yaml
   env:
     API_TOKEN: ${{ secrets.CLOUDFLARE_TOKEN }}
   ```

---

## 📦 Scheduled Tasks (Cron Jobs)
Run scripts at specific times (e.g., database backups or weekly reports).

```yaml
on:
  schedule:
    - cron: '0 0 * * *' # Every night at midnight
```

---

## 🛡️ Protected Branches
Go to **Settings > Branches** and add a rule for `main`:
- **Require a pull request before merging.**
- **Require status checks to pass before merging** (Connect this to your GitHub Actions!).
- **Require signed commits.**

---

[⬅️ Back to Home](../README.md)
