# Third-party notices

## Authored content

Authored repository content is distributed under the MIT license in
`LICENSE-MIT`.

## External works

Books, articles, dictionaries, facsimiles, datasets, and digital repositories
are cited rather than redistributed. Each cited item has an individual record
under `docs/bibliography/sources/` with its identity, repository use, and known
verification boundary.

## External tools and services

AI assistants, editors, browsers, shells, version-control systems, validation
tools, and hosted platforms are generally not distributed by this repository.
Their individual records live under `docs/bibliography/tools/`; standards and
formats live under `docs/bibliography/standards/`; legal identities live under
`docs/bibliography/legal/`.

## Jig compatibility source

`.github/patches/jig-linux.patch` contains and modifies portions of Jig source
from commit `015735e0dafb06b9d9c1016476416ae0f7caabe4`. Jig is copyright Alberto
Villa Osorno and distributed under the MIT License. The patch restores a POSIX
Git hook projection and fixes Linux-conditional imports required to compile and
validate the pinned source on Linux.

The patch is retained as explicit, reviewable source evidence. It must be
removed after an immutable public Jig revision includes the same corrections
and passes the Ameyalli workflow without compatibility changes.

The existence of a record does not imply endorsement, bundled licensing, or
factual authority.
