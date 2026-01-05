---
layout: default
title: yday - Day of Year
permalink: /yday/
---

# yday

**Current day of year (1-366)**

## Overview

yday is a simple utility that prints the current day of the year as a number from 1 to 366. Perfect for date calculations, logging, and automation scripts.

**Full Name:** Yesterday's Day (Year Day)  
**Version:** 0.1.1  
**Equivalent:** `date +%j`  
**Repository:** [github.com/pynosaur/yday](https://github.com/pynosaur/yday)

## Features

- Simple output - just the day number
- Pure Python - no external dependencies
- Cross-platform - works everywhere
- Fast execution - instant results
- Perfect for scripting and automation

## Installation

```bash
# Via pget
pget install yday

# From source
git clone https://github.com/pynosaur/yday.git
cd yday
bazel build //:yday_bin
cp bazel-bin/yday ~/.local/bin/
```

## Usage

### Basic Usage

```bash
# Print current day of year
yday

# Show help
yday --help

# Show version
yday --version
```

### Example Output

```bash
$ yday
5
```

This means today is the 5th day of the year (January 5th).

## Use Cases

### In Shell Scripts

```bash
#!/bin/bash
DAY=$(yday)
echo "Backup for day $DAY"
tar -czf "backup-day-$DAY.tar.gz" /data
```

### In Automation

```bash
# Daily log files
LOG_FILE="log-$(yday).txt"
echo "Process started" > "$LOG_FILE"
```

### Date Calculations

```bash
# Track days since start of year
echo "We are on day $(yday) of the year"
```

### File Naming

```bash
# Create numbered directories
mkdir "day-$(yday)-results"
```

## Output Format

yday outputs a single number representing the current day of the year:

- January 1 = 1
- December 31 = 365 (or 366 in leap years)

The output is always a plain number with no additional formatting, making it perfect for use in scripts and pipelines.

## Requirements

- Python 3.6 or higher
- No external dependencies

## Platform Support

- macOS
- Linux
- Windows

---

[← Back to Home](/) • [View on GitHub](https://github.com/pynosaur/yday)

