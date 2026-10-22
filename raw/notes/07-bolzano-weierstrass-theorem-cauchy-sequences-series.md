---
title: Lecture 7 — Bolzano–Weierstrass Theorem; Cauchy Sequences; Series (lecture notes)
lecture: 7
pages: 8
source_pdf: https://ocw.mit.edu/courses/18-100b-real-analysis-spring-2025/mit18_100b_s25_lec07.pdf
resource_page: https://ocw.mit.edu/courses/18-100b-real-analysis-spring-2025/resources/mit18_100b_s25_lec07_pdf/
numbering: PDF page N = printed page N (page 1 prints its number at the bottom, pages 2–7 in the running head; page 8 is the MIT OpenCourseWare back page, not lecture content). The notes have no equation numbers; the only lists are the unnumbered bullet lists of series tests (page 5) and of the ratio test cases (page 6).
figures: There are no figures. The small vector objects on pages 1–7 are all zero-height horizontal lines, that is fraction bars, not drawings; page 8's belong to the OCW back page.
---

# Lecture 7 — Bolzano–Weierstrass Theorem; Cauchy Sequences; Series: lecture notes

Full text of the course's written notes for Lecture 7 (MIT 18.100B/18.1002 Real Analysis, Spring 2025, Tobias Holck Colding), transcribed from the PDF. Cite as "notes p. N". The notes set the number sets in bold type, not blackboard bold, so they are written $\mathbf{R}$ here. The notes print no equation numbers. Page 8 is the OpenCourseWare citation page and is summarized, not transcribed as lecture content.

[wiki page for this lecture](../../wiki/07-bolzano-weierstrass-theorem-cauchy-sequences-series.md) · [transcript](../transcripts/07-bolzano-weierstrass-theorem-cauchy-sequences-series.md)

## Contents

| Section | Page(s) |
| --- | --- |
| Last time (recap); Bolzano-Weierstrass theorem (statement) and its proof by bisection | 1–2 |
| From Wikipedia: Karl Weierstrass | 2 |
| Series: partial sums $s_n$, convergence of a series | 2 |
| Geometric series: convergence for $\vert c \vert \lt 1$, the sum $\frac{1}{1-c}$, divergence otherwise | 2–3 |
| Harmonic series: divergence, with the estimate $s_{2^n - 1} \geq \frac{n}{2}$ | 3 |
| Absolutely convergent series; the example $\sum \frac{(-1)^n}{n}$; proof that absolutely convergent implies convergent | 3–4 |
| Theorem on series of non-negative numbers (convergent iff partial sums bounded above) | 4 |
| Example: $\sum \frac{1}{i^2}$ is convergent | 4–5 |
| Tests for convergence (list); comparison test, version 1, with example | 5 |
| Comparison test, version 2, with example | 6 |
| Ratio test, with Example 1 ($\frac{1}{n}$) and Example 2 ($\frac{1}{n^2}$) | 6–7 |
| References | 7 |
| OpenCourseWare back page | 8 |

## Printed slips

These are in the PDF as printed; the body below keeps them as printed.

- Page 1: "Weirstrass" should be "Weierstrass" (four places on page 1: "Bolzano-Weirstrass theorem." under Last time, "the Bolzano-Weirstrass implies the Cauchy theorem", the bold label "Bolzano-Weirstrass theorem" and "(of the Bolzano-Weirstrass theorem.)"). Page 2 spells it correctly in the Wikipedia quotation.
- Page 1: "the Bolzano-Weirstrass implies the Cauchy theorem" is missing the word "theorem" after Bolzano-Weierstrass.
- Page 1: "infinite many $n$" and "infinite many such $a_n$" should be "infinitely many".
- Page 1: "infinitely many $a_n$ lies in" and "infinitely many lies in" should be "lie".
- Page 1: "all the element $a_{n_i}$" should be "elements".
- Pages 1–2: "converges to the same number" (of $b_k$ and $c_k$) and "they also converges to that same number" should be "converge".
- Page 2: "if it do we also write" should be "does".
- Page 3: the harmonic series is printed as "the series is $\sum_{i=1}^{\infty} \frac{1}{2}$" where $\frac{1}{i}$ is meant ($a_n = \frac{1}{n}$ is stated just before, and the estimate that follows sums $\frac{1}{i}$).
- Page 4: "is Cauchy sequence if the series" is missing "a" ("is a Cauchy sequence").
- Page 4: the line $s_{n+1} = s_n + a_n \geq s_n$, in the proof of the theorem on non-negative series: with $s_n = \sum_{i=0}^{n} a_i$ the added term is $a_{n+1}$, not $a_n$.
- Page 4: "there exist $M$ such that for all $n$" should be "exists".
- Page 5: "This show the induction step" should be "shows".

