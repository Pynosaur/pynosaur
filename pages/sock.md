---
layout: default
title: sock - Socket Communication
permalink: /sock/
---

# sock

**Pure Python socket communication tool for sending and receiving messages and files**

## Overview

sock reimagines `netcat`/`telnet` for the Pynosaur ecosystem. Three clear modes — receive, send, and full duplex — with structured protocol for reliable message and file transfer.

**Full Name:** sock  
**Version:** 0.1.0  
**Equivalent:** `netcat` / `telnet`  
**Repository:** [github.com/pynosaur/sock](https://github.com/pynosaur/sock)

## Features

- Three modes — `rec`, `sen`, `mult`
- Structured binary framing protocol
- File transfer with metadata
- Network info and port testing
- Interactive full-duplex chat

## Installation

```bash
# Via pget
pget install sock

# From source
git clone https://github.com/pynosaur/sock.git
cd sock
python app/main.py --help
```

## Usage

### Receive (`rec`)

```bash
# Listen and receive messages/files
sock rec 8080

# Save received files to a directory
sock rec 8080 -d ~/Downloads
```

### Send (`sen`)

```bash
# Send a message
sock sen 192.168.1.10 8080 -m "hello"

# Send a file
sock sen 192.168.1.10 8080 -f document.txt
```

### Full Duplex (`mult`)

```bash
# Listen side
sock mult -l 8080

# Connect side
sock mult 192.168.1.10 8080
```

Interactive commands inside `mult`:

```
> hello                    (send text)
/file notes.txt            (send a file)
/ping                      (ping remote)
/quit                      (close connection)
```

### Network Utilities

```bash
# Show local IP, public IP, gateway
sock info

# Test if port can be bound
sock test 8080
```

## Protocol

sock uses a binary framing protocol over TCP:

```
[4 bytes: payload length (network byte order)]
[JSON header]\n[binary payload]
```

| Packet Type | Purpose |
|-------------|---------|
| `msg` | Text message |
| `file` | File (header has `name` and `size`) |
| `ping` | Ping |
| `pong` | Pong response |

## Examples

### Local messaging

```bash
# Terminal 1
sock rec 9000

# Terminal 2
sock sen localhost 9000 -m "hello"
```

### File transfer over LAN

```bash
# Computer A (192.168.1.10)
sock rec 9000 -d ~/received

# Computer B
sock sen 192.168.1.10 9000 -f report.pdf
```

### Interactive chat

```bash
# Terminal 1
sock mult -l 8080

# Terminal 2
sock mult localhost 8080
```

## Security Note

This is an educational tool with no encryption and no authentication. Do not send sensitive data. Use on trusted networks.
