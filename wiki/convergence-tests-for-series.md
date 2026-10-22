# Convergence tests for series

**The tests that decide whether a series converges, as far as the course has gone. The page covers the lists in Lectures 7 and 8 and the first check, that the terms go to $0$. It covers the comparison test in two versions, with Lecture 8's two proofs of the first and the worked examples. It covers the ratio test and the root test with their proofs, both by comparison with a geometric series. It covers the alternating series test and the integral test, which have only been sketched, and the notes' remark that $\limsup$ handles a ratio or root with no limit.**

Notation: $a_n$ and $b_n$ are sequences of real numbers, $\sum a_n$ the series with terms $a_n$, and $\vert x \vert$ the absolute value of $x$. What a series is, and what it means for one to converge, is on [series](series.md). Where a sum starts never affects whether it converges (Lecture 8, ≈35:26), and each section says where the course starts it. In the root test the limit is $c$ on the board and $r$ in the notes.

## The list

"So to determine whether or not a series is convergent, converge, then there are a number of tests. And then of course, the key point is to use the right test" (Lecture 7, ≈1:16:35–1:17:33). In Lecture 7 Colding names the comparison test, the ratio test, the root test, the integral test, "And then there's even one called the alternate series test" (≈1:17:33–1:18:21). Lecture 8 covers the comparison, ratio and root tests, "But there are other tests" (Lecture 8, ≈22:46). The notes list those three in both lectures, adding in Lecture 8 "Other tests that we will discuss later" (Lecture 7 notes p. 5; Lecture 8 notes p. 2).

