# Half of Git: The Basics

As a developer, you'll spend a significant amount of time using just a few essential Git commands. These commands form the foundation of your workflow and are crucial for managing your projects effectively. Here's a breakdown of what you need to know:

---

## The Core Git Workflow

The majority of your Git usage will revolve around three simple commands:

1. **`git status`**

   - **Purpose:** Check the current state of your repository.
   - **What it does:** Shows which files are untracked, modified, or staged for commit.
   - **Example:**
     ```bash
     git status
     ```

2. **`git add`**

   - **Purpose:** Stage changes for the next commit.
   - **What it does:** Marks specific files or changes to be included in the next snapshot (commit).
   - **Example:**
     ```bash
     git add <file>
     ```

3. **`git commit`**
   - **Purpose:** Save staged changes to the repository's history.
   - **What it does:** Creates a snapshot of the staged changes with a descriptive message.
   - **Example:**
     ```bash
     git commit -m "Your commit message"
     ```

These three commands make up **half of your Git workflow** as a solo developer. They allow you to track changes, organize your work, and maintain a history of your project.

---

## The Other Half of Git

While the core commands are essential, Git has much more to offer. The remaining usage can be divided into two main areas:

1. **Collaboration and Remote Work (40%)**

   - **Purpose:** Work with others and store your code on remote servers (e.g., GitHub, GitLab).
   - **Key Commands:**
     - `git clone`: Copy a remote repository to your local machine.
     - `git push`: Upload your commits to a remote repository.
     - `git pull`: Download changes from a remote repository and merge them into your local branch.
     - `git fetch`: Download changes from a remote repository without merging.

2. **Advanced Topics (10%)**
   - **Purpose:** Fix mistakes, roll back changes, and handle complex scenarios.
   - **Key Commands:**
     - `git reset`: Undo changes or move the HEAD pointer to a specific commit.
     - `git revert`: Create a new commit that undoes a previous commit.
     - `git rebase`: Reapply commits on top of another base tip.
     - `git stash`: Temporarily save changes that are not ready to be committed.

---

## Why Focus on the Basics First?

Mastering the core commands (`git status`, `git add`, `git commit`) is the first step to becoming proficient with Git. These commands are the foundation of your workflow and will be used in almost every project. Once you're comfortable with the basics, you can gradually explore collaboration and advanced topics to unlock Git's full potential.

---
