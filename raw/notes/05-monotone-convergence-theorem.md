---
title: Lecture 5 — Monotone Convergence Theorem (lecture notes)
lecture: 5
pages: 8
source_pdf: https://ocw.mit.edu/courses/18-100b-real-analysis-spring-2025/mit18_100b_s25_lec05.pdf
resource_page: https://ocw.mit.edu/courses/18-100b-real-analysis-spring-2025/resources/mit18_100b_s25_lec05_pdf/
numbering: PDF page N = printed page N (page 1 prints its number at the bottom, pages 2–7 in the running head; page 8 is the MIT OpenCourseWare back page, not lecture content). The notes have no equation numbers; the four algebraic properties of limits are numbered (1)–(4) in the notes.
figures: There are no figures. The small vector objects on pages 1–4 are fraction bars and radical rules, not drawings; page 8's belong to the OCW back page.
---

# Lecture 5 — Monotone Convergence Theorem: lecture notes

Full text of the course's written notes for Lecture 5 (MIT 18.100B/18.1002 Real Analysis, Spring 2025, Tobias Holck Colding), transcribed from the PDF. Cite as "notes p. N". The notes set the number sets in bold type, not blackboard bold, so they are written $\mathbf{N}$, $\mathbf{R}$ here. The notes print no equation numbers. Page 8 is the OpenCourseWare citation page and is summarized, not transcribed as lecture content.

[wiki page for this lecture](../../wiki/05-monotone-convergence-theorem.md) · [transcript](../transcripts/05-monotone-convergence-theorem.md)

## Contents

| Section | Page(s) |
| --- | --- |
| Sequences as functions $f : \mathbf{N} \to \mathbf{R}$; limit, convergent, divergent | 1 |
| Theorem: a convergent sequence is bounded (statement only) | 1 |
| Basic algebraic properties of limits: statement of (1)–(4) | 1 |
| Subsequence: definition | 1 |
| Example: $a_n = \frac{n^2 + 1}{n^2 + n + 1}$ converges to 1 | 2 |
| Monotone convergence theorem: increasing and decreasing versions | 2 |
| $\sqrt{2}$ as the limit of the decimals: $a_n = \frac{b_n}{10^{n-1}}$ increasing and bounded | 3 |
| Showing that the limit $a$ satisfies $a^2 = 2$ | 4 |
| Proof of the monotone convergence theorem (increasing version) | 5 |
| Cauchy sequence; theorem: convergent if and only if Cauchy | 6 |
| Fixed points, contracting map, contracting mapping theorem (statements); next time | 6 |
| References | 6–7 |
| OpenCourseWare back page | 8 |

## Printed slips

These are in the PDF as printed; the body below keeps them as printed.

- Page 1: "the sequence is convergenet" should be "convergent".
- Page 1: "A sequence that is not covergent" should be "convergent".
- Page 1: "Suppose that $a_n$ and $b_n$ are convergenet sequences" should be "convergent".
- Page 1: item (1) says that $c_n = C \thinspace a_n$ "is convergenet", which should be "convergent".
- Page 3: in the sentence that $b_n \leq 2 \cdot 10^{n-1}$, the reason is printed as $(2 \cdot 10^{2n-2})^2 \gt 2 \cdot 10^{2n-2}$; the exponent inside the parenthesis should be $n-1$, as in the claim it supports on the same line. The span layer confirms the printed $2n-2$. On the board Colding squares 2 times 10 to the power $n - 1$ and gets 4 times 10 to the power $2n - 2$ (transcript ≈54:12–54:57).
- Page 4: "This show that $a^2 \leq 2$" should be "shows".
- Page 6: "(Tail of the sequence bunch together.)" should be "bunches" (or "Tails of the sequence").
- Page 6: "Existence of fixed points for a maps" should be "a map" (or "for maps").

Not a slip, but worth knowing: the notes leave some steps unstated or use a different form from Lecture 4. They are reproduced as printed.

