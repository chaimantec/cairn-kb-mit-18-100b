# The Bolzano–Weierstrass theorem

**Every bounded sequence of real numbers has a convergent subsequence: the statement as Lecture 6 gives it, and its two uses there, in the proof of the Cauchy convergence theorem and in the proof of the extreme value theorem. Lecture 6 assumes the theorem; its proof, promised for the next lecture, is not yet in this knowledge base.**

Notation: $\mathbf{R}$ is the real numbers, set in bold as in the notes, $\vert x \vert$ is the absolute value of $x$, and a subsequence of $a_n$ is written $a_{n_k}$ (see [subsequences](subsequences.md)). The notes spell the name "Bolzano-Weirstrass", a printed slip for Weierstrass.

## The statement

**Bolzano–Weierstrass theorem** (Lecture 6 notes p. 3; Lecture 6, ≈51:05). Any bounded sequence has a convergent subsequence.

On the board: "So the Bolzano-Weierstrass theorem says that every bounded sequence has a convergent subsequence" (≈51:05). A sequence is bounded when the set of its terms is bounded from above and from below (Lecture 4; see [sequences and limits](sequences-and-limits.md)); Lecture 6 shows it by bounding every $\vert a_n \vert$ by one number. The theorem does not say that the sequence itself converges, only that some subsequence does. Colding makes the point in the proof of the extreme value theorem: "It's a good exercise to see that this sequence in itself-- you can just draw a little picture, and you convince yourself that this sequence in itself may not be convergent" (Lecture 6, ≈1:11:40). Lecture 4's example $(-1)^n$ shows the difference: it is bounded and does not converge (Lecture 4, ≈17:00), but its even-numbered terms form the constant subsequence $1, 1, 1, \cdots$ (Lecture 4, ≈1:04:28–1:06:05; see [subsequences](subsequences.md)).

## Assumed in Lecture 6, proved later

Lecture 6 uses the theorem without proving it. "But we're going to cheat just a little bit, because we are going to deduce it from another theorem that I will prove next time" (≈50:17), and again: "we'll assume this. Again, I'll prove this next time" (≈51:05). The notes: "Once we have the Bolzano-Weirstrass theorem we can prove the Cauchy theorem" (Lecture 6 notes p. 3).

## Use 1: the Cauchy convergence theorem

A Cauchy sequence is bounded, so by the Bolzano–Weierstrass theorem it has a convergent subsequence $a_{n_k} \to a$. Because the terms of a Cauchy sequence bunch together, the whole sequence then converges to $a$: for $n$ large, $\vert a_n - a \vert \leq \vert a_n - a_{n_k} \vert + \vert a_{n_k} - a \vert$, and each piece is less than $\frac{\epsilon}{2}$ (Lecture 6, ≈51:51–58:28; Lecture 6 notes p. 3). "So this is why the Bolzano-Weierstrass theorem implies the Cauchy convergence theorem" (≈58:28). The full proof is on [Cauchy sequences](cauchy-sequences.md#proof-that-a-cauchy-sequence-converges) and the [Lecture 6 page](06-cauchy-convergence-theorem.md).

## Use 2: the extreme value theorem

A continuous function $f$ on $[a, b]$ attains its supremum. Take $x_n \in [a, b]$ with $f(x_n) \to \sup f$. The sequence $x_n$ is bounded because it lies in $[a, b]$, so it has a convergent subsequence $x_{n_k} \to x$, with $x \in [a, b]$, and continuity gives $f(x_{n_k}) \to f(x)$, so $f(x) = \sup f$ (Lecture 6, ≈1:09:56–1:14:44; Lecture 6 notes p. 4). The notes call the extreme value theorem "Another application of the Bolzano-Weirstrass theorem" (p. 3). On the board Colding first calls it an application of the Cauchy convergence theorem (≈58:28), and then corrects the emphasis: "So then I'm using not Cauchy convergence theorem. I'm using the Bolzano-Weierstrass theorem, which implies the Cauchy convergence theorem. But I will use the Bolzano-Weierstrass theorem" (≈1:11:40). See [the extreme value theorem](extreme-value-theorem.md).

## Not yet in this knowledge base

On the OCW lecture list, Lecture 7 is "Bolzano–Weierstrass Theorem; Cauchy Sequences; Series" (TBB Sections 2.11–2.12 and 3.4), where the proof promised in Lecture 6 belongs, and Lecture 14 is "Sequential Compactness; Bolzano–Weierstrass Theorem in a Metric Space". Neither is covered here yet, so this knowledge base does not contain the course's proof of the theorem.

## Lectures

- [Lecture 6 — Cauchy Convergence Theorem](06-cauchy-convergence-theorem.md): the statement, assumed, and its use for the Cauchy convergence theorem and the extreme value theorem.
- [Subsequences](subsequences.md): what a subsequence is, and the theorem that a subsequence of a convergent sequence has the same limit.
