# Series

**What a series is in this course (the sequence of partial sums of a sequence), when it converges, the notation $\sum a_i$ and its two meanings, why the starting index does not affect convergence, the first check that the terms go to $0$, series of non-negative terms, and absolute convergence, which implies convergence. From Lecture 7.**

Notation: $\mathbf{R}$ is the real numbers, set in bold as in the notes. A sequence is written $a_n$ and $\vert x \vert$ is the absolute value of $x$, which Colding often calls "the norm". $s_n$ is the $n$-th partial sum. Where a sum starts ($i = 0$ or $i = 1$) varies in the lecture and the notes, and each section says which.

## Definition

**Series** (Lecture 7 notes p. 2; Lecture 7, ≈23:00–25:21). Given a sequence $a_n$, form a new sequence $s_n$ by adding up its first terms:

$$s_1 = a_1 , \quad s_2 = a_1 + a_2 , \quad s_3 = a_1 + a_2 + a_3 ,$$

and in general

$$s_n = a_1 + \cdots + a_n = \sum_{i=1}^{n} a_i .$$

A sequence of this form is called a series. "OK, another key concept in this class is the concept of a series" (≈23:00).

**Convergence** (Lecture 7 notes p. 2; ≈34:14–35:05). The series $\sum_{i=1}^{\infty} a_i$ converges if the sequence $s_n$ converges, and then its limit is also written $\sum_{i=1}^{\infty} a_i$. A series is therefore just a sequence, and everything known about sequences applies to its partial sums: see [sequences and limits](sequences-and-limits.md).

**One symbol, two meanings** (≈34:14–35:52). "But really, what you're thinking about is this sequence here. But you, with a slight abuse of notation, you write this here for series" (≈34:14). "So in a way, this symbol here is used for two different things. It's used for the series. And if the series is convergent, it's also used for the limit. This is like standard" (≈35:52). For a divergent series the infinite sum is only a name: of the harmonic series Colding says "it's not a convergent series, so the infinite sum doesn't really make sense" (≈44:50).

**Where the sum starts** (≈36:38, ≈54:24). "It's, of course, important where you start. I mean, the convergence is not important. But what the limit is depends on where you start" (≈36:38). Starting later or earlier changes finitely many terms, "because this is just adding something to it. It will matter where you start for the limit, but not whether or not the series is convergent" (≈54:24). The notes start at $i = 1$ for the definition and at $i = 0$ for the geometric series and for absolute convergence, without comment (notes pp. 2–4).

**Achilles and the turtle** (≈25:21–26:07). Colding connects series to "one of the famous Greek paradoxes": Achilles chasing a turtle that has a head start has to cover half the distance, then half of what remains, and so on, "And so this goes on infinitely long, and therefore, he can never catch up with the turtle" (≈26:07). "And that's exactly a series" (≈26:07). He does not work out the sum.

## The basic examples

- **The geometric series** $\sum_{i=0}^{\infty} c^i$ converges to $\frac{1}{1-c}$ when $\vert c \vert \lt 1$ and diverges otherwise (Lecture 7, ≈26:56–44:03; notes pp. 2–3). It is "the most important series" (≈26:56) because other series are compared with it. See [the geometric series](geometric-series.md).
- **The harmonic series** $\sum_{n=1}^{\infty} \frac{1}{n}$ diverges, because $s_{2^n - 1} \geq \frac{n}{2}$ (≈44:03–53:37; notes p. 3). See [the harmonic series](harmonic-series.md).
- **The alternating harmonic series** $\sum_{n=1}^{\infty} \frac{(-1)^n}{n}$ converges but not absolutely; its convergence is promised "in some later lecture" (≈1:00:40; notes p. 3). See below.
- **The series** $\sum_{n=1}^{\infty} \frac{1}{n^2}$ converges, by comparison of its partial sums with a geometric series (≈1:05:31–1:16:35; notes pp. 4–5). See [the harmonic series](harmonic-series.md).

## First check: do the terms go to zero?

(Lecture 7, ≈53:37–55:58; not in the notes.) "So for a series, always check if" the terms go to $0$ or not (≈54:24). Two consecutive partial sums differ by one term,

$$s_n - s_{n-1} = a_n$$

(≈55:11). If the series converges, the partial sums form a convergent sequence, hence a Cauchy sequence, so consecutive partial sums must bunch together: $a_n$ must go to $0$ (≈55:11). So if $a_n$ does not go to $0$, the series diverges, "There's no reason to continue" (≈55:58). The argument uses the direction "convergent implies Cauchy" of the Cauchy convergence theorem, for which this knowledge base has no proof (see [Cauchy sequences](cauchy-sequences.md)).

The check works in one direction only. The terms $\frac{1}{n}$ of the harmonic series go to $0$, and the series still diverges; Colding says the harmonic series "failed this test" (≈55:58).

## Series of non-negative terms

