
# Contributing to Zk-Arithmos

<div align="center">

![Contributing Banner](docs/assets/contributing-banner.svg)

**Welcome to the Zk-Arithmos community! We're excited that you want to contribute.**

[![Contributors](https://img.shields.io/github/contributors/zk-arithmos/zk-arithmos?style=flat-square)](https://github.com/zk-arithmos/zk-arithmos/graphs/contributors)
[![Good First Issues](https://img.shields.io/github/issues/zk-arithmos/zk-arithmos/good%20first%20issue?style=flat-square&color=7057ff)](https://github.com/zk-arithmos/zk-arithmos/issues?q=is%3Aissue+is%3Aopen+label%3A%22good+first+issue%22)
[![Help Wanted](https://img.shields.io/github/issues/zk-arithmos/zk-arithmos/help%20wanted?style=flat-square&color=008672)](https://github.com/zk-arithmos/zk-arithmos/issues?q=is%3Aissue+is%3Aopen+label%3A%22help+wanted%22)
[![Discord](https://img.shields.io/discord/1234567890?style=flat-square&logo=discord&logoColor=white)](https://discord.gg/zkarithmos)

</div>

---

## Table of Contents

- [Welcome](#welcome)
- [Code of Conduct](#code-of-conduct)
- [Ways to Contribute](#ways-to-contribute)
  - [Reporting Bugs](#reporting-bugs)
  - [Suggesting Features](#suggesting-features)
  - [Improving Documentation](#improving-documentation)
  - [Contributing Code](#contributing-code)
  - [Reviewing Pull Requests](#reviewing-pull-requests)
  - [Community Support](#community-support)
  - [Research Contributions](#research-contributions)
  - [Financial Contributions](#financial-contributions)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Development Environment Setup](#development-environment-setup)
  - [Project Structure](#project-structure)
  - [Building the Project](#building-the-project)
  - [Running Tests](#running-tests)
- [Development Workflow](#development-workflow)
  - [Finding Issues to Work On](#finding-issues-to-work-on)
  - [Creating a Branch](#creating-a-branch)
  - [Making Changes](#making-changes)
  - [Committing Changes](#committing-changes)
  - [Submitting a Pull Request](#submitting-a-pull-request)
  - [Code Review Process](#code-review-process)
  - [After Your PR is Merged](#after-your-pr-is-merged)
- [Coding Standards](#coding-standards)
  - [Rust Style Guide](#rust-style-guide)
  - [Code Formatting](#code-formatting)
  - [Linting](#linting)
  - [Naming Conventions](#naming-conventions)
  - [Error Handling](#error-handling)
  - [Comments and Documentation](#comments-and-documentation)
  - [Testing Standards](#testing-standards)
  - [Performance Considerations](#performance-considerations)
  - [Security Considerations](#security-considerations)
- [Documentation Guidelines](#documentation-guidelines)
  - [API Documentation](#api-documentation)
  - [User Guide](#user-guide)
  - [Examples](#examples)
  - [Changelog](#changelog)
- [Testing Guidelines](#testing-guidelines)
  - [Test Categories](#test-categories)
  - [Writing Good Tests](#writing-good-tests)
  - [Test Coverage](#test-coverage)
  - [Fuzzing](#fuzzing)
  - [Benchmarking](#benchmarking)
- [Cryptographic Contributions](#cryptographic-contributions)
  - [Security Requirements](#security-requirements)
  - [Review Process](#review-process)
  - [Constant-Time Code](#constant-time-code)
  - [Randomness](#randomness)
- [Architecture Decisions](#architecture-decisions)
  - [ADR Process](#adr-process)
  - [RFC Process](#rfc-process)
  - [Design Discussions](#design-discussions)
- [Release Process](#release-process)
  - [Versioning](#versioning)
  - [Release Checklist](#release-checklist)
  - [Backporting](#backporting)
- [Issue and PR Labels](#issue-and-pr-labels)
- [Community](#community)
  - [Communication Channels](#communication-channels)
  - [Meetings](#meetings)
  - [Governance](#governance)
- [Recognition](#recognition)
  - [Contributors File](#contributors-file)
  - [Release Credits](#release-credits)
  - [Swag Program](#swag-program)
- [Frequently Asked Questions](#frequently-asked-questions)
- [Resources](#resources)
- [License](#license)

---

## Welcome

First off, thank you for considering contributing to Zk-Arithmos! It's people like you who make Zk-Arithmos such a great tool for the zero-knowledge proof community.

We welcome contributions from everyone, regardless of experience level. Whether you're a seasoned cryptographer or just learning about zero-knowledge proofs, there's a place for you here. Every contribution matters, from fixing a typo in documentation to implementing a new proof system.

### Why Contribute?

Contributing to Zk-Arithmos is a great way to:

- **Learn**: Deep dive into zero-knowledge proofs, Rust, and cryptography
- **Build**: Create tools used by developers worldwide
- **Connect**: Join a community of passionate developers and researchers
- **Grow**: Develop skills valued in blockchain and privacy technology
- **Impact**: Help advance privacy-preserving technology for everyone

### What We're Looking For

We're always looking for:

- Bug fixes and improvements
- New features and gadgets
- Documentation improvements
- Test coverage expansion
- Performance optimizations
- Security enhancements
- Accessibility improvements
- Internationalization
- Design and UX feedback

---

## Code of Conduct

This project and everyone participating in it is governed by our [Code of Conduct](CODE_OF_CONDUCT.md). By participating, you are expected to uphold this code. Please report unacceptable behavior to conduct@zk-arithmos.dev.

### Our Pledge

We pledge to make participation in our project and our community a harassment-free experience for everyone, regardless of:

- Age
- Body size
- Disability
- Ethnicity
- Sex characteristics
- Gender identity and expression
- Level of experience
- Education
- Socio-economic status
- Nationality
- Personal appearance
- Race
- Religion
- Sexual identity and orientation

### Our Standards

**Positive behaviors include:**

- Using welcoming and inclusive language
- Being respectful of differing viewpoints and experiences
- Gracefully accepting constructive criticism
- Focusing on what is best for the community
- Showing empathy towards other community members

**Unacceptable behaviors include:**

- Trolling, insulting/derogatory comments, and personal attacks
- Public or private harassment
- Publishing others' private information without permission
- Other conduct which could reasonably be considered inappropriate

---

## Ways to Contribute

There are many ways to contribute to Zk-Arithmos beyond writing code.

### Reporting Bugs

Found a bug? We'd love to know about it!

#### Before Submitting a Bug Report

1. **Check the documentation** - The issue might be addressed there
2. **Search existing issues** - Someone may have already reported it
3. **Try the latest version** - The bug might already be fixed
4. **Collect information** - Gather details to help us understand the problem

#### How to Submit a Good Bug Report

Create an issue using our [bug report template](.github/ISSUE_TEMPLATE/bug_report.md):

```markdown
**Describe the bug**
A clear and concise description of what the bug is.

**To Reproduce**
Steps to reproduce the behavior:
1. Create a circuit with '...'
2. Generate witness with '...'
3. Call prove() with '...'
4. See error

**Expected behavior**
A clear and concise description of what you expected to happen.

**Actual behavior**
What actually happened.

**Environment**
- Zk-Arithmos version: [e.g., 1.0.0]
- Rust version: [e.g., 1.75.0]
- Operating system: [e.g., Ubuntu 22.04]
- CPU architecture: [e.g., x86_64]

**Additional context**
Add any other context about the problem here.

**Logs/Error Output**
```
Paste any relevant logs or error messages here
```
```

#### Bug Severity Levels

When reporting, help us prioritize by indicating severity:

| Severity | Description | Example |
|----------|-------------|---------|
| Critical | System unusable, data loss, security issue | Proof verification accepts invalid proofs |
| High | Major feature broken, no workaround | Prover crashes on valid circuits |
| Medium | Feature impaired, workaround exists | CLI flag doesn't work, can use config file |
| Low | Minor issue, cosmetic | Typo in error message |

### Suggesting Features

Have an idea for a new feature? We'd love to hear it!

#### Before Suggesting a Feature

1. **Check the roadmap** - It might already be planned
2. **Search existing issues** - Someone may have already suggested it
3. **Consider the scope** - Does it fit the project's goals?

#### How to Suggest a Feature

Create an issue using our [feature request template](.github/ISSUE_TEMPLATE/feature_request.md):

```markdown
**Is your feature request related to a problem?**
A clear and concise description of what the problem is.

**Describe the solution you'd like**
A clear and concise description of what you want to happen.

**Describe alternatives you've considered**
A clear and concise description of any alternative solutions.

**Use cases**
Describe specific use cases that would benefit from this feature.

**Additional context**
Add any other context, mockups, or examples about the feature request.
```

#### Feature Request Guidelines

Good feature requests:

- **Solve a real problem** - Explain the pain point
- **Are specific** - Describe exactly what you want
- **Consider alternatives** - Show you've thought about other solutions
- **Think about impact** - Consider how it affects existing users
- **Are realistic** - Understand scope and complexity

### Improving Documentation

Documentation is crucial for any project. Help us make it better!

#### Types of Documentation Contributions

- **Fix typos and grammar** - Small but valuable
- **Clarify confusing sections** - If something confused you, it confuses others
- **Add examples** - Real-world examples help understanding
- **Write tutorials** - Guide others through specific tasks
- **Translate** - Help non-English speakers
- **Update outdated content** - Keep docs current

#### Documentation Locations

| Type | Location | Format |
|------|----------|--------|
| API docs | Inline in code | Rust doc comments |
| User guide | `docs/` directory | Markdown |
| Tutorials | `docs/tutorials/` | Markdown |
| Examples | `examples/` directory | Rust code |
| Website | `website/` directory | MDX |

### Contributing Code

Ready to write some code? Here's how to contribute effectively.

#### Good First Contributions

If you're new, look for issues labeled:

- `good first issue` - Simple, well-defined tasks
- `help wanted` - We'd appreciate help
- `documentation` - Doc improvements
- `tests` - Test coverage improvements

#### Types of Code Contributions

| Type | Description | Complexity |
|------|-------------|------------|
| Bug fixes | Fix reported issues | Varies |
| Small features | Add minor functionality | Low-Medium |
| Large features | Major new functionality | High |
| Refactoring | Improve code structure | Medium-High |
| Performance | Optimize existing code | Medium-High |
| Tests | Add/improve tests | Low-Medium |
| Gadgets | New circuit gadgets | Medium |

### Reviewing Pull Requests

Code review is valuable contribution!

#### How to Review

1. **Understand the context** - Read the PR description and linked issues
2. **Check out the code** - Test it locally if possible
3. **Review thoroughly** - Check logic, style, tests, docs
4. **Be constructive** - Suggest improvements kindly
5. **Approve or request changes** - Make your verdict clear

#### Review Checklist

- [ ] Code is correct and solves the stated problem
- [ ] Code follows project style guidelines
- [ ] Tests are included and pass
- [ ] Documentation is updated
- [ ] No security concerns
- [ ] Performance is acceptable
- [ ] Error handling is appropriate

### Community Support

Help others in the community:

- **Answer questions** on Discord, GitHub Discussions, or Stack Overflow
- **Write blog posts** about using Zk-Arithmos
- **Give talks** at meetups or conferences
- **Create videos** or tutorials
- **Mentor newcomers** to the project

### Research Contributions

Academic or research contributions:

- **Publish papers** using or analyzing Zk-Arithmos
- **Propose improvements** based on research
- **Implement new algorithms** from papers
- **Conduct security analysis**
- **Benchmark comparisons** with other systems

### Financial Contributions

Support the project financially:

- **GitHub Sponsors** - Monthly sponsorship
- **Open Collective** - One-time or recurring donations
- **Gitcoin Grants** - Quadratic funding rounds
- **Corporate sponsorship** - Contact us for details

---

## Getting Started

### Prerequisites

Before you begin, ensure you have the following installed:

#### Required

| Tool | Minimum Version | Check Command | Installation |
|------|-----------------|---------------|--------------|
| Rust | 1.75.0 | `rustc --version` | [rustup.rs](https://rustup.rs) |
| Cargo | 1.75.0 | `cargo --version` | Included with Rust |
| Git | 2.30.0 | `git --version` | [git-scm.com](https://git-scm.com) |

#### Recommended

| Tool | Purpose | Installation |
|------|---------|--------------|
| cargo-watch | Auto-rebuild on changes | `cargo install cargo-watch` |
| cargo-audit | Security vulnerability checks | `cargo install cargo-audit` |
| cargo-deny | License and security checks | `cargo install cargo-deny` |
| cargo-tarpaulin | Code coverage | `cargo install cargo-tarpaulin` |
| cargo-criterion | Benchmarking | `cargo install cargo-criterion` |
| cargo-fuzz | Fuzzing | `cargo install cargo-fuzz` |
| just | Command runner | `cargo install just` |

#### Optional

| Tool | Purpose | Installation |
|------|---------|--------------|
| Docker | Containerized builds | [docker.com](https://docker.com) |
| CUDA Toolkit | GPU acceleration | [nvidia.com](https://developer.nvidia.com/cuda-toolkit) |
| wasm-pack | WebAssembly builds | `cargo install wasm-pack` |

### Development Environment Setup

#### 1. Fork the Repository

Click the "Fork" button on [GitHub](https://github.com/zk-arithmos/zk-arithmos) to create your own copy.

#### 2. Clone Your Fork

```bash
# Clone your fork
git clone https://github.com/YOUR_USERNAME/zk-arithmos.git
cd zk-arithmos

# Add upstream remote
git remote add upstream https://github.com/zk-arithmos/zk-arithmos.git

# Verify remotes
git remote -v
# origin    https://github.com/YOUR_USERNAME/zk-arithmos.git (fetch)
# origin    https://github.com/YOUR_USERNAME/zk-arithmos.git (push)
# upstream  https://github.com/zk-arithmos/zk-arithmos.git (fetch)
# upstream  https://github.com/zk-arithmos/zk-arithmos.git (push)
```

#### 3. Install Development Dependencies

```bash
# Run setup script
./scripts/setup-dev.sh

# Or manually install tools
rustup component add rustfmt clippy
cargo install cargo-watch cargo-audit cargo-tarpaulin just
```

#### 4. Configure Git Hooks

```bash
# Install pre-commit hooks
./scripts/install-hooks.sh

# Or manually
cp scripts/hooks/* .git/hooks/
chmod +x .git/hooks/*
```

#### 5. Verify Setup

```bash
# Build the project
cargo build

# Run tests
cargo test

# Run lints
cargo clippy

# Check formatting
cargo fmt -- --check

# Run full verification
just verify
```

#### IDE Setup

##### VS Code

Recommended extensions:

```json
{
  "recommendations": [
    "rust-lang.rust-analyzer",
    "tamasfe.even-better-toml",
    "serayuzgur.crates",
    "vadimcn.vscode-lldb",
    "zk-arithmos.zk-arithmos-vscode"
  ]
}
```

Recommended settings (`.vscode/settings.json`):

```json
{
  "rust-analyzer.cargo.features": "all",
  "rust-analyzer.checkOnSave.command": "clippy",
  "editor.formatOnSave": true,
  "[rust]": {
    "editor.defaultFormatter": "rust-lang.rust-analyzer"
  }
}
```

##### IntelliJ IDEA / CLion

1. Install the Rust plugin
2. Open the project (it will detect Cargo.toml)
3. Configure the toolchain in Settings → Languages & Frameworks → Rust

##### Vim / Neovim

Recommended plugins:

- `rust.vim` - Rust syntax and file detection
- `coc-rust-analyzer` or `nvim-lspconfig` - LSP support
- `vim-cargo` - Cargo integration

### Project Structure

Understanding the project structure helps you navigate effectively:

```
zk-arithmos/
├── .github/                    # GitHub configuration
│   ├── ISSUE_TEMPLATE/         # Issue templates
│   ├── PULL_REQUEST_TEMPLATE/  # PR templates
│   ├── workflows/              # CI/CD workflows
│   └── CODEOWNERS              # Code ownership
├── crates/                     # Rust crates (workspaces)
│   ├── zk-arithmos/            # Meta-crate (re-exports all)
│   ├── zk-arithmos-core/       # Core types and traits
│   │   ├── src/
│   │   │   ├── field/          # Field traits and implementations
│   │   │   ├── wire/           # Wire types
│   │   │   ├── gate/           # Gate definitions
│   │   │   ├── constraint/     # Constraint types
│   │   │   └── lib.rs          # Crate root
│   │   ├── tests/              # Integration tests
│   │   └── Cargo.toml          # Crate manifest
│   ├── zk-arithmos-circuit/    # Circuit building
│   │   ├── src/
│   │   │   ├── builder/        # Circuit builder
│   │   │   ├── gadget/         # Gadget implementations
│   │   │   ├── expression/     # Expression system
│   │   │   └── lib.rs
│   │   └── Cargo.toml
│   ├── zk-arithmos-witness/    # Witness generation
│   │   ├── src/
│   │   │   ├── provider/       # Witness providers
│   │   │   ├── solver/         # Witness solver
│   │   │   └── lib.rs
│   │   └── Cargo.toml
│   ├── zk-arithmos-proof/      # Proof systems
│   │   ├── src/
│   │   │   ├── groth16/        # Groth16 implementation
│   │   │   ├── plonk/          # PLONK implementation
│   │   │   ├── marlin/         # Marlin implementation
│   │   │   └── lib.rs
│   │   └── Cargo.toml
│   ├── zk-arithmos-dsl/        # DSL compiler
│   │   ├── src/
│   │   │   ├── lexer/          # Tokenization
│   │   │   ├── parser/         # Parsing
│   │   │   ├── semantic/       # Semantic analysis
│   │   │   ├── ir/             # Intermediate representation
│   │   │   ├── codegen/        # Code generation
│   │   │   └── lib.rs
│   │   └── Cargo.toml
│   └── zk-arithmos-cli/        # Command-line interface
│       ├── src/
│       │   ├── commands/       # CLI commands
│       │   └── main.rs
│       └── Cargo.toml
├── docs/                       # Documentation
│   ├── architecture/           # Architecture docs
│   ├── tutorials/              # Tutorial guides
│   ├── api/                    # API documentation
│   └── adr/                    # Architecture Decision Records
├── examples/                   # Example projects
│   ├── simple-proof/           # Basic proof example
│   ├── merkle-proof/           # Merkle tree example
│   ├── private-transfer/       # Token transfer example
│   └── voting/                 # Voting example
├── benches/                    # Benchmarks
│   ├── proving.rs              # Proving benchmarks
│   ├── verification.rs         # Verification benchmarks
│   └── circuit.rs              # Circuit construction benchmarks
├── fuzz/                       # Fuzzing targets
│   ├── fuzz_targets/           # Fuzz target definitions
│   └── corpus/                 # Fuzzing corpus
├── scripts/                    # Development scripts
│   ├── setup-dev.sh            # Development setup
│   ├── install-hooks.sh        # Git hooks installation
│   ├── release.sh              # Release automation
│   └── benchmark.sh            # Benchmark runner
├── tests/                      # Integration tests
│   ├── integration/            # Full integration tests
│   └── e2e/                    # End-to-end tests
├── .cargo/                     # Cargo configuration
│   └── config.toml             # Cargo settings
├── .rustfmt.toml               # Rustfmt configuration
├── .clippy.toml                # Clippy configuration
├── Cargo.toml                  # Workspace manifest
├── Cargo.lock                  # Dependency lock file
├── justfile                    # Just command runner recipes
├── deny.toml                   # cargo-deny configuration
├── README.md                   # Project README
├── CHANGELOG.md                # Version changelog
├── CONTRIBUTING.md             # This file
├── CODE_OF_CONDUCT.md          # Code of conduct
├── SECURITY.md                 # Security policy
├── LICENSE-MIT                 # MIT license
└── LICENSE-APACHE              # Apache 2.0 license
```

### Building the Project

#### Basic Build

```bash
# Debug build (faster compilation, slower execution)
cargo build

# Release build (slower compilation, faster execution)
cargo build --release

# Build specific crate
cargo build -p zk-arithmos-core

# Build with all features
cargo build --all-features

# Build for WebAssembly
cargo build --target wasm32-unknown-unknown -p zk-arithmos-wasm
```

#### Using Just

We provide a `justfile` for common tasks:

```bash
# List available commands
just --list

# Build everything
just build

# Build release
just build-release

# Clean build artifacts
just clean
```

### Running Tests

#### All Tests

```bash
# Run all tests
cargo test

# Run all tests with output
cargo test -- --nocapture

# Run tests in release mode
cargo test --release

# Run tests for specific crate
cargo test -p zk-arithmos-core
```

#### Specific Test Categories

```bash
# Unit tests only
cargo test --lib

# Integration tests only
cargo test --test '*'

# Documentation tests only
cargo test --doc

# Specific test
cargo test test_name

# Tests matching pattern
cargo test constraint
```

#### Test Options

```bash
# Show test output
cargo test -- --nocapture

# Run tests in single thread
cargo test -- --test-threads=1

# Run ignored tests
cargo test -- --ignored

# Run all tests including ignored
cargo test -- --include-ignored

# Show time taken
cargo test -- --show-output
```

---

## Development Workflow

### Finding Issues to Work On

#### Good Starting Points

1. **Good First Issues**
   - [View all good first issues](https://github.com/zk-arithmos/zk-arithmos/labels/good%20first%20issue)
   - Well-defined scope
   - Mentorship available
   - Good for learning the codebase

2. **Help Wanted**
   - [View all help wanted issues](https://github.com/zk-arithmos/zk-arithmos/labels/help%20wanted)
   - More complex but well-documented
   - Community input welcome

3. **Documentation**
   - [View documentation issues](https://github.com/zk-arithmos/zk-arithmos/labels/documentation)
   - No Rust expertise required
   - High impact

#### Claiming an Issue

1. Check if the issue is already assigned
2. Comment on the issue expressing interest
3. Wait for maintainer confirmation
4. Start working once assigned

```markdown
Hi! I'd like to work on this issue. I have experience with [relevant experience].
My approach would be to [brief description of planned approach].
```

### Creating a Branch

#### Branch Naming Convention

```
<type>/<issue-number>-<short-description>
```

| Type | Use For |
|------|---------|
| `feature/` | New features |
| `fix/` | Bug fixes |
| `docs/` | Documentation changes |
| `refactor/` | Code refactoring |
| `test/` | Test additions/changes |
| `perf/` | Performance improvements |
| `chore/` | Maintenance tasks |

#### Examples

```bash
# Feature branch
git checkout -b feature/123-add-poseidon-gadget

# Bug fix branch
git checkout -b fix/456-constraint-overflow

# Documentation branch
git checkout -b docs/789-update-installation-guide
```

#### Creating the Branch

```bash
# Ensure you're on main and up to date
git checkout main
git pull upstream main

# Create and switch to new branch
git checkout -b feature/123-my-feature

# Push branch to your fork
git push -u origin feature/123-my-feature
```

### Making Changes

#### Development Loop

```bash
# Watch for changes and rebuild
cargo watch -x check

# Watch and run tests
cargo watch -x test

# Watch specific crate
cargo watch -x "test -p zk-arithmos-core"
```

#### Code Quality Checks

Run these before committing:

```bash
# Format code
cargo fmt

# Run clippy
cargo clippy --all-targets --all-features -- -D warnings

# Run tests
cargo test

# Check documentation
cargo doc --no-deps

# Full verification
just verify
```

### Committing Changes

#### Commit Message Format

We follow [Conventional Commits](https://www.conventionalcommits.org/):

```
<type>(<scope>): <subject>

[optional body]

[optional footer]
```

#### Types

| Type | Description |
|------|-------------|
| `feat` | New feature |
| `fix` | Bug fix |
| `docs` | Documentation only |
| `style` | Formatting, no code change |
| `refactor` | Code change that neither fixes bug nor adds feature |
| `perf` | Performance improvement |
| `test` | Adding/updating tests |
| `chore` | Maintenance tasks |
| `ci` | CI/CD changes |
| `build` | Build system changes |
| `revert` | Reverting previous commit |

#### Scopes

| Scope | Description |
|-------|-------------|
| `core` | zk-arithmos-core crate |
| `circuit` | zk-arithmos-circuit crate |
| `witness` | zk-arithmos-witness crate |
| `proof` | zk-arithmos-proof crate |
| `dsl` | zk-arithmos-dsl crate |
| `cli` | zk-arithmos-cli crate |
| `deps` | Dependencies |
| `*` | Multiple scopes |

#### Examples

```bash
# Feature
git commit -m "feat(circuit): add Poseidon hash gadget

Implement Poseidon hash function as a reusable gadget.
Supports configurable width and number of rounds.

Closes #123"

# Bug fix
git commit -m "fix(proof): correct constraint generation for division

Division by zero was not properly constrained, allowing
invalid witnesses to pass verification.

Fixes #456"

# Documentation
git commit -m "docs(readme): update installation instructions

Add Windows-specific setup steps and troubleshooting."

# Breaking change
git commit -m "feat(core)!: redesign Field trait hierarchy

BREAKING CHANGE: Field trait now requires Send + Sync bounds.
This enables safe parallel proving but requires updating
custom field implementations.

Migration guide: docs/migration/1.0.md"
```

#### Commit Best Practices

1. **Atomic commits** - Each commit should be a single logical change
2. **Build passes** - Every commit should compile and pass tests
3. **Meaningful messages** - Describe what and why, not how
4. **Reference issues** - Link to relevant issues

### Submitting a Pull Request

#### Before Submitting

Ensure your PR is ready:

- [ ] Code compiles without warnings
- [ ] All tests pass
- [ ] Code is formatted (`cargo fmt`)
- [ ] No clippy warnings (`cargo clippy`)
- [ ] Documentation updated
- [ ] Changelog updated (if applicable)
- [ ] Commits are clean and well-messaged

#### Creating the PR

1. Push your branch to your fork
2. Go to [Pull Requests](https://github.com/zk-arithmos/zk-arithmos/pulls)
3. Click "New Pull Request"
4. Select your branch
5. Fill in the template

#### PR Template

```markdown
## Description

Brief description of the changes.

## Type of Change

- [ ] Bug fix (non-breaking change that fixes an issue)
- [ ] New feature (non-breaking change that adds functionality)
- [ ] Breaking change (fix or feature that would cause existing functionality to change)
- [ ] Documentation update
- [ ] Performance improvement
- [ ] Code refactoring

## Related Issues

Closes #(issue number)

## Changes Made

- Change 1
- Change 2
- Change 3

## Testing

Describe the tests you ran:

- [ ] Unit tests
- [ ] Integration tests
- [ ] Manual testing

## Screenshots (if applicable)

Add screenshots here.

## Checklist

- [ ] My code follows the project's style guidelines
- [ ] I have performed a self-review of my code
- [ ] I have commented my code, particularly in hard-to-understand areas
- [ ] I have made corresponding changes to the documentation
- [ ] My changes generate no new warnings
- [ ] I have added tests that prove my fix is effective or that my feature works
- [ ] New and existing unit tests pass locally with my changes
- [ ] Any dependent changes have been merged and published

## Additional Notes

Any additional information reviewers should know.
```

#### PR Title Format

Follow the same format as commit messages:

```
<type>(<scope>): <description>
```

Examples:
- `feat(circuit): add Poseidon hash gadget`
- `fix(proof): correct constraint generation`
- `docs: update contributing guide`

### Code Review Process

#### What to Expect

1. **Automated checks** run immediately (CI/CD)
2. **Maintainer triage** within 1-2 days
3. **Code review** within 1 week
4. **Iteration** based on feedback
5. **Approval and merge** when ready

#### Responding to Feedback

- Be responsive to comments
- Discuss if you disagree
- Push fixes as new commits (we'll squash on merge)
- Re-request review when ready

#### Review Criteria

Reviewers will check:

| Criteria | Description |
|----------|-------------|
| Correctness | Does the code work as intended? |
| Design | Is it well-designed and consistent? |
| Complexity | Is it as simple as possible? |
| Tests | Are there adequate tests? |
| Naming | Are names clear and descriptive? |
| Comments | Are comments helpful and accurate? |
| Style | Does it follow our style guide? |
| Documentation | Is documentation updated? |
| Security | Are there security concerns? |

### After Your PR is Merged

Congratulations! 🎉

1. **Delete your branch** (GitHub offers this automatically)
2. **Update your fork**:
   ```bash
   git checkout main
   git pull upstream main
   git push origin main
   ```
3. **Celebrate** - You're now a contributor!

---

## Coding Standards

### Rust Style Guide

We follow the [Rust API Guidelines](https://rust-lang.github.io/api-guidelines/) and standard Rust idioms.

#### General Principles

1. **Clarity over cleverness** - Write readable code
2. **Consistency** - Follow existing patterns
3. **Safety** - Avoid unsafe when possible
4. **Performance** - But not at the cost of clarity

#### Specific Guidelines

##### Imports

```rust
// Group imports: std, external crates, internal crates, local modules
use std::collections::HashMap;

use ark_ff::Field;
use serde::{Deserialize, Serialize};

use zk_arithmos_core::Wire;

use crate::gadget::Gadget;
use super::constraint::Constraint;
```

##### Struct Definitions

```rust
/// A constraint in the R1CS format.
///
/// Represents A · B = C where A, B, C are linear combinations.
#[derive(Debug, Clone, PartialEq, Eq)]
pub struct Constraint<F: Field> {
    /// Left input (A)
    pub a: LinearCombination<F>,
    /// Right input (B)
    pub b: LinearCombination<F>,
    /// Output (C)
    pub c: LinearCombination<F>,
}
```

##### Function Definitions

```rust
/// Generates a zero-knowledge proof for the given circuit and witness.
///
/// # Arguments
///
/// * `circuit` - The compiled circuit
/// * `witness` - The witness values
/// * `pk` - The proving key
///
/// # Returns
///
/// Returns `Ok(Proof)` on success, or an error if:
/// - The witness doesn't satisfy the constraints
/// - The proving key is invalid
///
/// # Example
///
/// ```
/// let proof = prove(&circuit, &witness, &pk)?;
/// ```
pub fn prove<F: Field>(
    circuit: &Circuit<F>,
    witness: &Witness<F>,
    pk: &ProvingKey<F>,
) -> Result<Proof<F>, ProofError> {
    // Implementation
}
```

##### Error Handling

```rust
/// Errors that can occur during proof generation.
#[derive(Debug, thiserror::Error)]
pub enum ProofError {
    /// The witness does not satisfy the circuit constraints.
    #[error("constraint {index} not satisfied: expected {expected}, got {actual}")]
    ConstraintNotSatisfied {
        index: usize,
        expected: String,
        actual: String,
    },

    /// The proving key is invalid or corrupted.
    #[error("invalid proving key: {reason}")]
    InvalidProvingKey { reason: String },

    /// An internal cryptographic error occurred.
    #[error("cryptographic error: {0}")]
    CryptoError(#[from] CryptoError),
}
```

### Code Formatting

We use `rustfmt` with the following configuration (`.rustfmt.toml`):

```toml
# Rustfmt configuration
edition = "2021"
max_width = 100
tab_spaces = 4
newline_style = "Unix"
use_small_heuristics = "Default"

# Imports
imports_granularity = "Module"
group_imports = "StdExternalCrate"
reorder_imports = true

# Comments
wrap_comments = true
comment_width = 80
normalize_comments = true

# Other
format_code_in_doc_comments = true
format_macro_matchers = true
format_strings = true
```

Run formatting:

```bash
# Format all code
cargo fmt

# Check formatting without changing
cargo fmt -- --check
```

### Linting

We use `clippy` with strict settings:

```bash
# Run clippy
cargo clippy --all-targets --all-features -- -D warnings

# With specific lints
cargo clippy -- \
    -D clippy::all \
    -D clippy::pedantic \
    -D clippy::nursery \
    -A clippy::module_name_repetitions \
    -A clippy::similar_names
```

#### Must-Fix Lints

These lints must be addressed:

- `clippy::correctness` - All correctness lints
- `clippy::suspicious` - Suspicious code patterns
- `clippy::complexity` - Unnecessarily complex code
- `clippy::perf` - Performance issues

#### Should-Fix Lints

Address these when practical:

- `clippy::pedantic` - Pedantic lints
- `clippy::style` - Style issues

### Naming Conventions

| Item | Convention | Example |
|------|------------|---------|
| Crates | `snake_case` | `zk_arithmos_core` |
| Modules | `snake_case` | `constraint_system` |
| Types | `PascalCase` | `CircuitBuilder` |
| Traits | `PascalCase` | `Field`, `Gadget` |
| Functions | `snake_case` | `generate_proof` |
| Methods | `snake_case` | `add_constraint` |
| Variables | `snake_case` | `constraint_count` |
| Constants | `SCREAMING_SNAKE_CASE` | `MAX_CONSTRAINTS` |
| Type parameters | `PascalCase`, single letter or descriptive | `F`, `Field` |
| Lifetimes | Lowercase, descriptive | `'a`, `'circuit` |

#### Naming Guidelines

- **Be descriptive** - `constraint_count` not `cc`
- **Be consistent** - Use the same term throughout
- **Avoid abbreviations** - Unless universally understood
- **Use domain terminology** - `witness`, `constraint`, `gadget`

### Error Handling

#### Use Result for Fallible Operations

```rust
// Good
pub fn parse(input: &str) -> Result<Circuit, ParseError> {
    // ...
}

// Avoid
pub fn parse(input: &str) -> Option<Circuit> {
    // ...
}
```

#### Create Meaningful Error Types

```rust
#[derive(Debug, thiserror::Error)]
pub enum CircuitError {
    #[error("wire {wire_id} is not defined")]
    UndefinedWire { wire_id: WireId },

    #[error("constraint references wire from different circuit")]
    WireCircuitMismatch,

    #[error("circuit has no public inputs")]
    NoPublicInputs,
}
```

#### Use ? Operator

```rust
// Good
fn process() -> Result<Output, Error> {
    let a = step_one()?;
    let b = step_two(a)?;
    let c = step_three(b)?;
    Ok(c)
}

// Avoid
fn process() -> Result<Output, Error> {
    match step_one() {
        Ok(a) => match step_two(a) {
            Ok(b) => step_three(b),
            Err(e) => Err(e),
        },
        Err(e) => Err(e),
    }
}
```

#### Avoid Panics in Library Code

```rust
// Good - Return error
pub fn divide<F: Field>(a: F, b: F) -> Result<F, DivisionError> {
    if b.is_zero() {
        return Err(DivisionError::DivideByZero);
    }
    Ok(a * b.inverse())
}

// Avoid - Panic
pub fn divide<F: Field>(a: F, b: F) -> F {
    assert!(!b.is_zero(), "division by zero");
    a * b.inverse()
}
```

### Comments and Documentation

#### When to Comment

- **Complex algorithms** - Explain the approach
- **Non-obvious code** - Explain why
- **Workarounds** - Explain what and why
- **Security considerations** - Highlight security-critical code
- **Performance considerations** - Explain optimization choices

#### Documentation Comments

```rust
/// A zero-knowledge circuit for proving knowledge of a preimage.
///
/// This circuit proves that the prover knows a value `x` such that
/// `hash(x) = y`, where `y` is a public input.
///
/// # Security
///
/// The security of this circuit relies on the collision resistance
/// of the Poseidon hash function.
///
/// # Example
///
/// ```
/// use zk_arithmos::prelude::*;
///
/// let circuit = HashPreimageCircuit::new();
/// let witness = circuit.generate_witness(preimage);
/// let proof = prove(&circuit, &witness, &pk)?;
/// ```
pub struct HashPreimageCircuit<F: Field> {
    // ...
}
```

#### Inline Comments

```rust
fn compute_witness(&self, input: &[F]) -> Vec<F> {
    let mut witness = Vec::with_capacity(self.num_wires());

    // Public inputs come first
    witness.extend_from_slice(input);

    // Compute intermediate values in topological order
    for gate in &self.gates {
        let output = gate.evaluate(&witness);
        witness.push(output);
    }

    // The last value is the output
    witness
}
```

#### TODO Comments

```rust
// TODO(#123): Implement batch verification for better performance
// TODO(@username): Review this algorithm for side-channel resistance
// FIXME: This is a temporary workaround for issue #456
// HACK: Working around limitation in dependency X
// SAFETY: This is safe because [explanation]
```

### Testing Standards

#### Test Organization

```rust
#[cfg(test)]
mod tests {
    use super::*;

    // Unit tests for specific functions
    mod add_constraint {
        use super::*;

        #[test]
        fn adds_valid_constraint() {
            // ...
        }

        #[test]
        fn rejects_invalid_wire() {
            // ...
        }
    }

    // Integration tests
    mod integration {
        use super::*;

        #[test]
        fn end_to_end_proof() {
            // ...
        }
    }
}
```

#### Test Naming

```rust
#[test]
fn function_name_condition_expected_result() {
    // ...
}

// Examples
#[test]
fn add_constraint_with_valid_wires_succeeds() { }

#[test]
fn add_constraint_with_invalid_wire_returns_error() { }

#[test]
fn prove_with_valid_witness_creates_valid_proof() { }

#[test]
fn verify_with_tampered_proof_returns_false() { }
```

#### Test Structure

```rust
#[test]
fn descriptive_test_name() {
    // Arrange - Set up test data
    let circuit = create_test_circuit();
    let witness = create_test_witness();

    // Act - Perform the action being tested
    let result = prove(&circuit, &witness);

    // Assert - Verify the results
    assert!(result.is_ok());
    let proof = result.unwrap();
    assert!(verify(&proof, &circuit.public_inputs()));
}
```

### Performance Considerations

#### Memory Efficiency

```rust
// Good - Avoid unnecessary allocation
fn process(data: &[F]) -> F {
    data.iter().sum()
}

// Avoid - Unnecessary clone
fn process(data: &[F]) -> F {
    let cloned: Vec<F> = data.to_vec();
    cloned.iter().sum()
}
```

#### Iterators Over Collections

```rust
// Good - Use iterators
let sum: F = values.iter().sum();

// Avoid - Manual indexing
let mut sum = F::zero();
for i in 0..values.len() {
    sum += values[i];
}
```

#### Preallocate When Possible

```rust
// Good - Preallocate
let mut result = Vec::with_capacity(expected_size);
for item in source {
    result.push(process(item));
}

// Avoid - Grow dynamically
let mut result = Vec::new();
for item in source {
    result.push(process(item));
}
```

### Security Considerations

#### Constant-Time Operations

```rust
// Good - Constant time comparison
use subtle::ConstantTimeEq;

fn compare_secrets(a: &[u8], b: &[u8]) -> bool {
    a.ct_eq(b).into()
}

// Avoid - Variable time comparison
fn compare_secrets(a: &[u8], b: &[u8]) -> bool {
    a == b
}
```

#### Secure Memory Handling

```rust
use zeroize::Zeroize;

struct SecretKey {
    bytes: [u8; 32],
}

impl Drop for SecretKey {
    fn drop(&mut self) {
        self.bytes.zeroize();
    }
}
```

#### Input Validation

```rust
pub fn process_input(input: &[u8]) -> Result<Output, Error> {
    // Validate input length
    if input.len() > MAX_INPUT_SIZE {
        return Err(Error::InputTooLarge);
    }

    // Validate input format
    if !is_valid_format(input) {
        return Err(Error::InvalidFormat);
    }

    // Process validated input
    process_validated(input)
}
```

---

## Documentation Guidelines

### API Documentation

Every public item must be documented:

```rust
/// Brief one-line description.
///
/// Longer description explaining the item in detail. This can span
/// multiple paragraphs if needed.
///
/// # Arguments
///
/// * `param1` - Description of first parameter
/// * `param2` - Description of second parameter
///
/// # Returns
///
/// Description of what is returned.
///
/// # Errors
///
/// This function returns an error if:
///
/// * Condition 1 occurs
/// * Condition 2 occurs
///
/// # Panics
///
/// This function panics if:
///
/// * Condition (only if it can actually panic)
///
/// # Safety
///
/// (For unsafe functions) Explanation of safety requirements.
///
/// # Examples
///
/// ```
/// use zk_arithmos::prelude::*;
///
/// let result = function_name(arg1, arg2)?;
/// assert!(result.is_valid());
/// ```
///
/// # See Also
///
/// * [`related_function`] - Description
/// * [`RelatedType`] - Description
pub fn function_name(param1: Type1, param2: Type2) -> Result<Output, Error> {
    // ...
}
```

### User Guide

The user guide in `docs/` uses Markdown:

#### Structure

```
docs/
├── README.md           # Documentation index
├── getting-started.md  # Quick start guide
├── concepts/           # Core concepts
│   ├── circuits.md
│   ├── witnesses.md
│   └── proofs.md
├── tutorials/          # Step-by-step tutorials
│   ├── first-circuit.md
│   └── merkle-proof.md
├── guides/             # How-to guides
│   ├── optimization.md
│   └── deployment.md
└── reference/          # Reference documentation
    ├── cli.md
    └── dsl.md
```

#### Writing Style

- Use second person ("you")
- Be concise but complete
- Include examples for every concept
- Link to related documentation
- Keep paragraphs short

### Examples

Examples live in the `examples/` directory:

```rust
//! # Example: Proving Knowledge of a Hash Preimage
//!
//! This example demonstrates how to create a circuit that proves
//! knowledge of a value whose hash equals a known value.
//!
//! ## Running
//!
//! ```bash
//! cargo run --example hash_preimage
//! ```

use zk_arithmos::prelude::*;

fn main() -> Result<(), Box<dyn std::error::Error>> {
    println!("=== Hash Preimage Example ===\n");

    // Step 1: Create the circuit
    println!("Step 1: Creating circuit...");
    let circuit = create_circuit()?;
    println!("Circuit created with {} constraints\n", circuit.num_constraints());

    // Step 2: Generate the witness
    println!("Step 2: Generating witness...");
    let secret_preimage = [1u8; 32];
    let witness = generate_witness(&circuit, &secret_preimage)?;
    println!("Witness generated\n");

    // Step 3: Create the proof
    println!("Step 3: Generating proof...");
    let proof = prove(&circuit, &witness)?;
    println!("Proof generated ({} bytes)\n", proof.size());

    // Step 4: Verify the proof
    println!("Step 4: Verifying proof...");
    let is_valid = verify(&proof)?;
    println!("Proof is valid: {}\n", is_valid);

    println!("=== Example Complete ===");
    Ok(())
}
```

### Changelog

Update `CHANGELOG.md` for user-facing changes:

```markdown
## [Unreleased]

### Added
- New feature description (#PR)

### Changed
- Change description (#PR)

### Fixed
- Bug fix description (#PR)
```

---

## Testing Guidelines

### Test Categories

#### Unit Tests

Test individual functions/methods in isolation:

```rust
#[cfg(test)]
mod tests {
    use super::*;

    #[test]
    fn wire_creation_assigns_unique_ids() {
        let mut circuit = Circuit::new();
        let w1 = circuit.alloc_wire();
        let w2 = circuit.alloc_wire();
        assert_ne!(w1.id(), w2.id());
    }
}
```

#### Integration Tests

Test multiple components together:

```rust
// tests/integration/proof_roundtrip.rs

use zk_arithmos::prelude::*;

#[test]
fn full_proof_roundtrip() {
    // Create circuit
    let circuit = create_test_circuit();

    // Generate keys
    let (pk, vk) = setup(&circuit).unwrap();

    // Create witness
    let witness = create_valid_witness(&circuit);

    // Generate proof
    let proof = prove(&circuit, &witness, &pk).unwrap();

    // Verify proof
    assert!(verify(&proof, &vk).unwrap());
}
```

#### Property Tests

Test properties that should hold for all inputs:

```rust
use proptest::prelude::*;

proptest! {
    #[test]
    fn field_addition_is_commutative(a: u64, b: u64) {
        let fa = F::from(a);
        let fb = F::from(b);
        prop_assert_eq!(fa + fb, fb + fa);
    }

    #[test]
    fn valid_witness_always_verifies(
        inputs in prop::collection::vec(any::<u64>(), 1..10)
    ) {
        let circuit = create_circuit_for_inputs(&inputs);
        let witness = compute_witness(&circuit, &inputs);
        prop_assert!(circuit.is_satisfied(&witness));
    }
}
```

#### Fuzzing Tests

Test robustness against malformed inputs:

```rust
// fuzz/fuzz_targets/parse_circuit.rs

#![no_main]
use libfuzzer_sys::fuzz_target;
use zk_arithmos_dsl::parser::parse;

fuzz_target!(|data: &[u8]| {
    if let Ok(s) = std::str::from_utf8(data) {
        // Parser should never panic, only return errors
        let _ = parse(s);
    }
});
```

### Writing Good Tests

#### Test One Thing

```rust
// Good - Tests one specific behavior
#[test]
fn add_constraint_increments_count() {
    let mut circuit = Circuit::new();
    assert_eq!(circuit.num_constraints(), 0);
    circuit.add_constraint(create_constraint());
    assert_eq!(circuit.num_constraints(), 1);
}

// Avoid - Tests multiple things
#[test]
fn circuit_operations() {
    let mut circuit = Circuit::new();
    let w = circuit.alloc_wire();
    circuit.add_constraint(create_constraint());
    assert_eq!(circuit.num_wires(), 1);
    assert_eq!(circuit.num_constraints(), 1);
    // ... more assertions
}
```

#### Use Descriptive Names

```rust
#[test]
fn verify_rejects_proof_with_wrong_public_inputs() {
    // ...
}

#[test]
fn merkle_proof_verification_succeeds_for_valid_path() {
    // ...
}
```

#### Test Edge Cases

```rust
#[test]
fn empty_circuit_has_no_constraints() { }

#[test]
fn circuit_with_one_constraint_works() { }

#[test]
fn maximum_size_circuit_works() { }

#[test]
fn division_by_zero_returns_error() { }
```

#### Test Error Conditions

```rust
#[test]
fn parse_invalid_syntax_returns_error() {
    let result = parse("invalid {{{{ syntax");
    assert!(matches!(result, Err(ParseError::SyntaxError { .. })));
}

#[test]
fn prove_with_unsatisfied_constraint_returns_error() {
    let circuit = create_circuit();
    let invalid_witness = create_invalid_witness();
    let result = prove(&circuit, &invalid_witness, &pk);
    assert!(matches!(result, Err(ProofError::ConstraintNotSatisfied { .. })));
}
```

### Test Coverage

We aim for high test coverage, but quality over quantity:

```bash
# Generate coverage report
cargo tarpaulin --out Html

# View report
open tarpaulin-report.html
```

#### Coverage Targets

| Type | Target |
|------|--------|
| Core crypto | 95%+ |
| Circuit building | 90%+ |
| DSL compiler | 85%+ |
| CLI | 80%+ |
| Examples | 100% (they should run) |

### Fuzzing

Fuzzing helps find edge cases:

```bash
# Install cargo-fuzz
cargo install cargo-fuzz

# Run fuzzer
cargo fuzz run parse_circuit

# With timeout
cargo fuzz run parse_circuit -- -max_total_time=300
```

#### Fuzz Targets

- Input parsing
- Deserialization
- Mathematical operations
- Proof verification

### Benchmarking

Use Criterion for benchmarks:

```rust
// benches/proving.rs

use criterion::{black_box, criterion_group, criterion_main, Criterion};
use zk_arithmos::prelude::*;

fn bench_prove(c: &mut Criterion) {
    let circuit = create_benchmark_circuit();
    let witness = create_benchmark_witness();
    let (pk, _) = setup(&circuit).unwrap();

    c.bench_function("prove 1000 constraints", |b| {
        b.iter(|| prove(black_box(&circuit), black_box(&witness), black_box(&pk)))
    });
}

criterion_group!(benches, bench_prove);
criterion_main!(benches);
```

Run benchmarks:

```bash
# Run all benchmarks
cargo bench

# Run specific benchmark
cargo bench -- prove

# Compare against baseline
cargo bench -- --save-baseline main
git checkout feature-branch
cargo bench -- --baseline main
```

---

## Cryptographic Contributions

Contributions to cryptographic code require extra care.

### Security Requirements

1. **Understand the cryptography** - Read relevant papers
2. **Follow existing patterns** - Consistency aids review
3. **Document assumptions** - State what must be true for security
4. **Consider side channels** - Think about timing, power, etc.
5. **Get expert review** - Crypto PRs require crypto-knowledgeable reviewers

### Review Process

Cryptographic PRs have additional requirements:

1. **Extended review period** - Minimum 1 week
2. **Multiple reviewers** - At least one with cryptographic expertise
3. **Security analysis** - Document threat model and mitigations
4. **Test vectors** - Include known-answer tests
5. **Reference comparison** - Compare against reference implementations

### Constant-Time Code

Cryptographic code must be constant-time:

```rust
// Use subtle crate for constant-time operations
use subtle::{Choice, ConditionallySelectable, ConstantTimeEq};

// Good - Constant time selection
fn select<T: ConditionallySelectable>(condition: Choice, a: T, b: T) -> T {
    T::conditional_select(&b, &a, condition)
}

// Avoid - Variable time branching on secrets
fn select<T>(condition: bool, a: T, b: T) -> T {
    if condition { a } else { b }
}
```

### Randomness

Use proper randomness sources:

```rust
use rand::{CryptoRng, RngCore};

// Good - Accept any cryptographic RNG
fn generate_random<R: CryptoRng + RngCore>(rng: &mut R) -> [u8; 32] {
    let mut bytes = [0u8; 32];
    rng.fill_bytes(&mut bytes);
    bytes
}

// Avoid - Using non-cryptographic RNG
fn generate_random() -> [u8; 32] {
    use rand::Rng;
    rand::thread_rng().gen()  // May not be crypto-secure
}
```

---

## Architecture Decisions

### ADR Process

Significant changes require an Architecture Decision Record:

```markdown
# ADR-001: Use R1CS as Primary Constraint System

## Status

Accepted

## Context

We need to choose a constraint system format for the core library.

## Decision

We will use R1CS (Rank-1 Constraint System) as the primary format because:

1. Wide support across proof systems
2. Well-understood by the community
3. Sufficient for most use cases

## Consequences

- Simple circuits are efficient
- Some advanced features require conversion
- Compatibility with existing tools
```

### RFC Process

Major features go through an RFC:

1. Open a discussion issue
2. Write RFC document
3. Community discussion period (2 weeks)
4. Core team review
5. Decision and implementation

### Design Discussions

For design questions:

1. Open a Discussion on GitHub
2. Tag appropriate maintainers
3. Participate in community calls
4. Document decisions

---

## Release Process

### Versioning

We follow [Semantic Versioning](https://semver.org/):

- **MAJOR** (1.0.0 → 2.0.0): Breaking changes
- **MINOR** (1.0.0 → 1.1.0): New features, backward compatible
- **PATCH** (1.0.0 → 1.0.1): Bug fixes, backward compatible

### Release Checklist

For maintainers releasing a new version:

- [ ] All tests passing
- [ ] CHANGELOG updated
- [ ] Version bumped in all Cargo.toml
- [ ] Documentation updated
- [ ] Release notes written
- [ ] Security review complete
- [ ] Performance benchmarks acceptable
- [ ] Git tag created and signed
- [ ] Crates published to crates.io
- [ ] GitHub release created
- [ ] Announcement posted

### Backporting

Security fixes are backported to:

- Current major version
- Previous major version (if in support window)

---

## Issue and PR Labels

### Issue Labels

| Label | Description | Color |
|-------|-------------|-------|
| `bug` | Something isn't working | Red |
| `feature` | New feature request | Blue |
| `enhancement` | Improvement to existing feature | Light Blue |
| `documentation` | Documentation improvement | Yellow |
| `good first issue` | Good for newcomers | Green |
| `help wanted` | Extra attention needed | Purple |
| `question` | Further information requested | Magenta |
| `wontfix` | This won't be worked on | White |
| `duplicate` | Duplicate of another issue | Gray |
| `invalid` | Not a valid issue | Gray |

### Priority Labels

| Label | Description |
|-------|-------------|
| `priority: critical` | Must be fixed immediately |
| `priority: high` | Important, fix soon |
| `priority: medium` | Normal priority |
| `priority: low` | Nice to have |

### Area Labels

| Label | Description |
|-------|-------------|
| `area: core` | Core library |
| `area: circuit` | Circuit building |
| `area: witness` | Witness generation |
| `area: proof` | Proof systems |
| `area: dsl` | DSL compiler |
| `area: cli` | Command-line interface |
| `area: docs` | Documentation |

### Status Labels

| Label | Description |
|-------|-------------|
| `status: needs-triage` | Needs maintainer review |
| `status: in-progress` | Being worked on |
| `status: blocked` | Blocked by something |
| `status: needs-info` | Waiting for information |
| `status: ready` | Ready for implementation |

---

## Community

### Communication Channels

| Channel | Purpose | Link |
|---------|---------|------|
| Discord | Real-time chat | [discord.gg/zkarithmos](https://discord.gg/zkarithmos) |
| GitHub Discussions | Long-form discussions | [Discussions](https://github.com/zk-arithmos/zk-arithmos/discussions) |
| Twitter | Announcements | [@zkarithmos](https://twitter.com/zkarithmos) |
| Blog | Articles and updates | [blog.zk-arithmos.dev](https://blog.zk-arithmos.dev) |
| Email | Private inquiries | hello@zk-arithmos.dev |

### Meetings

#### Community Call

- **When**: Every other Thursday, 4pm UTC
- **Where**: Discord #community-call
- **Agenda**: Posted 24 hours before
- **Notes**: Published after

#### Core Team Sync

- **When**: Weekly, internal
- **What**: Development priorities, issues, planning

### Governance

Zk-Arithmos uses a benevolent dictator model with community input:

- **Project Lead**: Final decision maker
- **Core Team**: Regular contributors with commit access
- **Contributors**: Anyone who has contributed
- **Community**: Everyone using or interested in the project

Major decisions go through community discussion.

---

## Recognition

### Contributors File

All contributors are listed in [CONTRIBUTORS.md](CONTRIBUTORS.md):

```markdown
# Contributors

## Core Team

- @maintainer1 - Project Lead
- @maintainer2 - Core Developer

## Contributors

- @contributor1 - Feature X, Bug fixes
- @contributor2 - Documentation
...
```

### Release Credits

Each release credits contributors:

```markdown
## Contributors to this release

- @user1 - #123, #456
- @user2 - #789
- @user3 - Documentation improvements
```

### Swag Program

Active contributors receive:

- **5+ contributions**: Stickers
- **15+ contributions**: T-shirt
- **50+ contributions**: Hoodie
- **Significant contribution**: Special recognition

Contact us at swag@zk-arithmos.dev to claim!

---

## Frequently Asked Questions

### General

**Q: I'm new to Rust. Can I still contribute?**

A: Absolutely! Start with documentation or simple bug fixes. The community is happy to help you learn.

**Q: I'm new to zero-knowledge proofs. Can I still contribute?**

A: Yes! We have documentation tasks, testing improvements, and CLI features that don't require cryptographic expertise.

**Q: How long until my PR gets reviewed?**

A: We aim to provide initial feedback within a week. Complex PRs may take longer.

**Q: My PR has been open for a while. What should I do?**

A: Politely ping reviewers. If there's no response, reach out on Discord.

### Technical

**Q: Which Rust version should I use?**

A: The minimum supported Rust version (MSRV) is specified in Cargo.toml. We recommend the latest stable.

**Q: How do I run only the tests I care about?**

A: Use `cargo test test_name` or `cargo test -p crate_name`.

**Q: How do I debug a failing test?**

A: Use `cargo test -- --nocapture` to see output, or use a debugger with `rust-lldb` or `rust-gdb`.

**Q: Why is CI failing?**

A: Check the GitHub Actions log. Common issues: formatting (`cargo fmt`), lints (`cargo clippy`), or failing tests.

### Process

**Q: Do I need to sign a CLA?**

A: No, we don't require a CLA. Your contribution is licensed under the project's dual MIT/Apache-2.0 license.

**Q: Can I work on multiple issues at once?**

A: Yes, but please don't claim issues you won't have time for. Others may be waiting.

**Q: What if I start an issue but can't finish it?**

A: That's okay! Let us know so we can unassign and someone else can continue.

---

## Resources

### Learning Resources

#### Zero-Knowledge Proofs

- [ZK Whiteboard Sessions](https://zkhack.dev/whiteboard/)
- [zkSNARKs Explainer](https://z.cash/technology/zksnarks/)
- [Vitalik's ZK SNARKs intro](https://vitalik.ca/general/2021/01/26/snarks.html)

#### Rust

- [The Rust Book](https://doc.rust-lang.org/book/)
- [Rust by Example](https://doc.rust-lang.org/rust-by-example/)
- [Rustlings](https://github.com/rust-lang/rustlings)

#### Cryptography

- [A Graduate Course in Applied Cryptography](https://toc.cryptobook.us/)
- [Proofs, Arguments, and Zero-Knowledge](https://people.cs.georgetown.edu/jthaler/ProofsArgsAndZK.html)

### Project Resources

- [API Documentation](https://docs.rs/zk-arithmos)
- [User Guide](https://zk-arithmos.dev/docs)
- [Architecture Docs](./docs/architecture/)
- [Examples](./examples/)

### Tools

- [Rust Analyzer](https://rust-analyzer.github.io/) - IDE support
- [cargo-watch](https://github.com/watchexec/cargo-watch) - Auto-rebuild
- [cargo-audit](https://github.com/RustSec/cargo-audit) - Security audit
- [cargo-tarpaulin](https://github.com/xd009642/tarpaulin) - Code coverage

---

## License

By contributing to Zk-Arithmos, you agree that your contributions will be licensed under the same dual MIT/Apache-2.0 license as the project.

```
This project is licensed under either of

 * Apache License, Version 2.0, ([LICENSE-APACHE](LICENSE-APACHE) or
   http://www.apache.org/licenses/LICENSE-2.0)
 * MIT license ([LICENSE-MIT](LICENSE-MIT) or
   http://opensource.org/licenses/MIT)

at your option.
```

---

<div align="center">

## Thank You! 🙏

**Every contribution makes Zk-Arithmos better.**

**We appreciate your time and effort.**

---

Have questions? Reach out:

[Discord](https://discord.gg/zkarithmos) • 
[Discussions](https://github.com/zk-arithmos/zk-arithmos/discussions) • 
[Email](mailto:hello@zk-arithmos.dev)

---

*Happy contributing!*

</div>
```

---

This comprehensive CONTRIBUTING.md includes:

1. **Welcome & Introduction** - Warm welcome and motivation to contribute
2. **Code of Conduct** - Community standards and expectations
3. **Ways to Contribute** - All types of contributions (code, docs, community)
4. **Getting Started** - Complete development environment setup
5. **Development Workflow** - End-to-end guide from issue to merge
6. **Coding Standards** - Comprehensive style and quality guidelines
7. **Documentation Guidelines** - How to write good documentation
8. **Testing Guidelines** - Testing standards and best practices
9. **Cryptographic Contributions** - Special requirements for crypto code
10. **Architecture Decisions** - ADR and RFC processes
11. **Release Process** - How releases are made
12. **Issue and PR Labels** - Label taxonomy
13. **Community** - Communication channels and governance
14. **Recognition** - How contributors are recognized
15. **FAQ** - Common questions answered
16. **Resources** - Learning and tooling resources
17. **License** - Contribution licensing