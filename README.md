> [!NOTE]
> **This skill lives in the main collection: [milad-ahmd/agent-skills](https://github.com/milad-ahmd/agent-skills/tree/main/skills/github-portfolio)**. Please ⭐ star it there; that's where updates land first.
> Docs: **https://milad-ahmd.github.io/agent-skills/skills/github-portfolio/** · Claude Code: `/plugin install all-skills --marketplace milad-ahmd/agent-skills`

<div align="center">

# 🌐 github-portfolio

**One-page portfolio site from your real GitHub repos, honest project write-ups, ready for GitHub Pages. An Agent Skill for Claude Code, Cline, Cursor, Codex and other AI coding agents.**

[![License: MIT](https://img.shields.io/github/license/milad-ahmd/github-portfolio)](LICENSE)
[![Stars](https://img.shields.io/github/stars/milad-ahmd/github-portfolio?style=social)](https://github.com/milad-ahmd/github-portfolio)
![Category](https://img.shields.io/badge/category-Growth-blue)
![Works with](https://img.shields.io/badge/works%20with-Claude%20Code%20%7C%20Cline%20%7C%20Cursor%20%7C%20Codex-8A2BE2)

[Install](#-install) · [Usage](#-usage) · [How it works](skills/github-portfolio/SKILL.md) · [All skills](https://github.com/milad-ahmd/agent-skills)

</div>

> Part of **[agent-skills](https://github.com/milad-ahmd/agent-skills)**, a growing collection of practical skills for AI coding agents.

## 📦 Install

**One command (installs the whole collection):**

```bash
curl -fsSL https://raw.githubusercontent.com/milad-ahmd/agent-skills/main/install.sh | bash -s -- github-portfolio
```

**Manually (Claude Code):**

```bash
git clone https://github.com/milad-ahmd/github-portfolio /tmp/github-portfolio
mkdir -p ~/.claude/skills && cp -r /tmp/github-portfolio/skills/github-portfolio ~/.claude/skills/
```

**Per project:** copy `skills/github-portfolio` into `<project>/.claude/skills/`.
**Any other agent:** paste [`SKILL.md`](skills/github-portfolio/SKILL.md) into your rules or system prompt.

## 💬 Usage

Just ask your agent:

```text
Make me a portfolio site from my GitHub
Build a github.io page I can link on my CV
```

The full workflow, rules and output format are in [`SKILL.md`](skills/github-portfolio/SKILL.md).

## 🔎 Sample output

`portfolio.py` is plain Python 3 with no dependencies and stays inside GitHub's unauthenticated rate limit. Real output for the made-up user that ships with it:

```text
$ python3 portfolio.py --user ada-dev --out site

Portfolio for ada-dev written to site/index.html
  * queue-lite                    412 stars  Durable job queue on Postgres with SKIP LOCKED
  * pg-migrate                     88 stars  Zero-downtime schema migrations for Postgres
  * ratelimit                      15 stars  Token-bucket rate limiter as HTTP middleware
  * kafka-tools                    40 stars  CLI for inspecting Kafka consumer lag
  * old-blog                      120 stars  My first blog engine
…
```

It writes `site/index.html` (no JavaScript, light and dark themes, every repo description escaped) and `site/data.json`; edit the wording there and re-run with `--overrides site/data.json` to keep it. `--publish-instructions` prints the git commands for USERNAME.github.io and never pushes for you.

## 🧩 More skills

See the full collection: **[milad-ahmd/agent-skills](https://github.com/milad-ahmd/agent-skills)**.

## 🤝 Contributing

This repo is a read-only mirror. Please open issues and PRs in **[milad-ahmd/agent-skills](https://github.com/milad-ahmd/agent-skills)**.

## 📄 License

[MIT](LICENSE) © Milad Ahmadi

<div align="center">

**If this skill saved you time, a ⭐ helps others find it.**

</div>
