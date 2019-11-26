# Helpful Git Snippets

The purpose of this document is to provide a place for me to document any helpful Git commands i've found. This will primarily be singular lines or small multi-line commands. Larger items will have their own documents.

## Index

1. [Create a local branch & push to remote](#sec_1)
2. [Delete both local and remote branches](#sec_2)
3. [Integrate remote changes into local branch](#sec_3)
4. [Merge local feature branch to master and push to remote](#sec_4)

## Snippets

#### 1. Create a local branch & push to remote <a name="sec_1"></a>

Create a branch with "branch_name" in the local repository
```bash
$ git checkout -b <branch_name>
```
Push the branch to the remote server name origin. This will create the branch in the remote repository (this could also be done using UI)
```bash
$ git push origin <branch_name>
```

#### 2. Delete both local and remote branches <a name="sec_2"></a>

This will delete the local branch if it has already been pushed and merged with remote branches.
```bash
$ git branch -d <branch_name>
```

This will delete the local branch regardless of if it has already been pushed and merged with remote branches
```bash
$ git branch -D <branch_name>
```

To delete the remote branch, you will need to run the following command. This will delete "branch_name" from the remote named origin.
```bash
$ git push origin --delete <branch_name>
```

#### 3. Integrate remote changes into local branch <a name="sec_3"></a>
`git pull` is a great way to integrate changes from a remote branch into a local branch. This command is shorthand for a *git fetch* which pulls down the remote branch followed by a `git merge`. You can can use the `--rebase` option to follow the fetch with a rebase instead of a merge.

Checkout your local branch to merge with.
```bash
$ git checkout <branch_name>
```
Pull down your remote changes and merge into local branch
```
$ git pull origin <branch_name>
```
Or, if you would like to rebase:
```bash
$ git pull --rebase origin <branch_name>
```

#### 4. Merge local feature branch to master and push to remote <a name="sec_4"></a>
First, we need to ensure that the dev branch is up to date with what is in the remote dev branch. We can simply use `git pull` to fetch our remote feature branch and merge it with our local feature branch.
```bash
$ git pull origin <branch_name>
```
Next, we'll checkout the branch we want to merge our feature into. In this case, this is the master branch.
```bash
$ git checkout master
```
Then, we'll merge in the new feature.
```bash
$ git merge <branch_name>
```
Next, we will push the master branch to remote so that all our changes we merged in are in the remote repository.
```bash
$ git push origin master
```
Finally, if we are happy with how things turned out, we can delete the feature branch.
```bash
$ git branch -d <branch_name>
```
