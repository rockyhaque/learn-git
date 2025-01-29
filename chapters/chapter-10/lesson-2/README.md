# GitHub Repo

Just like we created a webflyx-local repo and used webflyx as a remote, GitHub makes it easy to create "remote" repos that are hosted on their servers.

## Getting Started

### Create a New Repository

1. Create a new repository on GitHub named `webflyx`.
2. Ensure the repository is public and leave it blank.

### Authenticate with GitHub

Install the GitHub CLI using:

```sh
curl -sS https://webi.sh/gh | sh
```

Login to GitHub:

```sh
gh auth login
```

### Set Up the Remote Repository

Navigate to your local repository and add the remote:

```sh
git remote add origin https://github.com/your-username/webflyx.git
```

Replace `your-username` with your actual GitHub username.

Verify the remote:

```sh
git ls-remote
```
