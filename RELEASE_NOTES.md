# Release Notes

## v1.1.29
GH#1143 — remove 1 `default_from_previous` declaration. K-073 revoked the key, and the consumer wave has since bound every slot that carried it, so the fallback can no longer fire: the declaration was inert.

Measured before deleting rather than after: each of the 41 slots across the catalogue was resolved against **every** invocation, not just its carrier's own workflow, and all 41 were bound by every consumer. Nothing here changes behaviour — the fallback had no path to execution.

Removed: `decision-record-writer.decision_context`.

## v1.1.28
GH#1100 consumer wave (batch 4) — declare the data flow this workflow was resolving positionally.

Each stage below now receives its input through a declared `bindings:` entry instead of `default_from_previous`, which K-073 revoked. **The value is unchanged**: each binding names the step that actually produces what the stage consumes. What changes is that the dependency is stated rather than inferred from position, so a reorder can no longer silently feed a stage the wrong artefact.

Bindings added:
  `extract-action-items` ← `source: from_step "Retrospective Facilitation"` (step 2)

Dependency pins moved to the published versions that declare these slots:
  `action-item-extraction` 1.0.1 → 1.0.2
  `extract-action-items` 1.0.3 → 1.0.4
  `polish-language` 1.0.6 → 1.0.7

## v1.1.27
GH#863 (Wave 1, batch 4) — fix the intent/output mismatch where the promised deliverable was never produced (K-045). The bundle shipped the `decision-record-writer` prompt — the step that writes up the formal, archivable decision records the workflow promises — and the docs said to run it, but the `execution:` block never invoked it, so that deliverable was silently dropped. Added a **Decision Record Writer** step (backed by a new `decision-record-composition` skill so it is `from_step`-addressable) as the terminal synthesis step, ordered `Facilitate Retrospective → Extract Action Items → Record Decision → Decision Record Writer`. Rewired the writer's inputs from positional `{{steps.<Title>.output}}` refs to explicit `from_step` bindings via `context_params` (`retrospective_analysis` ← Facilitate Retrospective, `decision_context` ← Record Decision). Completed the tail: repinned `polish-language` 1.0.1→1.0.6 (the version exposing the bindable `source` slot) and bound `language-polish`'s `source` ← the Decision Record Writer output, so the `output_step` polishes the actual decision record rather than its positional previous. No new required inputs.

## v1.1.26
GH#845 — republish with American English (en-US) content, completing the source-only GH#805 flip that never reached the Hub. Copy only — no functional or behaviour change.

## v1.1.25
GH#745 — declare per-step `output: {name, type}` on every execution step (retrospective/text, decision_record/text, action_items/list, polished_report/text). Lights up the #744 rich flow-map with named, typed outputs. Content-only; no bindings or logic changes.

## v1.1.24
GH#645 Row 3b — migrate to K-037 dep-referenced schema. Strip 6 inline shared-content files and declare 6 hub-shared deps (UUID id + slug name + version + checksum from `gen-dep-checksums.mjs`). Internal slug references rewritten for E2 rename/mirror-drop pair(s): sprint-ceremony-playbook→retro-playbook. Closes pre-Step-3 inline-vendoring for this bundle.

## v1.1.23
Wave 2: re-signed with canonical engine signing pipeline.

## v1.1.22
Tags migrated inline into manifest (GH#586). tags.yaml retired.

## v1.1.21
Bundle re-signed with canonical engine signing pipeline (Wave 2 migration).

## v1.1.20
Signature fix — RELEASE_NOTES.md now included in integrity checksum.

## v1.1.19
Initial catalog release with full structural and content-quality validation. All scanner checks pass.
