# `rg`

## Name
rg - "ripgrep"

---
## Usage

```
$ rg magic
```
----
## Description
Source code: https://github.com/BurntSushi/ripgrep

Built by [Andrew Gallant](https://github.com/BurntSushi)

(Notes from source)
Built on top of Rust's regex engine.

How so fast? It uses...
- finite automata,
- SIMD, and
- aggressive literal optimizations


The binary name for ripgrep is rg


A recursive search of the current directory.

By default, ignores certain files...
- files listed in `.gitignore`
- hidden files
- directories
- binary files


---
## Options
```
-u    Ignore ignore files
      ie. include ignored files

-uu   Include hidden files and directories
      (similar `to grep -r`)

-uuu  Include binary files
      (similar to `grep -a -r`)
```

---
## Examples

Usage is very similar to other search tools (`grep`, `ag`, `ack`)
```
$ ifconfig | rg inet
```

```
$ ps | rg node
```
