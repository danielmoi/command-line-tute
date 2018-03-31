# `mv`

## Name
Move files

----
## Usage

```
$ mv [options] [source] [target]
```


----
## Description
`mv` is used to move and rename files.


---
## Examples
Move `file1.md` to `file2.md`.

This is the same as renaming `file1.md` to `file2.md`.
```
$ mv file1.md file2.md
```

---
Interactive mode: move `file1.md` to `file2.md`, but prompt user if this will overwrite an existing file.

```
$ mv -i file1.md file2.md

overwrite file2.md? (y/n [n]) n
not overwritten
```

---
Interactive mode is often a default alias in shell configurations:
```
$ alias mv
mv='mv -i'
```
