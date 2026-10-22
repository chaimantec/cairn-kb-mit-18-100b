# The geometric series

**The series $\sum_{i=0}^{\infty} c^i$: the formula for its partial sums, the theorem that it converges to $\frac{1}{1-c}$ when $\vert c \vert \lt 1$ and diverges otherwise, the board's and the notes' proofs of divergence, why it is the series other series are compared with, its role in the ratio and root tests, and $\sum x^n = \frac{1}{1-x}$ as the first power series. From Lectures 7 and 8.**

Notation: $c$ is a real number, $\vert c \vert$ its absolute value (Colding's "norm"), and $s_n$ the $n$-th partial sum. The geometric series starts at $i = 0$, so $s_n$ has $n + 1$ terms (Lecture 7, ≈33:22). What a series is, and what it means for one to converge, is on [series](series.md).

## The series

**Geometric series** (Lecture 7 notes p. 2; Lecture 7, ≈26:56–28:32). For a number $c$,

$$s_n = \sum_{i=0}^{n} c^i ,$$

so $s_0 = 1$ (since $c^0 = 1$), $s_1 = 1 + c$, $s_2 = 1 + c + c^2$, and so on. "So this is the most important series" (≈26:56).

**Why it matters** (≈26:56–29:17). It is "a non-trivial series that can be used to determine whether other series" converge: "you can compare other series with the geometric series. And the geometric series is easier … to determine whether it is convergent or not" (≈28:32–29:17). In Lecture 7 it is the comparison behind the convergence of $\sum \frac{1}{n^2}$ (see [the harmonic series](harmonic-series.md)), and, answering a question at the end, Colding says it is one that "come up often as a kind of comparison" (≈1:20:42). The notes' example of the comparison test compares with $\sum 2^{-n}$, the geometric series with $c = \frac{1}{2}$ started at $n = 1$ (Lecture 7 notes p. 5; see [convergence tests for series](convergence-tests-for-series.md)).

Lecture 8 makes the point again. "So the most important is the geometric series", because it is easy to decide whether it converges and it can be used to decide whether other series do (Lecture 8, ≈5:46–6:34). The ratio test and the root test "are based on comparison with the geometric series. And so this is explaining why the geometric series is so crucial" (≈41:18). Their proofs bound $\vert a_n \vert$ far out by a constant times $\alpha^m$, or by $c_0^n$, for a number $\alpha$ or $c_0$ less than $1$, and compare with the convergent geometric series (≈45:18–52:36, ≈59:46–1:04:09). In case 2 of each test the comparison is with a number greater than $1$, and the terms blow up. See [convergence tests for series](convergence-tests-for-series.md).

## The formula for the partial sums

(Lecture 7 notes p. 2; ≈29:17–32:27.) Multiplying $1 + c + c^2 + \cdots + c^n$ by $c$ shifts every power up by one, to $c + c^2 + \cdots + c^{n+1}$ (≈29:17–30:05). So multiplying by $1 - c$ makes "a lot of cancelation" (≈30:53): everything cancels except the first term and the last, which comes with a minus sign,

$$(1 - c) \sum_{i=0}^{n} c^i = 1 - c^{n+1} .$$

If $c \neq 1$ you can divide by $1 - c$:

$$s_n = \sum_{i=0}^{n} c^i = \frac{1 - c^{n+1}}{1 - c}$$

(notes p. 2; ≈31:40–32:27).

## The theorem

**Theorem** (Lecture 7 notes pp. 2–3; ≈36:38–38:29). The geometric series is convergent if $\vert c \vert \lt 1$ and divergent otherwise. When $\vert c \vert \lt 1$,

$$\sum_{i=0}^{\infty} c^i = \frac{1}{1 - c} .$$

The notes: "It is convergent precisely when $\vert c \vert \lt 1$" (notes p. 2). When Colding says the limit aloud he says "1 minus c" and later "1 minus c over 1"; the board and the notes have $\frac{1}{1-c}$ (≈38:29, ≈40:55; marked in the transcript). Where the series starts does not matter for convergence, but it does for the limit (≈36:38): $\frac{1}{1-c}$ is the sum from $i = 0$.

**Proof when $\vert c \vert \lt 1$** (≈39:21–41:43). Then $c \neq 1$, so the formula applies. Since $\vert c^{n+1} \vert = \vert c \vert^{n+1}$ and $\vert c \vert \lt 1$, the term $c^{n+1}$ goes to $0$ (≈40:10), and "just by the algebraic rules for limits" $s_n \to \frac{1}{1-c}$ (≈40:55; see [algebraic properties of limits](algebraic-properties-of-limits.md)). That $\vert c \vert^{n+1} \to 0$ is used without proof. Knowing the sum exactly is the exception: "usually you cannot actually determine what the limit is. But in this case, we could" (≈40:55).

**Proof of divergence when $\vert c \vert \geq 1$: the board** (≈41:43–44:03). Consecutive partial sums differ by one term,

$$s_{n+1} - s_n = c^{n+1} , \qquad \vert s_{n+1} - s_n \vert = \vert c \vert^{n+1} \geq 1 .$$

A convergent sequence is a Cauchy sequence (≈43:16), but here "not even two consecutive is bunching together, because independent on how far, how large n is, the difference is always at least 1" (≈43:16). So $s_n$ is not Cauchy and does not converge. This covers every $c$ with $\vert c \vert \geq 1$, including $c = 1$, where the formula for $s_n$ does not apply. It uses the direction "convergent implies Cauchy" of the Cauchy convergence theorem, for which this knowledge base has no proof (see [Cauchy sequences](cauchy-sequences.md)). The same idea is Lecture 7's first check for any series: if the terms do not go to $0$, the series diverges (see [series](series.md#first-check-do-the-terms-go-to-zero)).

**Proof of divergence: the notes** (notes p. 3). From the formula, "Therefore, $s_n$ converges with limit $\frac{1}{1-c}$ if $\vert c \vert \lt 1$ and diverges if $\vert c \vert \gt 1$ or $c = -1$. One easily checks, separately, that it also diverges for $c = 1$." The notes give no further detail for the divergent cases.

**Lecture 8's review** (Lecture 8, ≈7:26–8:59). In Lecture 8 the divergence is read off the terms. If $c = 1$, every term is $1$, "But that does not go to 0. So that's clearly diverging" (≈8:13). If $c = -1$, the terms alternate between $1$ and $-1$ and do not go to $0$ (≈8:13). If $\vert c \vert \gt 1$, they are "even blowing up" (≈8:59). This is the first check for any series (see [series](series.md#first-check-do-the-terms-go-to-zero)). The Lecture 8 notes state only "Convergent precisely when $\vert c \vert \lt 1$", and print the summand as $c^{i}n$, a slip (Lecture 8 notes p. 1).

## The first power series

With the number called $x$ instead of $c$, the geometric series is the first example of a power series (Lecture 8, ≈1:07:35):

$$\sum_{n=0}^{\infty} x^n = \frac{1}{1 - x} \qquad \text{for } \vert x \vert \lt 1$$

(Lecture 8 notes pp. 4–5). For each fixed $x$ it is the geometric series, so it converges for $\vert x \vert \lt 1$ and diverges otherwise (≈1:13:57–1:14:58), and "the sum here is just this familiar function" (≈1:09:12). See [power series](power-series.md).

## Not yet in this knowledge base

On the OCW lecture list, Lecture 9 is "Limsup and Liminf; Power Series; Continuous Functions; Exponential Function" (TBB Sections 2.13, 10.2, 5.4 and 5.5), which is not yet in this knowledge base.

## Lectures

- [Lecture 7 — Bolzano–Weierstrass Theorem; Cauchy Sequences; Series](07-bolzano-weierstrass-theorem-cauchy-sequences-series.md): the formula, the theorem and both proofs, and the comparison for $\sum \frac{1}{n^2}$.
- [Lecture 8 — Convergence Tests for Series; Power Series](08-convergence-tests-for-series-power-series.md): the review, the ratio and root tests built on it, and $\sum x^n$ as a power series.
