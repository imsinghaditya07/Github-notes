# 🤖 GitHub Copilot: Your AI Pair Programmer

GitHub Copilot is more than just autocomplete. It's an AI pair programmer that can explain code, generate tests, and refactor entire functions.

---

## 🚀 1. Getting Started
-   **Install:** Search for "GitHub Copilot" in the extensions marketplace of your editor (VS Code, JetBrains, Visual Studio, Neovim).
-   **Sign In:** You'll need an active GitHub Copilot subscription (or free trial).

---

## 💡 2. Triggering Suggestions (VS Code)
-   **Inline Suggestions:** Just start typing. Ghost text will appear.
    -   `Tab`: Accept suggestion.
    -   `Alt + [` / `Alt + ]` (Windows): Cycle through multiple suggestions.
    -   `Ctrl + Enter`: Open GitHub Copilot panel to see 10 different solutions at once.

---

## 💬 3. Copilot Chat (The Real Power)
Don't just rely on ghost text. Use the Chat sidebar (`Ctrl + I` inline or the Chat panel).

### Best Prompting Strategies
1.  **Be Specific:** Instead of "Fix this," say "Refactor this function to reduce complexity and add error handling."
2.  **Provide Context:** Select the code you want it to look at before asking.
3.  **Iterate:** If the first answer isn't perfect, tell it why using natural language ("Make it faster", "Use ES6 syntax").

**Slash Commands:**
-   `/tests`: Generate unit tests for the selected code.
-   `/fix`: Propose a fix for the bugs in the selected code.
-   `/explain`: Explain how the selected code works.
-   `/doc`: Add documentation comments (JSDoc, Python Docstrings).

---

## 🧠 4. Advanced Tricks
-   **Comment Driven Development:** Write a comment describing what you want, and let Copilot generate the code below it.
    ```python
    # Function to validate email address using regex
    def validate_email(email):
    ```
-   **Naming Matters:** Give your variables and functions descriptive names. Copilot uses these to infer intent.
-   **Open Files:** Copilot looks at other open tabs in your editor to understand your project's context/style. Keep relevant files open!

---
[⬅️ Back to Home](../README.md)
