# Git Fast-Forward Merge Guide

This guide explains what a **fast-forward merge** is, how it works, and provides a step-by-step assignment to practice performing a fast-forward merge and cleaning up branches.

---

## What is a Fast-Forward Merge?

A **fast-forward merge** occurs when the branch being merged (`feature`) is directly ahead of the base branch (`main`). In this case, Git simply moves the pointer of the base branch to the tip of the feature branch without creating a new merge commit.

### Example

#### Before the Merge:

```
      C     other_branch
     /
A - B       main
```

#### After the Merge (`git merge other_branch`):

```
            other_branch
A - B - C   main
```

Notice that no merge commit is created. The `main` branch pointer simply moves forward to commit `C`.

---

## Assignment: Perform a Fast-Forward Merge

### Steps to Complete the Assignment

1. **Switch to the `main` Branch**:
   Ensure you’re on the `main` branch by running:

   ```bash
   git switch main
   ```

2. **Verify the Commit History**:
   Check the commit history to confirm that the `G:` commit from `update_titles` is not yet in `main`:

   ```bash
   git log --oneline
   ```

   The output should look something like this:

   ```
   def5678 (HEAD -> main) F: Merge branch 'add_classics'
   ghi9012 E: Update contents.md
   jkl3456 D: Add classics.csv
   mno7890 C: Add quotes
   pqr1234 B: Add titles.md
   stu5678 A: Add contents.md
   ```

3. **Merge `update_titles` into `main`**:
   Perform the fast-forward merge by running:

   ```bash
   git merge update_titles
   ```

   Since `update_titles` is directly ahead of `main`, Git will perform a fast-forward merge, and the `main` branch pointer will move to the tip of `update_titles`.

4. **Verify the Merge**:
   Check the commit history again to confirm the merge:

   ```bash
   git log --oneline
   ```

   The output should now include the `G:` commit:

   ```
   abc1234 (HEAD -> main) G: Add 'The Curious Case of Benjamin Button' to titles.md
   def5678 F: Merge branch 'add_classics'
   ghi9012 E: Update contents.md
   jkl3456 D: Add classics.csv
   mno7890 C: Add quotes
   pqr1234 B: Add titles.md
   stu5678 A: Add contents.md
   ```

5. **Delete the `update_titles` Branch**:
   Since `update_titles` has been merged into `main`, it’s no longer needed. Delete it with:
   ```bash
   git branch -d update_titles
   ```

---

## Key Points to Remember

- **Fast-Forward Merge**: Occurs when the feature branch is directly ahead of the base branch. No merge commit is created.
- **Branch Cleanup**: Delete branches after they’ve been merged to keep your repository clean.
- **Verification**: Use `git log --oneline` to verify the commit history before and after the merge.

---

## Summary

1. Switch to `main`: `git switch main`.
2. Verify the commit history: `git log --oneline`.
3. Merge `update_titles` into `main`: `git merge update_titles`.
4. Verify the merge: `git log --oneline`.
5. Delete the `update_titles` branch: `git branch -d update_titles`.
