# Git-Github

Git is a mandatory tool for software development nowadays.

git is a software and github is a service to host that service online.

Git is a version control system that allows you to track changes to your files and collaborate with others. It is used to manage the history of your code and to merge changes from different branches.

Github is a web-based hosting service for Git repositories. Github is an online platform that is used to store and share your code with others. It is a popular platform for developers to collaborate on projects and to share code.

## Journey

1) Get the basics
2) Use it daily
3) Fact the problems
4) Solve them
5) Learn more

## Steps

1) Install Git
2) IDE (vs-code)
3) Account on Github

## Terminologies

### Check your git version

```bash
git --version
```

### Repository

```bash
git status
```

### Currect Directory

```bash
pwd (present working directory)
```

### Change Directory

```bash
cd "name"
(to check are you in the particular directory, use pwd command)
```

### Creating a repository

Always run first command.

```bash
git status
git init
```

### Flow

```bash
Write -> Add -> Commit
```

### Git complete flow

```bash
git init(Working Directory)---->git add(Staging Area)---->git commit(repo)--->git push(github)
```

### Add File

```bash
git init
git add file1-name file2-name...
git status
(add takes a floder into staging area)
```

### Add all files

```bash
git add .
(After commiting files are staged)
```

### To unstage

```bash
git rm --cached file-name
```

### To delete

```bash
git rm "file-name"
```

### Commit

```bash
git commit -m "message"
(After it, reached in repo but needed to push code on github)
```

### Logs

```bash
git log
git log --oneline
(using oneline commits shows in one line)
```

Note: After comnpletion of a required smaller or unit step in your project commit it.
Use present tense imperative form in commit(instructions) to codebase, eg: "Add footer to code." (Recommended)

### Ignore files from being tracked

Each file you place in .gitignore file will be ignored and not tracked.
For that create a file named as ".gitignore"
After creation open it and write the file name in it which you don't want to track by git.

### Empty folders for future work

If you want that git ignore your empty folders because by default git ignores empty folders then create .gitkeep file in it, then git track empty folder.

## Branches in Git

Multiple tasks at the same time it doesn't effect your any of other branch unless you merge yourself.

### Show branches

git branch
This command will show all branches and in which branch you are.

### Creation of new branch

```bash
git branch "name"
```

### Switch to another branch

```bash
git switch "name"
```

### To check use

```bash
git log
```

After doing some changes in y branch and after that if we switched to x branch all of those changes in y branch will not show in x branch unless and until we merge it, because each branch will work on its own file without messing with other branches.

### For switching at a specific branch if not existed then create it

```bash
git switch -c "name"
```

In this case if "branch-name" doesn't exist, in that scenario will not only create it but also switch to that branch.

### For check any branch is existed or not

```bash
git checkout "name"
```

If you want to check any branch exist or not, by running this command if branch with that name exist then your head will switched to that branch otherwise it will say not existed.

## Merging

### Fast-Forward Merge

```bash
git checkout main(master)
git merge "name"
```

In that case we're first switching our head to main branch and merging any x-branch into main branch.

### Not Fast-Forward Merge

After doing some changes or fixing bugs in "x-branch".
When you're changing files or fixing bugs etc in both branches in master(main) and "x-branch" as well. After doing this whatever you'll try to merge both branches it would throw conflicts. This is not fast forward merge.
You have to manually resolve conflicts, there is no automatic options or commands available for it.

### Rename a branch

```bash
git branch -m "old-branch-name" "new-branch-name"
```

### Delete a branch

```bash
git branch -d "branch-name"
```

### Checkout a branch

```bash
git checkout "branch-name"
```

### List all branches

```bash
git branch
(All git branches will be listed)
```

### Merging conflicts

Goto main(master) branch and write command

```bash
git merge "name"
```

By using it will fix git branches. But in case changes occur in main branch and some x branch as well. It will create conflicts.

### Abort Merge

```bash
git merge --abort
```

Merge conflicts can be resolved by using vs code as well but you always need to merge conflicts manually. There is no automatic way to resolve conflicts.
Note: After fixing conflicts, add and commit files

## Diff Stash and Tags

### Git diff

It is informative command that shows the difference between two commits. Git consider the changed versions of same file as two different files. Then it gives names to these two files and shows the difference between them.

```bash
git diff
```

By running git diff nothing will happen.

### To check difference between staging of file

```bash
git diff --staged
```

### Comparing between branches

```bash
git diff <branch-one-name> <branch-two-name>
```

This command compares the difference between two branches. There is also an alternative way of writing it.

```bash
git diff branch branch-one-name..branch-two-name
(common syntax)
```

### Comparing specific commits

```bash
git diff commit-one-hash commit-two-hash
or
git diff commit-one-hash..commit-two-hash
```

## Git Stash

It is a way to save your changes in a temporary location. It is useful when you want to make changes to a file don't want to commit them yet. You can then come back to the file later and apply the changes.

```bash
git stash
```

### Naming the stash

```bash
git stash save "message"
(It works like a stack i.e; most recent on top)
```

### View the stash listed

```bash
git stash list
```

### Apply the stash

```bash
git stash apply
(top stash will be applied)
```

### Apply the specific stash

```bash
git stash apply stash @{number}
```

### Applying & Dropping the stash

```bash
git stash pop
```

### Drop the stash

```bash
git stash drop
```

### Applying stash to a specific branch

```bash
git stash apply stash @{num} <branch-name>
```

### Clearing the stash

```bash
git stash clear
```

## Github

Github is a web-based Git repository hosting service. It is a popular platform for developers to collaborate on projects and to share code. Github provides a user-friendly interface for managing and tracking changes to your code, as well as a platform for hosting and sharing your projects with others.

Some other alternative of Github are:

- Gitlab
- Bitbucket
- Azure Repos
- Gitea

But mainstream popular tool these days is Github.

### Github Account

Creating a Github account is free and easy. You can create an account by visiting the [Github website](https://github.com/) and clicking on the “Sign up” button. You will be prompted to enter your email address and password, and then you will be redirected to the Github homepage.

Once you have created an account, you can start using Github to host and collaborate on your projects. Github provides a variety of features and tools that make it easy to manage and track your code, including issues, pull requests, and code reviews.

### Configure your config file

If you havn't done it already, you need to configure your git config file. You can do this by running the following command:

```bash
git config --global user.email "your-email@example.com"
git config --global user.name "Your Name"
```

This will set your email and name as your global settings. You can change these settings later by running the following command:

```bash
git config --global user.email "your-email@example.com"
git config --global user.name "Your Name"
```

For checking config settings:

```bash
git config --list
```

### Adding code to remote repository

```bash
git init
git add <files>
git commit -m "commit message"
```

### Check remote url setting

```bash
git remote -v
```

### Add remote repository

```bash
git remote add origin <remote-url>
```

### Push code to remote repository

```bash
git push origin main
```

### Setup an upstream remote

```bash
git remote add upstream <remote-url>
```

Or shorthand

```bash
git remote add -u <remote-url>
```

You can do this at the time of pushing your code to the remote repository.

```bash
git push -u origin main
```

### Get code from remote repository

There are two ways to get code from a remote repository:

- fetch the code
- pull the code

Fetch the code means that you are going to download the code from the remote repository to your local repository. Pull the code means that you are going to download the code from the remote repository and merge it with your local repository.

### Fetch code

```bash
git fetch <remote-name>
```

### Pull code

```bash
git pull origin main
```
