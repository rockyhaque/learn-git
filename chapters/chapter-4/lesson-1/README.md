# Git Configuration

Git allows you to configure settings at different levels: **global** (applies to all repositories) and **local** (applies to a specific repository). These configurations help Git track information like your name, email, and other custom settings. In this lesson, you'll learn how to configure Git and store custom key-value pairs in your repository's local configuration.

---

## How Git Configuration Works

Git configuration is stored in files:

- **Global Configuration:** Located at `~/.gitconfig`. Applies to all repositories on your system.
- **Local Configuration:** Located in the `.git/config` file of a specific repository. Applies only to that repository.

You can use the `git config` command to add, update, or view configuration settings.

---

## Setting Git Configuration

To set configuration values, use the following syntax:

```bash
git config [--global | --local] <section>.<key> "<value>"
```

### Example:

```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

- **`--global`:** Applies the setting to all repositories.
- **`--local`:** Applies the setting to the current repository only.
- **`<section>.<key>`:** The configuration key (e.g., `user.name`).
- **`"<value>"`:** The value to set for the key.

---

## Assignment: Set Custom Configuration

In this assignment, you'll set custom key-value pairs in the local Git configuration for the `Webflyx` repository.

1. **Set Custom Configuration:**  
   Run the following commands to set custom key-value pairs in the local configuration:

   ```bash
   git config --local webflyx.ceo "rokib"
   git config --local webflyx.cto "hasan"
   git config --local webflyx.valuation "mid"
   ```

2. **View the Configuration:**  
   Use the `git config --list --local` command to view the local configuration:

   ```bash
   git config --list --local
   ```

   Alternatively, you can view the contents of the `.git/config` file directly:

   ```bash
   cat .git/config
   ```

---

## Example Output of Local Configuration

After setting the custom configuration, the output of `git config --list --local` might look like this:

```
core.repositoryformatversion=0
core.filemode=true
core.bare=false
core.logallrefupdates=true
webflyx.ceo=rokib
webflyx.cto=hasan
webflyx.valuation=mid
```

---

## Why Configure Git?

- **Track Changes:** Git uses your name and email to track who made changes in the repository.
- **Custom Settings:** You can store custom key-value pairs for repository-specific settings or metadata.
- **Flexibility:** Git allows you to configure settings at both global and local levels, giving you control over how Git behaves in different contexts.

---
