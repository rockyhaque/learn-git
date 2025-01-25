# Git Branching and Merging Guide

This guide explains the purpose of using multiple branches in Git, how to merge them, and provides a step-by-step assignment to practice these concepts.

---

## Why Use Multiple Branches?

You might ask, _"What's the point of having multiple branches?"_ Branches are commonly used to safely make changes without affecting the primary branch (e.g., `main`). Once you're satisfied with your changes, you can merge them back into the main branch to incorporate them into the final product.

---

## Visual Example of Branching and Merging

Imagine you have two branches, each with their own unique commits:

```
A - B - C    main
   \
    D - E    other_branch
```

When you merge `other_branch` into `main`, Git combines both branches by creating a new merge commit. This commit has both histories as parents. In the diagram below, `F` is the merge commit that combines the changes from `D` and `E` into `main`:

```
A - B - C - F    main
   \     /
    D - E        other_branch
```

---

## Assignment: Update `contents.md` and Commit Changes

1. **Switch back to the `main` branch**:

   ```bash
   git checkout main
   ```

2. **Update the `contents.md` file**:
   Open `contents.md` and add the following content:

   ```markdown
   # contents

   - titles.md: The movie titles in the WebFlyx collection
   - classics.csv: A comma-separated list of classic movies
   - quotes: A directory of files containing memorable quotes from movies
   ```

3. **Commit the changes**:
   Use a commit message starting with `E:`:

   ```bash
   git add contents.md
   git commit -m "E: Update contents.md with file descriptions"
   ```

4. **View the commit history**:
   Run the following command to see a visual representation of your commit history:

   ```bash
   git log --oneline --graph --all
   ```

   Your commit history should now look like this:

   ```
   A - B - C - E    main
            \
              D     add_classics
   ```

---

## Additional Git Log Commands

- View a graphical representation of the commit history:

  ```bash
  git log --graph
  ```

- View the commit history for all branches:
  ```bash
  git log --all
  ```

---

## Summary

- Branches allow you to work on changes independently without affecting the main branch.
- Merging combines changes from one branch into another, creating a new merge commit.
- Use `git log --oneline --graph --all` to visualize your commit history.
