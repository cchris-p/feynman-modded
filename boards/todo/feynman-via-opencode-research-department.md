---
id: "FEYNMAN-001"
title: "Feynman research department via opencode - platform-agnostic CLI + accessible transcripts/reports"
priority: "high"
type: "feature"
area: "RESEARCH"
spec: "handoffs/feynman-via-opencode-research-loop-handoff.md"
status: "todo"
created: "2026-09-28"
---

# Feynman research department via opencode — platform-agnostic CLI + accessible transcripts/reports

## Summary

One canonical item, **merging** `opencode-modded-rust RESEARCH-006` and
`aa-studies INFRA-053` into a single intent tracked here on the **feynman board**.

Make the Feynman **research department** executable **through opencode** — as a
**platform-agnostic CLI** that both **ort** (opencode-modded-rust) and **vanilla
opencode** can invoke — with its **transcriptions/reports accessible** to the
calling session. That CLI is the consultative `research-department` sub-step of
the aa-studies `RSCH` research loop, and the full process is progressed through
to running the loop on `Balke`, `MTHR`, and the `GATE-AUX-*` strategies.

## Why

Balke's research "hasn't proven fruitful" because the redesign process had no
first-principles derivation and no external-evidence vetting (aa-studies
`BALKE-022` §Q2; `INFRA-051`/`INFRA-052`). The fix is to bake a research
department (Feynman) into the research loop as a **consultative** step. Before
that loop can run, the department must be invocable from opencode with auditable
output — and it must not be locked to a single platform.

## Intent (merged)

- **Prerequisite (first deliverable).** Feynman is executed **via opencode**; its
  transcriptions/reports are accessible to the caller.
- **Platform-agnostic.** The invocation surface is a CLI reachable from **both**
  `ort` and vanilla `opencode` — not a feature of either platform. One agnostic
  means of invoking it: a CLI.
- **Consultative only.** The department sharpens or refutes a pre-registered
  premise; it never green-lights and never becomes canonical
  (opencode-modded-rust `invariants/research-department.md`).
- **Progressed to Balke / MTHR / GATE-AUX.** The full runbook is the handoff
  (`spec` above).

## Phases (summary; full runbook in the handoff)

0. **Feynman-via-opencode CLI** + accessible transcripts/reports (this card's
   prerequisite).
1. Amend `invariants/research-department.md` (sequenced sub-steps; advisory
   boundary).
2. Enact the aa-studies `RSCH` loop expansion (`campaign-lifecycle-change`).
3. Vet the derivation step (`RESEARCH-005`) and external-evidence value
   (`RESEARCH-003`).
4. Re-point the blocked strategies (aa-studies `docs/strategy-registry.md` +
   `<AREA>-RSCH-I<n>` cards).
5. Run the loop on `Balke`, then `MTHR`, then `GATE-AUX-*`.

## Supersedes (merged here)

- `opencode-modded-rust RESEARCH-006` — Feynman remote execution + session
  analysis.
- `aa-studies INFRA-053` — RSCH derivation + external-consultation sub-loop.

## Done when

- A platform-agnostic CLI invokes Feynman from both `ort` and vanilla `opencode`,
  with transcriptions/reports accessible to the caller.
- The `RSCH` loop is enacted in aa-studies and the blocked strategies are
  re-pointed at it.
- At least one consultation disposition (`support`/`refute`/`ambiguous`/`nothing`/
  `error`) is recorded and consumed by the loop's premise gate.

## Non-goals

- Vendoring Feynman into either product; making it a runtime dependency.
- Granting external evidence canonical authority.
- Auto-promotion or changing any gate/disposition.
- Committing private aa-studies research outputs, prompts, or secrets.

## Related

- Handoff: `handoffs/feynman-via-opencode-research-loop-handoff.md`
- `opencode-modded-rust`: `RESEARCH-005`, `RESEARCH-003`,
  `invariants/research-department.md`
- `aa-studies`: `INFRA-051`, `INFRA-052`, `BALKE-021`, `BALKE-022`,
  `docs/strategy-registry.md`, `docs/results-versioning-standard.md`

## Notes

- Feynman is the reference harness, not a required one; model is not the variable.
- Keep the human in the loop; findings are advisory.
