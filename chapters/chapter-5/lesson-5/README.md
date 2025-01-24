# Upleveling Our Abilities with Git Branches

In Git, branches allow you to work on new features or changes without affecting the main branch. By creating a new branch, you can make commits that are isolated from the main branch until you're ready to merge them. In this lesson, you'll use the `add_classics` branch to add a new commit to your project, creating a branch structure like this:

```
          D    add_classics
         /
A - B - C      main
```

Here, the `add_classics` branch will have all the commits from the `main` branch, plus a new commit (`D`).

---

## Why Use Branches for New Features?

- **Isolation:** Work on new features or changes without affecting the main branch.
- **Flexibility:** Experiment with changes and easily revert if needed.
- **Collaboration:** Multiple developers can work on different branches simultaneously.

---

## Assignment: Add a New Commit to the `add_classics` Branch

1. **Switch to the `add_classics` Branch:**  
   If you're not already on the `add_classics` branch, switch to it:

   ```bash
   git switch add_classics
   ```

2. **Create a New File:**  
   Create a new file called `classics.csv` at the root of your project and add the following content:

   ```csv
   title, director, year
   One Crazy Summer, Savage Steve Holland, 1986
   The Princess Bride, Rob Reiner, 1987
   The Goonies, Richard Donner, 1985
   The Breakfast Club, John Hughes, 1985
   Monty Python and the Holy Grail, Terry Gilliam, 1975
   ```

3. **Stage the New File:**  
   Add the `classics.csv` file to the staging area:

   ```bash
   git add classics.csv
   ```

4. **Commit the Changes:**  
   Commit the changes with a message starting with `D:`. For example:

   ```bash
   git commit -m "D: Add classics.csv with a list of classic movies"
   ```

5. **Verify the Commit:**  
   Run `git log` to confirm that the new commit has been added to the `add_classics` branch:

   ```bash
   git log
   ```

   You should see the new commit (`D`) in the commit history.

---

## Example Branch Structure

After completing the assignment, your branch structure will look like this:

```
          D    add_classics
         /
A - B - C      main
```

- `A`, `B`, and `C` are the commits on the `main` branch.
- `D` is the new commit on the `add_classics` branch.

---
