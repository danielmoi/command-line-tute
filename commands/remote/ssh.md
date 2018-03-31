# `ssh`

## Name
SSH client

----
## Usage

```
$ ssh <ip-address>
```


----
## Description
`ssh` is a OpenSSH SSH client (remote login program)

It allows a user to "shell in" to a remote server.

Source code: https://github.com/openssh/openssh-portable


---
## Examples
```
$ ssh 111.111.1.1

[danielmoi@ip-111.111.1.1 ~]$
```
The command line is now the command line of the remote server, located at `111.111.1.1`

Any commands typed into the command line now will be processed by the remote server's shell and operating system!


After we have finished our work, we can disconnect:
```
[danielmoi@ip-111.111.1.1 ~]$ exit

logout
Connection to 54.79.13.56 closed.
```
