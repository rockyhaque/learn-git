# Pull

Fetching is nice, but most of the time we want the actual file changes from a remote repo, not just the metadata.

## Command Syntax

```sh
git pull [<remote>/<branch>]
```

The `[...]` syntax means that the bracketed remote and branch are optional. If you execute `git pull` without anything specified, it will pull your current branch from the remote repo.

## Assignment

Let's use the GitHub UI to commit a change to our remote repo. Then we'll pull that change down to our local repo.

1. Navigate to your GitHub repo in your browser.
2. Ensure the GH repo's `main` branch's latest commit is `G`.
3. Navigate to the `classics.csv` file on the `main` branch.
4. In the top right corner, click **"Edit this file"**.
5. Add a new line to the end of the file:

   ```
   Willow, Ron Howard, 1988
   ```

6. Commit the change using the UI, but change the commit message to: **"J: Update classics.csv"**. No need for an extended description.
7. On your command line, make sure you're on your `main` branch.
8. Run:

   ```sh
   git config pull.rebase false
   ```

   This ensures Git will merge on a pull.

9. Merge the changes from the `update_dune` branch back into `main` so that `main` has everything we've done so far (`A` through `I`).
10. Run:

    ```sh
    git pull origin main
    ```

    This pulls in the most recent `J` commit that you made remotely.

11. You should see that it starts a merge commit. Rename the merge commit message to start with `K:`.
12. Make sure everything worked:

    ```sh
    git log --oneline
    ```

    You should have commits `A` through `K` locally.

13. Delete the `update_dune` branch locally.
