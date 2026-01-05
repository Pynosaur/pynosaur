---
layout: default
title: yday - Day of Year
permalink: /yday/
---

# yday

**Current day of year (1-366)**

## Overview

yday is a simple utility that prints the current day of the year as a number from 1 to 366. Perfect for date calculations, logging, and automation scripts.

**Full Name:** Year Day  
**Version:** 0.1.2  
**Equivalent:** `date +%j`  
**Repository:** [github.com/pynosaur/yday](https://github.com/pynosaur/yday)

## Features

- **Day of year** - prints current day number (1-366)
- **Week number** - shows ISO week of the year with `-w`
- **Day name** - displays full localized day name in lowercase with `-n`
- **Monthly calendar** - shows current month calendar with `-m`
- **Complete date** - full date/time with timezone using `-c`
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

# Show week of year
yday -w

# Show full day name in lowercase (localized)
yday -n

# Show monthly calendar
yday -m

# Show complete date/time
yday -c

# Show help
yday --help

# Show version
yday --version
```

### Example Output

```bash
$ yday
5

$ yday -w
2

$ yday -n
monday

$ yday -m
   January 2026
Su Mo Tu We Th Fr Sa
          1  2  3  4
 5  6  7  8  9 10 11
12 13 14 15 16 17 18
19 20 21 22 23 24 25
26 27 28 29 30 31

$ yday -c
Mon Jan  5 11:37:49 WET 2026
```

## Use Cases

### In Shell Scripts

```bash
#!/bin/bash
DAY=$(yday)
WEEK=$(yday -w)
echo "Backup for day $DAY, week $WEEK"
tar -czf "backup-day-$DAY.tar.gz" /data
```

### In Automation

```bash
# Daily log files with day name
LOG_FILE="log-$(yday)-$(yday -n).txt"
echo "Process started on $(yday -c)" > "$LOG_FILE"
```

### Date Calculations

```bash
# Track days and weeks since start of year
echo "We are on day $(yday) of the year, week $(yday -w)"
```

### File Naming

```bash
# Create numbered directories with day names
mkdir "day-$(yday)-$(yday -n)-results"
```

### Display Calendar

```bash
# Show current month calendar in scripts
echo "Current month:"
yday -m
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

