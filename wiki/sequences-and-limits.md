# Sequences and limits

**What a sequence of real numbers is, the definition of convergence with $\epsilon$ and $N$, divergence, the course's examples (including $0.999 \cdots = 1$), the theorem that a convergent sequence is bounded, the first condition that guarantees convergence (the monotone convergence theorem), the definition of a Cauchy sequence, and the second condition, Lecture 6's Cauchy convergence theorem: every Cauchy sequence of real numbers converges, with Lecture 7's proof of the Bolzano–Weierstrass theorem behind it; and series, which are sequences of partial sums (Lectures 7 and 8). Covers Lectures 2 to 8.**

Notation: $\mathbf{N} = \lbrace 1, 2, 3, \cdots \rbrace$ is the natural numbers and $\mathbf{R}$ the real numbers, set in bold as in the notes. A sequence is written $a_n$, and $\vert x \vert$ is the absolute value of $x$, which Colding often calls the "norm".

## Why the course needs them

Sequences first come up as a way to place $\sqrt{2}$ on the real line. As a decimal, $\sqrt{2}$ begins $1.4142136$, and it can be thought of as the limit of the increasing sequence $1$, $1.4$, $1.41$, $1.414$, … (Lecture 2, ≈16:47–18:30; Lecture 2 notes p. 1). Lecture 2 calls this a preview: sequences and limits are "another really important concept that we will talk much more about later" (≈17:40). Lecture 3 starts them, saying "this will be a big topic" (≈1:14:20), and notes that to use this picture of $\sqrt{2}$ the course must make precise both what a sequence is and what its limit is (≈1:16:02). Lecture 4 opens with the same picture (Lecture 4, ≈0:00–0:55).

## Sequences

**Definition** (Lecture 3 notes p. 5; Lecture 3, ≈1:16:48; repeated in Lecture 4, ≈1:43, and Lecture 4 notes pp. 1–2). A sequence of real numbers is a function

$$f : \mathbf{N} \to \mathbf{R} .$$

For each natural number you get a real number. Rather than writing the argument in brackets, it is usual to write it as a subscript, $a_n = f(n)$ (Lecture 3, ≈1:17:35).

The course's first examples (Lecture 3 notes p. 5; Lecture 4 notes p. 2; Lecture 4, ≈2:28–4:45):

- **Example 1.** $a_1 = 1$, $a_2 = 1.4$, $a_3 = 1.41$, $a_4 = 1.414$, and so on, where $a_n$ keeps the first $n$ digits of $\sqrt{2}$. This sequence is increasing, $a_n \lt a_{n+1}$, and $\sqrt{2}$ is its limit (Lecture 3, ≈1:17:35–1:19:05).
- **Example 2.** $a_n = (-1)^n$: $-1, 1, -1, 1, \cdots$. "This sequence has NO limit": its terms alternate between $-1$ and $1$.
- **Example 3.** $a_n = \frac{1}{n}$: $1, \frac{1}{2}, \frac{1}{3}, \frac{1}{4}, \cdots$, all positive and becoming smaller and smaller. It has zero as its limit.

None of the three claims about limits is proved in the lectures or the notes; they motivate the definition below. Lecture 3's video stops before Examples 2 and 3, which Lecture 4 gives on the board.

## Convergence

**Definition** (Lecture 3 notes p. 5; Lecture 4 notes p. 2; Lecture 4, ≈5:30–8:46). Let $a_n$ be a sequence and $a$ a real number. The sequence $a_n$ **converges** to $a$ if for all $\epsilon \gt 0$ there exists an $N \in \mathbf{N}$ such that if $n \geq N$, then

$$\vert a_n - a \vert \lt \epsilon .$$

Then $a$ is the **limit** of the sequence, written $\lim_{n \to \infty} a_n = a$ or $a_n \to a$, and the sequence is **convergent**. A sequence that is not convergent is **divergent** (Lecture 4 notes p. 2; Lecture 4, ≈7:59–8:46). On the board Colding states the condition for $n$ bigger than $N$; the notes have $n \geq N$ (Lecture 4, ≈6:24).

