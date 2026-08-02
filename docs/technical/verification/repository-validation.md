# Repository validation

## Status

Active.

## Purpose

Define the reproducible validation entry point for this research repository.

## Scope

The contract covers tracked text, Git evidence, documentation structure,
changelog projection, TODO records, taxonomy, graph compilation, and configured
spelling evidence.

## Current behavior

Jig loads `.jig/jig.toml`, compiles repository evidence, refreshes owned
integrations when explicitly requested, and runs every registered rule in
exhaustive mode.

## Invariants

- No product language is declared.
- The Spanish research corpus remains authored evidence.
- Generated projections never become source authority.
- The required `commit-msg` hook has exact Jig ownership evidence.
- Configuration schema, taxonomy, and sidecars remain mutually consistent.

## Failure behavior

Unknown paths, stale projections, malformed records, incomplete graph evidence,
and failed configured gates produce deterministic nonzero validation.

## Verification

Run:

```text
jig integrations refresh --root .
jig validate --full --root . --max-diagnostics 1000
```

## References

- `.jig/jig.toml`.
- `.jig/taxonomy.json`.
- `.github/workflows/jig.yml`.
