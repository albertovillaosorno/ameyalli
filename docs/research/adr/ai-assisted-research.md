# Admit AI assistance without admitting AI authority

## Status

Accepted.

## Decision ID

`ADR-RESEARCH-002`

## Context

ChatGPT, Gemini, Claude, Cursor, and Model Context Protocol tools assisted with
research discovery, comparison, drafting, editing, and repository operation.
Their outputs can accelerate work but can also reproduce one another's errors,
invent citations, or obscure uncertainty behind fluent prose.

## Decision

AI output is treated as a lead, draft, or adversarial hypothesis. It is never a
source and cannot independently raise a claim to evidence level A or B. When
multiple assistants are used, their agreement is not counted as independent
evidence unless the underlying sources are independently verified. Accepted
changes remain attributable through Git history and human review.

The initial research used deliberately divergent prompts so that one report
received candidate analyses while another had to derive and falsify them
without seeing the first report. Divergence identified verification work;
convergence only became meaningful after direct source checks.

## Advantages

- Assisted research remains fast without laundering generated text into fact.
- Disagreements become explicit verification targets.
- Git retains the accepted human decision rather than transient model output.

## Disadvantages

- Prompt and model-version provenance is incomplete for early work.
- Repeating a result across assistants does not reduce source-verification cost.
- Some discovery paths cannot be reconstructed exactly.

## Consequences

Every AI tool has an individual non-authoritative bibliography record. Claims
must cite external sources, and unsupported assistant output is removed rather
than preserved as a citation. Future research should record model identity and
prompt intent when that information materially affects reproducibility.

## Rejected alternatives

- Cite AI output as a research source: rejected because it does not preserve a
  stable evidentiary chain.
- Prohibit AI assistance entirely: rejected because discovery and adversarial
  comparison remain useful when source verification is mandatory.
- Treat assistant agreement as replication: rejected because systems may share
  training data, search results, or anchoring assumptions.

## Evidence

- `docs/bibliography/provenance/research-assistance.md`.
- Individual records under `docs/bibliography/tools/`.
- Git history.
