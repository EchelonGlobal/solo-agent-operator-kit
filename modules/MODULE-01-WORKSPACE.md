---
type: kit-module
kit: kit-03
module: 1
status: BUILT 2026-09-17
---

# Module 1: Hardened starter workspace

Platform-agnostic markdown templates for a solo agent operator's workspace.
Copied into your workspace folder, filled in once, and read by your agent at
the start of every session. Works with OpenClaw, Claude Code, OpenCode, or any
agent that reads project files.

## Files

| File | Purpose |
|---|---|
| `AGENTS.template.md` | How the agent works in this workspace: conventions, tool quirks, lessons |
| `SOUL.template.md` | The agent's persona and tone |
| `USER.template.md` | Facts about the owner, communication preferences, boundaries |
| `TOOLS.template.md` | Local environment notes: machines, SSH, keys, quirks |
| `MEMORY.template.md` | Long-term memory: durable facts, preferences, commitments |
| `BOOT.template.md` | What the agent reads first, before anything else |
| `secrets-rules.md` | Never-commit-secrets rules + SecretRef naming pattern |
| `.gitignore.template` | Gitignore for a private agent vault repo |

## 15-minute setup

1. Copy the `.template.md` files into your workspace root, dropping `.template` from the name.
2. Copy `.gitignore.template` to `.gitignore` in your vault repo.
3. Fill in the `[FILL IN]` blanks in each file. Do not skip `secrets-rules.md`.
4. Read `secrets-rules.md` and move every existing API key out of files and into
   your secret store (OS keychain, Secure Vault, or environment variables).
5. Point your agent at the workspace files on boot (see `BOOT.template.md`).

## What this module is NOT

- Not a scanner. It does not inspect skills; that is Module 2.
- Not a loop system. Scheduling, ledgers, and approval gates are Modules 3-4.
- Not legal advice. The rules here are operational habits, not counsel.

## AI production disclosure

This kit was produced by an AI agent (AURA) with human review by the kit
author. Some content is derived from the author's own running operator vault.
Nothing in this kit is legal, financial, or compliance advice.
