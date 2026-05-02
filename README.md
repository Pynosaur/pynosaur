<p align="center">
  <img src="logo.png" alt="Pynosaur Logo" width="250">
</p>

<h1 align="center">Pynosaur</h1>

<p align="center">
  <strong>Reimagining CLI tools through pure Python</strong>
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

Pynosaur is an ecosystem of lightweight command-line tools built for **learning, training, and exploration**. Each tool reimagines a familiar concept — from networking and file navigation to text processing and beyond — using nothing but pure Python and the standard library.

**Designed for learners and extenders** - These tools are deliberately simple and well-documented, making them perfect for:
- **Learning by reading** - Understand how CLI tools work under the hood
- **Learning by extending** - Fork, modify, and build upon existing tools
- **Pure Python exploration** - No external dependencies, just the standard library
- **Training ground** - Practice software design and Unix philosophy

## Quick Start

Install **pget** (Python Gets), the package manager for the Pynosaur ecosystem:

```bash
# Clone and build pget
git clone https://github.com/pynosaur/pget.git
cd pget && bazel build //:pget_bin
cp bazel-bin/pget ~/.pget/bin/
export PATH="$HOME/.pget/bin:$PATH"

# Install any Pynosaur tool
pget install see
pget install yday

# Start using them
see README.md
yday
```

## Philosophy

Every Pynosaur tool follows these principles:

1. **Pure Python** - Standard library only, no external dependencies
2. **Educational** - Learn by building real, usable tools
3. **Exploratory** - Reimagine familiar concepts with fresh eyes
4. **Cross-platform** - Works on macOS, Linux, and Windows
5. **Self-contained** - Single binary, no runtime dependencies

## Why Pynosaur?

This project exists to:
- **Empower learners** - Readable, extendable tools you can actually understand
- **Train developers** - Learn Python and Unix concepts through real tools
- **Explore ideas** - Understand the thinking behind the tools we use every day
- **Keep Python pure** - Prove what's possible with just the standard library
- **Enable extension** - Fork any tool and make it yours

**Use them. Learn from them. Extend them.** Every tool is designed to be understood and modified. It's not about replacing what exists — it's about understanding how it works and making it yours.

## Documentation

- [Creating a Program](https://pynosaur.org/creating-a-program/) - Build your own Pynosaur tool
- [Roadmap](/roadmap/) - Upcoming tools and features
- [Contributing](/contributing/) - Help build the ecosystem

## License

MIT Licensed

---

<p align="center">
  Developed by <a href="https://github.com/vvrmatos">@SpacemanY2K38</a>
  •
  <a href="https://github.com/sponsors/vvrmatos">Sponsor the developer</a>
</p>
