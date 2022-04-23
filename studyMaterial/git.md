# Git

## What is it?

    Git is distributed version control software. Version control is a way to save changes over time without overwriting previous versions. Being distributed means that every developer working with a Git repository has a copy of that entire repository - every commit, every branch, every file. It helps you track different versions of your code and collaborate with other developers.
    Using Git you can make a "commit" to save changes to your project whenever you want.
## The most commond commands are:

    - git clone: creates a local copy of a project that already exists remotely. The clone includes all the project’s files, history, and branches.

    - git status: shows you what branch you are on and the status of changes as untracked, modified, or staged.

    - git add: adds new or changed files in your working directory to the Git staging area. Git add is used for stage a specific directory or file.

    - git branch: shows the branches being worked on your local repository.

    -git checkout: allows you to switch branches of work.

    - git commit:  captures a snapshot of the project's currently committed changes.

    - git pull: updates your local working branch with all the changes from the remote branch on GitHub. Developers use this command if a teammate has made commits to a branch on a remote, and they would like to reflect those changes in their local environment.

    - git push: updates the remote repository with any commits made locally to a branch.

## BRANCH:

    A branch represents an independent line of development. The branch that is created by default is the master branch, where the main code usually goes and which works correctly. Generally, it is usual to work in branches to have a more orderly history of work.

## TAGS:
Tags are references that point to specific points in a repository's history. Typically, tagging is used to capture a point in history that is used for a tagged version release (for example, v1.0.1).
Git supports two types of tags: lightweight and annotated. A lightweight tag is like a branch that doesn't change. However, annotated tags are stored as full objects in the Git databases.
They store additional metadata such as the following: the name of the person tagging, their email and the date. Like commits and commit messages, annotated tags have a tagging message.
The best practice for git tagging is to give preference to annotated tags over lightweight ones, in order to have all the associated metadata.

## STASH:
It's a quick way to save changes if you need to get to work on something else. It's useful when you couldn't finish something that isn't ready to commit but you need to save your changes. The command used is git stash, which takes the data, saves it aside, and undoes it from the code so you can go on to something else and use it later.

    You can run git stash multiple times to create multiple stashes, then use git stash list to view them. If you want to apply one of the older stashes, you can specify it by naming it, like this: git stash apply stash@{2}. If you don’t specify a stash, Git assumes the most recent stash and tries to apply it.

    If you decide that you don't need more a particular stash, you cand remove it using the command git stash drop stash@{2}. Also, you can delete all stashes using the command git stash clear.

    You can use git stash branch to create a new branch to apply the stashed changes. This pulls a new branch based on the commit you createdthe stash from, and then pops it with the stashed changes.
    The command git stash pop is used to apply the changes from the latest stash created.

## HOOKS:
Git hooks are scripts that run automatically every time a particular event occurs in a Git repository. They let you customize Git’s internal behavior and trigger customizable actions at key points in the development life cycle. You can use Git hooks to automate or optimize virtually any aspect of your development workflow. Hooks can reside in either local or server-side repositories, and they are only executed in response to actions in that repository.
When you initialize a repository, Git automatically creates certain scripts with hooks.
You can change or update these scripts as necessary, and Git will execute them when those events occur.
To enable a hook script, put a file in the hooks subdirectory of your .git directory that is named appropriately (without any extension) and is executable. From that point forward, it should be called.

    In the link below, we have the most useful local hooks:
    https://www.atlassian.com/git/tutorials/git-hooks
 
 ## Git merge VS rebase
    Both git merge and git rebase are used to merge diferent working branches into the main branch with some differences. But both function resolves the same problems. The most important difference between them is that the command merge preserves the commit history. However, the rebase command clears all previous history and overwrites the code. 

### Git merge:
    The merge command is very friendly because it allows you to unify different working branches without losing the commit history. 

### Git rebase:
    The rebase command has the same functionality as merge, with the difference that it rewrites the commit history and performs a single commit. In this way, it allows you to have a more orderly and clean work history.

### Git Squash:
    Squash merging is a merge option that allows you to combine the commit history in a one commit. A simple way to think about this is that squash merge gives you just the file changes, and a regular merge gives you the file changes and the commit history.

# Bibliography:

    https://github.com/git-guides/

    https://github.com/git-guides/git-add#:~:text=The%20git%20add%20command%20adds,an%20unnecessary%20step%20in%20development.

    https://www.atlassian.com/es/git/tutorials/saving-changes/git-commit

    https://www.atlassian.com/es/git/tutorials/using-branches

    https://www.atlassian.com/es/git/tutorials/inspecting-a-repository/git-tag

    https://www.atlassian.com/es/git/tutorials/saving-changes/git-stash#:~:text=El%20comando%20git%20stash%20almacena,aplicar%20los%20cambios%20m%C3%A1s%20tarde.

    https://www.atlassian.com/git/tutorials/git-hooks

    https://www.atlassian.com/es/git/tutorials/using-branches/git-merge

    https://betterprogramming.pub/differences-between-git-merge-and-rebase-and-why-you-should-care-ae41d96237b6#:~:text=Reading%20the%20official%20Git%20manual,it%20happened%2C%20rebase%20rewrites%20it%20.

    https://medium.com/@MiguelCasas/diferencia-entre-git-rebase-y-git-merge-workshop-de-git-8622dedde2d7

    https://docs.microsoft.com/en-us/azure/devops/repos/git/merging-with-squash?view=azure-devops#:~:text=Squash%20merging%20is%20a%20merge,commit%20on%20the%20default%20branch.