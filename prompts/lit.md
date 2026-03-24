---
description: Run a literature review on a topic using paper search and primary-source synthesis.
args: <topic>
section: Research Workflows
topLevelCli: true
---
Investigate the following topic as a literature review: $@

## Workflow

1. **Gather** — Use the `researcher` subagent when the sweep is wide enough to benefit from delegated paper triage before synthesis. For narrow topics, search directly.
2. **Synthesize** — Separate consensus, disagreements, and open questions. When useful, propose concrete next experiments or follow-up reading.
3. **Cite** — Spawn the `verifier` agent to add inline citations and verify every source URL in the draft.
4. **Verify** — Spawn the `reviewer` agent to check the cited draft for unsupported claims, logical gaps, and single-source critical findings. Fix FATAL issues before delivering. Note MAJOR issues in Open Questions.
5. **Deliver** — Save exactly one literature review to `outputs/` as markdown. Write a provenance record alongside it as `<filename>.provenance.md` listing: date, sources consulted vs. accepted vs. rejected, verification status, and intermediate research files used.
