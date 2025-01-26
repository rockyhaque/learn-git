# Git Assignment: Practicing Rebase with `update_dune` Branch

## Objective

This assignment walks you through adding commits to the `update_dune` branch and then rebasing it onto the `main` branch. By following these steps, you'll understand how rebasing integrates changes and creates a linear commit history.

---

## Steps to Complete the Assignment

### 1. Add Two Commits to the `update_dune` Branch

1. Ensure you are on the `update_dune` branch:
   ```bash
   git switch update_dune
   ```
2. Add the first quote to the `quotes/dune.md` file:
   - Open the file and add the following line:
     ```
     "The spice must flow."
     ```
   - Stage and commit the change with a commit message starting with `H:`:
     ```bash
     git add quotes/dune.md
     git commit -m "H: Add 'The spice must flow.'"
     ```
3. Add the second quote to the `quotes/dune.md` file:
   - Open the file and add the following line:
     ```
     "Fear is the mind-killer."
     ```
   - Stage and commit the change with a commit message starting with `I:`:
     ```bash
     git add quotes/dune.md
     git commit -m "I: Add 'Fear is the mind-killer.'"
     ```

### 2. Rebase `update_dune` onto `main`

1. While still on the `update_dune` branch, rebase your changes onto `main`:
   ```bash
   git rebase main
   ```
   - This will:
     1. Checkout the latest commit from `main` into a temporary location.
     2. Replay each commit from `update_dune` (e.g., `H` and `I`) one at a time onto this temporary location.
     3. Update the `update_dune` branch to point to the last replayed commit, making this the new permanent `update_dune`.
   - The `main` branch remains unaffected.

### 3. Verify the Commit History

1. Run the following command to view the commit history:
   ```bash
   git log --oneline
   ```
2. You should see a nice linear history from `A` to `I`, even though you originally branched off the `D` commit from `main`.

---

## Expected Outcome

- You have added two commits (`H` and `I`) to the `update_dune` branch.
- You have successfully rebased `update_dune` onto `main`, creating a linear history.
- The `update_dune` branch now includes all changes from `main` and your new commits.

---

## Key Takeaways

- **Rebasing** integrates changes by replaying commits on top of another branch, creating a clean, linear history.
- Rebasing is ideal for feature branches that need to stay up-to-date with the latest changes from `main`.
- Always resolve conflicts carefully during a rebase to ensure the integrity of your changes.

---
