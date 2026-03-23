---
layout: default
title: purl - URL Transfer Tool
permalink: /purl/
---

# purl

**Pure Python URL transfer tool**

## Overview

purl is a pure Python alternative to curl, providing HTTP request functionality without external dependencies. Perfect for downloading files, making API requests, and testing HTTP endpoints.

**Full Name:** Pure Python URL  
**Version:** 0.1.1  
**Equivalent:** `curl`  
**Repository:** [github.com/pynosaur/purl](https://github.com/pynosaur/purl)

## Features

- HTTP GET, POST, PUT, DELETE requests
- Custom headers
- Download to file or stdout
- Follow redirects
- Response headers display
- Verbose mode
- Pure Python - no external dependencies

## Installation

```bash
# Via pget
pget install purl

# From source
git clone https://github.com/pynosaur/purl.git
cd purl
bazel build //:purl_bin
cp bazel-bin/purl ~/.local/bin/
```

## Usage

### Basic Requests

```bash
# Basic GET request
purl https://example.com

# Show help
purl --help

# Show version
purl --version
```

### Download to File

```bash
# Save to file
purl -o page.html https://example.com

# Download archive
purl -o archive.tar.gz https://example.com/file.tar.gz
```

### Response Headers

```bash
# Show response headers
purl -i https://api.github.com

# Check headers only
purl -i https://example.com
```

### Custom Headers

```bash
# Single header
purl -H "Accept: application/json" https://api.github.com

# Multiple headers
purl -H "Authorization: Bearer token" -H "Content-Type: application/json" https://api.example.com
```

### POST Requests

```bash
# POST with data
purl -X POST -d "key=value" https://api.example.com

# POST JSON
purl -X POST -d '{"key":"value"}' -H "Content-Type: application/json" https://api.example.com
```

### Other HTTP Methods

```bash
# PUT request
purl -X PUT -d "data" https://api.example.com/resource

# DELETE request
purl -X DELETE https://api.example.com/resource
```

### Verbose Mode

```bash
# Show detailed output
purl --verbose https://example.com
```

## Options

- `-h, --help` - Show help message
- `-v, --version` - Show version information
- `-o, --output FILE` - Write output to file instead of stdout
- `-H, --header HEADER` - Add custom header (can be used multiple times)
- `-X, --request METHOD` - HTTP method (GET, POST, PUT, DELETE)
- `-d, --data DATA` - HTTP POST data
- `-i, --include` - Include response headers in output
- `-L, --location` - Follow redirects (default behavior)
- `--verbose` - Show verbose output

## Examples

Fetch a webpage:
```bash
purl https://example.com
```

API request with JSON:
```bash
purl -H "Accept: application/json" https://api.github.com/users/pynosaur
```

POST to API:
```bash
purl -X POST \
  -H "Content-Type: application/json" \
  -d '{"name":"test"}' \
  https://api.example.com/data
```

Download file with progress:
```bash
purl --verbose -o download.zip https://example.com/file.zip
```

Check API headers:
```bash
purl -i https://api.example.com/status
```

---

[← Back to Home](/) • [View on GitHub](https://github.com/pynosaur/purl)

