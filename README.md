# Riemann Hypothesis in Lean 4

This is a copy of the Lean 4 formalization that Levent Alpöge published with his note, [remark.pdf](https://alpo.ge/remark.pdf).

In the note he says that he found a proof of the Riemann Hypothesis while working with Claude. He says the method also resolves the Generalized Riemann Hypothesis. He and Claude formalized the arguments in Lean, and this repository holds those files.

## Credit

- **Author:** [Levent Alpöge](https://alpo.ge/). The mathematics and the Lean code are his work with Claude. Read his note first: [https://alpo.ge/remark.pdf](https://alpo.ge/remark.pdf)
- **Files:** thanks to [u/Background-Wafer-548](https://www.reddit.com/r/singularity/comments/1y14vi5/comment/19sxbe9yzep51/), who posted the links to the files on r/singularity.

## What is here

- [`src/Statements.lean`](src/Statements.lean) defines the four statements in plain Mathlib terms.
- [`src/Main.lean`](src/Main.lean) states the five final theorems, including `riemannHypothesis`.
- The rest of `src/` holds 175,185 more Lean files, about 1.3 GB in total.
- The project uses Lean `v4.33.1` and the Mathlib revision pinned in [`lakefile.toml`](lakefile.toml).

## Where the files came from

The author published the archive in 14 parts:

```
https://alpo.ge/lean.tar.gz.part01
...
https://alpo.ge/lean.tar.gz.part14
```

We joined the parts into `lean.tar.gz` and extracted it. The files are unchanged. This README is the only file we added.

SHA-256 of the joined `lean.tar.gz`:

```
9631b4f020199e580ba86178cb56c6e9b09f690c2369a80dc4334aa93f49c7fc
```

## Status

We have not built or checked this copy. To check it yourself, install Lean with [elan](https://github.com/leanprover/elan) and run:

```
lake build
```

The build is very large.

## License

The archive has no license file. All rights stay with the author.

---

Shared by [EveryDev.ai](https://www.everydev.ai)