- Page 1: the boundedness theorem, the algebraic properties and the subsequence definition are restated without proofs. Property (4) here is printed for $c_n = \frac{1}{b_n}$ with limit $\frac{1}{b}$, whereas the Lecture 4 notes print it for a quotient $\frac{a_n}{b_n}$.
- Page 1: the subsequence is written $b_k = f(g(k))$ and "often" as $a_{n_k}$; the notes do not say that $n_k$ stands for $g(k)$.
- Page 2: the example $a_n = \frac{n^2+1}{n^2+n+1}$ is shown to converge to 1 by dividing numerator and denominator by $n^2$ and citing the algebraic properties; the step that the quotient of the two limits gives 1 is left to the reader.
- Page 2: the monotone convergence theorem is stated for a sequence "bounded from above" in the increasing version and "bounded" in the decreasing version; the decreasing version is not proved ("proven similarly", page 5).
- Page 3: even with the exponent read as $n-1$, the page does not spell out how $(2 \cdot 10^{n-1})^2 \gt 2 \cdot 10^{2n-2}$ gives $b_n \leq 2 \cdot 10^{n-1}$, or how that bound on $b_n$ makes $a_n$ bounded.
- Page 3: the notes say $b_n$ is "the largest integer" with $b_n^2 \leq 2 \cdot 10^{2n-2}$ and that "obviously" $(10 \thinspace b_n)^2 \leq 2 \cdot 10^{2(n+1)-2}$; the page does not show the existence of this largest integer or give the reason for "obviously".
- Page 3: the sequence is described as starting $a_1 = 1$, $a_2 = 1.4$, $a_3 = 1.41$, $a_4 = 1.414$ and then $a_5 = \cdots$ with no value; the page does not check these values against the definition of $b_n$.
- Page 4: the page goes from $a_n^2 \leq 2$ for each $n$ to "This show that $a^2 \leq 2$" without saying why an inequality that holds for every term holds for the limit.
- Page 4: the inequality $(a_n + 10^{1-n})^2 \gt 2$ is turned into $2 \leq \lim (a_n + 10^{1-n})^2$ (strict to non-strict) and the equality $\lim (a_n + 10^{1-n})^2 = \lim a_n^2$ is used without comment; the page does not state that $a^2 \geq 2$ and $a^2 \leq 2$ together give $a^2 = 2$.
- Page 5: the proof assumes that $\sup \lbrace a_n \rbrace$ exists; the page does not name the completeness property it relies on.
- Page 6: the Cauchy theorem, the contracting mapping theorem and the application to ODEs are stated without proof; "More on all of this next time......". The contracting map definition says only that $c \lt 1$ and does not say that $c$ is non-negative.

---

## Page 1

SPRING 2025 - 18.100B/18.1002

TOBIAS HOLCK COLDING

**Lecture 5**

A sequence of real numbers is a function $f : \mathbf{N} \to \mathbf{R}$.

We usually use the notation $a_n = f(n)$.

Limit: Let $a_n$ be a sequence and $a$ a real number. We say that $a_n$ converges to $a$ if for all $\epsilon \gt 0$, there exists an $N \in \mathbf{N}$ such that if $n \geq N$, then

$$
\vert a_n - a \vert \lt \epsilon .
$$

If this is the case, then we also say that $a$ is the limit of the sequence and we say that the sequence is convergenet. A sequence that is not covergent is said to be divergent.

**Theorem** If $a_n$ is a convergent sequence, then the set $\lbrace a_n \rbrace$ is a bounded subset of $\mathbf{R}$.

Basic algebraic properties of limits:

**Theorem** Suppose that $a_n$ and $b_n$ are convergenet sequences with $\lim a_n = a$, $\lim b_n = b$ and $C \in \mathbf{R}$, then

(1) $c_n = C \thinspace a_n$ is convergenet and $\lim_{n \to \infty} c_n = C \thinspace a$.

(2) $c_n = a_n + b_n$ is convergent and $\lim_{n \to \infty} c_n = a + b$.

