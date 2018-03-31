# `curl`

## Name

---
## Usage
```
$ curl [options] [URL]
```

----
## Description
`curl` is a tool to transfer data TO or FROM a server.

It supports many protocols (such as HTTP, FTP, etc)

The server / resource location is at the specified URL.

----
## Options
```
-L, --location      Follow redirects (HTTP)
-O, --remote-name   Write output to a local file (use the name of the remote file)

-k, --insecure      Allow connections to SSL sites without certs (HTTP)
-s, --silent        Silent mode (don't output anything)
-S, --show-error    Show error. With -s, make curl show errors when they occur
```

----
## Examples

Let's do a simple GET request to `google.com`:

```
$ curl google.com

<HTML><HEAD><meta http-equiv="content-type" content="text/html;charset=utf-8">
<TITLE>301 Moved</TITLE></HEAD><BODY>
<H1>301 Moved</H1>
The document has moved
<A HREF="http://www.google.com/">here</A>.
</BODY></HTML>
```
The output to the terminal is the HTML in the body of the server response.


----
## Output the remote resource to terminal
```
curl https://raw.githubusercontent.com/danielmoi/dotfiles/master/vimrc
```

---
## Output the remote resource to a local file
Specify a local file name.

This will dump the HTML from `google.com` into a file called `google.html`
```
$ curl google.com > google.html


  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100   219  100   219    0     0    508      0 --:--:-- --:--:-- --:--:--   509


```

Or, we can fetch actual files:
```
curl https://raw.githubusercontent.com/danielmoi/dotfiles/master/vimrc > local-vimrc
```

Or we can use the same file name as the remote file, by using the `-O` flag:
```
curl -O https://raw.githubusercontent.com/danielmoi/dotfiles/master/vimrc
```
