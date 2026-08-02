# GitHub Actions integration

## Status

Active with a temporary Jig source-compatibility bridge.

## Purpose

Define the public Linux validation execution path.

## Scope

The tracked validation workflow, immutable Action dependencies, pinned Git
source, pinned Jig source, and the reviewed compatibility patch.

## Current behavior

The workflow checks out Ameyalli and Jig with immutable revisions, verifies and
applies the Linux compatibility patch, builds Git `2.55.0` from a tarball whose
SHA-256 is fixed, builds Jig with Rust `1.97.1`, refreshes the required
`commit-msg` hook, and runs exhaustive validation.

## Invariants

- Every `uses:` reference is an immutable commit SHA.
- Git source is verified before extraction.
- Jig source revision equals the declared upstream revision.
- The patched Jig identity reports `build_dirty=dirty` honestly.
- Integration refresh must not change tracked Ameyalli files.
- The workflow has read-only repository permissions.

## Failure behavior

An unresolved checkout, source-hash mismatch, rejected patch, build failure,
identity mismatch, tracked integration drift, or nonzero Jig result fails the
job.

## Verification

Dispatch the workflow and inspect the emitted `jig.validation` document. Remove
the compatibility bridge only after a new public Jig SHA contains the same
Linux and Action corrections and passes this workflow without the patch.

## References

- `.github/patches/jig-linux.patch`.
- `.github/workflows/jig.yml`.
- `docs/bibliography/tools/github-actions.md`.
- `docs/bibliography/tools/jig.md`.
