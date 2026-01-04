# Contributing to Pynosaur

We love contributions! Here's how you can help:

## Ways to Contribute

1. **Report bugs** - Open an issue in the relevant tool's repository
2. **Suggest new tools** - Open an issue in [pynosaur/pynosaur](https://github.com/pynosaur/pynosaur/issues)
3. **Improve documentation** - Submit PRs to any repo
4. **Build new tools** - Follow our [App Development Guidelines](https://github.com/pynosaur/pget#app-development-guidelines)

## Creating a New Tool

1. Read the [App Development Guidelines](https://github.com/pynosaur/pget#app-development-guidelines)
2. Check the [ROADMAP.md](ROADMAP.md) to see planned tools
3. Open an issue to discuss your idea
4. Build your tool following pynosaur conventions
5. Submit a PR to add it to the ecosystem

## Code Standards

- **Pure Python** - Use standard library when possible
- **Tests** - Include unit tests for core functionality
- **Documentation** - Clear README and `--help` output
- **Bazel Build** - Must build with Bazel/Nuitka
- **Cross-platform** - Works on macOS, Linux, Windows

## Tool Requirements

Each pynosaur tool should:

- Have a memorable, short name that doesn't conflict with existing Unix commands
- Do one thing well
- Provide better UX than existing alternatives
- Include `--help` and `--version` flags
- Exit with proper status codes
- Work as a standalone binary

## Questions?

Open an issue in the [main repository](https://github.com/pynosaur/pynosaur/issues) or start a discussion!
