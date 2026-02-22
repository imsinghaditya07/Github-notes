# 🔍 Advanced GitHub Search & Navigation

> *With millions of repositories and billions of lines of code, knowing how to search GitHub effectively is a superpower.*

GitHub isn't just a place to store your code; it's a massive database of how the world writes software. You can use it to find examples of API implementations, track down bugs, or discover open-source projects.

---

## ⌨️ 1. The GitHub Command Palette

The fastest way to navigate anywhere on GitHub is using your keyboard.

**Press `Ctrl + K` (Windows/Linux) or `Cmd + K` (Mac)** from anywhere on GitHub.

This opens a spotlight-like search bar that lets you:
*   Jump instantly to your repositories or organizations.
*   Run global searches.
*   Switch themes (type `> theme`).
*   Find settings quickly.

---

## 🔎 2. Advanced Search Syntax

When you type into the GitHub search bar, you can use special qualifiers to narrow down exactly what you're looking for.

### Scoping Your Search
*   `user:imsinghaditya07` - Search only within your account.
*   `org:microsoft` - Search within an organization.
*   `repo:facebook/react` - Search within a specific repository.

### Language and File Specifics
*   `language:python` - Only show results written in Python.
*   `extension:json` - Only search within `.json` files.
*   `path:src/components` - Only search inside specific directories.

### Project Characteristics
*   `stars:>1000` - Find popular projects (more than 1,000 stars).
*   `forks:>500` - Find heavily forked projects.
*   `size:<5000` - Find small, lightweight repositories (size is in KB).

### Combining Qualifiers (Magic 🪄)
**Example 1:** Find a Python script dealing with machine learning that has over 500 stars.
`machine learning language:python stars:>500`

**Example 2:** Inside the React repository, find everywhere the word `useEffect` is used, but only in `.ts` (TypeScript) files.
`useEffect repo:facebook/react extension:ts`

---

## 🛠️ 3. Searching Code (The Black Belt)

GitHub's new code search engine understands code structure. 

### Precise Symbol Search
If you are looking for a function declaration or a class, use the `symbol:` qualifier.

*   `symbol:React.Fragment` - Finds where `React.Fragment` is officially defined.
*   `/regular(.*)expressions?/` - GitHub code search supports **Regex**! Just wrap your search query in forward slashes `/`.

---

## 💬 4. Searching Issues and Pull Requests

Finding bug reports or pull requests can save you hours of debugging.

*   `is:issue is:open` - Find only open issues.
*   `is:pr is:closed` - Find closed pull requests.
*   `author:defunkt` - Find issues created by a specific user.
*   `mentions:imsinghaditya07` - Find issues where someone tagged you.
*   `label:bug` - Find issues tagged with the 'bug' label.

---

## 💡 Quick Navigation Shortcuts

If you are inside a repository's code view on GitHub, use these keyboard shortcuts:

*   **Press `t`**: Instantly search for specific files within the repository using a fuzzy finder (just like `Ctrl+P` in VS Code).
*   **Press `.` (Period Key)**: This is pure magic! Pressing `.` will instantly open the repository in **GitHub.dev** (a web-based VS Code editor), allowing you to browse the code using a familiar file tree and syntax highlighting without cloning!
*   **Press `l`**: Jump to a specific line number.
