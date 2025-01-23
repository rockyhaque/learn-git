# Creating a Second Commit

In this lesson, you'll create a second commit to add a new file to your Git repository. This will help you understand how Git tracks changes and builds a history of your project. You'll also inspect the commit object to see how it differs from the first commit.

---

## Steps to Create a Second Commit

1. **Create a New File:**  
   Create a file called `titles.md` in your repository and add the following content:

   ```markdown
   # Titles

   - A River Runs Through It
   - Fight Club
   - 12 Years a Slave
   - The Big Short
   - 12 Monkeys
   ```

2. **Stage the File:**  
   Use `git add` to stage the new file for the next commit:

   ```bash
   git add titles.md
   ```

3. **Commit the Changes:**  
   Commit the changes with a meaningful commit message. For example:
   ```bash
   git commit -m "Add titles.md with a list of movie titles"
   ```

---

## Inspecting the Second Commit

After creating the second commit, you can inspect it using `git cat-file -p`. Follow these steps:

1. **Find the Commit Hash:**  
   Use `git log` to find the hash of the second commit:

   ```bash
   git log
   ```

2. **Inspect the Commit Object:**  
   Use `git cat-file -p` to view the contents of the commit object:

   ```bash
   git cat-file -p <commit-hash>
   ```

   Replace `<commit-hash>` with the actual hash of the second commit.

---

## Example Output of the Second Commit

When you inspect the second commit, you'll see output similar to this:

```
tree 8c7e5a4d2f1e4f6e8a9b1c2d3e4f5a6b7c8d9e0f
parent 5ba786fcc93e8092831c01e71444b9baa2228a4f
author Your Name <your.email@example.com> 1698765432 +0000
committer Your Name <your.email@example.com> 1698765432 +0000

Add titles.md with a list of movie titles
```

### Explanation of the Output:

- **tree:** The hash of the tree object representing the directory structure at the time of the commit.
- **parent:** The hash of the previous commit. This links the second commit to the first commit, forming a chain of commits.
- **author:** The name, email, and timestamp of the person who made the changes.
- **committer:** The name, email, and timestamp of the person who committed the changes (usually the same as the author).
- **Commit Message:** The message describing the changes made in the commit.

---

## What's Different in the Second Commit?

The second commit includes a **parent** field, which references the hash of the first commit. This field is not present in the first commit because it has no parent. The parent field links commits together to form the repository's history.

---

## Why Create a Second Commit?

- **Build History:** Each commit represents a snapshot of your project, allowing you to track changes over time.
- **Understand Commit Structure:** Inspecting commit objects helps you understand how Git links commits together to form a history.
- **Practice Git Workflow:** Staging and committing changes is a fundamental part of using Git effectively.

---

## Next Steps

Now that you've created a second commit, you can continue making changes, staging files, and committing them to build a complete history of your project. Combine this knowledge with other Git commands to become a more effective developer.

Happy coding! 🚀

---

## Difference Between the First and Second Commit

The key difference between the first and second commit is the presence of the **parent** field in the second commit. Here's a comparison:

### First Commit:

```
tree 4e507fdc6d9044ccd8a4a3061324c9f711c4667d
author Your Name <your.email@example.com> 1698765432 +0000
committer Your Name <your.email@example.com> 1698765432 +0000

Add contents.md
```

### Second Commit:

```
tree 8c7e5a4d2f1e4f6e8a9b1c2d3e4f5a6b7c8d9e0f
parent 5ba786fcc93e8092831c01e71444b9baa2228a4f
author Your Name <your.email@example.com> 1698765432 +0000
committer Your Name <your.email@example.com> 1698765432 +0000

Add titles.md with a list of movie titles
```

The **parent** field in the second commit links it to the first commit, creating a chain of commits that represents the history of your repository.
