# repo-scout

Instant overview of any project. Clone a repo, run `repo-scout`, know what you're dealing with.

```
$ repo-scout ~/express

=== express ===

Type: Node.js, JavaScript, Express
Size: 213 files, 26056 lines
Entry: index.js

Commands:
  Lint: npm run lint
  Test: npm test

Dependencies:
  Prod (28): accepts, body-parser, content-disposition, cookie, debug...
  Dev (16): after, connect-redis, cookie-parser, eslint...

Structure:
  examples/              80 files  (examples)
  lib/                    6 files  (source code)
  test/                 112 files  (tests)

Key files:
  package.json
  LICENSE
  .github/workflows/ci.yml
  .gitignore

Git:
  Branch: master
  Commits: 5821 (last: 2 days ago)
  Contributors: 364
  CI: GitHub Actions

---
Scanned express in /home/user/express
```

## Install

```bash
curl -o repo-scout https://raw.githubusercontent.com/aurora2026ai/repo-scout/main/repo-scout
chmod +x repo-scout
sudo mv repo-scout /usr/local/bin/  # or anywhere on your PATH
```

## Usage

```bash
repo-scout              # Current directory
repo-scout ~/project    # Specific path
repo-scout .            # Explicit current directory
```

## What it detects

**Project type** — Node.js, Python, Rust, Go, Ruby, Java/Kotlin, PHP, Elixir, C/C++, Swift, Dart/Flutter, Deno. Plus frameworks: React, Next.js, Vue, Svelte, Angular, Express, Django, Flask, FastAPI, PyTorch, TensorFlow.

**Build commands** — Reads package.json scripts, Cargo.toml, go.mod, Makefile targets, pyproject.toml, Dockerfile. Detects package manager (npm/yarn/pnpm/bun).

**Dependencies** — Lists production and dev dependencies from package.json, requirements.txt, Cargo.toml, go.mod.

**Entry points** — Finds main files (index.ts, main.py, src/main.rs, etc.) and package.json `main` field.

**Directory structure** — Top-level directories with file counts and purpose labels (source code, tests, docs, config, etc.).

**Key files** — Config files, CI workflows, documentation, editor configs.

**Git info** — Branch, commit count, last commit, contributor count, CI system.

## Why

When you open a new project — a dependency, a colleague's repo, an open source tool — the first minutes are spent figuring out: What is this? How is it built? What does it depend on? Where's the code?

`repo-scout` answers all of that in under a second. No AI, no network, no config. Just bash and git.

## Requirements

- Bash 4+
- Git (optional, for git info)
- Python 3 (optional, for parsing JSON manifests)

## License

MIT
