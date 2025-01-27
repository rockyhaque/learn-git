# Git Reset Soft

The `git reset` command is a powerful tool for undoing changes in Git. It can be used to undo the last commit(s) or any changes in the index (staged but not committed changes) and the worktree (unstaged and not committed changes).

---

## Using `git reset --soft`

The `--soft` option is particularly useful if you want to go back to a previous commit while keeping all of your changes. Here’s how it works:

- **Committed changes**: These will be uncommitted and staged.
- **Uncommitted changes**: These will remain staged or unstaged as before.

### Command Syntax

```bash
git reset --soft COMMITHASH
```

---

## Assignment: Using `git reset --soft`

Your current branch, `update_dune`, should be at commit `J` with a changed `titles.md` file. Follow the steps below to go back to commit `I` while keeping the changes in `titles.md` staged but not committed.

---

### Steps to Complete the Assignment

1. **Check the Commit History**:
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

2. **Reset to Commit `I`**:
   Run the following command to reset to commit `I` while keeping your changes:

   ```bash
   git reset --soft def5678
   ```

   Replace `def5678` with the actual commit hash for commit `I`.

3. **Verify the Reset**:
   Check the commit history again to confirm that commit `J` is no longer in the log:

   ```bash
   git log --oneline
   ```

   Example output after reset:

   ```
   def5678 (HEAD -> update_dune) I: Add 'Dune' to titles.md
   ghi9012 H: Update contents.md
   ```

4. **Check the Status**:
   Verify that the changes to `titles.md` are still staged but not committed:

   ```bash
   git status
   ```

   You should see `titles.md` listed as a staged file.

---

## Key Points to Remember

- **`git reset --soft`**: Keeps your changes staged or unstaged while moving the branch pointer to a previous commit.
- **Commit Hash**: Use `git log` to find the commit hash for the commit you want to reset to.
- **Verification**: Always verify the commit history and status after performing a reset.

---

## Summary

1. Find the commit hash for commit `I`: `git log --oneline`.
2. Reset to commit `I`: `git reset --soft <hash>`.
3. Verify the reset: `git log --oneline`.
4. Check the status: `git status`.

---
