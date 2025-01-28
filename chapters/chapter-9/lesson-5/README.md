# Log Remote

The `git log` command is not just useful for your local repository. You can also use it to view the commits from a remote repository!

### Command Syntax

To log commits from a remote repository, use the following syntax:

```bash
git log <remote>/<branch>
```

For example, to see the commits from the `primeagen` branch on the `origin` remote:

```bash
git log origin/primeagen
```

---

## Assignment

### Goal

View the commit history from the remote `webflyx` repository’s `update_dune` branch using the `--oneline` flag.

### Steps

1. **Navigate to the `webflyx-local` Repository**

   ```bash
   cd path/to/webflyx-local
   ```

2. **Run the Git Log Command**  
   To view the commits on the remote `webflyx` repository's `update_dune` branch, run:

   ```bash
   git log origin/update_dune --oneline
   ```

3. **Expected Output**  
   You should see the commits "A" through "I" from the `update_dune` branch.

---

Done! 🎉
