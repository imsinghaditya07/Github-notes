# 📝 GitHub Flavored Markdown (GFM) Mastery

> *Mastering Markdown is essential for writing great `README` files, issues, pull requests, and documentation on GitHub.*

Markdown is a lightweight markup language that allows you to format text using a plain-text editor, which gets converted into structurally valid HTML. **GitHub Flavored Markdown (GFM)** is a variant specifically used across GitHub.

---

## 🏗️ 1. The Core Syntax (Standard Markdown)

These features work almost universally across any platform that supports Markdown.

### Headers
Use the hash/pound symbol (`#`) for headers. One hash for H1, two for H2...
```markdown
# Header 1 (Largest)
## Header 2
### Header 3
#### Header 4
##### Header 5
###### Header 6 (Smallest)
```

### Emphasis & Styling
```markdown
*This text will be italic*
_This will also be italic_

**This text will be bold**
__This will also be bold__

_You **can** combine them_
```

### Lists
Unordered Lists: Use `*`, `-`, or `+`
```markdown
* Item 1
* Item 2
  * Nested Item 2a
  * Nested Item 2b
```

Ordered Lists: Use numbers followed by periods.
```markdown
1. First item
2. Second item
   1. Subitem A
   2. Subitem B
```

### Links & Images
```markdown
[Click here to go to GitHub](https://github.com)

**Images:**
![Alt text describing the image](https://docs.github.com/assets/images/help/profile/example-image.png)
```

### Blockquotes
Use `>` for quoting text.
```markdown
> This is a blockquote. It's often used to quote other users in discussions.
> > Nested blockquotes work too!
```

---

## ⚡ 2. GitHub Flavored Markdown (GFM) Extensions

These are features specifically added by GitHub to make collaboration easier.

### Task Lists
Create checkboxes for your to-dos, issues, or pull request criteria. These can actually be clicked and toggled natively in the GitHub UI!
```markdown
- [x] Task completed
- [ ] Task pending
- [ ] Another pending task
```

### Code Formatting & Syntax Highlighting
Inline code:
```markdown
To install, run the `npm install` command.
```

Code Blocks: Use 3 backticks and append the language name for syntax highlighting.
```markdown
\```javascript
function greet(user) {
    console.log("Hello " + user);
}
greet("Aditya");
\```
```

### Tables
Create tabular data by using pipes (`|`) and hyphens (`-`).
```markdown
| Header 1 | Header 2 |
| -------- | -------- |
| Demo 1   | Cell A   |
| Demo 2   | Cell B   |
```
*Tip: Colons can be used to align columns!*
`| :--- | :---: | ---: |` (Left, Center, Right)

### Strikethrough
Use two tildes `~~` to cross out text.
```markdown
~~This was a mistake~~ The correct word is here.
```

### Mentions and References
- **@Mentions:** Mention users or teams using the `@` symbol. Ex: `@imsinghaditya07`
- **Issue/PR References:** Type `#` followed by the issue number. Ex: `Fixes #42` (this will automatically link to Issue #42).
- **Commit SHA:** GitHub auto-links any 40-character SHA hash to its commit page.

---

## 🎨 3. Advanced Features (Alerts & Math)

GitHub continues to add powerful features to markdown.

### Alerts/Callouts
Highlight important information.
```markdown
> [!NOTE]
> Useful information that users should know, even when skimming content.

> [!TIP]
> Helpful advice for doing things better or more easily.

> [!IMPORTANT]
> Key information users need to know to achieve their goal.

> [!WARNING]
> Urgent info that needs immediate user attention to avoid problems.

> [!CAUTION]
> Advises about risks or negative outcomes of certain actions.
```

### Math Expressions (KaTeX)
GitHub supports rendering LaTeX-style math formulas natively!

Inline Math (use `$`):
```markdown
This equation $x^2 + y^2 = z^2$ is the Pythagorean theorem.
```

Math Block (use `$$`):
```markdown
$$
\int_0^\infty e^{-x^2} dx = \frac{\sqrt{\pi}}{2}
$$
```

---

## 💡 Pro Tips

1. **Collapsible Sections:** Need to hide large error logs or huge blocks of text? Use HTML details tags!
   ```html
   <details>
   <summary>Click here to see the giant error log</summary>
   
   Here is the massive text that was hidden...
   </details>
   ```

2. **Emojis:** Use the format `:emoji_name:` (e.g., `:rocket:`, `:fire:` :star:).
3. **Keyboard Shortcuts:** You can represent keystrokes using HTML `<kbd>` tags.
   Ex: Press <kbd>Ctrl</kbd> + <kbd>C</kbd> to copy.

Use this cheatsheet next time you are writing documentation or opening an issue, and your repos will immediately look more professional.
