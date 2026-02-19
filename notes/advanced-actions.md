# 🚀 Advanced GitHub Actions: Beyond the Basics

Once you've mastered simple CI/CD, use these advanced features to make your workflows faster, DRY-er, and more powerful.

---

## ♻️ 1. Reusable Workflows
Don't copy-paste YAML between repositories. Define a workflow *once* and call it from anywhere.

**Scenario:** You have 10 microservices that all build using the same steps.
**Solution:** Create a `build-and-test.yml` in a central `infra` repo and call it.

**Central Workflow (`infra/build.yml`):**
```yaml
name: Reusable Build
on:
  workflow_call:
    inputs:
      node-version:
        required: true
        type: string
    secrets:
      token:
        required: true

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      ...
```

**Caller Workflow (`app/ci.yml`):**
```yaml
jobs:
  call-infra-build:
    uses: my-org/infra/.github/workflows/build.yml@v1
    with:
      node-version: '18'
    secrets:
      token: ${{ secrets.GITHUB_TOKEN }}
```

---

## 🧩 2. Composite Actions
Simplify complex steps in a single job. If your workflow has 50 lines of shell scripts, turn it into a Composite Action.

-   **Difference from Reusable Workflows:**
    -   **Reusable Workflow:** Calling an entire job/pipeline.
    -   **Composite Action:** Bundling steps to run *inside* a job (like a custom `uses:`).

**Example (`actions/setup/action.yml`):**
```yaml
name: 'Setup Environment'
description: 'Install Node & Cache'
runs:
  using: "composite"
  steps:
    - uses: actions/setup-node@v3
    - run: npm ci
      shell: bash
```

---

## ⚡ 3. Concurrency
Prevent multiple builds from running on the same branch simultaneously (saves money/time).

```yaml
concurrency:
  group: ${{ github.workflow }}-${{ github.ref }}
  cancel-in-progress: true
```
If you push twice in 10 seconds, the first run will be cancelled so the second (latest) one can run.

---

## 🕸️ 4. Matrix Strategy
Run the same job across multiple OS/Versions in parallel.

```yaml
jobs:
  test:
    strategy:
      matrix:
        os: [ubuntu-latest, windows-latest]
        node: [16, 18, 20]
    runs-on: ${{ matrix.os }}
    steps:
      - uses: actions/setup-node@v3
        with:
          node-version: ${{ matrix.node }}
```
This runs 6 jobs (2 OS * 3 Node versions) at the same time!

---
[⬅️ Back to Home](../README.md)
