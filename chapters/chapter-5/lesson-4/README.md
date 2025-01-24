# Switching Branches in Git

In Git, **switching branches** allows you to move between different versions of your project. This is essential for working on multiple features, experiments, or bug fixes simultaneously. Git provides two commands for switching branches: `git switch` (recommended) and `git checkout` (older but still widely used). In this lesson, you'll learn how to switch branches using the `git switch` command.

---

## Why Switch Branches?

- **Work on Different Features:** Switch between branches to work on different tasks or features.
- **Isolation:** Keep changes isolated in separate branches until they're ready to be merged.
- **Testing:** Test changes in a specific branch without affecting the main codebase.

---

## How to Switch Branches

To switch to a branch, use the `git switch` command:

```bash
git switch <branch-name>
```

### Example:

To switch to a branch called `prime`, run:

```bash
git switch prime
```

---

## Older Command: `git checkout`

The `git checkout` command can also be used to switch branches, but it has additional functionalities that can make it less intuitive for simple branch switching. For example:

```bash
git checkout prime
```

While `git checkout` is still widely used, `git switch` is recommended for switching branches because it is more straightforward and user-friendly.

---

## Assignment: Switch Between Branches

1. **Switch to the `main` Branch:**  
   Run the following command to switch to the `main` branch:

   ```bash
   git switch main
   ```

2. **Verify the Current Branch:**  
   Run `git branch` to confirm that you're on the `main` branch. The current branch will be highlighted with an asterisk (`*`):

   ```bash
   git branch
   ```

   Example output:

   ```
     add_classics
   * main
   ```

3. **Switch Back to the `add_classics` Branch:**  
   Run the following command to switch back to the `add_classics` branch:

   ```bash
   git switch add_classics
   ```

4. **Verify the Current Branch:**  
   Run `git branch` again to confirm that you're on the `add_classics` branch:

   ```bash
   git branch
   ```

   Example output:

   ```
   * add_classics
     main
   ```
