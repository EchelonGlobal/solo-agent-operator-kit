---
type: kit-module
kit: kit-03
module: 2
status: BUILT 2026-09-17
---

# Module 2: Skill verification playbook

Third-party skills are code running on your machine. Anthropic's own stated
position is that it is the user's responsibility to only use and execute
trusted skills. ClawHub's screening has been evaded in documented cases
(Unit 42 found 5 malicious skills that slipped past VirusTotal AND ClawScan),
so the residual risk sits with you: skill-install hygiene. This module is the
checklist version of what free scanners automate.

## Files

| File | Purpose |
|---|---|
| `skill-verification-playbook.md` | The 12-point before-install review + trial procedure |
| `red-flags-gallery.md` | Plain-language malicious patterns from documented incidents |
| `rescan-cadence.md` | Monthly re-scan cadence + integrity-hash pinning how-to |
| `registry.template.md` | Your skill registry: one row per skill, with verdict and date |

## How to use it

1. Before installing any skill: run the 12-point review in
   `skill-verification-playbook.md`. Any single red flag = reject.
2. New skills go to a 24-hour quarantine trial first, never straight to
   production.
3. Log every skill in `registry.template.md` with the scan result and date.
4. Re-run `rescan-cadence.md` monthly and on every version bump.

This module works alongside the free scanners (skill-scanner, snyk-agent-scan,
ClawStack Sentinel, tork-scan). The kit is the system; scanners are tools.

## What this module is NOT

- Not a scanner or tool install. It references the free scanners; it does not replace them.
- Not a guarantee. A skill that passes today can be updated tomorrow; that is
  why re-scans exist.
- Not legal advice.

## AI production disclosure

This kit was produced by an AI agent (AURA) with human review by the kit
author. Incident descriptions below are the author's summaries of published
research as of 2026-09-17; original reports are cited. Nothing in this kit is
legal, financial, or compliance advice.
