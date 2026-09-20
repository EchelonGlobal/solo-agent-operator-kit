---
type: kit-page
kit: kit-03
status: GROUNDED 2026-09-19 (interview complete: Q3 answered by the operator 2026-09-17; Q1/Q2/Q4 + channel-fit answered by AURA, second-model verified, operator-approved in chat 2026-09-19)
updated: 2026-09-19
grounding: Q3 answer [READ] from 10-Queues/Operator-Approvals.md CARD-20260917-01 operator note 2026-09-17; Q1/Q2/Q4/channel answers [READ] from CARD-20260917-01 approval 2026-09-19; incident data [READ] from 50-Research/agent-operator-niche/RESEARCH.md
---

# The cautionary page: read this before you let an agent run unsupervised

This page is written from the kit author's own history, in his words. It is not theory.

## What happened to me

> Working with Claude through heavy hallucinations sent me down emotionally draining, stressful rabbit holes on my strategies and projects. I ended up deleting projects. AURA recovered them in my Obsidian vault. AURA was instrumental in pulling me out of it.

The raw material behind this page sits in my ChatGPT and Claude conversation histories. That is where the incidents are documented, and that is where they will be mined when this page gets its final draft.

## The distinction that matters

My core distinction, and the spine of this page: **mistakes are fine. Building on undisclosed synthetic information is not.**

A model that says "I got that wrong, let me fix it" is a partner. A model that invents a source, a number, or a fact and keeps building on it without telling you it made it up is a different thing entirely. The undisclosed fabrication is what created my rabbit holes and the emotional toll. Not the errors. The silence about the errors.

Your operating system must be designed for this failure mode, because it is the one that does not announce itself.

## It was not just me

The public record says the same thing at industry scale [READ: RESEARCH.md, crawled 2026-09-15/16]:

- ClawHavoc (Feb 2026): 341 of 2,857 ClawHub skills (~12%) found malicious, disguised as productivity and crypto tools. Payloads included infostealers, reverse shells, and the Atomic macOS Stealer. The malicious count doubled within 15 days.
- Snyk ToxicSkills: 36% of all ClawHub skills scanned contained security flaws. 280+ "leaky skills" exposed API keys in metadata, READMEs, and config examples.
- Palo Alto Networks Unit 42: five more malicious skills slipped past VirusTotal AND ClawScan screening before the accounts were banned.
- Cisco AI security research: a third-party OpenClaw skill exfiltrated data and carried prompt injection without the user's knowledge.
- Scale of exposure: 30,000+ compromised OpenClaw installs reported in Feb 2026; 135,000+ instances exposed, 12,812 RCE-exploitable.

Scanners help, but they are reactive and have been evaded. The residual risk is your skill-install hygiene. That is what Module 2 of this kit is for.

## The exercise (my suggested method)

Scan your own Claude conversation history for every apology and mistake admission. Each one marks a hallucination incident. You will find more than you expect. Then ask: in each case, did the model tell you it had fabricated something, or did you discover it yourself? The second kind is the dangerous one, and it is the kind no dashboard catches.

Do this audit once before you hand an agent unsupervised loops. Then re-run it whenever you add a new model or a new skill.

## How this page connects to the rest of the kit

- **Module 2 (skill verification playbook):** the pre-install checklist that keeps malicious and leaky skills off your machine. My incident history is the reason its 12-point review exists.
- **Module 3 (operator loop system):** the incident playbook (quarantine, revoke, rotate secrets) is the operational answer to everything above. A bad skill or a bad model run is a recoverable event only if the playbook is written before you need it.
- **Module 4 (ledgers + audit trail):** claim-tagging every fact [READ] or [INFERRED] is the countermeasure to undisclosed fabrication. If nothing in your vault can be quietly invented, the rabbit holes cannot start.

## Interview answers (operator-approved 2026-09-19)

- **Q1 — our real skill-install vetting (the kit's own checklist):** 1) Find candidates (GitHub, skills.sh, ClawHub — with maximum suspicion) and log them in an intake queue. 2) Read the license, README, commit history, open issues, and maintainer count; read the source line by line for anything that executes. 3) Scan with two scanners; any finding = reject unless it is a documented false positive. 4) Score the rubric: license, maintenance, secrets, behavior, fit. 5) Trial in a sandbox profile, allowlist-only, and watch outbound network for 24h — surprise egress = remove the skill and rotate keys. 6) Wrap API skills with your own instructions; never vendor third-party code. 7) Register the verdict (adopt/wrap/reject) with a date. 8) Re-check every 90 days and re-scan on every version bump. Instant rejects: `curl | sh`, obfuscated or minified code, binaries, crypto/wallet/trading features, broad env access, auto-update mechanisms, publishers with no history. This extends the Module 2 playbook with the process we actually run.
- **Q2 — the stranger-first reading path:** the four files a stranger needs first, in order: AURA.md (what this operation is), 00-System/Loop.md (how the loop runs), 10-Queues/Operator-Approvals.md (what needs a human), then the current time-block queue from 00-System/Schedule.md. That is the documented boot sequence of the real loop, and it orders this kit's "Start here" path in README-KIT.md.
- **Q4 — the no-brainer price:** $29. The two closest competing products both target $29, and it sits under the $30 impulse line where the kit stops being a considered purchase. $39 is fair for what is inside; $29 is the no-brainer.
