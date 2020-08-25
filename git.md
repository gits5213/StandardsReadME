# Download and Install GIT & First time set up GITHub

<!-- topics-start -->
* [Download GIT](#Download-GIT)
* [Download for macOS](#Download-for-macOS)
* [SignUP GITHub](#SignUP-GITHub)
* [Colone the GitHub Repository](#Colone-the-GitHub-Repository)
* [Getting and Creating Projects](Getting-and-Creating-Projects)
* [Basic Snapshotting](Basic-Snapshotting)
* [Branching and Merging](Branching-and-Merging)
* [Sharing and Updating Projects](Sharing-and-Updating-Projects)
* [Inspection and Comparison](Inspection-and-Comparison)
* [Patching](Patching)

# Download GIT
- [Navigate to the URL](https://git-scm.com/downloads)
- Click on the Download Package based on the Operating System

# Download for macOS
### There are several options for installing Git on macOS. Note that any non-source distributions are provided by third parties, and may not be up to date with the latest source release.

## Homebrew
- Install [homebrew](https://brew.sh/) if you don't already have it, then:
    ```
    $ brew install git
    ```
## SignUP GITHub
- [Navigate to the URL](https://github.com/)
- Click on SingUp button
- Follow the Instruction
- Log into the GithHib Account
- Click on plus(+) icon uper-right hand corner to create a new repository 
- Enter Repository Name
- Select Public/Private
- Click on the Create repository button

## Clone the GitHub Repository
-  After log into the GitHub
- Click on profile (photo) icon uper-right hand corner 
- Click on Your Repository
- Click on the specific repository which you want to clone it
- Click on the "Code" button 
- Copy SSH url 
- Navigate to the Terminal or CMD Commnad Prompt 
- Change Directory where you want to place the project
- Import into Eclipse/intellij or Drag & Drop into the Editors
- Start writing code 

## GIT Basic Command 

## Getting and Creating Projects
```
> git init (Create an empty Git repository or reinitialize an existing one)
> git clone (Clone a repository into a new directory)
```

## Basic Snapshotting
```
> git add (Add file contents to the index)
> git add . (Add all untracted file contents to the index)
> git status (Show the working tree status)
> git add index.html
> git commit -m "Some meaningful Message" (Record changes to the repository)
> git rm (Remove files from the working tree and from the index)
> git mv (Move or rename a file, a directory, or a symlink)
```

## Branching and Merging
```
> git branch (List, create, or delete branches)
> git checkout -b "branchName" (Create a new branch)
> git checkout branchName (Switch to branch)
> git branch -d branch_name (delete branch)
> git branch --delete --force
> git stash (This will stash your changes and clear your status report)
```

## Sharing and Updating Projects
```
> git fetch (You can do this command at any time to update your remote-tracking branches)
> git pull (This will pull changes from upstream branch)
> git push (Update remote refs along with associated objects)
> git push <remote_name> --delete <branch_name> (Delete a remote GIT branch)
> git push <remote_name> :<branch_name>
> git remote add origin git@github.com:peter/first_app.git
```

## Inspection and Comparison
```
> git log (Show commit logs)
> git diff (Show changes between commits, commit and working tree, etc)
```

## Patching
```
> git cherry-pick (Cherry picking in Git means to choose a commit from one branch and apply it onto another.)
> git rebase (: git rebase -i master: Clean up the history of your dev branch with an interactive rebase)

> git rebase -i fires up an editor and gives you a list of commits on you branch. There is a default pick operation in front of each. If you keep pick nothing will change. You can replace pick with other operations.
    - "squash" the commit into the previous one, prompt for change description
    - "fixup" of previous commit, which automatically retains its original description
    - "edit" the contents and description of commit
```
