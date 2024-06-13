## Git Hidden Folder

There is a hidden folder called `.git` means our project is git repo.

For a new project to creat a new repository use `git init`

```sh
mkdir /workspaces/temp/new-project
cd /workspace/temp/new-project
git init
touch Readme.md
open Readme.md
```
## Cloning 

We can clone three ways: HTTPS, SSH, GitHub CLI.

Since we are using codespaces , make a temporaru directory to do this cloning.

```sh
mkdir /workspace/temp
cd workspace/temp
```

### HTTPS

```sh
git clone https://github.com/Naga-Manohar-Y/GitHub-Examples.git

cd GitHub-Examples
```

## Commits

```sh
git commit
```

Set the global editor

```sh
git config --global core.editor emacs
```
Make a commit and commit message without opening an editor

```sh
git commit -m "adding Readme file."
```


## Branches

## Remotes

## Stashing

## Merging

## Add

```sh
git add Readme.md
git add .
```

## Status

```sh
git status
```

## Reset
Reset allows you to move move staged changes to be unstaged. Useful when you don't want to commit all the files.

```sh
git add .
git revert
```
## Gitconfig file
The gitconfig file is what stores your global configurations for git such as email, name, editor and more.

Showing the contnets of our .gitconfig file

```sh
git config --list
```

When you first install Git on a machine you are suppose to set up your name and email

```sh 
git config --global user.name "John Doe"
git config --global user.email johndoe@example.com
```
## Log
git log will show recent git commits to the git tree
