# Part 1 - Routine Git Commands Cheatsheet

## Clone a Remote Git Repository

1. `git clone git@github.com:ebuilderCCO/service-entry-worker-mi.git`
2. `git branch -a`
3. `git status`

## Create a custom branch (e.g. wimal), Switch to Custom Branch

1. `git branch -a`
2. `git checkout -b wimal`
3. `git branch -a`
4. `git status`

## Add and Commit to Local GIT Repo Branch

1. `git add index.js public/myscripts.js`
2. `git commit -m "Adding changes"`

## Switch to a different branch

1. `git branch -a`
2. `git checkout develop`

## Update origin pointer of Local Repo from Remote Git Repo

1. `git branch -a`
2. `git fetch`

## Merge Committed files in custom branch (e.g. wimal) to local develop branch and push it to remote develop branch

1. `git branch -a`
2. `git pull` (update the local develop from remote develop branch)
3. `git merge wimal` (then resolve conflicts)
4. `git status`
5. `git add changed_file1.html changed_file2.js`
6. `git commit -m "Adding merged changes"`
7. `git push`

## Delete Temporary Branch (e.g. wimal)

`git branch -d wimal`

## Upload a New Branch to Remote Git Repo

`git push --set-upstream origin workflow`

## Revert a change for done for a file

`git checkout myfiletorevert.js`

## Create a new Repo in GitHub

1. Create a git repository in the github website (e.g. my-mi in organization tech-magic).
2. Prompt into the folder you want to associate the remote git repository.
3. `echo "# my-mi" >> README.md`
4. `git init`
5. `git add README.md`
6. `git commit -m "first commit"`
7. `git remote add origin git@github.com:tech-magic/my-mi.git`
8. `git push -u origin master`
9. `git branch -a`

## Remove files added accidentally

1. `git rm -f logstash-mi-appender/pom.xml~`
2. `git commit -m "Removing unwanted files"`

# Part 2 - Migrate from an old GIT repo to a new GIT repo while saving revision history

Let's assume we call "old repo" the repository you wish to move, and "new repo" the one you wish to move to. 

## Make sure you have a local copy of all "old repo" branches and tags.

1. Fetch all of the remote branches and tags: 
`git fetch origin`

2. View all "old repo" local and remote branches:
`git branch -a`

3. If some of the remotes/ branches doesn't have a local copy, checkout to create a local copy of the missing ones:
`git checkout -b <branch> origin/<branch>`

4. Now we have to have all remote branches locally.

## Add a "new repo" as a new remote origin:

git remote add new-origin git@github.com:user/repo.git

## Step 3. Push all local branches and tags to a "new repo".

1. Push all local branches (note we're pushing to new-origin):
`git push --all new-origin`

2. Push all tags:
`git push --tags new-origin`

## Remove "old repo" origin and its dependencies.

1. View existing remotes (you'll see 2 remotes for both fetch and push)
`git remote -v`

2. Remove "old repo" remote:
`git remote rm origin`

3. Rename "new repo" remote into just 'origin':
`git remote rename new-origin origin`

4. Done! Now your local git repo is connected to "new repo" remote which has all the branches, tags and commits history.


