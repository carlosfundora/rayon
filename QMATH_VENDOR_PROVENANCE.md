# Q-MATH Rayon vendor snapshot provenance

This directory is the canonical Q-MATH-local Rayon/rayon-core source used by the workspace's local-source policy.

- Relocated from `Q-MATH/vendor/rayon` on 2026-09-19 into the shared kernel tooling plane.
- Imported source tree digest (all files except the obsolete nested `.git` pointer): `eb0cd1bf2a9fab876b4524380d845864f915d890988798065084dc76bde33a09`.
- The source bytes were verified byte-identical to the existing local `/home/local/ai/projects/rust/vendor/rayon` checkout at migration time.
- The retained upstream base identity for that checkout was `9254f190aa7ee7521d528e839be3cd0921a04fd8` from `https://github.com/rayon-rs/rayon.git`.
- Q-MATH does not publish changes to the upstream Rayon repository. Local vendor maintenance follows `.agents/skills/local-vendor-maintenance/SKILL.md`.

`Cargo.toml` selects this directory and `rayon-core/` through `[workspace.metadata.qmath.local-sources]`.

## Fork (2026-11-05)

- This source is the Carlos-owned fork `https://github.com/carlosfundora/rayon`, branch `qmath`, forked from `rayon-rs/rayon` at `9254f190aa7ee7521d528e839be3cd0921a04fd8`.
- Q-MATH consumes it as the submodule `hardware/rayon`; it is not tracked as Q-MATH source. It replaces `Q-MATH/kernels/tools/rayon` and the shared `rust/vendor/rayon` checkout.
- Branch layout: upstream commit, then one commit importing the exact former Q-MATH tree, then Q-MATH changes. Keep that order so the Q-MATH delta stays one reviewable range.
- Updating: `git fetch upstream`, then `git rebase <new-upstream-commit> qmath` (or merge), qualify Q-MATH consumers, push `qmath` to `origin`, and advance the Q-MATH gitlink. `upstream` (rayon-rs/rayon) is fetch-only; never push to it.
- 2026-11-05: the `btc-mining` compile guard and marker features are removed. Rayon stays an optional kernel dependency: only `runtime_zen2` declares it, as `optional = true`.
