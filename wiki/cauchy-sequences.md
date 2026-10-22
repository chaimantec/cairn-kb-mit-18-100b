# Cauchy sequences

**The definition of a Cauchy sequence, how it differs from convergence, and the theorem, stated in Lecture 5 and promised for the next lecture, that a sequence of real numbers is convergent if and only if it is Cauchy. The proof is not yet in this knowledge base.**

Notation: $\mathbf{N}$ and $\mathbf{R}$ are the natural and the real numbers, set in bold as in the notes, and $\vert x \vert$ is the absolute value of $x$.

## Why the course needs them

Colding's motivation (Lecture 5, ≈1:08:10–1:08:56): for a monotone sequence you can write the limit down explicitly, as the $\sup$ or the $\inf$ of the terms, and in all the examples so far it was easy to write down the limits. "But in general, you might not be able to write down the limit, but you want to prove that the limit exists" (≈1:08:56). A Cauchy sequence is defined by a condition on its terms alone, with no candidate limit in it. See [the monotone convergence theorem](monotone-convergence-theorem.md).

## Definition

**Definition** (Lecture 5 notes p. 6; Lecture 5, ≈1:08:56–1:09:45). A sequence $a_n$ is a **Cauchy sequence** if for all $\epsilon \gt 0$ there exists an $N$ such that if $m, n \geq N$, then

$$\vert a_n - a_m \vert \lt \epsilon .$$

On the board the condition is stated for $n$ and $m$ bigger than $N$ (≈1:09:45). Compare the definition of convergence to $a$, which asks for $\vert a_n - a \vert \lt \epsilon$ for $n \geq N$ (see [sequences and limits](sequences-and-limits.md)).

## How it differs from convergence

"This is a different notion than convergence" (≈1:09:45). Convergence says that everything far out in the sequence "accumulates around the limit"; the Cauchy condition says that if you are far out, "things bunch together, basically" (≈1:10:32). The notes put it as "(Tail of the sequence bunch together.)" (Lecture 5 notes p. 6).

## The theorem

**Theorem** (Lecture 5 notes p. 6; Lecture 5, ≈1:10:32–1:12:08). A sequence of real numbers is convergent if and only if it is a Cauchy sequence.

Lecture 5 states it without proof. "For now, everything is in R at the moment", and "I won't prove this now, but I'll prove this next time" (≈1:11:21). Colding says the proof will use the construction from earlier in the lecture, the two monotone sequences formed from a bounded sequence by taking the $\sup$ and the $\inf$ of its tails (≈32:54, ≈1:11:21–1:12:08); that construction is on [the monotone convergence theorem](monotone-convergence-theorem.md#two-monotone-sequences-from-any-bounded-sequence).

## From the notes: Cauchy

The Lecture 5 notes quote a short biography "From Wikipedia": Baron Augustin-Louis Cauchy (1789–1857) was a French mathematician, engineer and physicist, one of the first to state and prove the key theorems of calculus rigorously, "thereby creating real analysis" (Lecture 5 notes p. 6). The lecture does not mention it.

## Not yet in this knowledge base

On the OCW lecture list, Lecture 6 is "Cauchy Convergence Theorem" (TBB Section 2.12) and Lecture 7 is "Bolzano–Weierstrass Theorem; Cauchy Sequences; Series" (TBB Sections 2.11–2.12 and 3.4). Neither is covered here yet, so this knowledge base does not contain the course's proof of the theorem above.

## Lectures

- [Lecture 5 — Monotone Convergence Theorem](05-monotone-convergence-theorem.md): the definition and the statement of the theorem.
