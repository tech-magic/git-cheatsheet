# Git Commands Cheatsheet

## Clone a Remote Git Repository

git clone git@github.com:ebuilderCCO/service-entry-worker-mi.git
git branch -a
git log
git status

## Create a custom branch (e.g. wimal), Switch to Custom Branch

git branch -a
git checkout -b wimal
git branch -a
git status

## Add and Commit to Local GIT Repo Branch

git add index.js public/myscripts.js
git commit -m "Adding changes"

## Switch to a different branch

git branch -a
git checkout develop

## Update origin pointer of Local Repo from Remote Git Repo

git fetch

## Merge Committed files in custom branch (e.g. wimal) to local develop branch and push it to remote develop branch

git pull (update the local develop from remote develop branch)
git merge wimal (then resolve conflicts)
git status
git add changed_file1.html changed_file2.js
git commit -m "Adding merged changes"
git push

## Delete Temporary Branch (e.g. wimal)

git branch -d wimal

## Upload a New Branch to Remote Git Repo

git push --set-upstream origin workflow

## Revert a change for done for a file

git checkout myfiletorevert.js

## Create a new Repo in GitHub

Create a git repository in the github website (e.g. my-mi in organization tech-magic).
Prompt into the folder you want to associate the remote git repository.

echo "# my-mi" >> README.md
git init
git add README.md
git commit -m "first commit"
git remote add origin git@github.com:tech-magic/my-mi.git
git push -u origin master
git branch -a

## Remove files added accidentally

git rm -f logstash-mi-appender/pom.xml~
git commit -m "Removing unwanted files"


