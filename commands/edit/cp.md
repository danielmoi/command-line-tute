# `cp`

## Name
Copy files

----
## Usage

```
$ cp [options] [source] [target]
```


----
## Description
`cp` is used to copy files (ie. duplicate file(s))


---
## Examples
Copy `file1.md` to `file2.md`.

```
$ cp file1.md file2.md
```

---
Interactive mode: copy `file1.md` to `file2.md`, but prompt user if this will overwrite an existing file.

```
$ cp -i file1.md file2.md

overwrite file2.md? (y/n [n]) n
not overwritten
```

---
Interactive mode is often a default alias in shell configurations:
```
$ alias cp
cp='cp -i'
```
