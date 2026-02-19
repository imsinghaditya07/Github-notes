# 🗂️ Project Management on GitHub

GitHub isn't just for code; it's a full project management suite. Forget Jira/Trello – keep your work where your code lives.

---

## 🏗️ 1. GitHub Projects (V2 / Beta)
The new GitHub Projects is a spreadsheet-database hybrid (like Notion/Airtable) but integrated with your Issues and Pull Requests.

-   **Views:**
    -   **Table:** Like a spreadsheet. Good for triage and backlog grooming.
    -   **Board:** Kanban style (To Do, In Progress, Done). Good for visualizing flow.
    -   **Roadmap:** Gantt chart style. Good for planning releases over time.

-   **Custom Fields:**
    -   Add fields like "Priority" (P0, P1, P2), "Size" (S, M, L), "Target Date", etc.
    -   These fields sync directly with the issues in the project.

-   **Automation:**
    -   Automatically move items to "In Progress" when a PR is opened.
    -   Automatically move items to "Done" when a PR is merged.
    -   Automatically archive items that have been "Done" for > 30 days.

---

## 🎯 2. Issues & Milestones

### Issues
Use issue templates! `.github/ISSUE_TEMPLATE/` allows you to create forms (bug reports, feature requests) so users provide the info you need upfront.

### Labels
Don't use random labels. Structure them:
-   `type: bug`, `type: feature`, `type: docs`
-   `priority: high`, `priority: low`
-   `status: needs-triage`, `status: blocked`

### Milestones
Group issues and PRs into a "Milestone" (e.g., "v1.0 Release" or "April Sprint").
-   Track progress towards a deadline.
-   See percentage completion based on closed issues.

---

## 🤖 3. Insights
The "Insights" tab gives you data on your team's velocity.
-   **Burn-up charts:** Are we closing issues faster than we open them?
-   **Cycle time:** How long does it take from "In Progress" to "Done"?

---
[⬅️ Back to Home](../README.md)
