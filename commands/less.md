# `less`

## Name
Less

----
## Usage

```
less fileName
```


----
## Description
A terminal pager program.

Allows a file to be viwed, one screen at a time.

Allows forward and backward navigation (unlike `more`, another terminal pager program, which only allows foward navigation)

Faster load times than other Unix editors/viewers because `less` doesn't read the entire file before loading.

---
## Examples
```
less README.md                View README.md, one screen at a time

ls | less                     List directory, one screen at a time

less +F /var/log/mail.log     Follow mode, for log file
```
