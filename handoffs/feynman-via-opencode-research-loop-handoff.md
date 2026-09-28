# Feynman-via-opencode research loop — main handoff

**Board card:** `FEYNMAN-001` (feynman repo, `boards/todo/feynman-via-opencode-research-department.md`)
**Task:** execute the Feynman research department **through opencode** via a
platform-agnostic CLI with accessible transcripts/reports, enact the aa-studies
`RSCH` research loop, and **apply it to `Balke`, `MTHR`, and the `GATE-AUX-*`
strategies**.
**Jump in when:** starting any phase below; `FEYNMAN-001` is the canonical tracker.
**Current next action:** Phase 0 — make Feynman invocable from opencode with
readable output (the prerequisite).
**Blocked on:** nothing for Phase 0; later phases gate on the noted items.

---

## Context (why this exists)

Balke's research "hasn't proven fruitful" — a research-process defect, not a
strategy fact. Every redesign attempt (Balke E1–E7, `STRAT-I2..I5`; MTHR R1–R4;
all 12 `GATE-AUX-*`) re-varianted an adjacent premise **without first deriving
why the mechanism should have an edge** and **without consulting external
evidence**. The negatives are scope-limited (aa-studies `BALKE-022` §Q2), not
premise-falsifying. The fix is a research loop that (a) derives from first
principles, then (b) consults external evidence (Feynman), then (c) evaluates
quantitatively — runnable **from opencode**, platform-agnostically.

This handoff merges the intent previously split across
`opencode-modded-rust RESEARCH-006` and `aa-studies INFRA-053` into `FEYNMAN-001`.

---

## Phase 0 — Feynman-via-opencode CLI (prerequisite)

**Where:** feynman repo (`bin/feynman.js`, `package.json`, `skills/`,
`outputs/`, `notes/`, `CHANGELOG.md`).

- **Invocation.** Shell out to the `feynman` binary (`feynman "<prompt>"`),
  pinned to the repo's Node range (`>=20.19.0 <25`). Record exact commands for
  provenance (feynman `AGENTS.md` "Tooling provenance").
- **Accessible output.** The caller reads results from feynman's on-disk
  conventions: `outputs/<slug>.md`, `papers/<slug>.md`, `notes/`, and the
  `.provenance.md` sidecars (`AGENTS.md` "Output conventions" / "Provenance").
- **Platform-agnostic (binding criterion).** The CLI is reachable from **both**
  `ort` (opencode-modded-rust) and vanilla `opencode` — a plain binary in `PATH`,
  not a feature of either product.
- **Done when:** a documented command (plus output-read path) that any opencode
  agent can use to execute Feynman and read the transcription/report back, with a
  recorded disposition (`support`/`refute`/`ambiguous`/`nothing`/`error`).

**Deliverable.** A short invocation + output-access spec in this repo (e.g.
`notes/` or `outputs/.plans/`), verified against one real run.

---

## Phase 1 — Amend `invariants/research-department.md`

**Where:** `opencode-modded-rust/invariants/research-department.md` (line 13).

Model the internal derivation step and the external department as **two sequenced
sub-steps of one loop**, preserving the advisory/never-canonical boundary:

- `project-principles-redesign` (derive from local canonical sources, pre-register)
  → `research-department` (consult external evidence) → evaluation.
- The external consultation is **consultative**: recorded disposition, may sharpen
  or refute, never green-lights, never canonical; `nothing`/`ambiguous` = "no
  external refutation", not confirmation.

**Gate:** operator approval (invariant amendment is a policy change).

---

## Phase 2 — Enact the `RSCH` loop expansion (aa-studies)

**Where:** `aa-studies` via the `campaign-lifecycle-change` skill
(`.opencode/skills/campaign-lifecycle-change/SKILL.md`).

Expand the `RSCH` redesign step into a **derivation-first, two-gate sub-loop**:

```
[RSCH entry] -> project-principles-redesign (derive, TSM) -> research-department
(consult, Feynman) -> premise gate (refute->loop; support/ambiguous/nothing->
advance; error->retry) -> evaluation gate (thin backtest, INFRA-MIN-BACKTEST-002)
-> promising->GAP | needs-redesign->loop | park->time-box
```

