# toilet-cli

The simple commandline interface for controling electrical toilets like "Washlet".


## Requirements

- Electrical toilet (温水洗浄便座) with buttons.
- open source hardware (based on Raspberry Pi)

## Hardware

## CLI Usage

### wash

Run "おしり" on the toilet.

```
$ toilet-cli wash
```

#### options

- `-d` (`--duration`) : set the duration in seconds
  - example: `$ toilet-cli wash -d 10`
  - default: 5
- `-s` (`--strength`) : set the strength of おしり
  - example: `$ toilet-cli wash -s 3`
  - default: as is (use default value)

### stop

Stop "おしり" immediately.

```
$ toilet-cli stop
```

### strength

Change strength of おしり washing.

```
$ toilet-cli strength 1
```


## Server mode

This app has a server mode. It works as a simple HTTP server which receive HTTP request via JSON.
Please be careful that this is just a "simple" HTTP server. The author strongly does NOT recommend to run this as a public HTTP server. It may break your toilet.

```
$ toilet-cli server
```

### JSON request format

TBD