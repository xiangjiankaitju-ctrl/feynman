# Release Notes

This file is the public release history for Feynman. Keep entries user-facing: what changed, why it matters, and anything users should do after upgrading.

GitHub release notes are generated from the matching `## vX.Y.Z` section in this file.

## v0.2.35 - 2026-04-18

### Fixes

- Restored the `/deepresearch` confirmation gate: the workflow now writes `outputs/.plans/<slug>.md`, summarizes the plan, and waits for explicit user approval before searching, drafting, citing, or delivering final artifacts.
- Changed top-level workflow invocation so `feynman deepresearch ...` behaves like the REPL workflow in a real terminal instead of forcing one-shot execution.
- Added a Feynman wrapper around Pi's CLI entrypoint so completed print-mode runs exit cleanly after Pi finishes.
- Tightened direct-mode `/deepresearch` artifact paths so research notes and verification files are written under `outputs/.drafts/`.

### Features

- Added section-focused `alpha_get_paper` extraction with `section` / `sections` filters for abstract, introduction, methodology, experiments, results, discussion, limitations, and conclusion.
- Added configurable `/summarize` context-window controls via flags and `FEYNMAN_SUMMARIZE_*` environment variables.

### Documentation

- Added public `RELEASES.md` and website release notes so each release has visible fix and feature history.
- Updated deep research docs to describe the plan-confirmation workflow and current PDF-safety behavior.

### Validation

- Real installed-global REPL test: typed `/deepresearch what is BM25`, verified that only the plan existed before approval, then replied `yes` and verified final report, provenance, draft, cited draft, research notes, and verification artifacts.
- Full local tests passed: 117/117.
- Typecheck, build, website build, local pack, and local global install checks passed.

## v0.2.34 - 2026-04-18

### Fixes

- Tightened `/deepresearch` so direct-mode research must use at least three distinct search terms or angles before drafting.
- Required direct-mode `/deepresearch` to record the exact search terms in the direct research artifact.
- Added regression coverage for the multi-query deep research contract.

### Validation

- Real RPC smoke test for `/deepresearch what is BM25` completed and wrote the required plan, draft, cited draft, final report, and provenance artifacts.
- Release CI published npm and native bundles for macOS arm64/x64, Linux x64, and Windows x64.

## v0.2.33 - 2026-04-18

### Fixes

- Rewrote `/deepresearch` from a long protocol-style prompt into a shorter execution checklist so local models are less likely to echo instructions instead of doing work.
- Made narrow direct-mode research complete without spawning verifier or reviewer subagents.
- Avoided the crash-prone PDF parser path in `/deepresearch` unless PDF extraction is explicitly requested.

### Validation

- Real RPC `/deepresearch what is BM25` completed with required artifacts and `agent_end`.
- Full local tests, typecheck, build, audits, website build, and pack dry-run passed before release.

## v0.2.32 - 2026-04-18

### Fixes

- Fixed Pi subagent parallel output propagation so top-level task `output` paths are honored.
- Added foreground and async regression coverage for subagent output handoff behavior.
- Hardened deep research prompts around durable artifacts and provenance.

## v0.2.31 - 2026-04-17

### Fixes

- Fixed Feynman runtime auth environment propagation so launched Pi sessions can see the expected model provider credentials.
- Revalidated setup and runtime startup paths after the auth fix.

## v0.2.30 - 2026-04-17

### Fixes

- Fixed Pi subagent task output handling in the runtime patch layer.
- Preserved bundled research-agent file handoffs for multi-agent workflows.

## v0.2.29 - 2026-04-17

### Maintenance

- Updated bundled Pi runtime packages.
- Rebuilt native release artifacts against the refreshed runtime package set.

## v0.2.28 - 2026-04-17

### Maintenance

- Removed runtime hygiene extension bloat and kept the bundled runtime closer to upstream Pi behavior.
- Reduced custom extension surface area to keep the research agent simpler.

## v0.2.27 - 2026-04-17

### Fixes

- Added Pi event guards for workflow state transitions.
- Improved workflow state tracking around long-running research operations.

## v0.2.26 - 2026-04-17

### Fixes

- Switched research context hygiene onto Pi runtime hooks instead of extra custom runtime logic.
- Improved compatibility with upstream Pi runtime behavior.

## v0.2.25 - 2026-04-17

### Fixes

- Fixed workflow continuation and provider setup gaps.
- Improved setup flow behavior for model-provider configuration.

## v0.2.24 - 2026-04-16

### Fixes

- Linked bundled runtime dependencies for core Pi packages.
- Addressed missing dependency errors for installed core packages.

## v0.2.23 - 2026-04-16

### Features

- Added LM Studio setup support for local model workflows.
- Added blocked-research artifact handling so interrupted runs keep useful state.

## v0.2.22 - 2026-04-16

### Features

- Added first-class LM Studio setup.
- Improved local model onboarding defaults.

## v0.2.21 - 2026-04-16

### Fixes

- Fixed extension repair behavior.
- Added the Opus 4.7 model overlay.

## v0.2.20 - 2026-04-16

### Release

- Restored publish workflow behavior after a duplicate npm version blocked release.
- Native bundles remained available through GitHub releases.

## v0.2.19 - 2026-04-16

### Fixes

- Skipped release publication when the npm version already exists.
- Prevented repeat publish attempts from failing the pipeline after npm publication succeeds.

## v0.2.18 - 2026-04-16

### Release

- Prepared the release automation baseline used by the current npm and native-bundle pipeline.
