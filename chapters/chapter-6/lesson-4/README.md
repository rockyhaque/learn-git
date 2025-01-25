# Git Fast-Forward Merge and Workflow Guide

This guide explains what a **fast-forward merge** is, how it works, and provides a step-by-step assignment to practice deleting a merged branch, creating a new branch, and making changes.

---

## What is a Fast-Forward Merge?

A **fast-forward merge** is the simplest type of merge in Git. It occurs when the branch being merged (`feature`) is directly ahead of the base branch (`main`). In this case, Git simply moves the pointer of the base branch to the tip of the feature branch without creating a new merge commit.

### Example

Starting with this commit history:

```
      C     delete_vscode
     /
A - B       main
```

When you run `git merge delete_vscode` while on `main`, Git performs a fast-forward merge:

```
            delete_vscode
A - B - C   main
```

Notice that no merge commit is created. The `main` branch pointer simply moves forward to commit `C`.

---

## Common Git Workflow

A typical Git workflow for teams involves:

1. **Create a branch** for a new change.
2. **Make the change** on the branch.
3. **Merge the branch** back into `main` (or the default branch).
4. **Remove the branch** after merging.
5. **Repeat** for the next change.

---

## Assignment: Update `titles.md`

### Steps to Complete the Assignment

1. **Delete the `add_classics` Branch**:
   Since `add_classics` has been merged into `main`, it’s no longer needed. Delete it with:

   ```bash
   git branch -d add_classics
   ```

2. **Create a New Branch Called `update_titles`**:
   Create and switch to a new branch using:

   ```bash
   git switch -c update_titles
   ```

3. **Update the `titles.md` File**:
   Open the `titles.md` file and add `"The Curious Case of Benjamin Button"` as the final entry in the list of movies. For example:

   ```markdown
   - Inception
   - The Matrix
   - Interstellar
   - The Curious Case of Benjamin Button
   ```

4. **Commit the Changes**:
   Stage and commit the changes with a commit message prefixed by `G:`:

   ```bash
   git add titles.md
   git commit -m "G: Add 'The Curious Case of Benjamin Button' to titles.md"
   ```

5. **Verify the Commit**:
   Run the following command to ensure the commit was successfully added:
   ```bash
   git log --oneline
   ```

---

### Expected Output of `git log --oneline`

After completing the assignment, the output of `git log --oneline` should look something like this:

```
abc1234 (HEAD -> update_titles) G: Add 'The Curious Case of Benjamin Button' to titles.md
def5678 (main) F: Merge branch 'add_classics'
ghi9012 E: Update contents.md
jkl3456 D: Add classics.csv
mno7890 C: Add quotes
pqr1234 B: Add titles.md
stu5678 A: Add contents.md
```

---

## Key Points to Remember

- **Fast-Forward Merge**: Occurs when the feature branch is directly ahead of the base branch. No merge commit is created.
- **Branch Workflow**: Create a branch, make changes, merge, and delete the branch.
- **Deleting Branches**: Use `git branch -d <branch_name>` to delete a merged branch.
- **Creating Branches**: Use `git switch -c <branch_name>` to create and switch to a new branch.

---
