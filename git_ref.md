# Helpful Git Snippets

The purpose of this document is to provide a place for me to document any helpful Git commands i've found. This will primarily be singular lines or small multi-line commands. Larger items will have their own documents.

## Index

1. Create a local branch & push to remote
2. Delete both local and remote branches

## Snippets

#### 1. Create a local branch & push to remote

Create a branch with "branch_name" in the local repository
```bash
$ git checkout -b <branch_name>
```
Push the branch to the remote server name origin. This will create the branch in the remote repository (this could also be done using UI)
```bash
$ git push origin <branch_name>
```
#### 2. Delete both local and remote branches

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
