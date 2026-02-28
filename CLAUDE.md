# CLAUDE.md — AI Assistant Guide for Hello_World

This file provides context for AI assistants (such as Claude) working in this repository.

## Repository Overview

**Hello_World** is a minimal starter repository created by [flairlion](https://github.com/flairlion). It currently contains only a README and this documentation file. There is no application code, build system, or test infrastructure.

- **Owner:** flairlion
- **Purpose:** Template / starter project
- **Initial commit:** November 29, 2016

## Directory Structure

```
Hello_World/
├── README.md      # Project title placeholder
└── CLAUDE.md      # This file — AI assistant guide
```

## Git Workflow

### Branches

| Branch | Purpose |
|--------|---------|
| `master` | Stable, production-equivalent branch |
| `claude/<description>-<session-id>` | AI-generated feature/documentation branches |

### Commit Signing

All commits in this repository are **GPG/SSH signed**. The global git config uses:

```
gpg.format = ssh
commit.gpgsign = true
user.signingkey = /home/claude/.ssh/commit_signing_key.pub
```

Do **not** bypass signing with `--no-gpg-sign` or `--no-verify`.

### Branch Naming Convention for AI Branches

AI assistant branches must follow the pattern:

```
claude/<short-description>-<session-id>
```

Example: `claude/add-claude-documentation-iXn1q`

### Push Workflow

```bash
git push -u origin <branch-name>
```

- Always use `-u` to set upstream tracking.
- Retry on network failure with exponential backoff (2s, 4s, 8s, 16s — up to 4 retries).

## Development Setup

This repository has **no dependencies** and requires no installation steps. To clone and start contributing:

```bash
git clone <repo-url>
cd Hello_World
```

## Adding Code to This Repository

Since this is a blank-slate project, here are conventions to follow when adding source files:

1. **Choose a language** appropriate for the use case and document it in README.md.
2. **Add a build/dependency file** (e.g., `package.json`, `requirements.txt`, `Makefile`) when introducing a language runtime.
3. **Add tests** from the start. Create a `tests/` or `__tests__/` directory and configure a test runner.
4. **Add a `.gitignore`** suited to the language before committing generated files.
5. **Update this CLAUDE.md** to reflect the new structure, build commands, and test commands.

## Key Conventions for AI Assistants

- **Never push to `master` directly** without explicit user permission.
- **Always develop on a `claude/` branch** and open a pull request.
- **Commit messages** should be clear and imperative (e.g., "Add CLAUDE.md with repository documentation").
- **Do not amend published commits** — create new commits instead.
- **Read files before editing them.** Do not suggest changes to code you haven't read.
- **Keep changes minimal and focused.** Avoid refactoring or adding features beyond what is requested.
- **No secrets** (API keys, credentials) should ever be committed.

## Contacts and Resources

- Repository: `http://local_proxy@127.0.0.1:49648/git/flairlion/Hello_World`
- Author: flairlion &lt;flairlion@me.com&gt;
