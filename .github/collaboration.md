# GitHub collaboration surface

GitHub publishes the repository, stores issues and pull requests, and runs the
Jig validation workflow on Linux. The workflow invokes Jig `26.3.0` through
immutable Action commit `44b6df689e0f52e30fe62f7c1773d885e232892c` and
verifies the official Git `2.55.0` source tarball before building it.

Graph metadata is not stored beside provider-controlled files. Tracked `.yml`
sidecars live in the incubation registry under `.jig/graph/`, where `root/`
contains metadata for root artifacts and `tree/` mirrors nested artifact paths.
The sidecars remain optional until Jig's manual and derived schema is accepted.

GitHub does not replace cited primary sources, local Git objects, or Jig's
repository authority.
