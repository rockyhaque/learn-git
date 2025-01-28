# Fetch in Git

Adding a remote to our Git repository does not automatically bring in the contents of the remote. To access the remote's contents, we need to explicitly fetch the data.

---

## Command

To fetch the contents from a remote, use:

```bash
git fetch
```

This command downloads all the data from the remote repository’s `.git/objects` directory (and other metadata) into your current repository.

---

## Assignment

### Goal

Examine the `.git/objects` directory in the new empty repository before fetching any data.

### Steps

1. **Navigate to the New Repository**

   ```bash
   cd path/to/webflyx-local
   ```

2. **Inspect the `.git/objects` Directory**  
   Use the `find` command to list the contents of the `.git/objects` directory:

   ```bash
   find .git/objects
   ```

3. **Expected Output**  
   The `.git/objects` directory should contain only 3 entries. This is because no data has been fetched yet, and the repository is still empty.

---

Done! 🎉
