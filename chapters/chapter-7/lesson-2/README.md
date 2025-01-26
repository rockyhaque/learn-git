# Git Assignment: Creating a New Branch

## Objective

This assignment guides you through creating a new feature branch (`update_dune`) that branches off a specific commit (`D`) to practice rebasing. By branching off an older commit, you can simulate working on a feature branch that doesn't include recent changes from `main`.

---

## Steps to Complete the Assignment

### 1. Identify the Commit Hash for `D`

1. Run the following command to view the commit history:
   ```bash
   git log --oneline
   ```
2. Locate the commit hash for `D` in the output. It will look something like this:
   ```
   abc1234 D
   ```

### 2. Create and Switch to the New Branch

1. Use the `git switch` command to create and switch to the new branch `update_dune`, branching off commit `D`:
   ```bash
   git switch -c update_done COMMITHASH
   ```
   Replace `COMMITHASH` with the actual hash of commit `D` (e.g., `abc1234`).

### 3. Verify the New Branch

1. Confirm that you are on the `update_dune` branch and that `D` is the last commit:
   ```bash
   git log --oneline -n 1
   ```
   The output should show the commit `D` as the most recent commit on the `update_dune` branch.

---

## Expected Outcome

- You have successfully created a new branch (`update_dune`) that branches off commit `D`.
- The `update_dune` branch does not include any commits after `D` (e.g., `E`, `F`, etc.).
- You are ready to practice rebasing this branch onto the latest `main` branch.

---
