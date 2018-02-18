# `ls`


## Name
List directory contents


----
## Usage
```
ls [-options] [dirName]
```

----
## Description
List directory contents


## Examples
```
ls -1                   List, 1 per line

ls -a                   List, "all" view (include hidden files)

ls -l                   List, "long" format

ls -la | less           ... pipe into "less", so it's paginated
```


---
## Defaults
```
$ which ls

ls: aliased to ls -G
# enable colorized output
```
