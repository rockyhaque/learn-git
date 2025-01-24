# Default Branch in Git

In Git, the **default branch** is the primary branch where your stable code typically resides. Historically, the default branch was named `master`, but many platforms, including **GitHub**, have transitioned to using `main` as the default branch name. This change promotes inclusivity and aligns with modern best practices.

---

## Why Use `main` as the Default Branch?

- **Modern Standard:** Platforms like GitHub now use `main` as the default branch name.
- **Inclusivity:** The term `main` is more inclusive and neutral compared to `master`.
- **Consistency:** Using `main` ensures consistency with remote repositories hosted on platforms like GitHub.

---

## How to Rename a Branch

To rename a branch, use the following command:

```bash
git branch -m <old-name> <new-name>
```

### Example:

To rename the `master` branch to `main`, run:

```bash
git branch -m master main
```

---

## Assignment: Switch to `main` as the Default Branch

1. **Change the Global Default Branch:**  
   Update your global Git configuration to use `main` as the default branch for new repositories:

   ```bash
   git config --global init.defaultBranch main
   ```

2. **Check the Current Branch:**  
   Run the following command to see which branch you're currently on:

   ```bash
   git branch
   ```

   You should still be on the `master` branch because changing the default branch only affects new repositories.

3. **Rename the Current Branch:**  
   Rename the `master` branch to `main` in your current repository:

   ```bash
   git branch -m master main
   ```

4. **Verify the Change:**  
   Run `git branch` again to confirm that you're now on the `main` branch:

   ```bash
   git branch
   ```

   The output should show `main` as the current branch.

---

## Why This Matters

- **Consistency:** Aligning your local repository with remote platforms like GitHub ensures smoother collaboration.
- **Best Practices:** Using `main` as the default branch follows modern Git conventions.
- **Future-Proofing:** New repositories created on your system will automatically use `main` as the default branch.

---
