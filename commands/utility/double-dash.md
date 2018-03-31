# Double Dash

## Name
Double dash operator

## Description
The `--` (double-dash) operator indicates the end of options/flags being passed to a command.

All subsequent characters are treated as arguments and/or file names.

## Example
Say we have a file `test.md`:
```
hello
-v
```

And we want to grep for the string `-v`:
```
$ grep -v test.md
```

What we will get is:
```
$ grep -v test.md
>
```

This is because `grep` has an OPTION `v`, which is shorthand for the option `--invert-match`...

(And the syntax for the `-v` option is taking `test.md` as the 1st argument (the string to search for), and is waiting for the 2nd argument at the command line)

Instead, we can use the `--` operator to indicate that we want to grep for the string `-v`:
```
$ grep -- -v test.md
-v
```
