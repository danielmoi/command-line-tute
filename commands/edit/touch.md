# `touch`

## Name
Touch

----
## Usage

```
$ touch [options] [filename]
```


----
## Description
`touch` creates a file without opening it.

The timestamps will be updated as a user has opened / "touched" the file.

As such, it is also used to change file access and modification times.

If any file does not exist, it is created with default permissions.

---
## Examples
Create a file called `file1.md` in the current directory
```
$ touch file1.md
```
