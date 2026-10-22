# Limsup and liminf

**What the course has said about $\limsup$ and $\liminf$ so far. Lecture 5 builds, on the board, two monotone sequences from any bounded sequence: the $\sup$ and the $\inf$ of its tails. Colding says this "is how one defines limsup and liminf", without defining either. The Lecture 8 notes define $\limsup$ as the limit of the $\sup$ of the tails, and use it for the radius of convergence of a power series. Lecture 8 says why it is needed: the ratio and root tests assume a limit that may not exist. $\liminf$ is not yet defined.**

Notation: $a_n$ is a sequence of real numbers. $\sup$ and $\inf$ are the least upper bound and the greatest lower bound (see [supremum and infimum](supremum-and-infimum.md)), and $\lbrace a_n, a_{n+1}, \cdots \rbrace$ is the set of the terms from $a_n$ on, the **tail** of the sequence.

## The construction behind it (Lecture 5, board only)

For a bounded sequence $a_n$, Colding defines on the board

$$b_n = \sup \lbrace a_n, a_{n+1}, \cdots \rbrace , \qquad c_n = \inf \lbrace a_n, a_{n+1}, \cdots \rbrace$$

(Lecture 5, ≈21:51–31:21). Since $b_{n+1}$ and $c_{n+1}$ are taken over a smaller set, the $b_n$ decrease and the $c_n$ increase, and $c_n \leq b_n$. Both are bounded, so both converge by the monotone convergence theorem (Lecture 5, ≈32:08). He then says: "This is how one defines limsup and liminf. We haven't talked about those yet" (Lecture 5, ≈1:07:23–1:08:10). The full construction is on [the monotone convergence theorem](monotone-convergence-theorem.md#two-monotone-sequences-from-any-bounded-sequence).

## Why the tests need it (Lecture 8)

The ratio test and the root test both assume that a limit exists: of $\vert \frac{a_{n+1}}{a_n} \vert$, or of $\vert a_n \vert^{\frac{1}{n}}$. "And I should also emphasize that it is crucial to have a limit" (Lecture 8, ≈44:26). At the end of Lecture 8 Colding says the notes have a little more, $\limsup$ and $\liminf$. "But what if it doesn't have a limit? And so it's dealing with that case" (Lecture 8, ≈1:19:46). The lecture stops there; he says he will start next time with "the stuff I didn't get to" (≈1:19:46). See [convergence tests for series](convergence-tests-for-series.md).

## The definition of $\limsup$ (Lecture 8 notes only)

"To talk about convergence of a general power series we need the notion of lim sup … of a sequence" (Lecture 8 notes p. 6). Let $a_n$ be a sequence.

- If $a_n$ is not bounded from above, $\limsup a_n$ is set to be $\infty$.
- Otherwise define

$$b_n = \sup \lbrace a_n, a_{n+1}, a_{n+2}, \cdots \rbrace .$$

Since the $a_n$ are bounded from above, the $b_n$ are real numbers, and the sequence $b_n$ is decreasing, since

$$b_n = \sup \lbrace a_n, a_{n+1}, a_{n+2}, \cdots \rbrace \geq \sup \lbrace a_{n+1}, a_{n+2}, \cdots \rbrace = b_{n+1}$$

"(For $b_{n+1}$ supremum is taken over a smaller set.)" (notes p. 6). "Since the sequence $b_n$ is decreasing it is converging with limit $b$ that possibly could be $-\infty$ if the sequence $b_n$ is not bounded from below" (notes p. 6). Then

$$\limsup_{n \to \infty} a_n = \lim_{n \to \infty} b_n = b$$

(notes p. 6).

So the notes define $\limsup$ for every sequence, not only bounded ones, and allow the values $\infty$ and $-\infty$. When the $b_n$ are bounded from below, their convergence is the [monotone convergence theorem](monotone-convergence-theorem.md). For the other case the notes do not say what a limit of $-\infty$ means. The notes do not define $\liminf$.

## Its use: the radius of convergence (Lecture 8 notes only)

For a power series $\sum_{n=0}^{\infty} a_n x^n$, the notes set

$$R = \frac{1}{\limsup_{n \to \infty} \vert a_n \vert^{\frac{1}{n}}} ,$$

with $R = \infty$ when the $\limsup$ is $0$ and $R = 0$ when it is $\infty$. "From the root test one can now show" that the series converges for $\vert x \vert \lt R$ and diverges for $\vert x \vert \gt R$ (notes p. 6), without proof. See [power series](power-series.md#from-the-notes-only-the-radius-of-convergence).

## Not yet in this knowledge base

The definition of $\liminf$, any theorem about $\limsup$ or $\liminf$, and the versions of the tests that use them. On the OCW lecture list, Lecture 9 is "Limsup and Liminf; Power Series; Continuous Functions; Exponential Function" (TBB Sections 2.13, 10.2, 5.4 and 5.5), which is not yet in this knowledge base.

## Lectures

- [Lecture 5 — Monotone Convergence Theorem](05-monotone-convergence-theorem.md): the $\sup$ and $\inf$ of the tails of a bounded sequence, on the board.
- [Lecture 8 — Convergence Tests for Series; Power Series](08-convergence-tests-for-series-power-series.md): why the tests need it, and in the notes the definition of $\limsup$ and the radius of convergence.
