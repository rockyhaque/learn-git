# Creating a New Branch in Git

In Git, creating a new branch allows you to work on a separate version of your project without affecting the main codebase. This is particularly useful for developing new features, fixing bugs, or experimenting with changes. When you create a new branch, it starts from the current commit you're on, meaning it inherits the entire commit history up to that point.

---

## Why Create a New Branch?

- **Isolation:** Work on new features or experiments without affecting the main branch.
- **Collaboration:** Multiple developers can work on different branches simultaneously.
- **Testing:** Test changes in a separate branch before merging them into the main branch.

---

## Two Ways to Create a Branch

1. **Create a Branch Without Switching:**  
   Use the `git branch` command to create a new branch:

   ```bash
   git branch <branch-name>
   ```

   Example:

   ```bash
   git branch my_new_branch
   ```

   This creates a new branch but does not switch to it.

2. **Create and Switch to a Branch:**  
   Use the `git switch -c` command to create a new branch and switch to it immediately:

   ```bash
   git switch -c <branch-name>
   ```

   Example:

   ```bash
   git switch -c my_new_branch
   ```

   This is the most common way to create and switch to a new branch in one step.

---

## How It Works

When you create a new branch, it uses the current commit you're on as the base. For example, if you're on the `main` branch with commits `A`, `B`, and `C`, and you run `git switch -c my_new_branch`, the new branch will start from commit `C` and inherit the same history.

---

## Assignment: Create and Switch to a New Branch

1. **Create and Switch to a New Branch:**  
   Create a new branch called `add_classics` and switch to it immediately:

   ```bash
   git switch -c add_classics
   ```

2. **Verify the Current Branch:**  
   Run the following command to confirm that you're on the `add_classics` branch:

   ```bash
   git branch
   ```

   The current branch will be highlighted with an asterisk (`*`). For example:

   ```
   * add_classics
     main
   ```
