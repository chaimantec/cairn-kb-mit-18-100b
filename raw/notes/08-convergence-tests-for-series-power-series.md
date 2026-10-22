---
title: Lecture 8 — Convergence Tests for Series; Power Series (lecture notes)
lecture: 8
pages: 8
source_pdf: https://ocw.mit.edu/courses/18-100b-real-analysis-spring-2025/mit18_100b_s25_lec08.pdf
resource_page: https://ocw.mit.edu/courses/18-100b-real-analysis-spring-2025/resources/mit18_100b_s25_lec08_pdf/
numbering: PDF page N = printed page N (page 1 prints its number at the bottom, pages 2–7 in the running head; page 8 is the MIT OpenCourseWare back page, not lecture content). The notes have no equation numbers; the only lists are the unnumbered bullet lists of series tests (page 2), of the ratio test cases (page 3), of the root test cases (page 4) and of four power series (pages 4–5).
figures: There are no figures. The PDF has no raster images, and the small vector objects on pages 1–7 are all fraction bars, not drawings; page 8's belong to the OCW back page.
---

# Lecture 8 — Convergence Tests for Series; Power Series: lecture notes

Full text of the course's written notes for Lecture 8 (MIT 18.100B/18.1002 Real Analysis, Spring 2025, Tobias Holck Colding), transcribed from the PDF. Cite as "notes p. N". The notes set the number sets in bold type, not blackboard bold, so they are written $\mathbf{R}$ here (this lecture's notes happen not to print a number set). The notes print no equation numbers. In the PDF some labels and sentences are coloured (red, blue, green); the colour is noted where it occurs. Page 8 is the OpenCourseWare citation page and is summarized, not transcribed as lecture content.

[wiki page for this lecture](../../wiki/08-convergence-tests-for-series-power-series.md) · [transcript](../transcripts/08-convergence-tests-for-series-power-series.md)

## Contents

| Section | Page(s) |
| --- | --- |
| Series: partial sums $s_n$, convergence of a series | 1 |
| Geometric series (statement: convergent precisely when $\vert c \vert \lt 1$) | 1 |
| Harmonic series (statement: divergent) | 1 |
| Absolutely convergent series (definition) | 1–2 |
| Theorem on series of non-negative numbers (convergent iff partial sums bounded above) | 2 |
| Tests for convergence (list); comparison test, version 1, with example | 2 |
| Comparison test, version 2, with example | 3 |
| Ratio test, with Example 1 ($\frac{1}{n}$) and Example 2 ($\frac{1}{n^2}$) | 3–4 |
| Root test and its proof | 4 |
| Power series: four examples, formal definition, the two questions | 4–5 |
| Example: $\sum \frac{x^n}{n!}$ by the ratio test; example $\sum x^n$ | 5 |
| $\limsup$; radius of convergence $R$; convention; convergence for $\vert x \vert \lt R$ and $\vert x \vert \gt R$ | 6–7 |
| References | 7 |
| OpenCourseWare back page | 8 |

## Printed slips

These are in the PDF as printed; the body below keeps them as printed.

- Page 1: "if it do we also write" should be "does".
- Page 1: the geometric series is printed as a sum over $i$ from $0$ to $\infty$ of $c^{i}n$: the exponent is $i$ and a baseline $n$ follows the $c^i$ (in the text layer the $i$ is a raised 8-point exponent and the $n$ sits on the baseline beside $c$). The index of the sum is $i$ and the summand has a stray $n$; presumably $c^i$ is meant, which is the geometric series the page then says converges precisely when $\vert c \vert \lt 1$.
- Page 1: the harmonic series is printed as the sum over $i$ from $1$ to $\infty$ of $\frac{1}{n}$: the index is $i$ but the summand is in $n$, so as printed the summand does not depend on the index. Presumably $\frac{1}{i}$ is meant (or the index letter $n$).
- Page 5: "Formel definition" should be "Formal definition".
- Page 6: "The power series in convergent if $\vert x \vert \lt R$" should be "is convergent".
- Page 7: "The case of where $\vert x \vert = R$" should be "The case where".

Not a slip, but worth knowing: the notes leave many steps unstated and vary their notation. They are reproduced as printed.

