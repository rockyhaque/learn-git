# Git Push

The `git push` command pushes (sends) local changes to any "remote" - in our case, GitHub. For example, to push our local `main` branch's commits to the remote `origin`'s `main` branch we would run:

```sh
git push origin main
```

You need to be authenticated with the remote to push changes, which you should have done in the last lesson.

## Alternative Options

You can also push a local branch to a remote with a different name:

```sh
git push origin <localbranch>:<remotebranch>
```

It's less common to do this, but nice to know.

You can also delete a remote branch by pushing an empty branch to it:

```sh
git push origin :<remotebranch>
```

## Assignment

Let's push our local `main` branch to the remote `origin` repo for safekeeping!

1. In your local `webflyx` repo, switch back to `main`. The most recent commit should be `G`.
2. Run:

```sh
git push origin main
```

3. Navigate to your GitHub repo in your browser and make sure that all the files and commits from your local `main` branch are there.