Most of the tests, "but again, not all", decide "whether the series is what's called absolutely convergent" (Lecture 8, ≈12:09). That is the case for the ratio and root tests below, whose proofs compare the absolute values $\vert a_n \vert$ with a geometric series (see [series](series.md#absolute-convergence)).

## Before any test: do the terms go to zero?

"So for a series, always check if" the terms go to $0$ (Lecture 7, ≈54:24). "The first thing that you check is that this element here goes to 0" (Lecture 8, ≈5:46). If the series converges, its partial sums $s_n$ form a Cauchy sequence, and taking $m = n - 1$ gives $s_n - s_{n-1} = a_n$, which must therefore go to $0$ (Lecture 8, ≈2:27–5:46). So if $a_n$ does not go to $0$, the series diverges and no test is needed. The converse fails: the harmonic series has terms going to $0$ and diverges. Two of the proofs below end with this check, since in case 2 of the ratio and root tests the terms do not go to $0$. The argument is on [series](series.md#first-check-do-the-terms-go-to-zero).

## The comparison test, version 1

**Comparison test, version 1** (Lecture 7 notes p. 5; Lecture 8 notes p. 2; Lecture 7, ≈1:18:21–1:19:10; Lecture 8, ≈23:46–24:38). Suppose that $a_n$ and $b_n$ are two sequences with

$$0 \leq a_n \leq b_n .$$

If $\sum_{n=1}^{\infty} b_n$ is convergent, then so is $\sum_{n=1}^{\infty} a_n$. "And this is the simplest version of the comparison test" (Lecture 7, ≈1:19:10).

**How it is used.** A complicated series can be compared with "a much simpler series that perhaps you already know whether it's converging" (Lecture 7, ≈1:19:56). It works in both directions: "It's used to both determine that a series is convergent. … And it's also used to determine that the series is divergent" (Lecture 7, ≈1:19:56–1:20:42). In Lecture 8 Colding calls the divergence form "just a negation of this statement" (≈24:38). As the contrapositive of the test, it says that if the series of the $a_n$ diverges, so does the series of the $b_n$. The comparison series is usually a geometric series (see [the geometric series](geometric-series.md)), and finding it is part of the problem: "So this is typically how it works" (Lecture 8, ≈31:34).

**Proof with Cauchy sequences** (Lecture 8, ≈24:38–29:17; the notes give no proof). Write $s_n^{a}$ and $s_n^{b}$ for the partial sums of the two series, "the superscript a just to denote that it's coming from the sequence" $a_n$ (≈26:12). For $m \lt n$, since every term is non-negative,

$$\vert s_n^{a} - s_m^{a} \vert = a_{m+1} + \cdots + a_n \leq b_{m+1} + \cdots + b_n = s_n^{b} - s_m^{b}$$

(≈26:58–29:17). The series of the $b_n$ converges, so the right side is as small as we want once $m$ and $n$ are large enough (≈29:17). So $s_n^{a}$ is a Cauchy sequence, and by the Cauchy convergence theorem it converges. □ This uses both directions of the Cauchy convergence theorem; "convergent implies Cauchy" has no proof in this knowledge base (see [Cauchy sequences](cauchy-sequences.md)).

Why Cauchy sequences? A student asked, and Colding answered that going back to the definition of convergence "you would have to determine what the limit was" (≈27:45), and knowing the sum of the $b_n$ does not tell you the sum of the $a_n$. "So the advantage with Cauchy sequence is that you don't have to figure out what the limit is" (≈28:31).

**Proof with the monotone convergence theorem** (Lecture 8, ≈29:17–30:48). The partial sums satisfy $s_n^{a} \leq s_n^{b}$, and the $s_n^{b}$ converge, so they are bounded by some real number $c$ for all $n$ (≈30:03–30:48). The $s_n^{a}$ form a monotone increasing sequence bounded by $c$, so they converge by the [monotone convergence theorem](monotone-convergence-theorem.md) (≈30:48). □ "So you can do it either of those two ways" (≈30:48).

**Example** (Lecture 7 notes p. 5; Lecture 8 notes p. 2; Lecture 8, ≈31:34–34:40). The series

$$\sum_{n=1}^{\infty} \frac{2^{-n}}{n}$$

is convergent: with $a_n = \frac{2^{-n}}{n}$ and $b_n = 2^{-n}$, "then $0 \leq a_n \leq b_n$ and since the series $\sum_{n=1}^{\infty} b_n$ is convergent, then by the comparison test so is the series $\sum_{n=1}^{\infty} a_n$" (Lecture 8 notes p. 2). The series of the $b_n$ is the geometric series with $c = \frac{1}{2}$ (Lecture 8, ≈33:09).

## The comparison test, version 2

**Comparison test, version 2** (Lecture 7 notes p. 6; Lecture 8 notes p. 3; Lecture 8, ≈34:40–37:19). Suppose that $a_n$ and $b_n$ are two sequences with $b_n \neq 0$ and

$$\lim_{n \to \infty} \frac{a_n}{b_n} = L \neq 0 .$$

Then $\sum_{n=1}^{\infty} a_n$ is convergent if and only if $\sum_{n=1}^{\infty} b_n$ is.

On the board in Lecture 8 the $a_n$ and $b_n$ are also taken non-negative, which the notes do not say, and $L$ "is not 0 and is not infinity. I mean that it really is a limit" (≈36:17). The test is not proved, on the board or in the notes.

**Example** (Lecture 7 notes p. 6; Lecture 8 notes p. 3; Lecture 8, ≈37:19–40:30). The series $\sum_{n=2}^{\infty} \frac{1}{n^2 - 1}$ starts at $2$ so as not to divide by $0$ (≈37:19). Its terms are bigger than $\frac{1}{n^2}$, so version 1 does not apply directly against $\sum \frac{1}{n^2}$, although "You could still use the first test" with more work (≈38:04–38:53). With $a_n = \frac{1}{n^2 - 1}$ and $b_n = \frac{1}{n^2}$,

$$\frac{a_n}{b_n} = \frac{n^2}{n^2 - 1} = \frac{1}{1 - \frac{1}{n^2}} \to 1$$

by the algebraic rules for limits (≈38:53–39:42; see [algebraic properties of limits](algebraic-properties-of-limits.md)). The limit is "neither zero nor infinity" (≈39:42), and $\sum \frac{1}{n^2}$ converges (Lecture 7; see [the harmonic series](harmonic-series.md)), so the series converges (≈40:30).

## The ratio test

"I mean, the comparison tests are typically almost the easiest tests. But this one here is extremely useful" (Lecture 8, ≈40:30). The ratio test and the root test "are based on comparison with the geometric series. And so this is explaining why the geometric series is so crucial" (≈41:18). No second series has to be found: "You don't have to look at any other series" (≈42:05).

**Ratio test** (Lecture 8, ≈42:05–45:18). Let all $a_n \neq 0$ (≈48:26), and suppose that

$$\lim_{n \to \infty} \left\vert \frac{a_{n+1}}{a_n} \right\vert = a$$

exists. If $a \lt 1$, the series $\sum a_n$ is convergent; if $a \gt 1$, it is divergent; if $a = 1$, the test is inconclusive (≈43:40–44:26). "And I should also emphasize that it is crucial to have a limit" (≈44:26).

The notes (Lecture 7 notes p. 6; Lecture 8 notes p. 3) state it for $a_n \geq 0$ with $\frac{a_{n+1}}{a_n} \to a$, and the same three cases, without proof.

**Proof of case 1, sketched** (Lecture 8, ≈45:18–52:36). Choose $\alpha$ with $a \lt \alpha \lt 1$ (≈46:54–48:26). There is an $N$ with $\vert a_{n+1} \vert \leq \alpha \vert a_n \vert$ for $n \geq N$: far enough out, "the next one is a fraction of the previous one" (≈49:17). Applying this repeatedly,

$$\vert a_{N+m} \vert \leq \alpha^m \vert a_N \vert$$

for all $m$ (≈50:08–51:01). "So the tail is bounded by a convergent geometric series" (≈51:49), and the first comparison test gives convergence (≈51:49). □

**Proof of case 2** (≈52:36–54:57). Choose $\alpha$ with $1 \lt \alpha \lt a$. Far enough out $\vert a_{n+1} \vert \gt \alpha \vert a_n \vert$, so the terms grow in absolute value, "So they don't converge to 0 as they were supposed to" (≈54:57). □ Case 3 has nothing to prove, "because it leaves open both possibilities" (≈54:57).

**The terms need not decrease.** Asked whether case 1 assumes the sequence is monotonically decreasing, Colding said no: "But I could alternate signs and things like that" (≈55:45). What is needed is that sufficiently far out the absolute values go down, as in a convergent geometric series, where "the next element is some fixed fraction of the previous one" (≈55:45–56:33).

**Two inconclusive examples** (Lecture 7 notes pp. 6–7; Lecture 8 notes pp. 3–4). For $a_n = \frac{1}{n}$ and for $a_n = \frac{1}{n^2}$ the ratio $\frac{a_{n+1}}{a_n}$ tends to $1$, "so the test is inconclusive", but the first series is divergent and the second convergent. Both were decided in Lecture 7 by other means (see [the harmonic series](harmonic-series.md)).

**Example: $\sum \frac{x^n}{n!}$** (Lecture 8 notes p. 5; ≈1:14:58–1:19:46). For a fixed $x \neq 0$ the ratio of consecutive terms is $\frac{x}{n+1}$, which goes to $0$, so the series converges for every $x$. See [power series](power-series.md).

## The root test

The root test also compares with the geometric series, but not consecutive terms, so a term may occasionally be larger than the one before: "And the root test is OK with that, whereas that test wasn't OK with that" (Lecture 8, ≈57:19).

**Root test** (Lecture 8, ≈58:05–59:46). Suppose that

$$\lim_{n \to \infty} \vert a_n \vert^{\frac{1}{n}} = c .$$

If $c \lt 1$, the series is convergent; if $c \gt 1$, it is divergent; if $c = 1$, the test is inconclusive (≈58:50–59:46).

The notes (Lecture 8 notes p. 4) state it for $a_n \geq 0$ with $\lim_{n \to \infty} (a_n)^{\frac{1}{n}} = r$ and the series $\sum_{n=0}^{\infty} a_n$, and prove it. It is the only test the notes prove.

**Proof of case 1** (Lecture 8, ≈59:46–1:04:09; Lecture 8 notes p. 4). Choose $c_0$ with $c \lt c_0 \lt 1$. There is an $N$ such that $\vert a_n \vert^{\frac{1}{n}} \leq c_0$ for $n$ larger than $N$, and taking $n$-th powers,

$$\vert a_n \vert \leq c_0^n .$$

From $N$ on, the $\vert a_n \vert$ are compared with the convergent geometric series $\sum c_0^n$, and the first comparison test gives convergence (≈1:01:28–1:03:20). Because the comparison is with absolute values, what is proved is absolute convergence, "But absolute convergence implies convergence. So you're actually proving absolute convergence" (≈1:04:09). □ The notes: $r \lt r_0 \lt 1$, $0 \leq a_n \leq r_0^n$, and "by the first version of the comparison test" the series converges (notes p. 4).

**Proof of case 2** (Lecture 8, ≈1:04:09–1:07:35; Lecture 8 notes p. 4). Choose $c_0$ with $1 \lt c_0 \lt c$. Far enough out $\vert a_n \vert \gt c_0^n$, which goes to infinity, so the terms do not go to $0$ and the series diverges (≈1:05:44–1:06:38): "it fails dramatically to be convergent" (≈1:04:09). □ The notes compare instead with the divergent geometric series $\sum r_0^n$: "Therefore, by the comparison test the original series is divergent" (notes p. 4).

## When the ratio or the root has no limit

Both tests assume that the ratio, or the $n$-th root, has a limit. "But what if it doesn't have a limit?" (Lecture 8, ≈1:19:46). That case is what $\limsup$ is for, which the Lecture 8 notes define and use to give the radius of convergence of a power series (notes pp. 6–7). The lecture does not reach it. See [limsup and liminf](limsup-and-liminf.md) and [power series](power-series.md).

## The alternating series test, sketched

Lecture 8 explains in words why the alternating harmonic series $\sum \frac{(-1)^n}{n}$ converges. Its partial sums go down to $-1$, back up but "you don't go as far up as you went down", down again by less, and so on, swinging in a shrinking interval (≈15:28–18:44). "And so you could make this more precise. It's quite easy" (≈18:44). This is "the basis for this alternating series test". In words, the test needs the signs of the terms to alternate and "the absolute value goes to 0" (≈18:44). The test is not stated precisely or proved; "We'll probably come back to that in a later lecture in a more general setting" (≈15:28). See [the harmonic series](harmonic-series.md#the-alternating-harmonic-series).

## The integral test, sketched

Colding mentions the integral test several times as the better way to handle the harmonic series and $\sum \frac{1}{n^2}$ (Lecture 7, ≈45:41, ≈48:06, ≈1:08:40). He sketches the idea in answer to a question at the end of Lecture 7 (≈1:21:28–1:22:19). For a series of non-negative numbers, picture each term as the area of a rectangle, so that the sum is a sum of areas, and compare it with "some curve and the area that lies below it" (≈1:22:19). In Lecture 8 it is "the typical thing to use" to show that $\sum \frac{1}{n^{\alpha}}$ converges for every $\alpha \gt 1$, to be discussed "at some later lecture" (Lecture 8, ≈11:16). The test is not stated.

## Not yet in this knowledge base

No proof of the second comparison test, and no statement or proof of the integral or alternating series tests. On the OCW lecture list, Lecture 9 is "Limsup and Liminf; Power Series; Continuous Functions; Exponential Function" (TBB Sections 2.13, 10.2, 5.4 and 5.5), which is not yet in this knowledge base.

## Lectures

- [Lecture 7 — Bolzano–Weierstrass Theorem; Cauchy Sequences; Series](07-bolzano-weierstrass-theorem-cauchy-sequences-series.md): the list of tests, the first comparison test, and in the notes the second comparison test and the ratio test.
- [Lecture 8 — Convergence Tests for Series; Power Series](08-convergence-tests-for-series-power-series.md): both comparison tests with two proofs of the first and the examples worked out, the ratio and root tests with proofs, the alternating series test sketched, and the ratio test applied to $\sum \frac{x^n}{n!}$.
