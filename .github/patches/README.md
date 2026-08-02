# GitHub compatibility patches

## Purpose

Index temporary, reviewed source transformations required by public workflow
baselines that cannot yet be replaced by an immutable corrected release.

## Contents

- [`jig-linux.patch`](jig-linux.patch) restores the POSIX commit hook and fixes
  Linux-conditional imports in Jig source commit
  `015735e0dafb06b9d9c1016476416ae0f7caabe4`.

## Removal rule

Remove a compatibility patch only after an immutable upstream revision contains
the same corrections and the repository workflow passes without applying it.
