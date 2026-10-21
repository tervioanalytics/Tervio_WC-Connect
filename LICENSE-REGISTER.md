# Licence register

Copyright (c) 2026 Tervio Analytics

Register of the licence for the upstream component this repository is built from. `LICENSE` is the licence text. This file does not change upstream copyright notices or licence headers.

## Starktail/woocommerce_fusion

- **Component:** Starktail/woocommerce_fusion
- **Licence:** GNU General Public License, version 3 (GPLv3)
- **Upstream URL:** https://github.com/Starktail/woocommerce_fusion
- **Upstream commit:** `ab71a15d322232fff58d93fa0aa469812bfa9a30`
- **Commit date:** 2026-08-27T22:22:54+02:00 (author date and committer date)
- **Commit subject:** Merge pull request #270 from Starktail/backport/sales-uom-v16
- **Commit URL:** https://github.com/Starktail/woocommerce_fusion/commit/ab71a15d322232fff58d93fa0aa469812bfa9a30

### Source of the licence statement

Read at `ab71a15d322232fff58d93fa0aa469812bfa9a30`. This branch's base (`version-16`) is that commit. This change adds only `LICENSE` and `LICENSE-REGISTER.md`.

`README.md`, lines 19–23:

```
### License

GNU GPL V3

The code is licensed as GNU General Public License (v3) and the copyright is owned by Starktail (Pty) Ltd and Contributors.
```

`woocommerce_fusion/hooks.py`, line 6 (Frappe `app_license` header; the file has no copyright comment above it):

```
app_license = "GNU GPLv3"
```

At that commit the upstream tree contains no `LICENSE`, `LICENCE`, `COPYING`, or `license.txt` file. The verbatim GPLv3 text added in this repository is `LICENSE`, fetched from https://www.gnu.org/licenses/gpl-3.0.txt (SHA-256 `3972dc9744f6499f0f9b2dbf76696f2ae7ad8af9b23dde66d6af86c9dfb36986`).

Upstream `license.txt` was deleted in `183ff1ec20a1025d0791580b0424d6bf475fa7dd` (2026-02-04T20:25:54+00:00, `chore: bring up to Starktail standard`). That commit is an ancestor of `version-16`. `git show --name-status` on it reports `D license.txt` (674 lines removed). The deleted blob (`e72bfddabc15be5718a7cc061ac10e47741d8219`) is the full GNU GPL v3 text and opens:

```
                    GNU GENERAL PUBLIC LICENSE
                       Version 3, 29 June 2007

 Copyright (C) 2007 Free Software Foundation, Inc. <https://fsf.org/>
 Everyone is permitted to copy and distribute verbatim copies
 of this license document, but changing it is not allowed.
```

The line `License: GNU GPLv3` is the original `license.txt`, added by `00a79da16dc6bdec79d9312cb0d12abb12bf5116` (2023-05-18, `feat: Initialize App`). Those bytes were `License: GNU GPLv3` with no trailing newline. `4d639922057691e2fd0b992fad0b79a3a2060d47` (2024-09-01) replaced that line with `License: Dirk van der Laarse`. `5dfff465e0b2636895b6a1d0625b08ed7f1185ae` (2024-11-25, `chore: update licence to GPLv3`) replaced that line with the full GPL text that `183ff1ec20a1025d0791580b0424d6bf475fa7dd` deleted.

Headers that point to `license.txt` are now covered by the top-level `LICENSE`.

### How the upstream commit was determined

1. Added a local git remote `upstream` for https://github.com/Starktail/woocommerce_fusion and fetched its branches. Upstream's HEAD branch is `version-16`. The remote is local git configuration and is not part of this change.
2. `git merge-base HEAD upstream/version-16` returned `ab71a15d322232fff58d93fa0aa469812bfa9a30`.
3. `git rev-parse HEAD`, `origin/version-16`, and `upstream/version-16` are that same hash. `git rev-list --count HEAD ^upstream/version-16` is 0, and the reverse count is 0. `git rev-list HEAD --not --remotes=upstream` is empty, so every commit in this history is already an upstream commit.
4. The histories are identical, so the merge-base is the upstream `version-16` tip. That commit is an ancestor of `HEAD`. No newer commit on any fetched upstream ref is an ancestor of `HEAD`. `upstream/version-15` (`dc0dda3e16a41a8433556c4eede444761b223803`, 2026-09-29) is newer by date and is not an ancestor of `HEAD`.
