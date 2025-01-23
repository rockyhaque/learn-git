# Storing Data in Git

Git stores data in a unique way that ensures efficiency and reliability. Unlike some version control systems that store only the changes (deltas) between commits, Git stores **entire snapshots** of your project for each commit. This approach, combined with optimizations like compression and deduplication, ensures that your repository remains efficient even as it grows.

---

## How Git Stores Data

1. **Snapshots, Not Deltas:**  
   Each commit in Git stores a complete snapshot of your project at that point in time. This means that every file in your repository is stored in its entirety for each commit.

2. **Optimizations:**  
   To prevent the `.git` directory from becoming excessively large, Git uses several optimizations:
   - **Compression:** Git compresses files to reduce storage size.
   - **Deduplication:** If a file remains unchanged between commits, Git stores it only once and references it in subsequent commits.

---

## Assignment: Exploring Git's Data Storage

In this assignment, you'll explore how Git stores data by creating new files and inspecting their blob hashes.

### Step 1: Inspect the Blob Hash for `titles.md`

1. Use `git cat-file -p` to view the hash of the blob for the `titles.md` file in your last commit:

   ```bash
   git cat-file -p <commit-hash> | grep titles.md
   ```

   Save this hash for later comparison.

### Step 2: Add New Files

1. Create a new directory called `quotes`:

   ```bash
   mkdir quotes
   ```

2. Add two files inside the `quotes` directory:

   - **`starwars.md`**:

     ```markdown
     - "May the Force be with you"
     - "I find your lack of faith disturbing"
     - "I am your father"
     - "Do or do not. There is no try"
     - "I've got a bad feeling about this"
     ```

   - **`dune.md`**:
     ```markdown
     - "May thy knife chip and shatter"
     - "A Great Man Doesn't Seek To Lead. He's Called To It."
     - "An Animal Caught In A Trap Will Gnaw Off Its Own Leg To Escape. What Will You Do?"
     - "When Is A Gift Not A Gift?"
     ```

### Step 3: Stage and Commit the Changes

1. Stage the new files:

   ```bash
   git add quotes/starwars.md quotes/dune.md
   ```

   Alternatively, stage all changes at once:

   ```bash
   git add .
   ```

2. Commit the changes with a meaningful commit message. For example:
   ```bash
   git commit -m "Add quotes directory with starwars.md and dune.md"
   ```

### Step 4: Inspect the Blob Hash for `titles.md` Again

1. Use `git cat-file -p` to view the hash of the blob for the `titles.md` file in the latest commit:

   ```bash
   git cat-file -p <new-commit-hash> | grep titles.md
   ```

   You'll notice that the hash for `titles.md` is the same as before because the file hasn't changed. This demonstrates Git's deduplication feature.

---

## Why This Matters

- **Efficiency:** By storing snapshots and deduplicating unchanged files, Git ensures that your repository remains efficient even as it grows.
- **Reliability:** Storing entire snapshots makes it easier to recover previous states of your project.
- **Understanding Git Internals:** Exploring how Git stores data helps you understand its architecture and use it more effectively.

---
