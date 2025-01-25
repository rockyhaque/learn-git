# Git Merge Log Explanation

This guide explains how to interpret the output of `git log --oneline --decorate --graph --parents` after performing a merge. It also provides a breakdown of the commit history structure.

---

## Understanding the Merge Log

After merging two branches, running the following command will display a detailed log of your commit history:

```bash
git log --oneline --decorate --graph --parents
```

Here’s an example of what the output might look like:

```
*   89629a9 d234104 b8dfd64 (HEAD -> main) F: Merge branch 'add_classics'
|\
| * b8dfd64 fba0999 (tag: 5.8, add_classics) D: add classics
* | d234104 fba0999 (tag: 6.1) E: update contents
|/
* fba0999 1381199 (tag: 3.8, origin/master, origin/main, master) C: add quotes
* 1381199 a21228f (tag: 3.7) B: add titles.md
* a21228f A: add contents.md
```

---

## Breakdown of the Merge Log

### 1. **Merge Commit**

```
*   89629a9 d234104 b8dfd64 (HEAD -> main) F: Merge branch 'add_classics'
```

- This is the **merge commit** created when you merged `add_classics` into `main`.
- **89629a9**: The hash of the merge commit.
- **d234104** and **b8dfd64**: The hashes of the two parent commits (from `main` and `add_classics`, respectively).
- **(HEAD -> main)**: Indicates that `main` is the current branch.
- **F: Merge branch 'add_classics'**: The commit message for the merge.

---

### 2. **Branch Structure**

```
|\
| * b8dfd64 fba0999 (tag: 5.8, add_classics) D: add classics
* | d234104 fba0999 (tag: 6.1) E: update contents
|/
```

- This section visually represents the branches before the merge:
  - The left branch (`|`) represents `main`.
  - The right branch (`| *`) represents `add_classics`.
- **b8dfd64**: The last commit on the `add_classics` branch before the merge.
- **d234104**: The last commit on the `main` branch before the merge.
- Both branches share a common ancestor (`fba0999`).

---

### 3. **Normal Commits**

```
* fba0999 1381199 (tag: 3.8, origin/master, origin/main, master) C: add quotes
* 1381199 a21228f (tag: 3.7) B: add titles.md
* a21228f A: add contents.md
```

- These are the commits that occurred before the branches diverged.
- Each commit points to its parent commit:
  - **fba0999**: The commit that added quotes.
  - **1381199**: The commit that added `titles.md`.
  - **a21228f**: The initial commit that added `contents.md`.

---

## Key Points to Remember

- **Asterisks (`*`)**: Represent commits in the repository.
- **Parent Hashes**: The `--parents` flag includes the parent commit hashes for each commit.
- **Merge Commit**: A merge commit has two parent hashes, one from each branch.
- **Branch Visualization**: The `--graph` flag creates a visual representation of the branch structure.
- **Tags and Branches**: The `--decorate` flag shows tags and branch names associated with commits.

---

## Tips

- **Amending a Commit Message**:
  If you make a mistake, you can amend the commit message with:

  ```bash
  git commit --amend -m "F: Merge branch 'add_classics'"
  ```

- **Exiting the Editor**:
  - **Vim**: Press `Esc`, then type `:wq` and press `Enter`.
  - **Nano**: Press `Ctrl + X`, then `Y` to confirm, and `Enter` to save.
  - **VSCode**: Save with `Ctrl + S` (Windows/Linux) or `Cmd + S` (Mac), then close the editor.

---
