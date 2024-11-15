
# Git Workflow Documentation

This document provides a step-by-step record of the Git operations performed, from repository setup to pushing changes to GitHub.

## Steps Followed

### 1. List the Contents of the Directory

Initially, check the contents of the `NewClient` directory:

```bash
ls
# Output:
# client-master
```

### 2. Initialize a New Git Repository

Initialize an empty Git repository in the current directory:

```bash
git init
# Output:
# Initialized empty Git repository in /Users/sandeepkalasagonda/Desktop/NewClient/.git/
```

### 3. Add a Remote Repository

Link the local repository to a remote GitHub repository:

```bash
git remote add origin https://github.com/sandeep-kalasgonda/SmartHRM.git
```

### 4. Create and Rename the Branch

Rename the current branch to `release-mvp-0.6`:

```bash
git branch -M release-mvp-0.6
```

### 5. Pull the Remote Branch

Fetch and merge updates from the remote branch `release-mvp-0.6`:

```bash
git pull origin release-mvp-0.6
# Output:
# remote: Enumerating objects: 151, done.
# ...
# From https://github.com/sandeep-kalasgonda/SmartHRM
#  * branch            release-mvp-0.6 -> FETCH_HEAD
#  * [new branch]      release-mvp-0.6 -> origin/release-mvp-0.6
```

### 6. Verify the Directory Contents After the Pull

List the contents of the directory to verify the files:

```bash
ls
# Output:
# LICENSE  SmartHRM-main.zip  client-jd-s3-rds-crud  dashboard-api  ...
```

### 7. Create a New Feature Branch

Create and switch to a new feature branch `feature7/client-master/api`:

```bash
git checkout -b feature7/client-master/api
```

### 8. Push the New Branch to the Remote Repository

Attempt to push to an incorrectly named branch (results in an error):

```bash
git push -u origin feature9/cand-master/api
# Error:
# error: src refspec feature9/cand-master/api does not match any
```

Push the correctly named branch `feature7/client-master/api`:

```bash
git push -u origin feature7/client-master/api
# Output:
# remote: Create a pull request for 'feature7/client-master/api' on GitHub by visiting:
# remote:      https://github.com/sandeep-kalasgonda/SmartHRM/pull/new/feature7/client-master/api
```

### 9. Check the Current Status of the Repository

Verify the current status to identify untracked files:

```bash
git status
# Output:
# On branch feature7/client-master/api
# Untracked files: client-master/
```

### 10. Stage All Changes

Add all files and changes to the staging area:

```bash
git add .
```

### 11. Commit the Changes

Commit the changes with a message:

```bash
git commit -m "issue #12: add end points to client master"
# Output:
# [feature7/client-master/api ca079d8] issue #12: add end points to client master
# 4 files changed, 320 insertions(+)
```

### 12. Push the Commit to the Remote Repository

Push the committed changes to the remote branch:

```bash
git push
# Output:
# Enumerating objects: 8, done.
# ...
```

## Summary

- Initialized a local Git repository and connected it to a GitHub repository.
- Pulled the latest changes from the `release-mvp-0.6` branch.
- Created and switched to a new branch `feature7/client-master/api`.
- Committed and pushed new changes to GitHub.

For further review or to create a pull request, visit the repository on GitHub:
[Feature Branch Pull Request](https://github.com/sandeep-kalasgonda/SmartHRM/pull/new/feature7/client-master/api)
