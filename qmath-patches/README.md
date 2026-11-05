# Q-MATH patch series

The complete Q-MATH delta of `carlosfundora/rayon` branch `qmath`, as `git format-patch` output from upstream `rayon-rs/rayon` commit `9254f190aa7ee7521d528e839be3cd0921a04fd8`. Use it to move the fork onto a newer upstream.

| Patch | Content |
|---|---|
| `0001-Q-MATH-local-maintenance-on-upstream-9254f19.patch` | Q-MATH local maintenance: toolchain 1.98.1 and edition 2021, correctness and cleanup items, policy headers and docs |
| `0002-Relax-Q-MATH-Rayon-guard-keep-Rayon-an-optional-kern.patch` | Removes the Q-MATH Rayon guard. Rayon stays an optional kernel dependency. |
| `0003-rayon-core-opt-in-batch-stealing-and-steal-groups.patch` | Opt-in `steal_batch_limit` and `steal_groups`, the `RAYON_STEAL_BATCH_LIMIT` and `RAYON_STEAL_GROUPS` fallbacks, and their tests |
| `0004-docs-describe-the-Q-MATH-fork-differences-and-how-to.patch` | The fork README differences table and the reapply procedure |

Generated from `qmath` at `d539e414b762984437f6dc494eb8b19b1ea8c719`. `SHA256SUMS` covers every `.patch` file.

## Verify

```sh
(cd qmath-patches && sha256sum -c SHA256SUMS)
git clone https://github.com/rayon-rs/rayon.git rayon-am && cd rayon-am
git checkout 9254f190aa7ee7521d528e839be3cd0921a04fd8
git am --3way ../qmath-patches/*.patch
git rev-parse HEAD^{tree}   # equals the qmath tree of the generating commit
```

At generation, applying the series to `9254f19` reproduced tree `863b86fbb977a1cf92f0b7a1b91e753f3cb537e7`, identical to `qmath` at `d539e414b762984437f6dc494eb8b19b1ea8c719`.

## Reapply on a newer upstream

```sh
git fetch upstream
git switch -c qmath-next <new-upstream-commit>
git am --3way qmath-patches/*.patch        # resolve conflicts, then: git am --continue
cargo test -p rayon-core && cargo test -p rayon
RAYON_STEAL_BATCH_LIMIT=8 RAYON_STEAL_GROUPS=contiguous:2 cargo test -p rayon-core -p rayon
```

Then requalify the Q-MATH consumers, regenerate this series (see `QMATH_VENDOR_PROVENANCE.md`), push `qmath` to `origin`, and advance the Q-MATH `hardware/rayon` gitlink.
