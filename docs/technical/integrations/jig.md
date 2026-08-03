# Jig integration

## Status

Active through immutable public source.

## Purpose

Define the repository-governance validator used by Ameyalli.

## Scope

Configuration schema 18, local hooks, graph-metadata incubation, and Linux
GitHub Actions.

## Current behavior

Local validation uses the maintained Jig checkout. CI invokes public Jig Action
commit `44b6df689e0f52e30fe62f7c1773d885e232892c`, verifies its build identity,
refreshes Jig-owned integrations, and runs exhaustive validation.

Tracked graph sidecars are stored below `.jig/graph/root/` and
`.jig/graph/tree/`. They retain manually authored repository knowledge but are
observational rather than imperative until Jig activates the next versioned
manual and derived schema.

## Invariants

- Configuration uses schema `18`.
- CI identifies Jig by an immutable source SHA.
- The Action build reports that revision and `build_dirty=clean`.
- `.yml` is the only sidecar suffix; `.yaml` remains ordinary configuration.
- Runtime and dependency roots are outside graph authority.
- Validation fails closed for active rules and emits machine-readable YAML.

## Failure behavior

A source-revision mismatch, identity mismatch, stale integration, incomplete
active evidence, or any active diagnostic fails the gate. Missing or provisional
graph sidecars do not fail while the schema remains in incubation.

## Verification

Run `jig validate --full --root . --max-diagnostics 1000` with Jig commit
`44b6df689e0f52e30fe62f7c1773d885e232892c`. The workflow reproduces the
same public Action path on Linux.

## References

- `.jig/jig.toml`.
- `.jig/taxonomy.json`.
- `.jig/version/jig.toml`.
- `.github/workflows/jig.yml`.
