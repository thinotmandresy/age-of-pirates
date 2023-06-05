# Age of Pirates contribution guide

> ⚠️ This guide assumes that you don't have any experience with git. If you already know how to use git, you can skip the "Initial setup" section.

## Table of contents

- [Preliminary steps](#preliminary-steps)
  - [Preliminary steps](#preliminary-steps)
  - [Installing Visual Studio Code](#installing-visual-studio-code)
  - [Installing and configuring Git](#installing-and-configuring-git)
  - [Cloning the repository](#cloning-the-repository)
  - [Opening the repository in VSCode](#opening-the-repository-in-vscode)
- [How to contribute](#how-to-contribute)
  - [Creating a new branch](#creating-a-new-branch)
  - [Making changes](#making-changes)
  - [Committing changes](#committing-changes)
  - [Pushing changes](#pushing-changes)
  - [Pulling changes](#pulling-changes)
  - [Viewing the history of changes](#viewing-the-history-of-changes)
- [What happens next?](#what-happens-next)
- [Conclusion](#conclusion)

## Preliminary steps

### Installing Visual Studio Code

While you can use any editor you want, you are encouraged to use [Visual Studio Code](https://code.visualstudio.com/) (VSCode), because it has built-in Git support. After installing VSCode, open it and install the following extensions (press `Ctrl+Shift+X` to open the extensions panel):

- Git History (because you might want to see the history of modifications)
- Git Blame (because you might want to see who made a specific modification)

### Installing and configuring Git

Download and install [Git](https://git-scm.com/download/win). During the installation process, you'll be asked to choose the default editor for Git. Choose Visual Studio Code. Use the default options for the rest of the installation.

Once you have Git installed, you need to configure it by following these steps:

- Open a command prompt (press `Win+R` and type `cmd`).
- Type `git config --global user.name "Your Name"` (don't remove the quotes) and press `Enter`.
- Type `git config --global user.email "youremail@example.com"` (don't remove the quotes) and press `Enter`.

You cannot make any contribution until you have done that configuration.

### Cloning the repository

All Age of Pirates files are stored in something called a "repository". That repository is stored here on GitHub (actually, you are currently viewing it on this very page). You can have a copy of the repository on your computer by "cloning" it. The repository on your computer is called a "local" repository, and the one on GitHub is called a "remote" repository. You will be working on your local repository using VSCode, and then you will "push" (upload) your changes to the remote repository so that everyone can see and use them.

To clone the repository, follow these steps:

- Open a command prompt (press `Win+R` and type `cmd`).
- Type `cd %USERPROFILE%\Games\Age of Empires 3 DE\XXXXXXXXXXXXXXXXX\mods\local` (replace `XXXXXXXXXXXXXXXXX` with whatever you have on your computer) and press `Enter`.
- Type `git clone https://github.com/thinotmandresy/age-of-pirates.git` and press `Enter`.
- Wait for the cloning to finish.

If the cloning was successful, you should now have a folder called `age-of-pirates` in your `mods\local` folder. That folder is your local repository. You can rename that folder if you want.

### Opening the repository in VSCode

You won't have the full power of VSCode + Git if you just edit files individually. Instead, you need to open the repository in VSCode. To do so, just run VSCode, click on "File" at the top left corner, then click on "Open Folder...", and select the folder you just cloned.

To verify that everything went well, click on "Terminal" in the top menu, then click on "New Terminal". A terminal should open at the bottom of the window. Type `git status` and press `Enter`. If everything went well, you should see something like this:

```text
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
```

Congratulations! You made it through the initial setup!

## How to contribute

### Creating a new branch

It is not possible to make changes directly on the main version of Age of Pirates (called the "main branch"). Instead, all changes must be made on a separate branch.

As a general rule, each contributor should have their own branch. Other branches can be created for specific purposes, such as fixing a specific bug or adding a specific feature. You can see the list of branches [here](https://github.com/thinotmandresy/age-of-pirates/branches).

To create a new branch, follow these steps:

- The current branch is displayed at the bottom left corner of the VSCode window. For now, it should say `main`. Click on it, then click on "Create new branch".
- Type the name of the branch and press `Enter`. This will create the branch on your local repository.
  You should now see the branch's name at the bottom left corner of the VSCode window. That means you are now working on that branch. You can switch between different branches by clicking on the branch name at the bottom left corner of the VSCode window.
  > ℹ️ **Notes**:
  >
  > - You should create a branch named after yourself, to make it clear that it is your branch. Contributors will avoid making changes to each other's branches.
  > - For branches that are created for specific purposes, you should use a short, descriptive name. For example, if you are adding a new feature, you could name your branch `add-feature-X` (where `X` is the name of the feature).
  >
  > ⚠️ **Important**: You should always make sure that you are working on the correct branch before making any changes. In fact, for good measure, you should frequently have your eyes on the bottom left corner of the VSCode window to make sure you are working on the correct branch.
- Press `Ctrl+Shift+G` to open the "Source Control" panel, then click on the "Publish branch" button. This will create the branch on the remote repository.

### Making changes

Now that you have your own branch, you can make changes to the game files. You can do that by editing the files directly in VSCode. You can also use the "Source Control" panel (`Ctrl+Shift+G`) to see the changes you made, and to revert them if necessary.

### Committing changes

Once you are done making changes, you need to "commit" them. Committing changes means that you are saving them to your local repository. To commit changes, follow these steps:

- Go to the "Source Control" panel (`Ctrl+Shift+G`).
- You should see a list of files that have been modified. Look for the files you want to add to the commit, and click on the "`+`" button next to them. This will add them to the commit.
- Type a message in the "Message" box at the top of the "Source Control" panel. This message should describe the changes you made. For example, if you added a new unit, you could type "Added a new unit X".
- Click on the "✓ Commit" button. This will commit the changes to your local repository.

### Pushing changes

Once you have committed your changes, you need to "push" them to the remote repository, so that everyone can see and use them. To push changes, follow these steps:

- Go to the "Source Control" panel (`Ctrl+Shift+G`).
- Click on the "⋯" button at the top of the "Source Control" panel, then click on "Push". This will push your changes to the remote repository.

### Pulling changes

Contributors will frequently push changes to different branches in the remote repository. To update the local versions of those branches, you need to "pull" them. To pull changes, follow these steps:

- Switch to the branch you want to update.
- Go to the "Source Control" panel (`Ctrl+Shift+G`).
- Click on the "⋯" button at the top of the "Source Control" panel, then click on "Pull". This will pull the changes from the remote repository.

> ⚠️ **Important**: You should always make sure that you are working on the latest version of a branch before making any changes.

### Viewing the history of changes

You might find it useful to view the commit history of a branch. To do so, follow these steps:

- Switch to the branch you want to view.
- Go to the "Source Control" panel (`Ctrl+Shift+G`).
- Click on the clock icon at the top of the "Source Control" panel. This will open the commit history of the branch.
  You can click on a commit to see the files that were added/modified/removed in that commit, and compare them to the previous version of the files (if any).

![Commit history](/docs/images/git-history.png)

## What happens next?

Once contributors agree that it's time to release a new version of Age of Pirates, here is what will happen:

- The different branches will be merged into the main branch.
- All branches will be deleted (except, of course, the main branch).
- The new version of Age of Pirates will be released.
- Contributors have to create new branches and start working on the next version of Age of Pirates.

## Conclusion

That's it! You now know how to contribute to Age of Pirates! If you have any questions, feel free to DM `AlistairJah#3499` or `roda2324#9206` on Discord.
