# Merge Between Local and Remote Repos

Just as we can merge branches within a local repository, we can also merge branches between local and remote repositories.

### Command Syntax

To merge a remote branch into your local branch, use:

```bash
git merge <remote>/<branch>
```

For example, to merge the `primeagen` branch from the `origin` remote into your local `main` branch:

```bash
git merge origin/primeagen
```

---

## Assignment

### Goal

Merge the remote `origin/main` branch into the local `main` branch.

### Steps

1. **Navigate to the `webflyx-local` Repository**

   ```bash
   cd path/to/webflyx-local
   ```

2. **Ensure You're on the `main` Branch**

   ```bash
   git checkout main
   ```

3. **Merge the Remote `origin/main` Branch**  
   Merge the remote `origin/main` branch into your local `main` branch:

   ```bash
   git merge origin/main
   ```

4. **Verify the Merge with `git log`**  
   Run the following command to check the commit history:
   ```bash
   git log --oneline
   ```
   You should see all the same commits on your local `main` branch as you do on the remote `origin/main` branch.

---

Done! 🎉
