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
> You'll need to generate a Personal Access Token (PAT) 
https://github.com/settings/token

You will use the PAT as your password when you login.

Give it access to Contents for Commits

### SSH
```sh
git clone git@github.com:andrew-wc-brown/Github-Examples.git
cd GitHub-Examples
```
We will need to create our own SSH rsa key pair
```sh
sshe-keygen -t rsa
```
For WSL users and if you crete a non default key you might need to add it

```sh
eval `ssh-agent`
ssh-add /home/andrew/.ssh/alt-github_id_rsa
```
We can test our connection here:

```sh
ssh -T git@github.com
```

### GitHub CLI

Install the CLI

eg. Linux (Ubuntu)

```sh
type -p curl >/dev/null || (sudo apt update && sudo apt install curl -y)
curl -fsSL https://cli.github.com/packages/githubcli-archive-keyring.gpg | sudo dd of=/usr/share/keyrings/githubcli-archive-keyring.gpg \
&& sudo chmod go+r /usr/share/keyrings/githubcli-archive-keyring.gpg \
&& echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/githubcli-archive-keyring.gpg] https://cli.github.com/packages stable main" | sudo tee /etc/apt/sources.list.d/github-cli.list > /dev/null \
&& sudo apt update \
&& sudo apt install gh -y
```
```sh
gh auth login
gh repo clone Naga-Manohar-Y/GitHub-Examples
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
List of branches
```sh
git branch
```
Create a new branch

```sh
git branch branch-name
```
Checkout the branch
```sh
git checkout dev
```

## Remotes

We can add remote but often you will just add remote via upsteam when adding a branch
```sh
git remote add ...
git branch -u origin new-feature
```

## Stashing
```sh
git stash list
git stash
git stash save my-name
git stash apply
git stash pop
```

## Merging
```sh
git checkout dev
git merge main
```

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
