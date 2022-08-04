# Quick-start a HTTP server

### netcat

#### Serve an empty response once and exit

{% code title="macOS" %}
```bash
$ { echo "HTTP/1.0 200 OK" } | nc -l 8080
```
{% endcode %}

#### Serve an empty response

{% code title="macOS" %}
```bash
$ while :; do { echo "HTTP/1.0 200 OK" } | nc -l 8080; done
```
{% endcode %}

#### Serve a file once and exit

{% code overflow="wrap" %}
```bash
$ { echo -n "HTTP/1.0 200 OK\r\nContent-Length: $(wc -c </path/to/file)\r\n\r\n"; cat /path/to/file; } | nc -l 8080
```
{% endcode %}

#### Serve a file

{% code title="macOS" overflow="wrap" %}
```bash
$ while :; do { echo -n "HTTP/1.0 200 OK\r\nContent-Length: $(wc -c </path/to/file)\r\n\r\n"; cat /path/to/file; } | nc -l 8080; done
```
{% endcode %}

### Static file/directory server

#### Serve the working directory and its files

```bash
$ npx serve # requires npm
```

[`serve`](https://github.com/vercel/serve) by [Vercel](https://vercel.com/).

