# Preserve Spanish research prose and evidence-first composition

## Status

Accepted.

## Decision ID

`ADR-RESEARCH-001`

## Context

The object of study is a Spanish-language personal name formed from Nahuatl
material and investigated through Spanish and Nahuatl sources. Translating the
study into English would change its audience and complicate quoted forms,
while leaving all repository documentation in Spanish would reduce operational
interoperability. The article also needs stable conventions that distinguish
attested evidence from interpretive prose.

## Decision

`THESIS.md` remains Spanish. Governance, methodology, provenance, bibliography,
integration, and contributor documentation are English. Spanish prose uses
Spanish punctuation and first-level angle quotation marks. Nahuatl forms and
work titles are italicized; morphemes and machine identities use code style.

The study uses APA 7 author-year citations. The formal reference list may omit
URLs when the work is otherwise identifiable, while individual source records
must retain reproducible links when available. Running prose in the study uses
four-sentence paragraphs except where lists, tables, quotations, or source
material make that structure inapplicable. Authored Markdown uses ATX headings,
hyphen bullets, `1.` ordered-list markers, fenced language labels, and an
eighty-column prose limit.

No research argument identifies private people merely because scattered
public records make identification possible. Aggregated demographic evidence
is preferred, and records that may identify minors are excluded.

## Advantages

- The study remains natural for its actual readership and sources.
- Operational documentation remains usable by general repository tooling.
- Evidence and interpretation stay visibly distinct.
- Privacy limits are explicit before data is collected.

## Disadvantages

- Contributors must work across English, Spanish, and Nahuatl conventions.
- The paragraph rule requires manual editorial review.
- Formal references and reproducibility records live in separate surfaces.

## Consequences

Automated agents must not translate `THESIS.md`, normalize Nahuatl forms into
plain Spanish, or treat English-only repository policy as applying to the
study. Source URLs belong in bibliography records rather than being injected
into every formal citation.

## Rejected alternatives

- Translate the full study into English: rejected because it changes the
  intended audience and object-language context.
- Keep every repository document in Spanish: rejected because tooling and
  operational contracts need a shared English surface.
- Remove evidence labels in favor of uniform academic tone: rejected because
  tone cannot encode claim strength.

## Evidence

- `THESIS.md`.
- `docs/research/methodology/evidence-methodology.md`.
- `docs/bibliography/provenance/verification-status.md`.