**How to picture it** (Lecture 4, ≈6:24–7:59). Around $a$ on the real line, take the interval from $a - \epsilon$ to $a + \epsilon$. Convergence means that from some $N$ on, every term of the sequence lies in that interval, however small the interval is. The order of the quantifiers is the whole point. First "someone else is allowed to pick the epsilon" (≈7:11), and only then do you have to produce an $N$ that works for it. The $N$ may depend on $\epsilon$: as $\epsilon$ gets smaller, presumably $N$ has to be chosen larger (Lecture 4, ≈41:21).

**Choosing the $\epsilon$ to use.** Because the definition holds for every $\epsilon \gt 0$, a proof may apply it to whatever positive number it needs, not only to the $\epsilon$ it was given. Lecture 4's proofs apply it to $1$ (boundedness), to $\frac{\epsilon}{\vert C \vert}$ and $\frac{\epsilon}{2}$ (the algebraic properties), and to $\frac{\vert a \vert}{2}$ (to keep $\vert a_n \vert$ away from $0$). "I'm basically using that for all epsilon, that it wasn't just for a fixed epsilon" (Lecture 4, ≈42:08). See [algebraic properties of limits](algebraic-properties-of-limits.md).

**When does a limit exist?** The Lecture 3 notes pose the question and leave it open (Lecture 3 notes p. 5). Lecture 4 gives a necessary condition, the boundedness theorem below. Lecture 5 gives the first sufficient one: a bounded monotone sequence converges (see [monotone sequences](#monotone-sequences) below).

## Example: $0.999 \cdots = 1$

(Lecture 4 notes pp. 2–3; Lecture 4, ≈8:46–15:23.) The left side is defined as the limit of the sequence

$$a_1 = 0.9, \quad a_2 = 0.99, \quad a_3 = 0.999, \quad a_4 = 0.9999, \quad \cdots$$

**Claim.** $\lim_{n \to \infty} a_n = 1$.

**Proof.** Given $\epsilon \gt 0$, the [Archimedean property](archimedean-property.md) gives an $N$ with $\frac{1}{N} \lt \epsilon$. Since $\vert a_n - 1 \vert = 10^{-n}$, for $n \geq N$

$$\vert a_n - 1 \vert = 10^{-n} \lt \frac{1}{n} \leq \frac{1}{N} \lt \epsilon .$$

□

Colding calls $10^{-n} \lt \frac{1}{n}$ obvious, and neither the board nor the notes prove it (≈14:36). The [Lecture 4 page](04-sequences-convergence.md) has the board's version.

## A convergent sequence is bounded

**Theorem** (Lecture 4 notes p. 3; Lecture 4, ≈15:23–24:53). If $a_n$ is a convergent sequence, then the set $\lbrace a_n \rbrace$ is a bounded subset of $\mathbf{R}$.

**Proof.** Let $a$ be the limit. Applying the definition with $\epsilon = 1$ gives an $N$ with $\vert a - a_n \vert \lt 1$ for $n \geq N$. The finitely many terms $a_1, \cdots, a_{N-1}$ are bounded, say $\vert a_n \vert \leq C$ for $n = 1, \cdots, N - 1$. For $n \geq N$,

$$\vert a_n \vert \leq \vert a \vert + \vert a_n - a \vert \leq \vert a \vert + 1 .$$

So $\vert a_n \vert \leq \max\lbrace C, \vert a \vert + 1 \rbrace$ for all $n$. □

The converse is false: $(-1)^n$ is bounded but not convergent. "It's not enough to be bounded to be convergent, but it is a necessary criterion" (Lecture 4, ≈17:00). The bound is used again in the proof that a product of convergent sequences converges. The choice $\epsilon = 1$ is arbitrary, "the 1 really, to some extent, could be almost anything", but a smaller $\epsilon$ would push $N$ out and probably make $C$ jump up (Lecture 4, ≈25:43–26:28). The details, and the board's version stated with $\sup$, are on the [Lecture 4 page](04-sequences-convergence.md).

## Limits and the algebraic operations

If $a_n \to a$, $b_n \to b$ and $C \in \mathbf{R}$, then $C a_n \to C a$, $a_n + b_n \to a + b$, $a_n b_n \to a b$, and, when $b_n \neq 0$ and $b \neq 0$, $\frac{a_n}{b_n} \to \frac{a}{b}$ (Lecture 4 notes p. 3). Statements, proofs and the "halfway" trick behind the product are on [algebraic properties of limits](algebraic-properties-of-limits.md). Lecture 5 reviews them with the sum as the first rule and the fourth as a reciprocal, $\frac{1}{a_n} \to \frac{1}{a}$, and applies them to show that $\frac{n^2 + 1}{n^2 + n + 1} \to 1$ (Lecture 5, ≈4:50–13:46; Lecture 5 notes pp. 1–2).

## Subsequences

A subsequence of $a_n$ keeps some of its terms, infinitely many, in their original order: formally $f \circ g$ for a strictly increasing $g : \mathbf{N} \to \mathbf{N}$. A sequence converges to $a$ if and only if all its subsequences converge to $a$ (Lecture 4 notes pp. 5–6). Convergence "is always something about the tail, about the end": it never cares about finitely many terms at the start (Lecture 4, ≈1:17:28). See [subsequences](subsequences.md).

## Monotone sequences

A sequence is **monotone increasing** if $a_n \leq a_{n+1}$ for all $n$ and **monotone decreasing** if $a_{n+1} \leq a_n$ for all $n$ (Lecture 5 notes p. 2; Lecture 5, ≈16:07–16:54). The **monotone convergence theorem**: a monotone increasing sequence that is bounded from above converges, with limit $\sup \lbrace a_n \rbrace$, and a monotone decreasing sequence that is bounded from below converges, with limit $\inf \lbrace a_n \rbrace$ (Lecture 5 notes p. 2; Lecture 5, ≈17:43–21:51). It is the first result in the course that proves a limit exists, and Lecture 5 uses it to show that the decimals $1$, $1.4$, $1.41$, $1.414$, … converge to a number whose square is $2$. On the board, any bounded sequence gives two monotone ones, the $\sup$ and the $\inf$ of its tails (Lecture 5, ≈21:51–33:39). The theorem, its proof and both applications are on [the monotone convergence theorem](monotone-convergence-theorem.md).

## Cauchy sequences

A sequence $a_n$ is a **Cauchy sequence** if for all $\epsilon \gt 0$ there is an $N$ such that $\vert a_n - a_m \vert \lt \epsilon$ for $m, n \geq N$ (Lecture 5 notes p. 6; Lecture 5, ≈1:08:56–1:09:45). Unlike convergence, the definition names no limit: far out, the terms "bunch together" (≈1:10:32). Lecture 5 states, without proof, that a sequence of real numbers converges if and only if it is Cauchy (≈1:11:21).

Lecture 6 proves that a Cauchy sequence is bounded and that it converges (Lecture 6, ≈3:24–8:26, ≈49:32–58:28; Lecture 6 notes p. 3). The proof uses the [Bolzano–Weierstrass theorem](bolzano-weierstrass-theorem.md), that every bounded sequence has a convergent subsequence, which Lecture 6 assumes and promises for the next lecture (≈50:17) and Lecture 7 proves (Lecture 7, ≈2:25–22:12). Like the monotone convergence theorem, the Cauchy convergence theorem proves that a limit exists without naming it, but it asks nothing about the order of the terms. The converse, that a convergent sequence is Cauchy, is said in Lecture 6 to have been proved "last time" (≈9:27), but no proof of it is in the material here; Lecture 7 uses it for series (≈43:16, ≈55:11, ≈1:04:44), and Lecture 8 again (Lecture 8, ≈2:27–5:46, ≈29:17). See [Cauchy sequences](cauchy-sequences.md).

## Series

A series is a sequence too: given $a_n$, its partial sums $s_n = a_1 + \cdots + a_n = \sum_{i=1}^{n} a_i$ form a new sequence, and the series $\sum_{i=1}^{\infty} a_i$ converges when $s_n$ does (Lecture 7 notes p. 2; Lecture 7, ≈23:00–25:21, ≈34:14). "But s n is just a sequence" (Lecture 7, ≈25:21). The theorems about sequences therefore apply to series: the harmonic series diverges because a subsequence of its partial sums is unbounded (≈47:16), a series of non-negative terms converges exactly when its increasing partial sums are bounded (Lecture 7 notes p. 4), and absolute convergence implies convergence by the Cauchy convergence theorem (≈1:02:21–1:05:31). Lecture 8 adds the tests for convergence (comparison, ratio and root) and power series $\sum a_n x^n$, whose convergence is decided for each fixed $x$ (Lecture 8, ≈21:58–1:19:46). See [series](series.md), [the geometric series](geometric-series.md), [the harmonic series](harmonic-series.md), [convergence tests for series](convergence-tests-for-series.md) and [power series](power-series.md).

## A related fact

As a corollary of the [Archimedean property](archimedean-property.md), for any $\epsilon \gt 0$ there exists an $n \in \mathbf{N}$ such that $\frac{1}{n} \lt \epsilon$ (Lecture 3 notes p. 4). That is the fact the proof of $0.999 \cdots = 1$ uses to choose $N$. In Lecture 5, that $\frac{1}{n} \to 0$ "essentially just follows from the Archimedean property. But we've already seen this" (Lecture 5, ≈9:00).

## Not yet in this knowledge base

Lecture 5 says that the $\sup$ and $\inf$ of the tails are how limsup and liminf are defined (≈1:08:10). The Lecture 8 notes define $\limsup$ that way (see [limsup and liminf](limsup-and-liminf.md)); $\liminf$ is not yet defined. On the OCW lecture list, Lecture 9 is "Limsup and Liminf; Power Series; Continuous Functions; Exponential Function" (TBB Sections 2.13, 10.2, 5.4 and 5.5), which is not yet in this knowledge base.

## Lectures

- [Lecture 2 — Introduction to Real Numbers (cont.)](02-introduction-to-real-numbers-cont.md): $\sqrt{2}$ as the limit of its decimals, as a preview.
- [Lecture 3 — How to Write a Proof; Archimedean Property](03-how-to-write-a-proof-archimedean-property.md): the definition of a sequence, and in the notes, the examples and the definition of convergence.
- [Lecture 4 — Sequences; Convergence](04-sequences-convergence.md): convergence on the board, divergence, $0.999 \cdots = 1$, boundedness, the algebraic properties of limits, and subsequences.
- [Lecture 5 — Monotone Convergence Theorem](05-monotone-convergence-theorem.md): monotone sequences and the monotone convergence theorem, $\sqrt{2}$ as the limit of its decimals, and the definition of a Cauchy sequence.
- [Lecture 6 — Cauchy Convergence Theorem](06-cauchy-convergence-theorem.md): a Cauchy sequence is bounded and converges, and a continuous function takes convergent sequences to convergent sequences.
- [Lecture 7 — Bolzano–Weierstrass Theorem; Cauchy Sequences; Series](07-bolzano-weierstrass-theorem-cauchy-sequences-series.md): the proof of the Bolzano–Weierstrass theorem, and series as sequences of partial sums.
- [Lecture 8 — Convergence Tests for Series; Power Series](08-convergence-tests-for-series-power-series.md): tests for the convergence of series, power series, and in the notes $\limsup$.
