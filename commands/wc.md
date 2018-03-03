# `wc`

## Name
Word, Line, Character, and Byte count

----
## Usage

```
wc [-clmw] [file]
```


----
## Description
A utility that displays the number of lines, words, and bytes contained in each input file,
or standard input (if no file is specified) to the standard output.

---
## Examples
List the line count, word count, and character count
```
wc test.md

47     189    1213 README.md
```

----
List only the line count
```
wc -l test.md

47 README.md
```

----
List the line count for text entered as standard input (ie. in the terminal)
```
wc -l
hello
hello
<CTRL-D>

2
```
----
List all processes, grep for 'node', then print the line count (ie. this will be the number of processes)

```
ps | grep node | wc -l

3
```
