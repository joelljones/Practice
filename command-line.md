# Command Line

The _command line_ is a text interface for the computer's operating system. To access the command line, we use the terminal.

## Table of Contents

- [Navigation](#navigation)
- [Manipulation](#manipulation)
- [Redirection](#redirection)
- [Environment](#environment)

### Resources

- [Bash](https://en.wikipedia.org/wiki/Bash_(Unix_shell))

---

# Navigation

- A _filesystem_ organizes a computer's files and directories into a tree structure. It starts with the _root directory_. Each parent directory can contain more child directories and files.

- From the command line, you can navigate through files and folders on your computer:

  - `pwd` outputs the name of the current working directory.
  - `ls` lists all files and directories in the working directory.
  - `cd` switches you into the directory you specify.
  - `mkdir` creates a new directory in the working directory.
  - `touch` creates a new file inside the working directory.

- The `clear` command clears the terminal window of any text, including previous commands and output.

# Manipulation

- Options modify the behavior of commands:

  - `ls -a` lists all contents of a directory, including hidden files and directories
  - `ls -l` lists all contents in long format
  - `ls -t` orders files and directories by the time they were last modified
  - Multiple options can be used together, like `ls -alt`

- From the command line, you can also copy, move, and remove files and directories:

  - `cp` copies files
  - `mv` moves and renames files
  - `rm` removes files
  - `rm -r` removes directories

- Wildcards are useful for selecting groups of files and directories

# Redirection

- _Redirection_ reroutes standard input, standard output, and standard error.

- The common redirection commands are:

  - `>` redirects standard output of a command to a file, overwriting previous content.
  - `>>` redirects standard output of a command to a file, appending new content to old content.
  - `<` redirects standard input to a command.
  - `|` redirects standard output of a command to another command.

- A number of other commands are powerful when combined with redirection commands:

  - `sort`: sorts lines of text alphabetically.
  - `uniq`: filters duplicate, adjacent lines of text.
  - `grep`: searches for a text pattern and outputs it.
  - `sed`: searches for a text pattern, modifies it, and outputs it.

# Environment

- The _environment_ refers to the preferences and settings of the current user.

- The _nano_ editor is a command line text editor used to configure the environment.

- __~/.bash_profile__ is where environment settings are stored. You can edit this file with nano.

- _environment variables_ are variables that can be used across commands and programs and hold information about the environment.

  - `export VARIABLE="Value"` sets and exports an environment variable.
  - `USER` is the name of the current user.
  - `PS1` is the command prompt.
  - `HOME` is the home directory. It is usually not customized.
  - `PATH` returns a colon separated list of file paths. It is customized in advanced cases.
  - `env` returns a list of environment variables.
