# Exploring Git Log Flags

The `git log` command is a powerful tool for viewing the commit history of your repository. By default, it shows a detailed list of commits, but you can customize its output using various flags. In this lesson, you'll learn about two useful flags: `--decorate` and `--oneline`. These flags help you make the output of `git log` more readable and informative.

---

## Why Use Git Log Flags?

- **Readability:** Customize the output of `git log` to make it easier to understand.
- **Efficiency:** Quickly view the commit history without unnecessary details.
- **Debugging:** Identify specific commits or branches more easily.

---

## Git Log Flags

### 1. `--decorate`

The `--decorate` flag adds information about **references** (e.g., branches, tags) to the commit history. It has three options:

- **`short` (default):** Shows abbreviated branch and tag names.
- **`full`:** Shows the full reference names.
- **`no`:** Hides all references.

#### Example:

- **Full Decoration:**

  ```bash
  git log --decorate=full
  ```

  This shows the full reference names, such as `refs/heads/main` or `refs/heads/add_classics`.

- **No Decoration:**

  ```bash
  git log --decorate=no
  ```

  This hides all branch and tag information.

### 2. `--oneline`

The `--oneline` flag condenses each commit into a single line, showing only the commit hash and the commit message. This is useful for quickly scanning the commit history.

#### Example:

```bash
git log --oneline
```

Output:

```
5ba786f (HEAD -> main, origin/main) Add README file
4e507fd Update dependencies
3c1a2b0 Fix bug in login feature
```

---

## Assignment: Use Git Log Flags

1. **Run `git log` with Full Decoration and Oneline Flag:**  
   Combine the `--decorate=full` and `--oneline` flags to view a compact commit history with full reference names:

   ```bash
   git log --decorate=full --oneline
   ```

   Example output:

   ```
   5ba786f (HEAD -> refs/heads/main, refs/remotes/origin/main) Add README file
   4e507fd (refs/heads/add_classics) Update dependencies
   3c1a2b0 Fix bug in login feature
   ```

---
