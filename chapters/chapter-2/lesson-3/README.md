# Staging Files in Git

When you create or modify files in your Git repository, they start as **untracked** or **modified**. To include these changes in your next commit, you need to **stage** them using the `git add` command. Staging allows you to selectively choose which changes to include in your commit, giving you control over what gets saved in the repository's history.

---

## What is Staging?

Staging is the process of adding files to the **index** (also called the staging area). Files in the staging area are marked for inclusion in the next commit. Without staging, every file in the repository would be included in every commit, which is often not what you want.

---

## How to Stage Files

To stage a file, use the `git add` command followed by the file path or pattern. For example:

```bash
git add <path-to-file | pattern>
```

### Example:

```bash
git add contents.md
```

This command stages the `contents.md` file, preparing it for the next commit.

---

## Assignment: Stage `contents.md`

Let's stage the `contents.md` file that you created earlier.

1. **Stage the File:**  
   Run the following command to stage `contents.md`:

   ```bash
   git add contents.md
   ```

2. **Check the Status:**  
   After staging the file, run `git status` to see the updated state of your repository:

   ```bash
   git status
   ```

   You should see output indicating that `contents.md` is now **staged** and ready to be committed.

---

## Example Output of `git status` After Staging

After running `git add contents.md` and `git status`, you might see something like this:

```bash
On branch main

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   contents.md
```

This output tells you that `contents.md` is staged and ready to be committed.

---
