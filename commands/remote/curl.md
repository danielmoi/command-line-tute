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

---
## HTTP Methods
By default you use curl without explicitly saying which request method to use.

If you just pass in a HTTP URL like `curl http://example.com` it will use `GET`.

If you use `-d` or `-F` `curl` will use `POST`

`-I` will cause a `HEAD`

and `-T` will make it a `PUT`.

If for whatever reason you're not happy with these default choices that curl does for you, you can override those request methods by specifying -X [WHATEVER]. This way you can for example send a DELETE by doing curl -X DELETE [URL].

It is thus pointless to do curl -XGET [URL] as GET would be used anyway. In the same vein it is pointless to do curl -X POST -d data [URL]... But you can make a fun and somewhat rare request that sends a request-body in a GET request with something like curl -X GET -d data [URL]

https://stackoverflow.com/questions/8498371/curl-get-and-x-get


```
curl -X POST \
  https://something.com \
  -H 'Authorization: Bearer myTokenString' \
  -H 'Content-Type: application/json' \
  -d '{
    "accountId": "8c0e5092-602e-4fd7-82e9-64e2cee82e9b"
}'
```