# `>`, `<`, `>>`

## Name
Redirection operators

---
## Usage
```
<command> <redirection-operator> <file-name>
```

---
## Description
The redirection operators are used between a PROCESS and a FILE

Redirection connects the contents of a file with a command.

They allow you to control the input and output of commands.

Redirections are processed in the order they appear, from left to right.


---
## `<` operator

This operator directs input to a command
## Examples
Give the file `readme.md` to the `wc` command
```
$ wc < readme.md

      47     189    1213
```


----
## `>` operator
This operator directs the standard output `stdout` of a command into a file

## Examples
Save the list of files and directories in current directory to a file.
- the output of the `ls` command is a list of files and directories
- that output is directed into a file

If the file doesn't exist, it will be created.

If the file already exists, the content will be overwritten.
```
$ ls > details.md

readme.md
code.js
```

---
Same, but include hidden files:
```
$ ls -a > details.md

.
..
.gitignore
readme.md
code.js
```

---
Note that `>` is shorthand for `1>` - `2>` redirects standard error `stderr`.

```
$ command < file.txt > out.txt 2> error.txt
```
- run `command` on `file.txt`,
- save the output to `out.txt`
- save any error messages to `error.txt`


---
## `>>` operator
This operator redirects standard output, but if the target file exists,
the new data is APPENDED to the target file (instead of overwriting the target file)

```
$ command >> out.txt
```
List all files and directories and save it to `out.txt`:
```
$ ls -a >> out.txt
```