Not a slip, but worth knowing: the notes leave some steps unstated and vary their notation. They are reproduced as printed.

- Page 1: under Last time the Cauchy convergence theorem is stated only as "Every Cauchy sequence is convergent"; Lecture 6's notes stated it as an if and only if.
- Page 1: in the proof of the Bolzano-Weierstrass theorem, only the case $a_n \in [0, 1]$ is treated ("for simplicity"). The notes do not say how the general bounded case follows. They also do not justify the bound $\vert a_{n_{k_1}} - a_{n_{k_2}} \vert \leq 2^{1-k}$ beyond the description of the halving, and they observe that it makes $a_{n_k}$ a Cauchy sequence without using that fact: "However, more is true", and the proof goes on to squeeze $a_{n_k}$ between $b_k$ and $c_k$.
- Page 2: the series is introduced with the index starting at 1 ($s_n = \sum_{i=1}^{n} a_i$), the geometric series starts at $i = 0$ ($a_n = c^n$, $s_n = \sum_{i=0}^{n} c^i$), the harmonic series at $i = 1$, and the absolute convergence discussion on pages 3–4 and the non-negative series theorem on page 4 start at $0$ and write the terms as $a_n$ or $a_i$ interchangeably. The notes do not comment on these changes.
- Pages 2–3: the geometric series is said to be "convergent precisely when $\vert c \vert \lt 1$"; the proof given covers $c \neq 1$ via $s_n = \frac{1 - c^{n+1}}{1 - c}$ and leaves the cases $\vert c \vert \gt 1$ and $c = -1$ (divergence) and $c = 1$ ("one easily checks, separately") without further argument.
- Page 3: in the harmonic series estimate, the first step $s_{2^{n+1}-1} \geq s_{2^n - 1} + \sum_{i=2^n}^{2^{n+1}-1} \frac{1}{i}$ is printed with $\geq$ where the two sides are equal, and the step $2^n \frac{1}{2^{n+1} - 1} \geq \frac{1}{2}$ is not explained.
- Page 3: "Absolutely convergent implies convergent but not the other way around" is followed by the example $\sum \frac{(-1)^n}{n}$, whose convergence is deferred ("We will see later").
- Page 4: the proof that absolutely convergent implies convergent writes the partial sums of $\sum \vert a_i \vert$ as a bold $\mathbf{s}_ n$ (in red in the PDF) to distinguish it from $s_n = \sum_{i=0}^{n} a_i$; the last line of the proof, that $s_n$ is Cauchy because $\mathbf{s}_ n$ is, uses that the convergent sequence $\mathbf{s}_ n$ is a Cauchy sequence. That is the direction of the Cauchy convergence theorem (convergent implies Cauchy) which the recap on page 1 does not state and which the Lecture 6 notes do not prove.
- Page 4: in the example $\sum \frac{1}{i^2}$, the claim $s_{2^n-1} \leq \sum_{i=0}^{n-1} \left(\frac{1}{2}\right)^i$ is proved by induction on page 5; the inductive step uses the induction hypothesis and the estimate $\frac{1}{i^2} \leq \frac{1}{(2^n)^2}$ for $i \geq 2^n$ without saying so.
- Page 5: the list of tests names the Comparison test, Ratio test and Root test; the Root test is not stated in these notes.
- Page 6: the ratio test is stated for $a_n \geq 0$ with $\frac{a_{n+1}}{a_n} \to a$ and does not say that $a_n \gt 0$ is needed for the quotient to be defined; no proof is given.

---

## Page 1

SPRING 2025 - 18.100B/18.1002

