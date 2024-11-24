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

git --version

### Repository

git status

### Currect Directory

pwd (present working directory)

### Change Directory

cd "name"
(to check are you in the particular directory, use pwd command)

### Creating a repository

Always run first command.
git status
git init

### Flow

Write -> Add -> Commit

### Git complete flow

git init(Working Directory)---->git add(Staging Area)---->git commit(repo)--->git push(github)

### Add File

git init
git add file1-name file2-name...
git status
(add takes a floder into staging area)

### Add all files

git add .
(After commiting files are staged)

### To unstage

git rm --cached file-name

### Commit

git commit -m "message"
(After it, reached in repo but needed to push code on github)

### Logs

git log
git log --oneline
(using oneline commits shows in one line)

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

git branch "name"

### Switch to another branch

git switch "name"

### To check use

git log

After doing some changes in y branch and after that if we switched to x branch all of those changes in y branch will not show in x branch unless and until we merge it, because each branch will work on its own file without messing with other branches.

### For switching at a specific branch if not existed then create it

git switch -c "name"
In this case if "branch-name" doesn't exist, in that scenario will not only create it but also switch to that branch.

### For check any branch is existed or not

git checkout "name"
If you want to check any branch exist or not, by running this command if branch with that name exist then your head will switched to that branch otherwise it will say not existed.

## Merging

### Fast-Forward Merge

git checkout main(master)
git merge "name"

In that case we're first switching our head to main branch and merging any x-branch into main branch.

### Not Fast-Forward Merge

After doing some changes or fixing bugs in "x-branch".
When you're changing files or fixing bugs etc in both branches in master(main) and "x-branch" as well. After doing this whatever you'll try to merge both branches it would throw conflicts. This is not fast forward merge.
You have to manually resolve conflicts, there is no automatic options or commands available for it.

### Rename a branch

git branch -m "old-branch-name" "new-branch-name"

### Delete a branch

git branch -d "branch-name"

### Checkout a branch

git checkout "branch-name"

### List all branches

git branch
(All git branches will be listed)
