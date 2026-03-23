---
layout: default
title: see - File Viewer
permalink: /see/
---

# see

**Display file contents with optional formatting, slicing, and emphasis**

## Overview

see is a modern file viewer that extends the functionality of traditional tools like `cat` with powerful features for slicing, highlighting, and formatting text output.

**Full Name:** see  
**Version:** 0.1.1  
**Equivalent:** `cat`  
**Repository:** [github.com/pynosaur/see](https://github.com/pynosaur/see)

## Features

- Line Slicing - Display specific line ranges
- Character Slicing - Display specific character ranges
- Pattern Emphasis - Highlight specific patterns with colors
- Line Numbers - Display files with line numbers
- stdin Support - Read from standard input

## Installation

```bash
# Via pget
pget install see

# From source
git clone https://github.com/pynosaur/see.git
cd see
bazel build //:see_bin
cp bazel-bin/see ~/.local/bin/
```

## Usage

### Basic Usage

```bash
# Display a file
see file.txt

# Show help
see --help

# Show version
see --version
```

### Line Slicing

```bash
# Lines 0-10
see -l 0:10 file.txt

# First 5 lines
see -l :5 file.txt

# From line 5 to end
see -l 5: file.txt

# Last 5 lines
see -l -5: file.txt

# Every 2nd line from 0-20
see -l 0:20:2 file.txt

# Reverse file
see -l ::-1 file.txt
```

### Specific Line Indices

```bash
# Single line
see -l 5 file.txt

# Multiple specific lines
see -l 0,2,4 file.txt
see -l 10,20,30 file.txt
```

### Character Slicing

```bash
# First 100 characters
see -c 0:100 file.txt

# Characters 50-150
see -c 50:150 file.txt
```

### Pattern Emphasis (Highlighting)

```bash
# Highlight "error"
see -e "error" file.txt

# Multiple patterns
see -e "TODO" -e "FIXME" file.txt

# Custom color and bold
see --color=yellow --bold -e "warning" file.txt

# Case-insensitive
see -i -e "warning" file.txt
```

### Line Emphasis

```bash
# Emphasize specific lines
see -E 1,3,5 file.txt

# Emphasize line range
see -E 0:10 --color=green file.txt
```

### Line Numbers

```bash
# Show line numbers
see -n file.txt
```

### Combined Features

```bash
# Lines 0-20 with numbers, highlighting errors in red
see -n -l 0:20 -e "error" --color=red file.txt
```

### stdin Support

```bash
echo "Hello, World!" | see
cat file.txt | see -e "important"
ls -la | see -e ".py"
```

## Options

- `-h, --help` - Show help message
- `-v, --version` - Show version information
- `-l, --lines SLICE` - Display lines: `start:stop[:step]` or `N,N,N`
- `-c, --chars SLICE` - Display characters: `start:stop[:step]`
- `-e, --emphasize PATTERN` - Highlight pattern
- `-E, --emphasize-lines LINES` - Emphasize entire lines
- `--color COLOR` - Emphasis color (red, green, yellow, blue, magenta, cyan)
- `--bold` - Use bold text for emphasis
- `-i, --ignore-case` - Case-insensitive pattern matching
- `-n, --number` - Show line numbers

## Examples

Preview last 20 lines of a log file:
```bash
see -l -20: large_file.log
```

Highlight errors and warnings in logs:
```bash
see -e "error" -e "warning" --color=red --bold log.txt
```

Find TODO items in source code:
```bash
see -e "TODO" -e "FIXME" --color=yellow src/main.py
```

Show specific lines with numbers:
```bash
see -n -l 0:10 README.md
```

---

[← Back to Home](/) • [View on GitHub](https://github.com/pynosaur/see)

