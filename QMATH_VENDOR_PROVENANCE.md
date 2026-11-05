# Q-MATH Rayon vendor snapshot provenance

This directory is the canonical Q-MATH-local Rayon/rayon-core source used by the workspace's local-source policy.

- Relocated from `Q-MATH/vendor/rayon` on 2026-09-19 into the shared kernel tooling plane.
- Imported source tree digest (all files except the obsolete nested `.git` pointer): `eb0cd1bf2a9fab876b4524380d845864f915d890988798065084dc76bde33a09`.
- The source bytes were verified byte-identical to the existing local `/home/local/ai/projects/rust/vendor/rayon` checkout at migration time.
- The retained upstream base identity for that checkout was `9254f190aa7ee7521d528e839be3cd0921a04fd8` from `https://github.com/rayon-rs/rayon.git`.
- Q-MATH does not publish changes to the upstream Rayon repository. Local vendor maintenance follows `.agents/skills/local-vendor-maintenance/SKILL.md`.

`Cargo.toml` selects this directory and `rayon-core/` through `[workspace.metadata.qmath.local-sources]`. Do not recreate `Q-MATH/vendor/rayon` or redirect Q-MATH consumers back to that retired path.
