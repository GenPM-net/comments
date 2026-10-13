# @core/comments

[![genpm](https://api.genpm.net/v1/badge/@core/comments.svg)](https://genpm.net/p/@core/comments) ![license](https://img.shields.io/badge/license-MIT-blue)

> Moderated comments on any entity: guest or user, replies, optional 1–5 ratings, bans, GDPR erasure, safe HTML

A [GenPM](https://genpm.net) module: **source code + AI rules + MCP config**, injected into your project instead of hidden in `node_modules`. The code lands in `src/lib/comments`, pinned to a verified commit, and you own it.

## Install

```bash
genpm add @core/comments
```

No genpm yet? `curl -fsSL https://genpm.net/install.sh | sh` (macOS/Linux), `irm https://genpm.net/install.ps1 | iex` (Windows), or one-off with `npx @genpm-net/cli add @core/comments`.

Or let your AI agent do it: run `genpm mcp setup` once, then ask *"add @core/comments with genpm"* in Claude Code, Cursor, VS Code, Windsurf, Codex or Gemini CLI. It shows you a dry-run plan before writing anything.

## What it does

Comments on anything (`entityType` + `entityId`: posts, products, pages): guests (name + email, stored only as a hash)
or signed-in users, one level of replies, optional 1–5 rating (reused by @core/reviews), moderation queue with email
alerts, bans, GDPR erasure and safe HTML rendering. Anti-spam via @core/antispam. Tables: `comments`, `comment_bans`.

## At a glance

- **GenPM dependencies** (installed with it): [@core/db](https://genpm.net/p/@core/db), [@core/auth](https://genpm.net/p/@core/auth), [@core/antispam](https://genpm.net/p/@core/antispam), [@core/email](https://genpm.net/p/@core/email), [@core/jobs](https://genpm.net/p/@core/jobs), [@core/contracts](https://genpm.net/p/@core/contracts)
- **npm dependencies** (proposed, never installed without asking): `zod`
- **Environment variables** (added to `.env.example`): `COMMENTS_NOTIFY_TO`
- **AI rules**: [`AGENTS.md`](AGENTS.md), loaded by your agent only when it works in `src/lib/comments`

## Security

GenPM installs a 40-character commit SHA (never a branch), verifies an Ed25519-signed manifest, never runs install scripts and scans AI rules for prompt injection. Details: [genpm.net/docs/security](https://genpm.net/docs/security).

## License

MIT — see [LICENSE](LICENSE). Browse the full catalog at [genpm.net](https://genpm.net).
