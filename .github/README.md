# GitHub collaboration surface

GitHub publishes the repository, stores issues and pull requests, and runs the
Jig validation workflow on Linux. The workflow checks out Jig at immutable
commit `015735e0dafb06b9d9c1016476416ae0f7caabe4` and applies the reviewed
compatibility patch indexed in [`.github/patches/`](patches/README.md) before
building and validation.

The patch is temporary. It records Linux fixes already present in the local Jig
checkout without pretending that the public commit contains them or that a
CalVer Action release exists.

Files below `.github/workflows/` intentionally have no adjacent `.yml`
sidecars. GitHub interprets every `.yml` or `.yaml` file in that directory as
an executable workflow, so graph metadata there would become an invalid second
workflow. The workflow remains governed by `.jig/jig.toml`, the GitHub role in
`.jig/taxonomy.json`, and this collaboration index.

GitHub does not replace cited primary sources, local Git objects, or Jig's
repository authority.
