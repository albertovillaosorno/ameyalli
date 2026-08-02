# Jig integration

## Status

Active with a temporary, reviewed Linux compatibility bridge.

## Purpose

Define the repository-governance validator used by Ameyalli.

## Scope

Configuration schema 18, local hooks, and Linux GitHub Actions.

## Current behavior

Local validation uses the updated Jig checkout. CI checks out public Jig source
at commit `015735e0dafb06b9d9c1016476416ae0f7caabe4`, applies the tracked
compatibility patch, builds it with Rust `1.97.1`, refreshes Jig-owned
integrations, and runs exhaustive validation.

## Invariants

- Configuration uses schema `18`.
- CI identifies upstream Jig by an immutable source SHA.
- The compatibility patch must apply without context inference.
- The patched build reports the upstream revision and `build_dirty=dirty`.
- Validation fails closed and emits machine-readable YAML.

## Failure behavior

A source-revision mismatch, rejected patch, identity mismatch, stale
integration, incomplete evidence, or any diagnostic fails the gate.

## Verification

Run `jig validate --full --root . --max-diagnostics 1000` with the updated
local Jig checkout. The workflow reproduces the public-source bridge on Linux.

## References

- `.jig/jig.toml`.
- `.github/patches/jig-linux.patch`.
- `.github/workflows/jig.yml`.