(3) $c_n = a_n \thinspace b_n$ is convergent with $\lim_{n \to \infty} c_n = a \thinspace b$.

(4) If $b_n \neq 0$, $b \neq 0$ and $c_n = \frac{1}{b_n}$, then $c_n$ is convergent and $\lim_{n \to \infty} c_n = \frac{1}{b}$.

**Subsequence:** A subsequence $b_k$ of $a_n$ is a composition of functions $f \circ g$ where $g : \mathbf{N} \to \mathbf{N}$ is a strictly increasing function. So $b_k = f(g(k))$. We often write $a_{n_k}$ for $b_k$.

1

## Page 2

2 — TOBIAS HOLCK COLDING

**Example**: A sequence is defined by $a_n$

$$
a_n = \frac{n^2 + 1}{n^2 + n + 1} .
$$

We will show that $a_n$ is convergent with limit 1. We have

$$
a_n = \frac{1 + \frac{1}{n^2}}{1 + \frac{1}{n} + \frac{1}{n^2}} .
$$

Since $\frac{1}{n} \to 0$ and $\frac{1}{n^2} \to 0$ we have that

$$
1 + \frac{1}{n^2} \to 1
$$

and

$$
1 + \frac{1}{n} + \frac{1}{n^2} \to 1 .
$$

It now follows from the algebraic properties of limits that

$$
a_n \to 1 .
$$

**Example**: To show that $\sqrt{2}$ is the limit of $a_1 = 1$, $a_2 = 1.4$, $a_3 = 1.41$, $a_4 = 1.414$, .... we need something else. We need the monotone convergence theorem.

**Monotone convergence theorem**: Increasing version. Let $a_n$ be a monotone increasing sequence. This means that $a_1 \leq a_2 \leq a_3 \leq \cdots$. (Which we can also write this as $a_n \leq a_{n+1}$). If the sequence is bounded from above so that there exists $A$ with

$$
a_n \leq A ,
$$

then $a_n$ is convergent with limit $\sup \lbrace a_n \rbrace$.

**Monotone convergence theorem**: Decreasing version. Similarly, for a bounded monotone decreasing sequence $a_n$ where $a_{n+1} \leq a_n$, we have that $a_n$ converges and

$$
\lim_{n \to \infty} a_n = \inf \lbrace a_n \rbrace .
$$

## Page 3

SPRING 2025 - 18.100B/18.1002 — 3

Using the monotone convergence theorem we can now show that $\sqrt{2}$ is the limit of $a_1 = 1$, $a_2 = 1.4$, $a_3 = 1.41$, $a_4 = 1.414$, $a_5 = \cdots$.

To show this we argue as follows:

Let

$$
a_n = \frac{b_n}{10^{n-1}}
$$

where $b_n$ is the largest integer so that

$$
b_n^2 \leq 2 \cdot 10^{2n-2} .
$$

We will show that $a_n$ is an increasing and bounded sequence and that the limit $a$ has the property that $a^2 = 2$.

So suppose that $b_n$ is an integer and that

$$
b_n^2 \leq 2 \cdot 10^{2n-2} ,
$$

then obviously

$$
(10 \thinspace b_n)^2 \leq 2 \cdot 10^{2(n+1)-2} .
$$

This implies that $b_{n+1} \geq 10 \thinspace b_n$; so $a_{n+1} \geq a_n$ and the sequence is increasing.

It is clear that $b_n \leq 2 \cdot 10^{n-1}$, since $(2 \cdot 10^{2n-2})^2 \gt 2 \cdot 10^{2n-2}$.

Therefore the sequence $a_n = \frac{b_n}{10^{n-1}}$ is bounded and by the monotone convergence theorem $a_n \to a$.

## Page 4

4 — TOBIAS HOLCK COLDING

To show that $a^2 = 2$ we argue as follows:

