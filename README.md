# 15 — Legal

> Part of the **Kojiki Decision System**. This repo is the
> **Legal** line. It references the shared ontology in
> [`00-kojiki-ontology`](https://github.com/robfuj/kojiki-ontology) for the
> canonical schemas, taxonomy, decision-rights, and handoff standards.

## Primary question
> What can we legally do, under what conditions, through which structures, and with what risk?

## Purpose
Determine legal possibility, prohibition, uncertainty, and risk-managing structure.

## Sub-functions
Commercial Law, Contracts, IP, Employment Law, Regulatory Liaison, Disputes

## Typical roles
General Counsel, VP Legal, Legal Director, Senior Counsel, Contract Manager

## Inputs
Business objective, jurisdiction, applicable law, facts, precedent, contracts.

## Outputs
Legal opinions, structures, contracts, approvals, monitoring requirements.

## Learning focus
Recurring interpretations; successful structures; contract risks; negotiation patterns; regulatory changes.

## Operating tree
```text
BUSINESS OBJECTIVE →
    JURISDICTION →
    LEGAL / REGULATORY FRAMEWORK →
    FACT PATTERN →
    CONSTRAINTS →
    INTERPRETATION →
    AVAILABLE STRUCTURES →
    RISK →
    MITIGATION →
    DECISION →
    MONITORING
```

## Decision states
```text
INTAKE → FRAMEWORK-MAPPED → CONSTRAINED → INTERPRETED → STRUCTURED → MITIGATED → APPROVED → MONITORING → ESCALATED
```

## Decision outputs
`Approve · Approve With Conditions · Restructure · Escalate · Reject · Monitor`

## Critical prompts (what this function thinks about)
> What are we trying to accomplish?
> Which jurisdictions matter?
> Which laws apply?
> Which facts determine applicability?
> What is prohibited?
> What is permitted?
> What is uncertain?
> What interpretation are we relying on?
> What alternative structures exist?
> What is the risk of each?
> What controls reduce the risk?
> What evidence would change the legal conclusion?
> What approvals are required?
> What needs ongoing monitoring?
> What regulatory change could invalidate this structure?

## Canonical record schema (docx Learning Ledger + Decision Object Fields)
Every decision in this line is recorded as:
- a **Decision Object** (docx S9) — see `schema/decision-object.json`
- a **Learning Ledger** entry (docx S7) — see `schema/learning-ledger.json`

and the agent must run the **Orientation Protocol** first (see `AGENT.md`).

## How this line runs on SYNAPSIS (the cognitive substrate)
Every decision in this line is decomposed through the shared SYNAPSIS transformation
chain ([`00-kojiki-ontology/synapsis`](https://github.com/robfuj/kojiki-ontology/synapsis)):
```
SOURCE → RECORD → EVIDENCE → INTERPRETATION → STRATEGY → INTERACTION → OUTPUT → OUTCOME → LEARNING
```
- **Three steps are dedicated niche bots**: `bots/evidence/` (this line's extraction
  specialist); the shared `synapsis/audit-bot/` (independent audit, org-wide) and
  `synapsis/learning-bot/` (cross-line memory). See `AGENT.md` for the full contract.
- The rest run inline inside this line's agent, each bounded to one authority.
- Meta-rule: *evidence ≠ interpretation ≠ belief ≠ doctrine.* Validate with
  `python3 synapsis/validate.py <record.json>` (in the ontology repo).

## How to use
1. Read `AGENT.md` — the first-run Orientation Protocol.
2. Read `SCHEMA.md` — how this line maps to the universal schema.
3. Read `data/15-legal.json` — the machine-readable spec.
4. See `data/example.json` — one fully worked decision (Decision Object + Ledger).
5. Use `decision-graph.mmd` — agent-decodable operating tree + state model.
6. Validate new records: `python3 tools/validate.py data/<name>.json`
