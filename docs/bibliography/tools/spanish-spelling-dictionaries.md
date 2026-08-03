# Spanish spelling dictionaries

## Status

Pinned and redistributed for repository spelling validation.

## Subject

Spanish and Mexican Spanish word forms used by CSpell.

## Repository use

The tracked `.jig/cspell/spanish.txt` file is generated from the `es_ES` and
`es_MX` Hunspell dictionaries. It validates authored Spanish prose without
building a whitelist from the research corpus.

## Provenance

Both dictionaries come from `LibreOffice/dictionaries` commit
`f2ff99058268502bdcf4cad25c1ca2935ad8aa7d`. CSpell-compatible word expansion
uses `hunspell-reader` version `10.0.1`; the two outputs are combined, sorted,
and deduplicated. The generated file contains 670,757 forms and has SHA-256
`703401d2433a3c850e99ad615e5a6697ea3701ec08e696dcac94edf96f24be91`.

## Identity and version

- Upstream repository: `LibreOffice/dictionaries`.
- Upstream commit: `f2ff99058268502bdcf4cad25c1ca2935ad8aa7d`.
- Locales: `es_ES` and `es_MX`.
- Expansion tool: `hunspell-reader` `10.0.1`.

## License or terms

The upstream dictionaries permit use under GPL-3.0-or-later,
LGPL-3.0-or-later, or MPL-1.1-or-later. This repository redistributes the
combined word list under LGPL-3.0-or-later. The license text is retained at
`.jig/cspell/LICENSE-spanish-LGPL-3.0.txt`.

## Evidence

- `.jig/cspell/spanish.txt`.
- `.jig/cspell/LICENSE-spanish-LGPL-3.0.txt`.
- `.jig/cspell/cspell.json`.
- `.jig/jig.toml`.

## Sources

<!-- jig-ignore-next-line: immutable source URL is indivisible -->
- https://github.com/LibreOffice/dictionaries/tree/f2ff99058268502bdcf4cad25c1ca2935ad8aa7d/es
- https://www.npmjs.com/package/hunspell-reader/v/10.0.1
