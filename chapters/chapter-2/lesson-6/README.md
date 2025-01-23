# Exploring Git Log

The `git log` command is a powerful tool that allows you to view the history of commits in a Git repository. Each commit represents a snapshot of the repository at a specific point in time, and `git log` provides detailed information about these commits, including who made them, when they were made, and what changes were included.

---

## What is a Commit?

A commit is a snapshot of your repository's state at a given point in time. It includes:

- **Commit Hash:** A unique identifier (e.g., `5ba786fcc93e8092831c01e71444b9baa2228a4f`) that represents the commit. For convenience, you can refer to a commit using the first 7 characters of its hash (e.g., `5ba786f`).
- **Author:** The person who made the commit.
- **Date:** When the commit was made.
- **Message:** A description of the changes made in the commit.

---

## Using `git log`

The `git log` command displays the commit history of your repository. By default, it shows the most recent commits first and uses an interactive pager to allow you to scroll through the log.

### Basic Usage:

```bash
git log
```

This command will display the commit history, including the commit hash, author, date, and commit message.

---

## Navigating `git log`

When you run `git log`, it opens an interactive pager. Here are some useful shortcuts:

- **Arrow Keys:** Scroll up and down through the log.
- **`q`:** Exit the pager and return to the terminal.

---

## Limiting and Formatting `git log`

You can customize the output of `git log` using various options. For example:

1. **Limit the Number of Commits:**  
   Use the `-n` option to limit the number of commits displayed. For example, to show the last 10 commits:

   ```bash
   git log -n 10
   ```

2. **Disable the Interactive Pager:**  
   Use the `--no-pager` option to display the log directly in the terminal without opening the pager. For example:
   ```bash
   git --no-pager log -n 10
   ```

---

## Assignment: Explore `git log`

1. **View the Commit History:**  
   Run the following command to see the commit history:

   ```bash
   git log
   ```

   Use the arrow keys to scroll through the log and press `q` to exit.

2. **Limit and Disable the Pager:**  
   Run the following command to view the last 10 commits without the interactive pager:
   ```bash
   git --no-pager log -n 10
   ```

---

## Why Use `git log`?

- **Track Changes:** View the history of your project and understand how it has evolved over time.
- **Debug Issues:** Identify when and where a bug was introduced by examining past commits.
- **Collaborate Effectively:** Understand what changes your team members have made and when.

---
