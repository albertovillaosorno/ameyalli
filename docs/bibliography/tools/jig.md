# Jig

## Status

Active repository record.

## Subject

Repository governance validator used by hooks and GitHub Actions.

## Repository use

Loads `.jig/jig.toml`, owns the configured Git hook projection, collects
repository evidence, and fails closed.

## Provenance

The public source baseline is commit
`015735e0dafb06b9d9c1016476416ae0f7caabe4`. Ameyalli carries a reviewed,
temporary compatibility patch for Linux behavior already corrected in the
local Jig checkout.

## Identity and version

Ameyalli targets Jig `26.3.0`, configuration schema `18`, and the exact public
source revision above. Patched CI builds report that revision with dirty state
instead of claiming release identity.

## License or terms

Jig is MIT-licensed. The compatibility patch contains and modifies Jig source
under those terms; `THIRD-PARTY-NOTICES.md` records this redistribution.

## Evidence

`.jig/jig.toml`, `.githooks/`, the compatibility patch, and the workflow.

## Sources

- `.jig/jig.toml`.
- `.github/patches/jig-linux.patch`.
- `.github/workflows/jig.yml`.
- `THIRD-PARTY-NOTICES.md`.
- `https://github.com/albertovillaosorno/jig`.
