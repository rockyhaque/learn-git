# Understanding File States in Git

In a Git repository, a file can be in one of several states. Understanding these states is crucial for effectively managing your project. Here are the key states:

1. **Untracked:**  
   The file is not being tracked by Git. It exists in your working directory but has not been added to the repository.

2. **Staged:**  
   The file has been marked for inclusion in the next commit. Changes to the file are ready to be saved in the repository's history.

3. **Committed:**  
   The file has been saved to the repository's history. It is part of a snapshot (commit) in the Git timeline.

---

## Checking File Status with `git status`

The `git status` command shows the current state of your repository. It tells you which files are untracked, staged, or committed. This command is essential for understanding the changes in your working directory and staging area.

---

## Assignment: Create and Check Status of a File

Let's create a file and check its status using `git status`.

1. **Create a File:**  
   In the root of your `webflyx` directory, create a file called `contents.md` and add the following text to it:

   ```markdown
   # contents
   ```

2. **Save the File:**  
   Save the file after adding the text.

3. **Check the Status:**  
   Run the following command to check the status of your repository:

   ```bash
   git status
   ```

   You should see output indicating that `contents.md` is an **untracked file**.

---

## Example Output of `git status`

After running `git status`, you might see something like this:

```bash
On branch main

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        contents.md

nothing added to commit but untracked files present (use "git add" to track)
```

This output tells you that `contents.md` is untracked and not yet staged for commit.

---