**Steps (stage-set change):**
1. **Model** — `docs/results-versioning-standard.md` `RSCH` paragraph.
2. **Propagate** — `docs/strategy-readiness.md`, `docs/v1-readiness-gate.md`,
   `docs/mt-aa-parity-investigation-loop.md`, `docs/promotion-runbook.md`,
   `docs/walkforward-standard.md`, `docs/strategy-development-policy.md`,
   `AGENTS.md`.
3. **Enforcement** — `sequential-iteration-integrity-audit` expected chain +
   compliance rules; check `aa-canonical-readiness`,
   `aa-canonical-handoff-implementation`, `strategy-stage-progression`,
   `strategy-readiness-eval`, `strategy-card-refinement`.
4. One PR per pass (model → propagation → enforcement), forward-only.

**Gate:** operator approval (see `FEYNMAN-001`).

---

## Phase 3 — Vet the derivation step + external-evidence value

**Where:** `opencode-modded-rust`.

- `RESEARCH-005` — vet the internal derivation step (first-principles causal
  derivation) via the A/B protocol in
  `docs/research/RESEARCH-005-internal-research-process-vetting.md`. Gates
  applying the loop to research-stage strategies.
- `RESEARCH-003` — evaluate external-evidence value (Feynman remote vs
  `ort`-only). Decides whether the consultative step is worth its cost.

---

## Phase 4 — Re-point the blocked strategies (aa-studies)

**Where:** `aa-studies/docs/strategy-registry.md` + board cards.

- Update each research-stage row's reopen condition to reference the new `RSCH`
  loop (`Balke`, `MTHR`, and the 12 `GATE-AUX-*`).
- Seed `<AREA>-RSCH-I<n>` cards (`INFRA-051` Pass 4) for each blocked strategy
  (concrete IDs in Phase 5 below).
- **Forward-only** — never touch `done`/`qa`/frozen cards or dated
  `boards/audits/*`.

---

## Phase 5 — Apply to Balke, MTHR, and GATE-AUX

Application order: **Balke → MTHR → GATE-AUX**. Each application seeds its own
`<AREA>-RSCH-I1` card and charges the `PIPE-025` ledger per iteration.

### 5.1 Balke

**Current state:** `blocked` (provisional; pending `RESEARCH-005`) — reclassified
from `park`/B.7 negative (`INFRA-052`).

**Board items — reference (never mutate):**
- `BALKE-022` — retrospective; records the scope-limited negative and "first-principles
  redesign unperformed".
- `BALKE-021` — the **mechanism menu** (untested, documented-not-pursued):
  volatility-expansion momentum ignition, session-close extreme reversion,
  magnitude/extension filter, instrument-universe expansion (non-FX), cross-sectional,
  opening-range/session-structure variants.
- `BALKE-STRAT-I2`, `BALKE-STRAT-I3`, `BALKE-STRAT-I4`, `BALKE-STRAT-I5` — historical
  parked iterations (E5/E6/E7 and the construction change).
- `BALKE-020` — fresh 2026+ corpus (hold, operator-gated; **not** consumed here —
  the first run uses the canonical corpus).
- `BALKE-FP-*` / `BALKE-ATR-*` / `BALKE-QNT-*` — mode-branch chains (Balke area
  exception; reference only).

**Board item — seed:** `BALKE-RSCH-I1` (research/redesign loop, campaign 1).

**Apply:** pick a mechanism from `BALKE-021` (default first: volatility-expansion
momentum ignition, FX-compatible), then:
1. **Derive** — `project-principles-redesign` over `docs/tsm/` (Ch.8/15/16/20/22),
   emit the five-artifact derivation + spec-basis/divergence, pre-registered.
2. **Consult** — Feynman (Phase 0 CLI) against the premise; record disposition.
3. **Premise gate** — `refute` → loop back with the refutation recorded; else advance.
4. **Evaluate** — `strategy-feasibility-conversion` + `shared/min_backtest/` against
   `INFRA-MIN-BACKTEST-002` (corrected T2).
5. **Evaluation gate** — `promising` → `GAP` (Stage 0/parity, `BALKE-016` re-opened
   first); `needs-redesign` → loop; `park` → time-box.

### 5.2 MTHR (MACD Thresholds)

