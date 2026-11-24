# Riemann Hypothesis in Lean 4

This is a copy of the Lean 4 formalization that Levent Alpöge published with his note, [remark.pdf](https://alpo.ge/remark.pdf).

In the note he says that he found a proof of the Riemann Hypothesis while working with Claude. He says the method also resolves the Generalized Riemann Hypothesis. He and Claude formalized the arguments in Lean, and this repository holds those files.

## What this is, in plain words

### The problem

Prime numbers are numbers like 2, 3, 5 and 7. Each one divides evenly only by 1 and by its own value. Every other whole number is made by multiplying primes together. That makes primes the building blocks of all numbers.

Primes look scattered along the number line. Nobody has a simple rule that tells you where the next one will show up.

The Riemann Hypothesis is a guess about how primes are spread out. It was made more than 150 years ago. It says the primes follow their pattern as closely as they possibly can. If the guess is true, we can count how many primes sit below any number with the smallest possible error.

The exact statement is about a formula called the Riemann zeta function. The formula gives zero at certain special inputs. The hypothesis says all the interesting ones sit on a single straight line.

### Why it's a big deal

- **It's old and unsolved.** Mathematicians have worked on it for over 150 years.
- **A lot depends on it.** Many results in mathematics start with the words "if the Riemann Hypothesis is true".
- **It has a prize.** The Clay Mathematics Institute lists it as one of its [Millennium Prize Problems](https://www.claymath.org/millennium/riemann-hypothesis/) with a one million dollar award.
- **An AI helped.** The note says a mathematician and an AI model found the proof together.

### What the note says

Levent Alpöge is a mathematician who works at Anthropic, the company that makes Claude. His four-page note says this:

1. He believes he and Claude found a proof of the Riemann Hypothesis.
2. He says the same method proves a wider version called the Generalized Riemann Hypothesis. He expects it to reach a third version, the Extended Riemann Hypothesis, with more time.
3. He had planned since his student days to spend decades on this problem. He chose the direction and brought two ideas together. He writes that Claude then moved faster than he could follow near the end.
4. The work went quickly. His timeline lists 20 steps between October 6 and November 16, 2026.
5. The argument is very long. A written-out version passed 250,000 pages, so he published only the Lean files.

He is open about the gaps. He says he hasn't yet mastered every part of the argument. He expects much shorter proofs to follow, and he plans to write a proper explanation.

### What Lean is

A proof is a chain of steps. Each step has to follow from the ones before it. A person can miss a mistake in a long chain.

Lean is a program that checks a proof one step at a time. It accepts a step only when the step follows the rules of logic. The note says the arguments were written in Lean "without assumptions". In plain words, no step is taken on trust.

That changes how a claim like this gets tested. People only need to read the short file of statements in [`src/Statements.lean`](src/Statements.lean) and agree it says the right thing. The computer checks the other 175,000 files.

### What still has to happen

We haven't run that check on this copy. A claim this big needs other mathematicians to build the files and read the statements. Treat it as a claim until they have.

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
