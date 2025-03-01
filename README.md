# rportscan

A fast, asynchronous TCP port scanner written in Rust.

## Features

- Scan thousands of ports in seconds
- Specify custom port ranges
- Simple command-line interface
- Asynchronous scanning using Tokio

## Usage

```
rportscan [OPTIONS]
```

### Options:

```
-a, --address <Address>  Target IP address (defaults to 127.0.0.1)
-s, --start <PORT>       Start port (defaults to 1)
-e, --end <PORT>         End port (defaults to 65535)
-h, --help               Print help
```

### Examples:

Scan all ports on localhost:
```
$ rportscan
```

Scan a specific IP address:
```
$ rportscan -a 192.168.1.1
```

Scan a specific port range:
```
$ rportscan -s 20 -e 100
```

## Sample Output

```
$ rportscan -a 192.168.1.1 -s 20 -e 100
....
22 is open
53 is open
80 is open
84 is open
```

Each dot represents a connection attempt, and found open ports are listed at the end.