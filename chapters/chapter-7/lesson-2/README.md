# Git Merge Commits Guide

This guide explains what a merge commit is, how it works, and provides a step-by-step assignment to practice merging branches in Git.

---

## What is a Merge Commit?

A **merge commit** is the result of combining two branches. When you merge one branch into another, Git creates a new commit that incorporates the changes from both branches. This commit has two parent commits, one from each branch.

---

## Visual Example of a Merge Commit

Let's say you start with the following commit history:

```
A - B - C    main
   \
    D - E    vimchadsonly
```

When you merge `vimchadsonly` into `main` by running `git merge vimchadsonly` while on the `main` branch, Git will:

1. Find the **merge base** (the best common ancestor of the two branches). In this case, it's commit `A`.
2. Replay the changes from `main` (starting from `A`) into a new commit.
3. Replay the changes from `vimchadsonly` (starting from `A`) onto `main`.
4. Record the result as a new commit, in this case, `F`.

The resulting commit history will look like this:

```
A - B - C - F    main
   \     /
    D - E        vimchadsonly
```

Here, `F` is a special merge commit with two parents: `C` (from `main`) and `E` (from `vimchadsonly`).

---

## Assignment: Merge `add_classics` into `main`

Your current `webflyx` commit history looks like this:

```
A - B - C - E    main
         \
           D     add_classics
```

### Steps to Complete the Assignment

1. **Switch to the `main` branch**:

   ```bash
   git checkout main
   ```

2. **Merge `add_classics` into `main`**:
   Run the following command to initiate the merge:

   ```bash
   git merge add_classics
   ```

3. **Update the commit message**:

   - Git will open a code editor (e.g., Vim, Nano, or your default editor) with a default merge commit message.
   - Update the commit message to start with `F:`. For example:
     ```
     F: Merge branch 'add_classics'
     ```
   - Save the file and close the editor:
     - In **Vim**: Press `Esc`, then type `:wq` and press `Enter`.
     - In **Nano**: Press `Ctrl + O` to save, then `Ctrl + X` to exit.
     - In **VSCode**: Press `Ctrl + S` (Windows/Linux) or `Cmd + S` (Mac) to save, then close the editor.

4. **View the commit history**:
   After the merge is complete, run the following command to see a visual representation of the commit history:

   ```bash
   git log --oneline --decorate --graph --parents
   ```

   Your commit history should now look like this:

   ```
   *   F: Merge branch 'add_classics'    main
   |\
   | * D: Add classics.csv              add_classics
   * | E: Update contents.md            main
   |/
   * C: Initial commit
   * B: Add titles.md
   * A: Initialize repository
   ```

---

### Tips

- **Fixing a Commit Message**:
  If you mess up the commit message, you can amend it using:

  ```bash
  git commit --amend -m "F: Merge branch 'add_classics'"
  ```

- **Exiting the Editor**:
  - **Nano**: Press `Ctrl + X`, then `Y` to confirm, and `Enter` to save.
  - **Vim**: Press `Esc`, then type `:wq` and press `Enter`.
  - **VSCode**: Save with `Ctrl + S` (Windows/Linux) or `Cmd + S` (Mac), then close the editor.

---

## Summary

- A merge commit combines changes from two branches into one.
- Use `git merge <branch>` to merge a branch into the current branch.
- Update the commit message to include a meaningful prefix (e.g., `F:`).
- Use `git log --oneline --decorate --graph --parents` to visualize the commit history.
