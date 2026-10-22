# The harmonic series

**The harmonic series $\sum \frac{1}{n}$ and the proof that it diverges ($s_{2^n - 1} \geq \frac{n}{2}$, by induction); the alternating harmonic series, which converges but not absolutely; and the series of $\frac{1}{n^2}$, which converges, proved by the same halving idea run the other way. From Lecture 7.**

Notation: $s_n$ is the $n$-th partial sum of the series in question, and $s_{2^n - 1}$ the partial sum up to the term with index $2^n - 1$. What a series is, and what it means for one to converge, is on [series](series.md). The captions write the powers $2^n$ as "2n".

## The harmonic series diverges

"Maybe the second most important is what's called the harmonic series", after the geometric series, and it "is unfortunately not a series that is convergent" (Lecture 7, ≈44:03). The **harmonic series** is

$$\sum_{n=1}^{\infty} \frac{1}{n} ,$$

which starts at $1$ "because I'm dividing by n" (≈44:50). The notes write $a_n = \frac{1}{n}$ and print the series as $\sum_{i=1}^{\infty} \frac{1}{2}$, a slip for $\frac{1}{i}$ (Lecture 7 notes p. 3).

**Theorem** (Lecture 7 notes p. 3; ≈45:41–46:30). The harmonic series is divergent.

The test Colding says is "particularly useful in this case" is the integral test, "But I won't talk about that today. But instead, I will show you a very simple proof of why this here is not convergent" (≈45:41).

**Claim** (notes p. 3; ≈46:30–47:16). For every $n$,

$$s_{2^n - 1} = \sum_{i=1}^{2^n - 1} \frac{1}{i} \geq \frac{n}{2} .$$

