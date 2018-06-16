# `|`

---
## Name

Pipe operator

---
## Usage
```
<command-1> | <command-2>
```

---
## Description
The pipe operator is used between two PROCESSES

Piping connects the STANDARD OUTPUT (`stdout`) of one command,
to the STANDARD INPUT (`stin`) of another command.

We can think of it a literal PIPE - there is a stream of data from the command to the LEFT of the pipe symbol to the command on the RIGHT of the pipe symbol.


---
## Examples
Count the number of files and directories in current directory.
```
ls | wc -l
```

* Command 1
  - `ls`
  - the standard output from `ls` is a list of file and directory names

* Command 2
  - `wc`
  - we then pass that list of file and directory names to `wc`
  - that list is now the standard input to `wc`
  - ie. the standard output from `ls` is piped as the standard input to `wc`
  - `wc` will then count the number of lines (using the `-l` option)
  - the standard output from `wc` will equate to the number of files and directories

Sample result for a directory with 10 files/directories:
```
ls | wc -l

10
```

Copy string to clipboard
```
$ echo 'HELLO' | pbcopy

# <PASTE / CTRL-V>
HELLO
```

Copy current directory path to clipboard
```
$ pwd | pbcopy
```
