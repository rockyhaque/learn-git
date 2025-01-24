# What is a Git Branch?

A **Git branch** is a lightweight pointer to a specific commit in your repository. It allows you to work on different versions of your project simultaneously without affecting the main codebase. Branches are essential for managing features, experiments, and bug fixes in a structured and organized way.

---

## Why Use Branches?

Branches are useful for:

- **Isolating Changes:** Work on new features or experiments without affecting the main codebase.
- **Collaboration:** Multiple developers can work on different branches simultaneously.
- **Testing:** Test changes in a separate branch before merging them into the main branch.
- **Versioning:** Maintain different versions of your project (e.g., stable, development, experimental).

---

## Example: Using Branches

Suppose you're working on a web project and want to experiment with a new color scheme. Instead of making changes directly to the `master` branch, you can create a new branch called `color_scheme`. This allows you to work on the new color scheme in isolation. When you're done, if you like the changes, you can merge the `color_scheme` branch back into the `master` branch to keep the changes. If you don't like the changes, you can simply delete the `color_scheme` branch and go back to the `master` branch.

---

## Under the Hood

- **Branch as a Pointer:** A branch is simply a named pointer to a specific commit. When you create a branch, Git creates a new pointer to the current commit.
- **Lightweight:** Branches are lightweight because they only store a pointer to a commit, not a full copy of the project.
- **Default Branch:** The default branch in most repositories is called `main` or `master`. This is where your stable code typically resides.

---

## Assignment: Check Your Current Branch

1. **Check the Current Branch:**  
   Run the following command to see which branch you're currently on:

   ```bash
   git branch
   ```

   If you followed the course setup, you should be on the `master` branch.

---
