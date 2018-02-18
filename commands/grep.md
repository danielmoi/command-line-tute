# `grep`

## Name
Grep

----
## Usage

```
grep [--options] [pattern] [filenames]
```


----
## Description
A file pattern searcher.

A command line utility that searches plain-text data sets for LINES that match a regular expression.

It's name comes from the `ed` command `g/re/p` (Globally search a Regular Expression and Print).

(Do a global search with the regular expression and print all matching lines)

Searches input file(s), selecting lines that match particular pattern(s).

The pattern can be a simple string, or a basic regular expression (regex).

----
## Examples
```
grep Hello file1.md       Grep for 'Hello' in 'file1.md'

grep Hello                Grep for 'Hello' in the subsequent `stdin` (standard input)

grep -r Hello .           Grep for 'Hello' in the current directory, recursively

grep -i hello file.md     Grep, case-insensitive

```

----
## Defaults
```
# which grep

grep: aliased to grep  --color=auto --exclude-dir={.bzr,CVS,.git,.hg,.svn}
```

---
## Tutorial
---
## Setup
Let's create some empty files

```
$ touch file1.md file2.md; mkdir dir1; touch dir1/file3.md
```

Let's put some content in our files (we are using the REDIRECTION operator (`>`):
```
$ echo 'Hello ONE' > file1.md
$ echo 'Hello TWO' > file2.md
$ echo 'Hello THREE' > dir1/file3.md
```

----
## Basic grep
Now let's search for the string 'Hello' in 'file1.md'

NB. the quotes can be omitted for single words

```
$ grep 'Hello' file1.md

Hello ONE
```


```
$ grep Hello file2.md

Hello TWO
```


----
## Pattern with multiple words
Now let's search for multiple words.
```
$ grep Hello ONE file1.md

grep: ONE: No such file or directory
file1.md:Hello ONE
```
This produces an error, because `grep` is looking for the string `Hello`
in files called `ONE` and `file1.md`.

Arguments after the PATTERN are the file names.

---
We can fix this:
```
$ grep 'Hello ONE' file1.md

Hello ONE
```

Note that `grep` is CASE SENSITIVE. This returns empty:
```
$ grep 'Hello One' file1.md

```
---
## Multiple input files

We can search across multiple files:
```
$ grep Hello file1.md file2.md

file1.md:Hello ONE
file2.md:Hello TWO
```

We can also use fuzzy search (use a GLOB PATTERN, with WILDCARD characters):
```
$ grep Hello file*

file1.md:Hello ONE
file2.md:Hello TWO
```

We can search the entire directory:
```
$ grep Hello *

grep: dir1: Is a directory
file1.md:Hello ONE
file2.md:Hello TWO
```

Or we can pass the `recursive` flag (`-r`) to search inside child directories:
```
$ grep -r Hello .

./file1.md:Hello ONE
./dir1/file3.md:Hello THREE
./file2.md:Hello TWO
```

----
## Standard input grep
If we don't pass a filename (as the 2nd argument), `grep` will search STANDARD INPUT:
```
$ grep Hello

```


After pressing `<Enter>`, `grep` will await further keystrokes (this is `stdin` - standard input)

Now if we type 'Hello there!', `grep` will return a match:
```
$ grep Hello
Hello there!  <<< This is standard input
Hello there!  <<< This is the match
```

Now if we type 'What', `grep` will return empty:
```
$ grep Hello
Hello there!
Hello there!
What          <<< Standard input
              <<< No match

```

---
## Case insensitive grep
Let's perform a case-insensitive grep:
```
$ grep -i -r hello .

./file1.md:Hello ONE
./dir1/file3.md:Hello THREE
./file2.md:Hello TWO
```


## References
https://unix.stackexchange.com/questions/192698/why-is-grep-keyword-causing-the-terminal-to-stand-by-forever
