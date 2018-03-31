# `rm`

## Name
Remove files or direct

----
## Usage

```
$ rm [options] [filename or dirname]
```


----
## Description
`rm` is used to remove files and/or directories


---
## Examples
Remove `file1.md`

```
$ rm file1.md
```

---
Interactive mode:  Remove `file1.md` but prompt user:

```
$ rm -i file1.md

remove file1.md? y
```

---
We can make interactive mode the default behaviour by using an alias:
```
# .zshrc
alias rm="rm -i"

$ alias rm
rm='rm -i'
```

----
Remove directories, and do not prompt user.

`-r` option = recursive
`-f` option = force (do not prompt)


Be VERY careful with `rm -rf` (also pronounced "rimraf") - there is no "Trash" to recover files from!
```
$ rm -rf node_modules
```