If every $a_n \geq 0$, each partial sum is the previous one plus a non-negative term, $s_{n+1} = s_n + a_{n+1} \geq s_n$, so the partial sums are monotone increasing (Lecture 7, ≈56:43–57:30). By the [monotone convergence theorem](monotone-convergence-theorem.md), the question of convergence becomes whether the partial sums are bounded: "So you just need to find a bound" (≈57:30).

**Theorem** (Lecture 7 notes p. 4). A series of non-negative numbers $\sum_{i=0}^{\infty} a_i$, where $a_n \geq 0$, is convergent if and only if the sequence $s_n$ is bounded from above. The notes prove it in one line from the monotone convergence theorem (notes p. 4; the notes print $s_{n+1} = s_n + a_n$, a slip for $a_{n+1}$).

Both examples in Lecture 7 that go beyond the geometric series use this. The harmonic series has non-negative terms and unbounded partial sums; the series of $\frac{1}{n^2}$ has non-negative terms and partial sums bounded by $2$ (≈1:11:04). In the second proof only the subsequence $s_{2^n - 1}$ is bounded directly, and Colding concludes, "if a subsequence is bounded, then the original sequence is bounded and so convergent" (≈1:10:18), using that $s_n$ is increasing; the step is not spelled out. See [the harmonic series](harmonic-series.md).

## Absolute convergence

"So this naturally leads to looking at what's called absolute convergence. So this is something stronger than convergence" (Lecture 7, ≈58:19).

**Definition** (Lecture 7 notes p. 3; ≈59:09). A series $\sum_{n=0}^{\infty} a_n$ is **absolutely convergent** if the series

$$\sum_{n=0}^{\infty} \vert a_n \vert$$

is convergent: the series "where you slap absolute values on them" (≈59:09). On the board the series "converge absolutely".

**Theorem** (Lecture 7 notes p. 3; ≈59:55). Absolute convergence implies convergence. "But it's not the other way around" (≈59:55).

**The example** (notes p. 3; ≈1:00:40–1:02:21). The alternating harmonic series

$$\sum_{n=1}^{\infty} \frac{(-1)^n}{n}$$

is convergent, but with absolute values it becomes the harmonic series, which is divergent. Its terms alternate in sign, "the first one is negative. The next one is positive" (≈1:01:34). "And we haven't yet proved that it's converging, but we'll do that in some later lecture" (≈1:00:40); the notes say the same, "We will see later" (notes p. 3). This knowledge base does not yet contain that proof.

**Proof** (Lecture 7 notes pp. 3–4; ≈1:02:21–1:05:31). Let

$$s_n = \sum_{i=0}^{n} a_i , \qquad \bar{s}_ n = \sum_{i=0}^{n} \vert a_i \vert ,$$

the partial sums of the series and of the series of absolute values; on the board the second has a bar, "I denote it with a bar" (≈1:02:21), and in the notes it is a bold red $\mathbf{s}_ n$ (notes p. 4). For $m$ larger than $n$, the triangle inequality gives

$$\vert s_m - s_n \vert = \vert a_{n+1} + \cdots + a_m \vert \leq \vert a_{n+1} \vert + \cdots + \vert a_m \vert = \vert \bar{s}_ m - \bar{s}_ n \vert$$

(≈1:03:11–1:03:57; the notes write it with $m \lt n$, p. 4). If the series is absolutely convergent, $\bar{s}_ n$ converges, so it is a Cauchy sequence; by the inequality, so is $s_n$; and by the Cauchy convergence theorem $s_n$ converges (≈1:04:44–1:05:31). "So it means that the original series was convergent" (≈1:05:31). □

The proof uses both directions of the [Cauchy convergence theorem](cauchy-sequences.md): Cauchy implies convergent, proved in Lecture 6, and convergent implies Cauchy, for which this knowledge base has no proof.

## Tests for convergence

"And then of course, the key point is to use the right test" (Lecture 7, ≈1:17:33). Lecture 7 names the comparison, ratio, root, integral and alternating series tests and states the simplest comparison test; the notes add a second comparison test and the ratio test. See [convergence tests for series](convergence-tests-for-series.md).

## Not yet in this knowledge base

On the OCW lecture list, Lecture 8 is "Convergence Tests for Series; Power Series" (TBB Sections 3.5–3.6) and Lecture 9 is "Limsup and Liminf; Power Series; Continuous Functions; Exponential Function". Neither is covered here yet. The convergence of the alternating harmonic series is promised for a later lecture (Lecture 7, ≈1:00:40).

## Lectures

- [Lecture 7 — Bolzano–Weierstrass Theorem; Cauchy Sequences; Series](07-bolzano-weierstrass-theorem-cauchy-sequences-series.md): everything on this page.
- [Lecture 6 — Cauchy Convergence Theorem](06-cauchy-convergence-theorem.md): the Cauchy convergence theorem that the proofs about series use.
- [Lecture 5 — Monotone Convergence Theorem](05-monotone-convergence-theorem.md): the monotone convergence theorem, used for series of non-negative terms.
