# Quick-start a HTTP server

## Serve an empty response once and exit

### macOS

```bash
$ { echo "HTTP/1.0 200 OK" } | nc -l 8080
```

## Serve an empty response

### macOS

```bash
$ while :; do { echo "HTTP/1.0 200 OK" } | nc -l 8080; done
```

## Serve a file once and exit

### macOS

```bash
$ { echo -n "HTTP/1.0 200 OK\r\nContent-Length: $(wc -c </path/to/file)\r\n\r\n"; cat /path/to/file; } | nc -l 8080
```

## Serve a file

### macOS

```bash
$ while :; do { echo -n "HTTP/1.0 200 OK\r\nContent-Length: $(wc -c </path/to/file)\r\n\r\n"; cat /path/to/file; } | nc -l 8080; done
```

## Serve the working directory and its files statically

```bash
$ npx serve # requires npm
```

[`serve`](https://github.com/vercel/serve) by [Vercel](https://vercel.com/).

