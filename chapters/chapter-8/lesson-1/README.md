# Undoing Changes in Git

One of the major benefits of using Git is the ability to undo changes. This guide walks you through how to simulate and fix a common mistake: overwriting a file.

---

## Assignment: Simulating a Mistake

The new intern at Webflyx tried to add their favorite movie to the `titles.md` file but accidentally overwrote the entire file. To simulate this, follow the steps below.

---

### Steps to Complete the Assignment

1. **Overwrite the `titles.md` File**:
   Simulate the intern's mistake by overwriting the `titles.md` file with the following line:

   ```bash
   echo "* The Internship" > titles.md
   ```

2. **Check the Status**:
   Verify that the file has been changed by running:

   ```bash
   git status
   ```

   You should see `titles.md` listed as a modified file.

3. **Commit the Changes**:
   Commit the changes with a commit message starting with `J:` (as per the assignment instructions). For example:

   ```bash
   git add titles.md
   git commit -m "J: Overwrote titles.md with The Internship"
   ```

4. **Verify the Commit**:
   Check the commit history to confirm the commit:

   ```bash
   git log --oneline
   ```

   You should see your commit with the message `J: Overwrote titles.md with The Internship`.

---

## Key Points to Remember

- **Overwriting Files**: Be cautious when using `>` in the command line, as it replaces the entire file content.
- **Checking Status**: Always use `git status` to verify changes before committing.
- **Commit Messages**: Use clear and descriptive commit messages to track changes effectively.

---

## Summary

1. Overwrite the file: `echo "* The Internship" > titles.md`.
2. Check the status: `git status`.
3. Commit the changes: `git add titles.md` and `git commit -m "J: Overwrote titles.md with The Internship"`.
4. Verify the commit: `git log --oneline`.

---