By the algebraic properties of limits we have that $a^2 = \lim_{n \to \infty} a_n^2$, but for each $n$ we have that $a_n^2 \thinspace 10^{2n-2} = b_n^2 \leq 2 \cdot 10^{2n-2}$ so $a_n^2 \leq 2$.

This show that $a^2 \leq 2$.

Similarly, since $(b_n + 1)^2 \gt 2 \cdot 10^{2n-2}$ we have that $(a_n + 10^{1-n})^2 = \frac{(b_n + 1)^2}{10^{2n-2}} \gt 2$.

Therefore, $2 \leq \lim_{n \to \infty} (a_n + 10^{1-n})^2 = \lim_{n \to \infty} a_n^2 = a^2$.

## Page 5

SPRING 2025 - 18.100B/18.1002 — 5

**Proof of the monotone convergence theorem** (Increasing version):

The decreasing version is proven similarly.

So suppose that we have a sequence with

$$
a_n \leq a_{n+1} \leq A
$$

and set

$$
a = \sup \lbrace a_n \rbrace .
$$

We want to show that

$$
a_n \to a .
$$

Given $\epsilon \gt 0$, since $a - \epsilon \lt a$ we have that $a - \epsilon$ is not an upper bound for the sequence, therefore there exists $N$ such that

$$
a_N \gt a - \epsilon .
$$

Since the sequence is increasing we have for $n \geq N$ that

$$
a - \epsilon \lt a_N \leq a_n \leq a
$$

Here the last inequality used that $a$ is an upper bound for the sequence.

We now have that for $n \geq N$

$$
0 \leq a - a_n \lt \epsilon .
$$

This shows that the sequence is convergent with limit $a$.

## Page 6

6 — TOBIAS HOLCK COLDING

**Cauchy sequence:** A sequence $a_n$ is said to be a Cauchy sequence if for all $\epsilon \gt 0$, there exists an $N$ such that if $m, n \geq N$, then

$$
\vert a_n - a_m \vert \lt \epsilon .
$$

(Tail of the sequence bunch together.)

From Wikipedia: Baron Augustin-Louis Cauchy (1789 – 1857) was a French mathematician, engineer, and physicist. He was one of the first to rigorously state and prove the key theorems of calculus (thereby creating real analysis), pioneered the field complex analysis, and the study of permutation groups in abstract algebra. Cauchy also contributed to a number of topics in mathematical physics, notably continuum mechanics.

**Theorem**: A sequence is convergent if and only if it is a Cauchy sequence.

Application: Existence of fixed points for a maps. If $T : \mathbf{R} \to \mathbf{R}$ is a map, then $x_0 \in \mathbf{R}$ is a fixed point if

$$
T(x_0) = x_0 .
$$

**Definition** A contracting map is a map $T : \mathbf{R} \to \mathbf{R}$ such that there exists $c \lt 1$ so for all $x, y \in \mathbf{R}$ we have that

$$
\vert T(x) - T(y) \vert \leq c \thinspace \vert x - y \vert .
$$

(Points are squeezed together under the map.)

**Contracting mapping theorem:** Any contracting map has a fixed point.

Application of contracting mapping theorem: Existence of solutions to ODEs.

More on all of this next time......

REFERENCES

[TBB] B.S. Thomson, J.B. Bruckner, and A.M. Bruckner, *Elementary Real Analysis, 2nd edition*
TBB can be downloaded at:
https://classicalrealanalysis.info/com/documents/TBB-AllChapters-Landscape.pdf
(screen-optimized)

## Page 7

SPRING 2025 - 18.100B/18.1002 — 7

https://classicalrealanalysis.info/com/documents/TBB-AllChapters-Portrait.pdf
(print-optimized)

MIT, Dept. of Math., 77 Massachusetts Avenue, Cambridge, MA 02139-4307.

## Page 8

MIT OpenCourseWare back page (not lecture content): "MIT OpenCourseWare https://ocw.mit.edu — 18.100B Real Analysis — Spring 2025 — For information about citing these materials or our Terms of Use, visit: https://ocw.mit.edu/terms."