**Current state:** `blocked` (provisional; pending `RESEARCH-005`) — reclassified
from `park`/B.7 negative (`INFRA-052`).

**Board items — reference (never mutate):**
- `MTHR-STRAT-I2`, `MTHR-STRAT-I3`, `MTHR-STRAT-I4`, `MTHR-STRAT-I5` — historical
  rounds R1/R2/R3/R4 (all negative; per-symbol D1 fade family + cross-sectional
  portfolio round exhausted).
- `MTHR-SEL-I2`, `MTHR-GAP-I2`, `MTHR-GAP-I3`, `MTHR-DEV-I2`, `MTHR-DEV-I3` — the
  failed selection/dev passes.
- `MTHR-010` — universe re-evaluation question (holds for the `promising` path).

**Board item — seed:** `MTHR-RSCH-I1` (research/redesign loop, campaign 1).

**Apply:** the incumbent MTHR search was re-variant/trial without a derivation.
Restart with a derivation from `docs/tsm/` (Ch.9 momentum/oscillators, Ch.7/8
moving-average/trend, Ch.20 volatility); then run the same 1–5 loop steps as Balke.
If `promising` → `GAP` and re-answer `MTHR-010` before any universe spend.

### 5.3 GATE-AUX (12 auxiliary strategies)

**Current state:** all 12 `blocked` (provisional; pending `RESEARCH-005`).

**Board items — reference (never mutate):**
- `GATE-AUX` (epic, `done`) — "nothing proposed for `GATE-001` addition", now the
  canonical documented-negative outcome for the aux set.
- Per-strategy cards: `GATE-AUX-ATRO`, `GATE-AUX-DONCH`, `GATE-AUX-ICHI`,
  `GATE-AUX-SMCAND`, `GATE-AUX-NYSB`, `GATE-AUX-ASCT`, `GATE-AUX-TBIP`,
  `GATE-AUX-MACDE`, `GATE-AUX-VWAP`, `GATE-AUX-MANOJ`, `GATE-AUX-TAYL`,
  `GATE-AUX-SATO` — each holds its former `park`/`retired` disposition + reopen
  condition.
- `GATE-AUX-RULESET` — **precondition** for `GATE-AUX-TAYL` (declare a canonical
  Taylor rule set) and `GATE-AUX-SATO` (reconcile the two implementations).

**Board items — seed (one per strategy, campaign 1):**
`GATE-AUX-ATRO-RSCH-I1`, `GATE-AUX-DONCH-RSCH-I1`, `GATE-AUX-ICHI-RSCH-I1`,
`GATE-AUX-SMCAND-RSCH-I1`, `GATE-AUX-NYSB-RSCH-I1`, `GATE-AUX-ASCT-RSCH-I1`,
`GATE-AUX-TBIP-RSCH-I1`, `GATE-AUX-MACDE-RSCH-I1`, `GATE-AUX-VWAP-RSCH-I1`,
`GATE-AUX-MANOJ-RSCH-I1`, `GATE-AUX-TAYL-RSCH-I1`, `GATE-AUX-SATO-RSCH-I1`.

**Apply:** each strategy derives from first principles before any new PoC; the
consultation + two-gate loop applies per strategy. `TAYL` and `SATO` additionally
require `GATE-AUX-RULESET` first (declare/reconcile a canonical rule set) before
their `-RSCH-I1` can derive against a real rule set.

---

## Verification

- Phase 0: a real `feynman "..."` run from both `ort` and vanilla `opencode`,
  output readable back.
- Phase 2: drift greps clean; audit skill's expected chain matches the new loop;
  no historical card mutated.
- Phase 4/5: registry rows + `-RSCH-I1` cards present; `done`/frozen untouched.
- Phase 5: each strategy's derivation + consultation disposition + evaluation
  disposition recorded; no promotion from inside the loop; `PIPE-025` charged.

## Related

- `opencode-modded-rust`: `RESEARCH-005`, `RESEARCH-003`,
  `invariants/research-department.md`
- `aa-studies`: `INFRA-051`, `INFRA-052`, `BALKE-021`, `BALKE-022`, `MTHR-010`,
  `docs/results-versioning-standard.md`, `docs/strategy-registry.md`, `docs/tsm/`,
  `shared/min_backtest/`
