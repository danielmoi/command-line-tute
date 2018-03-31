# RG - ripgrep

https://github.com/BurntSushi/ripgrep

Built by [Andrew Gallant](https://github.com/BurntSushi)

Built on top of Rust's regex engine.

How so fast? It uses...
- finite automata,
- SIMD, and
- aggressive literal optimizations


The binary name for ripgrep is rg

## Usage

```
$ rg magic
```

A recursive search of the current directory.

Ignores files...
- in .gitignore
- hidden files
- directories
- binary files


### Flags
-u    Ignore ignore files

-uu   Include hidden files and directories
      (similar `to grep -r`)

-uuu  Include binary files
      (similar to `grep -a -r`)