So the subsequence $s_{2^n - 1}$ of the partial sums is unbounded. If the series converged, every subsequence of its partial sums would converge (≈47:16; Lecture 4's theorem, see [subsequences](subsequences.md)), and a convergent sequence is bounded (Lecture 4; see [sequences and limits](sequences-and-limits.md#a-convergent-sequence-is-bounded)). "So of course, the original harmonic series is not convergent" (≈47:16). The notes: "Since $\frac{n}{2} \to \infty$ it follows that the subsequence $s_{2^n - 1}$ is divergent and therefore so is the original series" (notes p. 3).

**Proof of the claim, by induction** (notes p. 3; ≈48:06–53:37).

1. **$n = 1$.** Then $2^1 - 1 = 1$, and the claim is $s_1 \geq \frac{1}{2}$, which holds since $s_1 = 1$ (≈48:51; notes p. 3).
2. **From $n$ to $n + 1$.** Assume $s_{2^n - 1} \geq \frac{n}{2}$. The next partial sum is the old one plus the terms from $i = 2^n$ to $i = 2^{n+1} - 1$:

$$s_{2^{n+1} - 1} = s_{2^n - 1} + \sum_{i=2^n}^{2^{n+1} - 1} \frac{1}{i}$$

(≈50:30–51:20). There are $2^n$ new terms and the smallest is the last, $\frac{1}{2^{n+1} - 1}$; "if I take the smallest of these guys and I multiply it by 2n, then that's definitely a lower bound" (≈52:05). On the board Colding replaces $2^{n+1} - 1$ by the larger $2^{n+1}$, which makes the bound smaller still (≈52:51):

$$s_{2^{n+1} - 1} \geq \frac{n}{2} + 2^n \frac{1}{2^{n+1}} = \frac{n}{2} + \frac{1}{2} = \frac{n+1}{2} .$$

"And that's exactly the claim for n plus 1" (≈52:51). □ The notes go directly from $2^n \frac{1}{2^{n+1} - 1}$ to $\frac{1}{2}$ (notes p. 3).

Colding calls it a "very simple-minded proof": "Once we learn about the integral test and so on, there are other way better ways of doing it" (≈48:06).

**The terms go to zero anyway.** The terms $\frac{1}{n}$ tend to $0$, so the first check for a series, whether the terms go to $0$, does not detect this divergence; Colding says the harmonic series "failed this test" (≈55:58). See [series](series.md#first-check-do-the-terms-go-to-zero).

## The alternating harmonic series

(Lecture 7 notes p. 3; ≈1:00:40–1:02:21.) The series

$$\sum_{n=1}^{\infty} \frac{(-1)^n}{n}$$

"It's called the alternating harmonic series" (≈1:00:40). Its signs alternate, "the first one is negative. The next one is positive" (≈1:01:34). It is convergent but not absolutely convergent, since with absolute values it is the harmonic series (≈1:01:34; notes p. 3). It is the course's example that convergence does not imply absolute convergence (see [series](series.md#absolute-convergence)). Its convergence is not proved in Lecture 7: "And we haven't yet proved that it's converging, but we'll do that in some later lecture" (≈1:00:40).

## The series of $\frac{1}{n^2}$ converges

"So maybe the most important series is the geometric series. After that, you can debate a little bit which series is the most important" (Lecture 7, ≈1:06:20). The series

$$\sum_{n=1}^{\infty} \frac{1}{n^2}$$

is the case of power $2$; "you could do it more generally where you raise it to some power", and power $1$ gives the harmonic series (≈1:06:20). "I mean, this one doesn't really have a name, but it is a key series" (≈1:07:08). On the board Colding first starts the sum at $0$ and then corrects it to $1$ (≈1:07:55).

**Theorem** (Lecture 7 notes p. 4; ≈1:07:08). The series $\sum_{i=1}^{\infty} \frac{1}{i^2}$ is convergent.

The terms are non-negative, so it is enough to show that the partial sums are bounded (≈1:07:55; notes p. 4; see [series](series.md#series-of-non-negative-terms)).

**Claim** (notes p. 4; ≈1:08:40–1:10:18). For every $n$,

$$s_{2^n - 1} \leq \sum_{i=0}^{n-1} \left( \frac{1}{2} \right)^i .$$

The right side is a partial sum of the [geometric series](geometric-series.md) with $c = \frac{1}{2}$, so it is at most $\frac{1}{1 - c} = 2$ (≈1:11:04). The subsequence $s_{2^n - 1}$ is therefore bounded, and since the partial sums increase, "if a subsequence is bounded, then the original sequence is bounded and so convergent" (≈1:10:18). That step is not spelled out further.

**Proof of the claim, by induction** (notes pp. 4–5; ≈1:11:51–1:16:35).

1. **$n = 1$.** $s_1 = 1 = \left( \frac{1}{2} \right)^0$ (≈1:12:37; notes p. 5).
2. **From $n$ to $n + 1$.** Split as for the harmonic series. This time the goal is an upper bound, so "instead of what is the smallest, we think about what is the largest of these numbers. But that's the first one" (≈1:15:01). Each of the $2^n$ new terms is at most $\frac{1}{(2^n)^2}$, so

$$s_{2^{n+1} - 1} \leq \sum_{i=0}^{n-1} \left( \frac{1}{2} \right)^i + 2^n \frac{1}{(2^n)^2} = \sum_{i=0}^{n-1} \left( \frac{1}{2} \right)^i + \frac{1}{2^n} = \sum_{i=0}^{n} \left( \frac{1}{2} \right)^i$$

(notes p. 5; ≈1:15:01–1:15:50). □

"I mean, again, this is not necessarily how I would do it. But the advantage with this here is that it doesn't use anything fancy" (≈1:08:40). Asked at the end how one finds such a claim, Colding said: "Obviously you don't start with the claim. You're looking at the first few things and you see a pattern, basically" (≈1:21:28), and sketched the integral test, which compares the sum with the area under a curve (≈1:21:28–1:22:19). The integral test is not stated in the lecture or the notes.

**The ratio test cannot decide either series.** The notes' ratio test (see [convergence tests for series](convergence-tests-for-series.md)) gives $\frac{a_{n+1}}{a_n} \to 1$ for both $a_n = \frac{1}{n}$ and $a_n = \frac{1}{n^2}$, "so the test is inconclusive", although the first series diverges and the second converges (Lecture 7 notes pp. 6–7).

## Not yet in this knowledge base

The convergence of the alternating harmonic series and the integral test are promised for later. On the OCW lecture list, Lecture 8 is "Convergence Tests for Series; Power Series" (TBB Sections 3.5–3.6), which is not covered here yet.

## Lectures

- [Lecture 7 — Bolzano–Weierstrass Theorem; Cauchy Sequences; Series](07-bolzano-weierstrass-theorem-cauchy-sequences-series.md): the harmonic series, the alternating harmonic series and the series of $\frac{1}{n^2}$.
