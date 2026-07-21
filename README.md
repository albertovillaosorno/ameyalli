# Ameyalli

A single-paper repository. It holds a philological study of the compound
personal name «Ameyalli Yetlanezi»: where each element comes from, what each
one means on its own, what the pair means together, and when the combination
actually entered use as a person's name.

The paper is [`THESIS.md`](THESIS.md). Everything else in this repository
exists to support it.

## What this is not

**This is not a serious repository, in two specific senses.** It contains no
code — nothing here builds, runs, imports, or does anything at all. And the
paper is not peer-reviewed scholarship: it is a careful weekend study written
as a favour for a friend who asked what her name means, not a publication
that has been through anyone's referees.

Take the strength of its claims from the evidence labels, not from the fact
that it looks like a paper. Every substantive statement carries an **(A)**,
**(B)**, or **(C)** tag for attested, inferred, or speculative, and the
verification that is still outstanding is listed openly in
[`docs/procedencia-de-fuentes.md`](docs/procedencia-de-fuentes.md). Several
citations still need to be checked page by page against facsimile editions.
The structural conclusions are solid; the bibliographic apparatus is a draft
wearing a suit.

The layout, the citation style, and the validation gates are all real, and
the reasoning genuinely tries to be falsifiable. That is a matter of taking
the question seriously, not of claiming authority the work has not earned.

## Why this repository exists

The name circulates widely in central Mexico and in the Mexican diaspora,
but almost everything written about it online comes from baby-name sites,
which reliably assert meanings no morpheme in the name encodes. The
underlying question — is it Nahuatl, and if so which Nahuatl — has a real
answer, reachable through colonial lexicography and historical morphology.
This repository is an attempt to write that answer down once, carefully,
with every claim labelled by the evidence that supports it. It was written
as a favour for a friend and is published under MIT so it can be reused,
corrected, or argued with.

The study reaches a two-part conclusion. Both lexical elements are securely
Nahuatl of colonial central Mexico, and the fused form of the second one is
already recorded as a dictionary entry around 1780; what has no documented
precedent is the pairing of the two as the name of a person, which the
public record only shows from the twenty-first century onward.

## Layout

- [`THESIS.md`](THESIS.md) — the paper, in Spanish.
- [`docs/`](docs) — editorial and methodological annotations.
- `LICENSE` — MIT.

The annotations in `docs/` are not appendices to the paper. They record how
the work was produced and which conventions bind it:

- [`docs/metodologia.md`](docs/metodologia.md) — the source hierarchy and the
  three-tier evidence-labelling protocol used throughout the paper.
- [`docs/procedencia-de-fuentes.md`](docs/procedencia-de-fuentes.md) — where
  the draft material came from, what has been verified, and what has not.
- [`docs/convenciones-editoriales.md`](docs/convenciones-editoriales.md) —
  typography, citation style, paragraph rule, and the privacy constraint on
  naming living individuals.

## Language policy

**The body of this repository is in Spanish on purpose.** This is a
deliberate exception to the English-only source and documentation
conventions otherwise in force across this workspace in 2026. The exception
is not an oversight and should not be «corrected» by a later contributor or
by an automated agent.

The reason is that the object of study is a Spanish-language and
Nahuatl-language artefact, its primary sources are colonial documents in
Spanish and Nahuatl, and its intended readers are Spanish speakers. The
Spanish typographic conventions apply in full inside the paper, including
angular quotation marks. Only this README is written in English, as the
repository's entry point for a general audience.

## Verification status

Structural claims — morpheme segmentation, the impersonal reading of the
verb, the absence of the compound from the colonial record, the
twentieth-century dating — rest on grammatical facts described in the cited
literature. Citations are given in APA 7 without URLs, by editorial choice.
Page-level and folio-level verification against the primary editions is
still outstanding and is tracked in `docs/procedencia-de-fuentes.md`.

Corrections are welcome, particularly from readers with access to
digitised notarial corpora in Nahuatl. The most valuable possible
contribution would be an attestation of either element used as a personal
name before 1900, which would falsify the paper's central historical claim.

## Validation

Markdown is validated with markdownlint against the canonical shared
configuration: 80-column lines including tables and headings, ATX headings,
dash bullets, no inline HTML, no bare URLs. There is no repository-local
lint configuration; adding one would be ignored by the gate anyway.

The `validate.sh` wrapper is operator-local and deliberately untracked,
because it invokes a private orchestrator outside this repository. Readers
cloning this repository do not need it — any standard markdownlint run
against the same rule set reproduces the gate.

## Figure 1

![Rendering of a small yellow cartoon character in denim overalls and
goggles, standing in for a photograph that this study deliberately does not
include](bob_minion.png)

*Figure 1. Placeholder for the referent.* Onomastic studies routinely
illustrate a name with a portrait of someone who bears it. This one does
not, and the substitution is the point: the argument concerns a name, not
any individual who carries it, and every demographic claim in the paper is
deliberately aggregate. A placeholder that is obviously not a person keeps
that methodological commitment visible instead of leaving it implicit.

**Rights notice.** The character depicted is not an original work of this
repository and is not covered by its license. It remains the intellectual
property of its respective rights holders, including Universal Studios and
Illumination Entertainment. No affiliation, endorsement, or claim of
ownership over that character, or over any film or franchise in which it
appears, is asserted here. Use is incidental and non-commercial; the rights
holders may request removal at any time.

## License

MIT, covering the authored text of this repository. See `LICENSE`. The
figure asset `bob_minion.png` is excluded from that grant, as stated in its
rights notice.
