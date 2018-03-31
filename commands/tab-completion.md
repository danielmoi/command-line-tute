# Tab Completion

## Usage
```
$ <char><TAB>
```

---
## Description
The command line allows the user to type the first (few) characters of a command or filename, and
pressing a completion key (`<TAB>`) to fill in the rest of the string.

There are several benefits to this:
- TIME: fewer keystrokes are needed to access a particular command/filename
- ACCURACY: strings are easy to mis-type, and commands/filenames with long/unusual names are easily mis-typed


---
## Examples

Using tab completion on `ls` displays a list of 11 commands that start with `ls`
```
$ ls <TAB>
LSCOLORS   ls         lsa        lsappinfo  lsbom      lskq       lsl        lsm        lsmp       lsof       lsvfs
```

----
We can also use tab completion when moving files with the `mv` command:
```
$ mv file<TAB>
file1.md  file2.md
```
We can see that there are 3 files starting with `file`, and if we type an additional `1` character,
tab completion will auto-fill it with `file1.md` - the full filename for the only file that starts with  `file1`.

```
$ mv file1<TAB>

$ mv file1.md
```
