# Subsequences

**What a subsequence is, by example and by the formal definition (composition with a strictly increasing map $g : \mathbf{N} \to \mathbf{N}$), what is not a subsequence, and the theorem that a sequence converges to $a$ exactly when all its subsequences do. From Lecture 4, reviewed in Lecture 5; the Bolzano–Weierstrass theorem (Lecture 7) is not yet in this knowledge base.**

Notation: $\mathbf{N} = \lbrace 1, 2, 3, \cdots \rbrace$ and $\mathbf{R}$, set in bold as in the notes. A sequence $a_n$ is a function $f : \mathbf{N} \to \mathbf{R}$ with $a_n = f(n)$; see [sequences and limits](sequences-and-limits.md).

## The idea, by example

A subsequence keeps infinitely many of the terms of a sequence, in their original order. Colding gives examples before the definition, and indexes the subsequence by $k$ so as not to confuse it with the $n$ of the original sequence (Lecture 4, ≈1:03:38–1:04:28).

**From $a_n = (-1)^n$** (Lecture 4 notes p. 5, Example 1; Lecture 4, ≈1:04:28–1:06:05). The terms alternate $-1, 1, -1, 1, \cdots$.

- The even-numbered terms give the constant subsequence $1, 1, 1, \cdots$.
- The odd-numbered terms give the constant subsequence $-1, -1, -1, \cdots$.
- The notes add $(-1)^{n+1}$, and $1, 1, -1, -1, 1, 1, -1, -1, \cdots$. On the board the more elaborate example takes the first two odd-numbered terms, then the next two even-numbered ones, and so on, starting $-1, -1$.

**From $a_n = n$** (notes p. 5, Example 2; ≈1:06:53). The odd numbers $1, 3, 5, 7, 9, \cdots$ and the even numbers $2, 4, 6, 8, 10, \cdots$ are both subsequences.

**Not subsequences** (notes p. 5; ≈1:07:40–1:08:28).

- $1, 1, 2, 2, 3, 3, 4, 4, 5, 5 \cdots$ is "NOT" a subsequence of $a_n = n$ (notes p. 5): it takes the same term several times, though the value appears only once in the original (≈1:07:40).
- $3, 2, 4, 5, \cdots$ is not a subsequence either, "because things are taken out of order" (≈1:08:28; board only).

## The definition

**Definition** (Lecture 4 notes p. 5; ≈1:08:28–1:11:01). Let $a_n = f(n)$ be a sequence. A **subsequence** of $a_n$ is the composition $f \circ g$, where $g : \mathbf{N} \to \mathbf{N}$ is a **strictly increasing** function. On the board it is written $b_k = f(g(k))$, in the notes $b_n = f(g(n))$. A subsequence of $a_n$ is also denoted $a_{n_k}$, where $n_k$ is the value of $g$ at $k$ (≈1:11:01, ≈1:15:51).

Strictly increasing is what excludes both non-examples. The first term can be any term of the original sequence, "but once you have fixed the first one, you can't look back": each next term has to come from further out (≈1:10:15). And because $g$ is defined on all of $\mathbf{N}$, every subsequence is infinite: "all sequences, including subsequences, are infinite things" (≈1:18:13).

**Lecture 5's review** (Lecture 5, ≈0:47–3:10; Lecture 5 notes p. 1) gives the same reason for strictly increasing: the subsequence should keep the terms "in the same order than it was in the original sequence", and no term should be "picked more times than it was in the original sequence". It also says what the index means: "n k, really, you should think about it as g of k" (≈2:21). The Lecture 5 notes write the subsequence as $b_k = f(g(k))$ and add "We often write $a_{n_k}$ for $b_k$".

## Convergence of subsequences

**Theorem** (Lecture 4 notes p. 5; ≈1:11:48). A sequence $a_n$ is convergent with limit $a$ if and only if all subsequences of $a_n$ are also convergent with limit $a$.

**Proof** (notes pp. 5–6; ≈1:12:37–1:16:38).

- If every subsequence converges to $a$, then so does $a_n$, trivially: $a_n$ is a subsequence of itself, taking $g$ to be the identity, $g(k) = k$ (≈1:13:25–1:14:14).
- Suppose $a_n \to a$, and let $\epsilon \gt 0$. Choose $N$ so large that $\vert a_n - a \vert \lt \epsilon$ for $n \geq N$. Because $g$ is strictly increasing, $n_k \geq k$ (≈1:15:51), so for $k \geq N$ we have $n_k \geq k \geq N$, and therefore $\vert a_{n_k} - a \vert \lt \epsilon$. □

Neither the board nor the notes prove that $n_k \geq k$.

**How it is used** (≈1:16:38–1:17:28). If a sequence has a subsequence that does not converge, or two subsequences with different limits, then the sequence itself does not converge. Convergence "is always something about the tail, about the end": finitely many terms at the beginning never matter (≈1:17:28).

## Not yet in this knowledge base

On the OCW lecture list, Lecture 7 is "Bolzano–Weierstrass Theorem; Cauchy Sequences; Series" (TBB Sections 2.11–2.12 and 3.4) and Lecture 14 is "Sequential Compactness; Bolzano–Weierstrass Theorem in a Metric Space". Neither is covered here yet.

## Lectures

- [Lecture 4 — Sequences; Convergence](04-sequences-convergence.md): the examples, the definition, the theorem, and the closing questions about finite subsequences.
- [Lecture 5 — Monotone Convergence Theorem](05-monotone-convergence-theorem.md): the review of the definition, with $n_k$ read as $g(k)$.
