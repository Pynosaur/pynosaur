<p align="center">
  <img src="https://pynosaur.org/logo.png" alt="Pynosaur Logo" width="250">
</p>

<h1 align="center">Pynosaur</h1>

<p align="center">
  <strong>Exploring classic Unix concepts through pure Python</strong>
</p>

<p align="center">
  <code>v0.2.0</code>
</p>

<p align="center">
  Pure Python • Cross-platform • Educational
</p>

<p align="center">
  <a href="https://github.com/sponsors/Pynosaur">
    <img src="https://img.shields.io/badge/Sponsor-Support_Pynosaur-green?style=for-the-badge" alt="Sponsor Pynosaur">
  </a>
</p>

---

## Overview

Pynosaur is an ecosystem of lightweight command-line tools built for **learning, training, and exploration**. Each tool recreates classic Unix utilities using pure Python, breathing fresh life into old concepts while keeping the purity of Python alive.

**Designed for learners and extenders** - These tools are deliberately simple and well-documented, making them perfect for:
- **Learning by reading** - Understand how CLI tools work under the hood
- **Learning by extending** - Fork, modify, and build upon existing tools
- **Pure Python exploration** - No external dependencies, just the standard library
- **Training ground** - Practice software design and Unix philosophy

## Available Tools

| Tool | Description | Equivalent |
|------|-------------|------------|
| [**pget**](https://github.com/pynosaur/pget) | Package manager (Python Gets) | `apt` / `brew` |
| [**see**](https://github.com/pynosaur/see) | File viewer with slicing & highlighting | `cat` |
| [**purl**](https://github.com/pynosaur/purl) | Pure Python URL transfer tool | `curl` |
| [**yday**](https://github.com/pynosaur/yday) | Current day of year (1-366) | `date +%j` |
| [**doc**](https://github.com/pynosaur/doc) | Documentation viewer | `man` |
| [**sock**](https://github.com/pynosaur/sock) | Socket communication tool | `netcat` / `telnet` |

## Quick Start

Install **pget** (Python Gets), the package manager for the Pynosaur ecosystem:

```bash
git clone https://github.com/pynosaur/pget.git
cd pget && bazel build //:pget_bin
cp bazel-bin/pget ~/.pget/bin/
export PATH="$HOME/.pget/bin:$PATH"

pget install see
pget install yday

see README.md
yday
```

## Philosophy

1. **Pure Python** - Standard library only, keeping Python's purity alive
2. **Educational** - Learn by recreating classic Unix tools
3. **Exploratory** - Breathe fresh software into old concepts
4. **Cross-platform** - Works on macOS, Linux, and Windows
5. **Self-contained** - Single binary, no runtime dependencies

## Why Pynosaur?

This project exists to:
- **Empower learners** - Readable, extendable tools you can actually understand
- **Train developers** - Learn Python and Unix concepts through real tools
- **Explore history** - Understand why classic tools were designed the way they were
- **Keep Python pure** - Prove what's possible with just the standard library
- **Enable extension** - Fork any tool and make it yours

**Use them. Learn from them. Extend them.** Every tool is designed to be understood and modified.

## Documentation

- [Website](https://pynosaur.org) - Tool pages and documentation
- [Roadmap](ROADMAP.md) - Upcoming tools and features
- [Contributing](CONTRIBUTING.md) - Help build the ecosystem

## License

MIT Licensed

---

<p align="center">
  Developed by <a href="https://github.com/vvrmatos">@SpacemanY2K38</a>
  •
  <a href="https://github.com/sponsors/vvrmatos">Sponsor the developer</a>
</p>
