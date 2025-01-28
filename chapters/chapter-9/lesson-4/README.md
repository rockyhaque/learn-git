# Making Fetch Happen

Fetching from a remote repository brings in metadata and objects, but it does not automatically merge them into the working directory.

---

## Assignment

### Goal

Fetch the remote `webflyx` repository's data into the `webflyx-local` repository and verify that files are not yet present.

### Steps

1. **Navigate to the `webflyx-local` Repository**

   ```bash
   cd path/to/webflyx-local
   ```

2. **Fetch Data from the Remote**

   ```bash
   git fetch
   ```

3. **Inspect the `.git/objects` Directory**

   ```bash
   find .git/objects
   ```

   This will now show new objects that were fetched.

4. **Check for Commits**  
   Run the following command to check if any commits are present:
   ```bash
   git log
   ```
   Since we have only fetched metadata and not checked out any branches, you should see no commit history.

---

### Conclusion

Fetching downloads data from the remote but does not integrate it into the working directory. The commits exist in the repository, but we haven’t checked them out yet.

Done! 🎉