TOBIAS HOLCK COLDING

**Lecture 7**

**Last time:**

Cauchy convergence theorem: Every Cauchy sequence is convergent.

Bolzano-Weirstrass theorem.

Last time we showed that the Bolzano-Weirstrass implies the Cauchy theorem.

**Bolzano-Weirstrass theorem**: Any bounded sequence has a convergent subsequence.

*Proof.* (of the Bolzano-Weirstrass theorem.) Suppose that $a_n$ is a bounded sequence. For simplicity assume that $a_n \in [0, 1]$.

Defining the subsequence $a_{n_k}$. Either there are infinite many $n$ such that $a_n \in [0, \frac{1}{2}]$ or there are infinite many such $a_n$ in $[\frac{1}{2}, 1]$ (or both). Assume that there are infinitely many in $[0, \frac{1}{2}]$. Set $a_{n_1} = a_1$. Let $a_{n_2}$ be the next $a_n$ such that $a_n \in [0, \frac{1}{2}]$. We have

$$
n_2 \gt n_1 = 1 ,
$$

$$
a_{n_1} \in [0, 1] ,
$$

$$
a_{n_2} \in \left[ 0, \frac{1}{2} \right] .
$$

Next either infinitely many $a_n$ lies in $[0, \frac{1}{4}]$ or infinitely many $a_n$ lies in $[\frac{1}{4}, \frac{1}{2}]$. Assume that infinitely many lies in $[\frac{1}{4}, \frac{1}{2}]$. Pick an $n \gt n_2$ such that $a_n \in [\frac{1}{4}, \frac{1}{2}]$ and set $a_{n_3} = a_n$. We continue this way.

Convergence of $a_{n_k}$. Note that for $k_1, k_2 \geq k$ we have that

$$
\vert a_{n_{k_1}} - a_{n_{k_2}} \vert \leq 2^{1-k} .
$$

Since $2^{-k} \to 0$ as $k \to \infty$ this shows that the subsequence $a_{n_k}$ is a Cauchy sequence. However, more is true. Squeezed between two other sequences $b_k \leq a_{n_k} \leq c_k$. We will define sequences $b_k$ and $c_k$ as follows. The sequence $b_k$ will be the left endpoint of the interval of length $2^{1-k}$ that all the element $a_{n_i}$ will lie in when $i \geq k$ and $c_k$ will be the right end point of the same interval. We have now that the sequence $b_k$ is increasing and the sequence $c_k$ is decreasing and the $a_{n_k}$ are squeezed between the two. It follows that $b_k$ is convergent (as it is also bounded) and likewise for $c_k$. Since $c_k - b_k = 2^{1-k}$ it follows that $b_k$ and $c_k$ converges to the

1

## Page 2

2 — TOBIAS HOLCK COLDING

same number and since the later $a_{n_k}$ are all squeezed between the two they also converges to that same number. $\square$

From Wikipedia: Karl Theodor Wilhelm Weierstrass (1815 – 1897) was a German mathematician often cited as the ”father of modern analysis”. Despite leaving university without a degree, he studied mathematics and trained as a school teacher, eventually teaching mathematics, physics, botany and gymnastics. Among many other contributions, Weierstrass formalized the definition of the continuity of a function and complex analysis, proved the intermediate value theorem and the Bolzano–Weierstrass theorem, and used the latter to study the properties of continuous functions on closed bounded intervals.

**Series**: Suppose that $a_n$ is a sequence, we can form a new sequence $s_n$ as follows. We let

$$
s_1 = a_1 ,
$$

$$
s_2 = a_1 + a_2
$$

$$
s_3 = a_1 + a_2 + a_3 ,
$$

and in general set

$$
s_n = a_1 + \cdots + a_n = \sum_{i=1}^{n} a_i .
$$

A series $\sum_{i=1}^{\infty} a_i$ converges if the sequence $s_n$ converges and if it do we also write $\sum_{i=1}^{\infty} a_i$ for the limit.

**Geometric series:** Suppose now that $a_n = c^n$ so the series is

$$
s_n = \sum_{i=0}^{n} c^i .
$$

