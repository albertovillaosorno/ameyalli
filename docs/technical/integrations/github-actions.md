# GitHub Actions integration

## Status

Active through an immutable public Jig Action.

## Purpose

Define the public Linux validation execution path.

## Scope

The tracked validation workflow, immutable checkout and Action dependencies,
and the verified Git source archive required by Ameyalli's tool authority.

## Current behavior

The workflow checks out Ameyalli, invokes Jig commit
`44b6df689e0f52e30fe62f7c1773d885e232892c`, builds configured Git `2.55.0`
from its official source tarball after SHA-256 verification, builds Jig with
Rust `1.97.1`, refreshes Jig-owned integrations, and runs exhaustive validation.

## Invariants

- Every `uses:` reference is an immutable commit SHA.
- Git source is verified before extraction.
- Built Jig identity equals the Action commit and reports clean source state.
- Integration refresh must not change tracked or unignored Ameyalli files.
- Provider-controlled workflow directories contain no graph sidecars.
- The workflow has read-only repository permissions.

## Failure behavior

An unresolved checkout, source-hash mismatch, tool build failure, identity
mismatch, integration drift, or nonzero Jig result fails the job.

## Verification

Run the workflow on Linux and inspect the emitted `jig.validation` document. A
successful run must report `status: clean`, exhaustive collection, and zero
diagnostics.

## References

- `.github/workflows/jig.yml`.
- `docs/bibliography/tools/github-actions.md`.
- `docs/bibliography/tools/jig.md`.
