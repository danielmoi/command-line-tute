# `chmod`

## Name
Change File Modes (or Access Control Lists)


----
## Usage
```
$ chmod [options] [filename]
```


----
## Description
The `chmod` utility modifies the file mode bits of the listed files as specified by the mode operand.

It may also be used to modify the Access Control Lists (ACLs) associated with the listed files.

---
## Examples
The "755" will give you read, write, and execute permission.

Everybody else = only read and execute permission.

If you want your script to be private (i.e., only you can read and execute), use "700" instead.
```
$ chmod 755 hello_world
```
