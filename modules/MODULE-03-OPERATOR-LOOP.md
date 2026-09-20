---
type: kit-module
kit: kit-03
module: 3
status: BUILT 2026-09-17
grounding: ported from the kit author's running operator vault ([verified]: vault files AURA.md, 00-System/Loop.md, 00-System/Schedule.md as of 2026-09-17); all operator-specific details replaced with [FILL IN] blanks; cautionary-page.md drafted 2026-09-17 (14:48 cycle) from the author's Q3 interview answer + published incident record; Q1/Q2/Q4 interview answers still open and will be folded into that page's pending slots
---

# Module 3: The operator loop system

The scheduling and procedure system that keeps a 24/7 agent safe,
recoverable, and auditable. This is the operating system the kit author's own
vault has run since 2026-09-15. Copy these files next to Module 1's workspace
templates and point your agent at them on boot.

## Files

| File | Purpose |
|---|---|
| `standing-orders.template.md` | What the agent reads first: the cycle, the rules, the exclusions |
| `loop-procedure.template.md` | The priority rule, definition of done, and sprint limits |
| `schedule-blocks.template.md` | The 24-hour block schedule (build, measure, publish, fulfill, review) |
| `cron-starter-set.md` | The five watchdog cron jobs: heartbeat, deadman, metrics-pull, backup, brief |
| `incident-playbook.md` | What to do when a skill goes bad: quarantine, contain, rotate, record |

## How to use it

1. Fill in the `[FILL IN]` blanks in `standing-orders.template.md` first. The
   exclusions and the spend cap are yours to set; the cycle order is not.
2. Adjust `schedule-blocks.template.md` to your hours, but keep the sequence:
   build, then measure, then an operator window, then publish, then fulfill,
   then review. The operator window is the only block where you are expected
   to be awake and answering.
3. Install the five cron jobs from `cron-starter-set.md` with your scheduler.
   The deadman is the most important one: it is the alarm that fires when
   everything else is silent.
4. Read `incident-playbook.md` BEFORE anything breaks. The first incident is
   not the time to design the response.

## Where this came from

Every procedure here is ported from a real operator vault that has run this
system daily since 2026-09-15. The author's scariest real incident is now the
kit's cautionary page (../cautionary-page.md, drafted 2026-09-17 from his Q3
interview answer; Q1/Q2/Q4 slots still interview-pending). Until then, any
numbers in the cron examples are [INFERRED] placeholders, and everything
operator-specific is a blank.

## What this module is NOT

- Not code. The cron entries are templates for your scheduler, not scripts.
- Not enterprise compliance. No SOC2/ISO claims; this is a solo operator's
  hygiene system.
- Not a substitute for Module 2. The loop keeps you organized; the
  verification playbook keeps you safe.
- Not legal advice.

## AI production disclosure

This kit was produced by an AI agent (AURA) with human review by the kit
author. Some content is derived from the author's own running operator vault.
Nothing in this kit is legal, financial, or compliance advice.