This is the geometric series. It is convergent precisely when $\vert c \vert \lt 1$. Moreover, when $\vert c \vert \lt 1$, then the limit (infinite sum) is

$$
\sum_{i=0}^{\infty} c^i = \frac{1}{1 - c} .
$$

To see this observe that

$$
(1 - c) \sum_{i=0}^{n} c^i = 1 - c^{n+1} .
$$

It follows from this that if $c \neq 1$, then

$$
s_n = \sum_{i=0}^{n} c^i = \frac{1 - c^{n+1}}{1 - c} .
$$

## Page 3

SPRING 2025 - 18.100B/18.1002 — 3

Therefore, $s_n$ converges with limit $\frac{1}{1-c}$ if $\vert c \vert \lt 1$ and diverges if $\vert c \vert \gt 1$ or $c = -1$. One easily checks, separately, that it also diverges for $c = 1$.

**Harmonic series**: For the harmonic series $a_n = \frac{1}{n}$ so the series is $\sum_{i=1}^{\infty} \frac{1}{2}$. This series is divergent. To see this we will show that

$$
s_{2^n - 1} \geq \frac{n}{2} .
$$

This is true for $n = 1$ as $s_1 = 1 \geq \frac{1}{2}$.

Assume that it is true for $n$ we will show that it is also true for $n + 1$. Namely,

$$
s_{2^{n+1} - 1} \geq s_{2^n - 1} + \sum_{i=2^n}^{2^{n+1} - 1} \frac{1}{i} \geq \frac{n}{2} + 2^n \frac{1}{2^{n+1} - 1} \geq \frac{n}{2} + \frac{1}{2} = \frac{n+1}{2} .
$$

So the formula also holds for $n + 1$ and therefore for all $n$.

Since $\frac{n}{2} \to \infty$ it follows that the subsequence $s_{2^n - 1}$ is divergent and therefore so is the original series.

**Absolutely convergent;** We say that a series

$$
\sum_{n=0}^{\infty} a_n
$$

is absolutely convergent if the series

$$
\sum_{n=0}^{\infty} \vert a_n \vert
$$

is convergent. Absolutely convergent implies convergent but not the other way around.

**Example**: We will see later that the series

$$
\sum_{n=1} \frac{(-1)^n}{n}
$$

is convergent but if we take the absolute values of the $a_n$'s, then we get the harmonic series which is divergent.

*Proof.* (of why absolutely convergent implies convergent.) By the Cauchy convergence theorem we only need to show that the sequence

$$
\sum_{i=0}^{\infty} a_i
$$

## Page 4

4 — TOBIAS HOLCK COLDING

is Cauchy sequence if the series

$$
\sum_{n=0}^{\infty} \vert a_n \vert
$$

is convergent. Set

$$
s_n = \sum_{i=0}^{n} a_i ,
$$

$$
\mathbf{s}_ n = \sum_{i=0}^{n} \vert a_i \vert .
$$

For $m \lt n$ we have

$$
\vert s_n - s_m \vert = \vert a_n + \cdots + a_{m+1} \vert \leq \vert a_n \vert + \cdots + \vert a_{m+1} \vert = \vert \mathbf{s}_ n - \mathbf{s}_ m \vert .
$$

Since the sequence $\mathbf{s}_ n$ is a Cauchy sequence it now follows that $s_n$ is. $\square$

**Theorem**: A series of non-negative numbers

$$
\sum_{i=0}^{\infty} a_i ,
$$

where $a_n \geq 0$, is convergent if and only if the sequence $s_n$ is bounded from above.

*Proof.* The sequence $s_n$ is monotone nondecreasing since

$$
s_{n+1} = s_n + a_n \geq s_n .
$$

The claim now follows from the monotone convergence theorem. $\square$

**Example**: The series

$$
\sum_{i=1}^{\infty} \frac{1}{i^2}
$$

is convergent. This is a sequence of non-negative numbers so we only need to show that there exist $M$ such that for all $n$

$$
s_n = \sum_{i=1}^{n} \frac{1}{i^2} \leq M .
$$

Claim:

$$
s_{2^n - 1} \leq \sum_{i=0}^{n-1} \left( \frac{1}{2} \right)^i .
$$

This would be enough because the last is a convergent geometric series so in particular bounded.

