---
layout: default
title: pget - Package Manager
permalink: /pget/
---

# pget

**Pure Python package manager for the Pynosaur ecosystem**

## Overview

pget (Python Gets) is a minimalist package manager designed specifically for standalone Python CLI applications in the Pynosaur ecosystem. Unlike pip which manages libraries and dependencies, pget focuses on distributing self-contained executable tools.

**Full Name:** Python Gets  
**Version:** 0.1.4  
**Equivalent:** `apt` / `brew`  
**Repository:** [github.com/pynosaur/pget](https://github.com/pynosaur/pget)

## Why pget?

- No dependency conflicts - each app is a standalone binary
- Works without pip, virtualenv, or conda
- Perfect for simple CLI utilities that do one thing well
- Automatically downloads pre-built binaries for your platform
- Falls back to building from source when needed
- Everything lives in `~/.pget/bin` - clean and isolated

## Installation

### Quick Start (No Build Required)

```bash
git clone https://github.com/pynosaur/pget.git
cd pget
python app/main.py --help
```

### Build Standalone Binary (Recommended)

```bash
git clone https://github.com/pynosaur/pget.git
cd pget
bazel build //:pget_bin
mkdir -p ~/.pget/bin
cp bazel-bin/pget ~/.pget/bin/
export PATH="$HOME/.pget/bin:$PATH"
```

## Commands

### install

Install a package from the Pynosaur ecosystem:

```bash
pget install <app_name>
```

Example:
```bash
pget install yday
pget install see
```

### remove

Uninstall a package:

```bash
pget remove <app_name>
```

### list

Show all installed packages:

```bash
pget list
```

### update

Update a package to the latest version:

```bash
pget update <app_name>
```

### search

Search for available packages:

```bash
pget search
pget search date
```

## Features

- Pure Python - Standard library only
- Cross-platform - macOS, Linux, Windows
- Smart installation - Downloads binaries or builds from source
- Simple CLI - Familiar package manager commands
- Self-contained - Everything in `~/.pget/bin`
- Standalone binaries - Fast startup, no runtime dependencies

## Platform Support

- macOS (ARM64 and x86_64)
- Linux (x86_64 and ARM64)
- Windows (x86_64)

## Requirements

- Python 3.6 or higher
- Internet connection
- Bazel or Bazelisk (optional, for source builds)

## Use Cases

- System utilities and CLI tools
- Developer productivity tools
- Simple data processing scripts
- Cross-platform command-line applications

---

[← Back to Home](/) • [View on GitHub](https://github.com/pynosaur/pget)

