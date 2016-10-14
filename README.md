# Git Commands Cheatsheet

## Clone a Remote Git Repository

1. git clone git@github.com:ebuilderCCO/service-entry-worker-mi.git
2. git branch -a
3. git status

## Create a custom branch (e.g. wimal), Switch to Custom Branch

1. git branch -a
2. git checkout -b wimal
3. git branch -a
4. git status

## Add and Commit to Local GIT Repo Branch

1. git add index.js public/myscripts.js
2. git commit -m "Adding changes"

## Switch to a different branch

1. git branch -a
2. git checkout develop

## Update origin pointer of Local Repo from Remote Git Repo

1. git branch -a
2. git fetch

## Merge Committed files in custom branch (e.g. wimal) to local develop branch and push it to remote develop branch

1. git branch -a
2. git pull (update the local develop from remote develop branch)
3. git merge wimal (then resolve conflicts)
4. git status
5. git add changed_file1.html changed_file2.js
6. git commit -m "Adding merged changes"
7. git push

## Delete Temporary Branch (e.g. wimal)

git branch -d wimal

## Upload a New Branch to Remote Git Repo

git push --set-upstream origin workflow

## Revert a change for done for a file

git checkout myfiletorevert.js

## Create a new Repo in GitHub

1. Create a git repository in the github website (e.g. my-mi in organization tech-magic).
2. Prompt into the folder you want to associate the remote git repository.
3. echo "# my-mi" >> README.md
4. git init
5. git add README.md
6. git commit -m "first commit"
7. git remote add origin git@github.com:tech-magic/my-mi.git
8. git push -u origin master
9. git branch -a

## Remove files added accidentally

1. git rm -f logstash-mi-appender/pom.xml~
2. git commit -m "Removing unwanted files"