## Page 5

SPRING 2025 - 18.100B/18.1002 — 5

We will show this by induction. For $n = 1$ we have that

$$
s_1 = 1 = \left( \frac{1}{2} \right)^0 .
$$

So it is correct for $n = 1$. Assume next that it is true for $n$; we will show that it also holds for $n + 1$.

$$
s_{2^{n+1} - 1} = s_{2^n - 1} + \sum_{i=2^n}^{2^{n+1} - 1} \frac{1}{i^2} \leq \sum_{i=0}^{n-1} \left( \frac{1}{2} \right)^i + 2^n \frac{1}{(2^n)^2}
$$

$$
\leq \sum_{i=0}^{n-1} \left( \frac{1}{2} \right)^i + \frac{1}{2^n} = \sum_{i=0}^{n} \left( \frac{1}{2} \right)^i .
$$

This show the induction step and completes the proof.

To help determine whether or not a series converges there are a number of tests:

- Comparison test.
- Ratio test.
- Root test.

**Comparison test; version 1**: Suppose that $a_n$ and $b_n$ are two sequences with

$$
0 \leq a_n \leq b_n .
$$

If

$$
\sum_{n=1}^{\infty} b_n
$$

is convergent, then so is

$$
\sum_{n=1}^{\infty} a_n .
$$

**Example**: The series

$$
\sum_{n=1}^{\infty} \frac{2^{-n}}{n}
$$

is convergent. Namely, if we set

$$
a_n = \frac{2^{-n}}{n}
$$

and

$$
b_n = 2^{-n} ,
$$

then $0 \leq a_n \leq b_n$ and since the series $\sum_{n=1}^{\infty} b_n$ is convergent, then by the comparison test so is the series $\sum_{n=1}^{\infty} a_n$.

## Page 6

6 — TOBIAS HOLCK COLDING

**Comparison test; version 2**: Suppose that $a_n$ and $b_n$ are two sequences with $b_n \neq 0$ and

$$
\lim_{n \to \infty} \frac{a_n}{b_n} = L \neq 0 ,
$$

The series

$$
\sum_{n=1}^{\infty} a_n
$$

is convergent if and only if

$$
\sum_{n=1}^{\infty} b_n
$$

is.

**Example**: The series

$$
\sum_{n=2}^{\infty} \frac{1}{n^2 - 1}
$$

is convergent since

$$
\frac{n^2}{n^2 - 1} \to 1 ,
$$

and the series

$$
\sum_{n=2}^{\infty} \frac{1}{n^2}
$$

is convergent.

**Ratio test**: Let $a_n \geq 0$ and assume that

$$
\frac{a_{n+1}}{a_n} \to a
$$

. If

- $a \lt 1$, then the series $\sum a_n$ is convergent.
- $a \gt 1$, then the series $\sum a_n$ is divergent.
- $a = 1$, it is inconclusive.

**Example 1**:

$$
a_n = \frac{1}{n} .
$$

In this case

$$
\frac{a_{n+1}}{a_n} \to 1
$$

so the test is inconclusive, but the series is divergent.

## Page 7

SPRING 2025 - 18.100B/18.1002 — 7

**Example 2**:

$$
a_n = \frac{1}{n^2} .
$$

In this case

$$
\frac{a_{n+1}}{a_n} \to 1
$$

so the test is inconclusive, but the series is convergent.

REFERENCES

[TBB] B.S. Thomson, J.B. Bruckner, and A.M. Bruckner, *Elementary Real Analysis, 2nd edition*
TBB can be downloaded at:
https://classicalrealanalysis.info/com/documents/TBB-AllChapters-Landscape.pdf
(screen-optimized)
https://classicalrealanalysis.info/com/documents/TBB-AllChapters-Portrait.pdf
(print-optimized)

MIT, Dept. of Math., 77 Massachusetts Avenue, Cambridge, MA 02139-4307.

## Page 8

MIT OpenCourseWare back page (not lecture content): "MIT OpenCourseWare https://ocw.mit.edu — 18.100B Real Analysis — Spring 2025 — For information about citing these materials or our Terms of Use, visit: https://ocw.mit.edu/terms."
