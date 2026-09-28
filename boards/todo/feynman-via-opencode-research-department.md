---
id: "FEYNMAN-001"
title: "Feynman research department via opencode - platform-agnostic CLI + accessible transcripts/reports"
priority: "high"
type: "feature"
area: "RESEARCH"
spec: "aa-studies/handoffs/feynman-via-opencode-research-loop-handoff.md"
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

- Handoff (aa-studies, where the loop application lives):
  `aa-studies/handoffs/feynman-via-opencode-research-loop-handoff.md`
- `opencode-modded-rust`: `RESEARCH-005`, `RESEARCH-003`,
  `invariants/research-department.md`
- `aa-studies`: `INFRA-051`, `INFRA-052`, `INFRA-053`, `BALKE-021`, `BALKE-022`,
  `docs/strategy-registry.md`, `docs/results-versioning-standard.md`

## Notes

- Feynman is the reference harness, not a required one; model is not the variable.
- Keep the human in the loop; findings are advisory.

## Progress (2026-09-28)

- **Phase 0 DONE.** Feynman runs from opencode as a platform-agnostic CLI.
  Invocation + output-access spec added to `AGENTS.md` ("Tooling provenance" ->
  "Invoking Feynman from opencode"); verified with a real consultative run
  (`--model deepseek/deepseek-flash`) whose answer ended
  `DISPOSITION: ambiguous` (session JSONL under `~/.feynman/sessions/`).
- **Phase 1 DONE.** `opencode-modded-rust/invariants/research-department.md`
  amended: `project-principles-redesign` (derive) and `research-department`
  (consult) are two sequenced sub-steps of one loop; advisory/never-canonical
  boundary preserved.
- **Phase 2 DONE.** aa-studies `RSCH` expanded to the derivation-first two-gate
  sub-loop via `campaign-lifecycle-change` (model -> propagation -> enforcement).
- **Phase 0 extended (2026-09-28).** Remote/headless (no-TUI) execution verified:
  non-TTY parent; one-shot `--prompt`, `--mode json`, and `--mode rpc` all exit 0
  with empty stderr and write a session JSONL (`--mode rpc` via
  `scripts/check-pi-rpc.mjs` -> `pi rpc ok: 77 commands`). See `AGENTS.md`
  "Invoking Feynman from opencode".
- **Phase 3 advanced (2026-09-28).** `opencode-modded-rust` `RESEARCH-005` A/B run
  executed: Arm A (derivation-first) **stronger** than Arm B (incumbent) for a
  scope-correct decision; both arms `park`. Results:
  `opencode-modded-rust/docs/research/RESEARCH-005-ab-run-results.md`. Invariant
  decision drafted (KEEP as amended) and **surfaced for operator approval**;
  `RESEARCH-003` (external-evidence value) remains open.
- **Phases 4–5 wait** on the operator's `RESEARCH-005` approval/unblock; the
  `GATE-AUX-*` application is out of scope on `matrillosub1`.
