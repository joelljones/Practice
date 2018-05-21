# Git and GitHub

Git is the industry-standard version control system for web developers.

_GitHub_ is a service for hosting remote repositories on the web.


## Table of Contents

- [Basic Git Workflow](#basic-git-workflow)
- [How to Backtrack](#how-to-backtrack)
- [Git Branching](#git-branching)
- [Git Teamwork](#git-teamwork)


### Resources

- [Wikipedia](https://en.wikipedia.org/wiki/Git)
- [Git](https://git-scm.com)
- [GitHub](https://github.com)

---

# Basic Git Workflow

- Use Git commands to help keep track of changes made to a project:

  - `git init` creates a new Git repository
  - `git status` inspects the contents of the working directory and staging area
  - `git add <filename>` adds files from the working directory to the staging area
  - `git add .` adds all files from the working directory to the staging area
  - `git diff` shows the difference between the working directory and the staging area
  - `git commit -m <message>` permanently stores file changes from the staging area in the repository
  - `git log` shows a list of all previous commits


# How to Backtrack

- `git checkout HEAD filename`: Discards changes in the working directory.

- `git reset HEAD filename`: Unstages file changes in the staging area.

- `git reset commit_SHA`: Resets to a previous commit in your commit history.


# Git Branching

- Git _branching_ allows users to experiment with different versions of a project by checking out separate _branches_ to work on.

- The following commands are useful in the Git branch workflow:

  - `git branch`: Lists all of a Git project's branches.
  - `git branch branch_name`: Creates a new branch.
  - `git checkout branch_name`: Used to switch from one branch to another.
  - `git merge branch_name`: Used to join file changes from one branch to another.
  - `git branch -d branch_name`: Deletes the branch specified.


# Git Teamwork

- A _remote_ is a Git repository that lives _outside_ your Git project folder. Remotes can live on the web, on a shared network or even in a separate folder on your local computer.

- The _Git Collaborative Workflow_ are steps that enable smooth project development when multiple collaborators are working on the same Git project.

- The following commands are useful:

  - `git clone`: Creates a local copy of a remote.
  - `git remote -v`: Lists a Git project's remotes.
  - `git remote add origin <url>` specifies the remote repository using Git.
  - `git fetch`: Fetches work from the remote into the local copy.
  - `git merge origin/master`: Merges `origin/master` into your local branch.
  - `git push origin <branch_name>`: Pushes a local branch to the `origin` remote.
  - `git push -u origin master` pushes the changes to the master branch on the remote repository, linking the local repository to the remote repository.
  - `git push origin master` pushes the changes to the master branch on the remote repository, given that the local repository and the remote repository are already linked.
