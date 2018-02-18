# `grep`

## Name
Grep

----
## Usage

```
```


----
## Description
A file pattern searcher.

Searches input file(s), selecting lines that match particular pattern(s).

The pattern can be a simple string, or a basic regular expression (regex).

---
## Examples
```
# Create some empty files
$ touch file1.md file2.md

# Redirect the string 'Hello ONE' into 'file1.md'
$ echo 'Hello ONE' > file1.md
$ echo 'Hello TWO' > file2.md

# Search for the string 'Hello' in 'file1.md'
# NB. the quotes can be omitted for single words
$ grep 'Hello' file1.md


grep Hello file2.md

```
