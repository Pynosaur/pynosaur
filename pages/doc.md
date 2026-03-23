---
layout: default
title: doc - Documentation Viewer
permalink: /doc/
---

# doc

**Documentation viewer for Pynosaur CLI tools**

## Overview

doc is a documentation viewer designed for Pynosaur CLI tools. It reads YAML documentation files packaged with each tool and displays them in a pager with a clean, man-like interface.

**Full Name:** Documentation Viewer  
**Version:** 0.1.1  
**Equivalent:** `man`  
**Repository:** [github.com/pynosaur/doc](https://github.com/pynosaur/doc)

## Features

- Man-like pager interface with black background
- Reads YAML documentation files
- Supports local and installed tools
- Fallback to plain output when not in TTY
- Pure Python - no external dependencies

## Installation

```bash
# Via pget
pget install doc

# From source
git clone https://github.com/pynosaur/doc.git
cd doc
bazel build //:doc_bin
cp bazel-bin/doc ~/.local/bin/
```

## Usage

### Basic Usage

```bash
# View documentation for a tool
doc <tool_name>

# Examples
doc pget
doc see
doc yday

# Show help
doc --help

# Show version
doc --version
```

## How It Works

doc searches for documentation in the following order:

1. Bundled `doc/` directory in the doc tool itself
2. Installed helper docs at `~/.pget/helpers/<tool>/doc/<tool>.yaml`
3. If nothing is found, exits with an error

### Documentation Format

Documentation is stored in YAML files with the following structure:

```yaml
NAME: tool_name
VERSION: "0.1.0"
DESCRIPTION: Brief description of the tool
USAGE:
  - "tool_name [options]"
  - "tool_name --help"
OPTIONS:
  - "-h, --help        Show help message"
  - "-v, --version     Show version"
OUTPUT: Description of output format
AUTHOR: "@username"
DATE: "YYYY-MM-DD"
NOTES: []
```

## Navigation

When viewing documentation in the pager:

- **Space** - Scroll down one page
- **b** - Scroll up one page
- **q** - Quit the pager
- **Arrow keys** - Navigate up/down

## Use Cases

### Quick Reference

```bash
# Quickly check command syntax
doc see
doc purl
```

### Learning Tools

```bash
# Understand what a tool does
doc pget
```

### Offline Documentation

```bash
# No internet needed - docs are local
doc yday
```

## Requirements

- Python 3.6 or higher
- Works with any Pynosaur tool that includes a YAML doc file

## Platform Support

- macOS
- Linux
- Windows

---

[← Back to Home](/) • [View on GitHub](https://github.com/pynosaur/doc)

