# Jig

## Status

Active repository record.

## Subject

Repository governance validator used by hooks and GitHub Actions.

## Repository use

Loads `.jig/jig.toml`, owns the configured Git hook projection, collects
repository evidence, compiles tracked graph metadata for observation, and fails
closed for active repository policy.

## Provenance

The public Action baseline is immutable Jig commit
`44b6df689e0f52e30fe62f7c1773d885e232892c`. Ameyalli invokes that commit
directly; no local compatibility patch is applied.

## Identity and version

Ameyalli targets Jig `26.3.0`, configuration schema `18`, and the exact public
source revision above. The Action verifies that the built validator reports the
same revision with clean source state.

## License or terms

Jig is MIT-licensed. The Action source is fetched from its public repository and
is not redistributed or modified by Ameyalli.

## Evidence

`.jig/jig.toml`, `.jig/version/jig.toml`, `.githooks/`, and the workflow.

## Sources

- `.jig/jig.toml`.
- `.jig/version/jig.toml`.
- `.github/workflows/jig.yml`.
- `https://github.com/albertovillaosorno/jig`.
