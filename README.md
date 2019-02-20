# C_HTTP

Demonstrate how to performe an HTTP GET request with the the C language using sockets, for Linux and Windows.

Most of the calls are wrapped in http.c

test.c uses  http.c to demonstrate how to actually do a request.

# build

```
gcc test.c http.c -o http_req
```

# Usage

`hostname` is mandatory, `page` is optional (defaults to `/`)

```
./http_req <hostname> [<page>]
```

# example

```
./http_req www.example.com "/"
```

```
./http_req www.example.com "/index.php?id=42&action=foo"
```

* the hostname is not prefixed by 'http://'
* the usage of quotes to prevent special character to mess with the terminal
