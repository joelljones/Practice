# Command Line and Git

summary...


## Table of Contents

- [Command Line Navigation](#command-line-navigation)
- [Git Workflow](#git-workflow)


### Resources

- [Wikipedia](https://en.wikipedia.org/wiki/Git)
- [Git](https://git-scm.com)
- [GitHub](https://github.com)
- [Bash](https://en.wikipedia.org/wiki/Bash_(Unix_shell)

---

# Command Line Navigation

- The _command line_ is a text interface for the computer's operating system. To access the command line, we use the terminal.

- A _filesystem_ organizes a computer's files and directories into a tree structure. It starts with the _root directory_. Each parent directory can contain more child directories and files.

- From the command line, you can navigate through files and folders on your computer:

  - `pwd` outputs the name of the current working directory.
  - `ls` lists all files and directories in the working directory.
  - `cd` switches you into the directory you specify.
  - `mkdir` creates a new directory in the working directory.
  - `touch` creates a new file inside the working directory.

- The `clear` command clears the terminal window of any text, including previous commands and output.


# Git Workflow

_Git_ is the industry-standard version control system for web developers.

- `git init` creates a new Git repository.
- `git status` inspects the contents of the working directory and staging area.
- `git add <filename>` adds files from the working directory to the staging area.
- `git add .` adds all files from the working directory to the staging area.
- `git commit -m <message>` permanently stores file changes from the staging area in the repository.

_GitHub_ is a service for hosting remote repositories on the web

- `git remote add origin <url>` specifies the remote repository using Git.
- `git push -u origin master` pushes the changes to the master branch on the remote repository, linking the local repository to the remote repository.
- `git push origin master` pushes the changes to the master branch on the remote repository, given that the local repository and the remote repository are already linked.
