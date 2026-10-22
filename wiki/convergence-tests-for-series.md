# Convergence tests for series

**The tests that decide whether a series converges, as far as the course has gone: the list Lecture 7 gives, the first check that the terms go to $0$, the comparison test in the form stated in the lecture and the second form in the notes, and the ratio test from the notes with its two inconclusive examples. None of the tests is proved yet.**

Notation: $a_n$ and $b_n$ are sequences of real numbers and $\sum a_n$ the series with terms $a_n$; what a series is, and what it means for one to converge, is on [series](series.md). The notes start the sums in this part at $n = 1$.

## The list

"So to determine whether or not a series is convergent, converge, then there are a number of tests. And then of course, the key point is to use the right test" (Lecture 7, ≈1:16:35–1:17:33). On the board Colding names the comparison test, the ratio test, the root test, the integral test, "And then there's even one called the alternate series test" (≈1:17:33–1:18:21). The notes list three, in a bulleted list: the comparison test, the ratio test and the root test (Lecture 7 notes p. 5). Lecture 7 states only the first version of the comparison test, with four minutes left (≈1:16:35); the notes also state a second version and the ratio test. The root, integral and alternating series tests are named but not stated.

## Before any test: do the terms go to zero?

"So for a series, always check if" the terms go to $0$ (Lecture 7, ≈54:24). If $a_n$ does not go to $0$, the series diverges and "there's no reason to start with any kind of test" (≈55:58). The converse fails: the harmonic series has terms going to $0$ and diverges. The argument is on [series](series.md#first-check-do-the-terms-go-to-zero).

## The comparison test

**Comparison test, version 1** (Lecture 7 notes p. 5; ≈1:18:21–1:19:10). Suppose that $a_n$ and $b_n$ are two sequences with

$$0 \leq a_n \leq b_n .$$

If $\sum_{n=1}^{\infty} b_n$ is convergent, then so is $\sum_{n=1}^{\infty} a_n$. "And this is the simplest version of the comparison test" (≈1:19:10). The captions garble the spoken inequality (≈1:18:21); the notes have $0 \leq a_n \leq b_n$. Neither the lecture nor the notes prove the test.

**How it is used** (≈1:19:10–1:20:42). A complicated series can be compared with "a much simpler series that perhaps you already know whether it's converging" (≈1:19:56). "It's used to both determine that a series is convergent. … And it's also used to determine that the series is divergent", by comparing with a series "you already know is divergent" (≈1:19:56–1:20:42). The geometric series is the usual comparison (see [the geometric series](geometric-series.md)); Lecture 7's proof that $\sum \frac{1}{n^2}$ converges compares its partial sums with those of a geometric series by hand, without the test (see [the harmonic series](harmonic-series.md)).

**Example** (notes p. 5). The series

$$\sum_{n=1}^{\infty} \frac{2^{-n}}{n}$$

is convergent: with $a_n = \frac{2^{-n}}{n}$ and $b_n = 2^{-n}$, "then $0 \leq a_n \leq b_n$ and since the series $\sum_{n=1}^{\infty} b_n$ is convergent, then by the comparison test so is the series $\sum_{n=1}^{\infty} a_n$" (notes p. 5).

**Comparison test, version 2** (notes p. 6; not in the lecture). Suppose that $a_n$ and $b_n$ are two sequences with $b_n \neq 0$ and

$$\lim_{n \to \infty} \frac{a_n}{b_n} = L \neq 0 .$$

Then $\sum_{n=1}^{\infty} a_n$ is convergent if and only if $\sum_{n=1}^{\infty} b_n$ is.

**Example** (notes p. 6). The series $\sum_{n=2}^{\infty} \frac{1}{n^2 - 1}$ is convergent, since

$$\frac{n^2}{n^2 - 1} \to 1$$

and the series $\sum_{n=2}^{\infty} \frac{1}{n^2}$ is convergent (notes p. 6). Here $a_n = \frac{1}{n^2 - 1}$ and $b_n = \frac{1}{n^2}$; the convergence of $\sum \frac{1}{n^2}$ is proved in Lecture 7 (see [the harmonic series](harmonic-series.md)).

## The ratio test

**Ratio test** (notes p. 6; not in the lecture). Let $a_n \geq 0$ and assume that

$$\frac{a_{n+1}}{a_n} \to a .$$

If $a \lt 1$, then the series $\sum a_n$ is convergent; if $a \gt 1$, it is divergent; if $a = 1$, "it is inconclusive" (notes p. 6). The notes do not say that the $a_n$ must be non-zero for the quotient to be defined, and give no proof.

**Two inconclusive examples** (notes pp. 6–7). For $a_n = \frac{1}{n}$ and for $a_n = \frac{1}{n^2}$ the ratio $\frac{a_{n+1}}{a_n}$ tends to $1$, "so the test is inconclusive", but the first series is divergent and the second convergent. Both were decided in Lecture 7 by other means (see [the harmonic series](harmonic-series.md)).

## The integral test, sketched

Colding mentions the integral test several times as the better way to handle the harmonic series and $\sum \frac{1}{n^2}$ (Lecture 7, ≈45:41, ≈48:06, ≈1:08:40), and sketches the idea in answer to a question at the end (≈1:21:28–1:22:19). For a series of non-negative numbers, picture each term as the area of a rectangle, so that the sum is a sum of areas, and compare it with "some curve and the area that lies below it" (≈1:22:19). He does not state the test.

## Not yet in this knowledge base

On the OCW lecture list, Lecture 8 is "Convergence Tests for Series; Power Series" (TBB Sections 3.5–3.6), where the tests continue: "we will, anyway, talk about it more next time" (Lecture 7, ≈1:20:42). It is not covered here yet, so this knowledge base has no proof of any of these tests and no statement of the root, integral or alternating series tests.

## Lectures

- [Lecture 7 — Bolzano–Weierstrass Theorem; Cauchy Sequences; Series](07-bolzano-weierstrass-theorem-cauchy-sequences-series.md): the list of tests, the first comparison test, and in the notes the second comparison test and the ratio test.
