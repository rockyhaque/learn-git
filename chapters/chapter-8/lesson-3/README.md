# Git Reset Hard

The `git reset --hard` command is used to undo changes and reset your working directory to a specific commit. Unlike `git reset --soft`, this command discards all changes in the working directory and staging area, bringing your repository back to the exact state of the specified commit.

---

## Using `git reset --hard`

The `--hard` option is useful when you want to completely discard all changes and go back to a previous commit. Here’s how it works:

- **Committed changes**: These will be removed, and the branch pointer will move to the specified commit.
- **Uncommitted changes**: These will be discarded, and the working directory will match the state of the specified commit.

### Command Syntax

```bash
git reset --hard COMMITHASH
```

---

## Assignment: Using `git reset --hard`

Your current branch, `update_dune`, has a staged change to the `titles.md` file. Follow the steps below to reset your branch to commit `I` and discard all changes.

---

### Steps to Complete the Assignment

1. **Check the Status**:
   Confirm that there is a staged change to the `titles.md` file by running:

   ```bash
   git status
   ```

   You should see `titles.md` listed as a modified file.

2. **Find the Commit Hash for Commit `I`**:
   Use `git log` to find the commit hash for commit `I`:

   ```bash
   git log --oneline
   ```

   Example output:

   ```
   abc1234 (HEAD -> update_dune) J: Overwrote titles.md with The Internship
   def5678 I: Add 'Dune' to titles.md
   ghi9012 H: Update contents.md
   ```

   Copy the commit hash for commit `I` (e.g., `def5678`).

3. **Reset to Commit `I`**:
   Run the following command to reset to commit `I` and discard all changes:

   ```bash
   git reset --hard def5678
   ```

   Replace `def5678` with the actual commit hash for commit `I`.

4. **Verify the Reset**:
   Check the commit history again to confirm that commit `J` is no longer in the log:

   ```bash
   git log --oneline
   ```

   Example output after reset:

   ```
   def5678 (HEAD -> update_dune) I: Add 'Dune' to titles.md
   ghi9012 H: Update contents.md
   ```

5. **Check the Status**:
   Verify that the `titles.md` file has been reset and there are no changes:

   ```bash
   git status
   ```

   You should see a clean working directory with no changes.

---

## Key Points to Remember

- **`git reset --hard`**: Discards all changes and resets the working directory to the specified commit.
- **Commit Hash**: Use `git log` to find the commit hash for the commit you want to reset to.
- **Verification**: Always verify the commit history and status after performing a reset.

---

## Summary

1. Check the status: `git status`.
2. Find the commit hash for commit `I`: `git log --oneline`.
3. Reset to commit `I`: `git reset --hard <hash>`.
4. Verify the reset: `git log --oneline`.
5. Check the status: `git status`.

---