- Which statements are proved. Only the root test (page 4) is proved. Everything else is stated without proof on these pages: that the geometric series is convergent precisely when $\vert c \vert \lt 1$ and the harmonic series divergent (page 1, no sum formula and no estimate), that absolutely convergent implies convergent (page 2, "but not the other way around" has no example), the theorem on non-negative series (page 2), the comparison test in both versions, the ratio test, the claim that $\sum x^n$ converges for $\vert x \vert \lt 1$ and diverges otherwise (page 5), and the claim "From the root test one can now show the following" (page 6) that the power series converges for $\vert x \vert \lt R$ and diverges for $\vert x \vert \gt R$. The Lecture 7 notes carry proofs of several of the first group; these pages do not refer back to them.
- Page 2: the theorem on non-negative series says "the sequence $s_n$" but this series starts at $i = 0$ while $s_n$ was defined on page 1 as a sum starting at $i = 1$.
- Indices and letters change from display to display without comment: the series is introduced from $i = 1$ (page 1), the geometric series from $i = 0$, the harmonic series from $i = 1$, absolute convergence and the non-negative theorem from $0$, the comparison tests from $n = 1$, the example of version 2 from $n = 2$, the root test and the power series from $n = 0$. The terms are written $a_n$ or $a_i$ interchangeably. The coefficients of a power series are $c_n$ in the formal definition (page 5) and $a_n$ in the definition of the radius of convergence (page 6); on page 5 $a_n$ also names the terms $\frac{x^n}{n!}$ of the example.
- Page 3: comparison test, version 2, requires $b_n \neq 0$ and $L \neq 0$ but does not say that $a_n$ and $b_n$ are non-negative (version 1 does say $0 \leq a_n \leq b_n$). In the example the sequences are not named: they are presumably $a_n = \frac{1}{n^2 - 1}$ and $b_n = \frac{1}{n^2}$, from the displayed quotient $\frac{n^2}{n^2 - 1} \to 1$, and the convergence of $\sum \frac{1}{n^2}$ is asserted, not shown.
- Page 3: the ratio test is stated for $a_n \geq 0$ with $\frac{a_{n+1}}{a_n} \to a$ and does not say that $a_n \gt 0$ is needed for the quotient to be defined. In Examples 1 and 2 (pages 3–4) the limit $\frac{a_{n+1}}{a_n} \to 1$ is stated, not computed, and the divergence of $\sum \frac{1}{n}$ and convergence of $\sum \frac{1}{n^2}$ are asserted with no argument.
- Page 4: the root test is stated with $\lim_{n\to\infty}(a_n)^{\frac{1}{n}} = r$ for $a_n \geq 0$ and sums from $n = 0$, where $(a_0)^{\frac{1}{0}}$ is not defined. The comparison test (page 2) is stated with sums from $n = 1$. The notes say nothing about either.
- Page 4: in the proof of the root test, "It follows that for $r \lt r_0 \lt 1$, there exists $N$ such that if $n \geq N$, then $(a_n)^{\frac{1}{n}} \leq r_0$" uses the definition of the limit without saying so, and no choice of $r_0$ is given. The next line "Therefore, $0 \leq a_n \leq r_0^n$" is printed without "for $n \geq N$", although the previous line holds only for $n \geq N$; the comparison test (version 1, stated for all $n$) is then applied without a remark on the first $N$ terms. The same holds for the case $r \gt 1$, where the notes also use the divergence of the geometric series $\sum r_0^n$ for $r_0 \gt 1$ (page 1 says only that the geometric series is "convergent precisely when $\vert c \vert \lt 1$") and conclude "by the comparison test the original series is divergent", although version 1 as stated derives convergence from convergence: the divergence follows from its contrapositive, which the notes do not state. The case $r = 1$ is stated as inconclusive with no example.
- Pages 4–5: the four power series are listed with no range of $x$ given for any of them, and with $\exp x$, $\cos x$ and $\sin x$ not defined anywhere else in these notes; the first is later said (page 5) to converge only for $\vert x \vert \lt 1$. The two questions on page 5 are posed; the second ("Why does it give familiar functions?") is promised "next time for the exponential function".
- Page 5: the ratio test is applied to $a_n = \frac{x^n}{n!}$ although the test is stated for $a_n \geq 0$, and these terms are not non-negative for $x \lt 0$ (and the quotient is not defined at $x = 0$). The notes conclude "the power series is convergent for all $x$" from $\frac{x}{n+1} \to 0$ without saying how negative $x$ is handled.
- Page 6: the $\limsup$ definition has two cases. If $a_n$ is not bounded from above, $\limsup a_n$ is set to $\infty$. Otherwise $b_n = \sup\lbrace a_n, a_{n+1}, a_{n+2}, \cdots \rbrace$ is a real number for each $n$, the sequence $b_n$ is "decreasing" (each term at most the one before, the course's sense of the word), and "it is converging with limit $b$ that possibly could be $-\infty$": the notes do not prove this monotone-limit statement, nor say that a limit of $-\infty$ means convergence in an extended sense.
- Page 6: the radius of convergence is defined by $R = \frac{1}{\limsup_{n\to\infty} \vert a_n \vert^{\frac{1}{n}}}$, with the convention covering $0$ (then $R = \infty$) and $\infty$ (then $R = 0$). The sentence "R is said to be the radius of convergence" is printed before the convention, which is needed for the formula to make sense in these cases.
- Page 7: the case $\vert x \vert = R$ is left "to be examined on a case by case basis", with no example.

---

## Page 1

SPRING 2025 - 18.100B/18.1002

TOBIAS HOLCK COLDING

**Lecture 8** (red in the PDF)

**Series** (red label): Suppose that $a_n$ is a sequence, we can form a new sequence $s_n$ as follows. We let

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

**Geometric series:** (red label)

$$
\sum_{i=0}^{\infty} c^{i} n .
$$

Convergent precisely when $\vert c \vert \lt 1$.

**Harmonic series** (red label):

$$
\sum_{i=1}^{\infty} \frac{1}{n} .
$$

This series is divergent.

**Absolutely convergent**; (red label) We say that a series

$$
\sum_{n=0}^{\infty} a_n
$$

1

## Page 2

2 — TOBIAS HOLCK COLDING

is absolutely convergent if the series

$$
\sum_{n=0}^{\infty} \vert a_n \vert
$$

is convergent. Absolutely convergent implies convergent but not the other way around.

**Theorem**: A series of non-negative numbers $a_n \geq 0$

$$
\sum_{i=0}^{\infty} a_i ,
$$

is convergent if and only if the sequence $s_n$ is bounded from above.

To help determine whether or not a series converges there are a number of tests:

- Comparison test.
- Ratio test.
- Root test.
- Other tests that we will discuss later.

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

## Page 3

SPRING 2025 - 18.100B/18.1002 — 3

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

.

If

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

## Page 4

4 — TOBIAS HOLCK COLDING

**Example 2**:

$$
a_n = \frac{1}{n^2} .
$$

In this case

$$
\frac{a_{n+1}}{a_n} \to 1
$$

so the test is inconclusive, but the series is convergent.

**Root test**: Let $a_n \geq 0$ be a sequence of non-negative numbers. Suppose $\lim_{n \to \infty} (a_n)^{\frac{1}{n}} = r$. If

- $r \lt 1$, then the series $\sum_{n=0}^{\infty} a_n$ is convergent.
- $r \gt 1$, then the series $\sum_{n=0}^{\infty} a_n$ is divergent.
- $r = 1$, then it is inconclusive.

*Proof.* (of root test.) Suppose that $r \lt 1$. It follows that for $r \lt r_0 \lt 1$, there exists $N$ such that if $n \geq N$, then

$$
(a_n)^{\frac{1}{n}} \leq r_0 .
$$

Therefore,

$$
0 \leq a_n \leq r_0^n .
$$

However, the series $\sum_{n=0}^{\infty} r_0^n$ is a geometric series that is convergent since $r_0 \lt 1$. We now have by the first version of the comparison test that also the series $\sum_{n=0}^{\infty} a_n$ is convergent.

Suppose that $r \gt 1$. In that case we have that for $1 \lt r_0 \lt r$, there exists $N$ such that if $n \geq N$, then

$$
(a_n)^{\frac{1}{n}} \geq r_0 .
$$

Hence, for $n \geq N$

$$
a_n \geq r_0^n ,
$$

where, the series $\sum_{n=0}^{\infty} r_0^n$ is a divergent geometric series. Therefore, by the comparison test the original series is divergent. $\square$

**Power series** (blue label):

$$
\sum_{n=0}^{\infty} x^n = \frac{1}{1 - x} .
$$

$$
\sum_{n=0}^{\infty} \frac{x^n}{n!} = \exp x .
$$

(In the PDF these displays are a bulleted list: each bullet marker stands alone on a line with its formula below it, and the list continues on page 5. They are written here as plain displays so that they render.)

## Page 5

SPRING 2025 - 18.100B/18.1002 — 5

$$
\sum_{n=0}^{\infty} (-1)^n \frac{x^{2n}}{(2n)!} = \cos x .
$$

$$
\sum_{n=0}^{\infty} (-1)^n \frac{x^{2n+1}}{(2n+1)!} = \sin x .
$$

**Formel definition**: Let $c_n$ be a sequence, then $\sum_{n=0}^{\infty} c_n x^n$ is a power series.

When does a power series converge? (the whole sentence is red in the PDF)

Why does it give familiar functions? (the whole sentence is blue in the PDF)

We will answer the second question next time for the exponential function.

The answer to the first question comes from the root test or the ratio test.

**Example**: Consider the power series:

$$
\sum_{n=0}^{\infty} \frac{x^n}{n!} .
$$

By the ratio test with $a_n = \frac{x^n}{n!}$ we have

$$
\frac{a_{n+1}}{a_n} = \frac{n! \thinspace x^{n+1}}{(n+1)! \thinspace x^n} = \frac{x}{n+1} \to 0 .
$$

It follows that the power series is convergent for all $x$.

**Example**:

$$
\sum_{n=0}^{\infty} x^n .
$$

This series is convergent for $\vert x \vert \lt 1$ and divergent otherwise.

## Page 6

6 — TOBIAS HOLCK COLDING

To talk about convergence of a general power series we need the notion of lim sup (the words "lim sup" are red in the PDF) of a sequence. This is defined as follows.

Let $a_n$ be a sequence. If it is not bounded from above, then we set $\limsup a_n$ to be $\infty$. Otherwise we will define a new sequence $b_n$ from $a_n$ as follows.

$$
b_n = \sup \lbrace a_n, a_{n+1}, a_{n+2}, \cdots \rbrace .
$$

Note that since we are assuming that the $a_n$'s are bounded from above the $b_n$'s are real numbers and the sequence $b_n$ is decreasing. – It is decreasing since

$$
b_n = \sup \lbrace a_n, a_{n+1}, a_{n+2}, \cdots \rbrace \geq \sup \lbrace a_{n+1}, a_{n+2}, \cdots \rbrace = b_{n+1} .
$$

(For $b_{n+1}$ supremum is taken over a smaller set.)

Since the sequence $b_n$ is decreasing it is converging with limit $b$ that possibly could be $-\infty$ if the sequence $b_n$ is not bounded from below.

**Definition** (of lim sup) (the parenthesis is blue in the PDF):

$$
\limsup_{n \to \infty} a_n = \lim_{n \to \infty} b_n = b .
$$

Back to power series. Suppose that

$$
\sum_{n=0}^{\infty} a_n x^n
$$

is a power series. Set

$$
R = \frac{1}{\limsup_{n \to \infty} \vert a_n \vert^{\frac{1}{n}}} .
$$

$R$ is said to be the radius of convergence (the words "radius of convergence" are blue in the PDF).

Convention (the word "Convention" is green in the PDF): If $\limsup_{n \to \infty} \vert a_n \vert^{\frac{1}{n}} = 0$, then the radius of convergence is said to be $\infty$. If $\limsup_{n \to \infty} \vert a_n \vert^{\frac{1}{n}} = \infty$, then we set $R = 0$.

From the root test one can now show the following:

The power series in convergent if $\vert x \vert \lt R$ and divergent if $\vert x \vert \gt R$.

## Page 7

SPRING 2025 - 18.100B/18.1002 — 7

The case of where $\vert x \vert = R$ has to be examined on a case by case basis.

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
