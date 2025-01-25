# Committing Changes in Git

After staging files, the next step is to **commit** them. A commit is a snapshot of your repository at a specific point in time. It saves the current state of your project and includes a message describing the changes made. Commits are the building blocks of your project's history in Git.

---

## What is a Commit?

A commit is a way to save the state of your repository. It includes:

- **Changes:** All the modifications that were staged using `git add`.
- **Message:** A description of the changes made in the commit. This helps you and others understand what was done and why.

---

## How to Commit Changes

To commit staged files, use the `git commit` command followed by the `-m` flag to include a commit message. For example:

```bash
git commit -m "your message here"
```

### Example:

```bash
git commit -m "Add initial project structure"
```

This command creates a commit with the message `"Add initial project structure"`.

---

## Steps to Commit Changes

1. **Stage the Files:**  
   Use `git add` to stage the files you want to include in the commit:

   ```bash
   git add <file1> <file2>
   ```

2. **Commit the Changes:**  
   Use `git commit` to create a commit with a descriptive message:

   ```bash
   git commit -m "A: add contents.md"
   ```

3. **Check the Status:**  
   After committing, you can verify the status of your repository using:

   ```bash
   git status
   ```

   You should see output indicating that there are no changes to commit and the working directory is clean.

---

## Fixing a Commit Message

If you make a mistake in your commit message, you can change it using the `--amend` flag. For example:

```bash
git commit --amend -m "Updated commit message"
```

This command updates the message of the most recent commit.

---

## Why Commit Changes?

- **Track Progress:** Commits allow you to save and track the progress of your project over time.
- **Collaborate Effectively:** Clear commit messages help team members understand the changes made.
- **Revert Mistakes:** If something goes wrong, you can revert to a previous commit to undo changes.

---
