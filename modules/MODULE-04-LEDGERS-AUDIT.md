---
type: kit-module
kit: kit-03
module: 4
status: BUILT 2026-09-17
grounding: ported from the kit author's running operator vault ([verified]: vault files 30-Ledgers/Hours.md, 60-Daily/_template.md, 10-Queues/Operator-Approvals.md as of 2026-09-17); all operator-specific details replaced with [FILL IN] blanks
---

# Module 4: Ledgers + audit trail templates

The paper trail that makes a solo operator auditable: where every hour went,
what happened each day, and which irreversible actions are waiting on the
human's word. Ported from the author's own vault ledgers.

## Files

| File | Purpose |
|---|---|
| `hours-ledger.template.md` | Every work session, one line: date, block, category, hours, item, notes |
| `daily-log.template.md` | One page per day: facts, money, experiments, incidents, approval cards |
| `approval-cards.template.md` | The gate for irreversible actions: money, publish, deletion, policy |

## How to use it

1. The hours ledger gets a line for EVERY session, including the short ones.
   If `idle` is not zero, the daily log explains why.
2. The daily log is closed in the review block, every night, before sleep.
   Facts carry [verified] (seen in a file, page, or API result this session)
   or [inferred]. Never overturn a written record on inference.
3. Approval cards are the only way irreversible actions happen. The agent
   writes the card; the human flips `status:` to APPROVED or DENIED. No card,
   no action.

## Why this matters

When something goes wrong (see Module 3's incident playbook), the audit
trail is how you reconstruct what the agent did, when, and why. It is also
how you prove to a partner, a platform, or yourself that the operation is
real. The author's rule: an empty log is a bug, not a quiet day.

## What this module is NOT

- Not accounting software. Track money in your money tool; these ledgers
  track time and decisions.
- Not tax advice. Keep receipts; ask an accountant.
- Not a permission system. The approval cards are a convention between you
  and your agent, not a technical lock.

## AI production disclosure

This kit was produced by an AI agent (AURA) with human review by the kit
author. Some content is derived from the author's own running operator vault.
Nothing in this kit is legal, financial, or compliance advice.
