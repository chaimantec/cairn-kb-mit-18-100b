---
title: Lecture 2 — Introduction to Real Numbers (cont.) (lecture notes)
lecture: 2
pages: 5
source_pdf: https://ocw.mit.edu/courses/18-100b-real-analysis-spring-2025/mit18_100b_s25_lec02.pdf
resource_page: https://ocw.mit.edu/courses/18-100b-real-analysis-spring-2025/resources/mit18_100b_s25_lec02_pdf/
numbering: PDF page N = printed page N (page 1 prints its number at the bottom, pages 2–4 in the running head; page 5 is the MIT OpenCourseWare back page, not lecture content). The notes have no equation numbers.
figures: There are no figures. The small vector objects on pages 1–4 are fraction bars and square-root bars, not drawings.
---

# Lecture 2 — Introduction to Real Numbers (cont.): lecture notes

Full text of the course's written notes for Lecture 2 (MIT 18.100B/18.1002 Real Analysis, Spring 2025, Tobias Holck Colding), transcribed from the PDF. Cite as "notes p. N". The notes set the number sets in bold type, not blackboard bold, so they are written $\mathbf{N}$, $\mathbf{Z}$, $\mathbf{Q}$, $\mathbf{R}$ here; the ordered set is likewise the bold $\mathbf{S}$. The notes print no equation numbers. Page 5 is the OpenCourseWare citation page and is summarized, not transcribed as lecture content.

[wiki page for this lecture](../../wiki/02-introduction-to-real-numbers-cont.md) · [transcript](../transcripts/02-introduction-to-real-numbers-cont.md)

## Contents

| Section | Page(s) |
| --- | --- |
| $\mathbf{R}$ versus $\mathbf{Q}$; theorem: no rational $x$ with $x^2 = 2$ (proof by contradiction) | 1 |
| Adding $\sqrt{2}$ to the number system: limit of a sequence | 1 |
| Completeness: upper bound, least upper bound, complete ordered set | 2 |
| Theorem: a complete ordered Field containing $\mathbf{Q}$ exists (not proved) | 2 |
| Theorem: $\sqrt{2} \in \mathbf{R}$ (first half of proof) | 2 |
| Theorem: $\sqrt{2} \in \mathbf{R}$ (second half of proof) | 3 |
| Corollary: $\mathbf{Q}$ is not complete | 3 |
| Archimedean property | 3 |
| Corollary: a rational number between any two reals | 3–4 |
| References | 4 |
| OpenCourseWare back page | 5 |

## Printed slips

These are in the PDF as printed; the body below keeps them as printed.

- Page 1: "There does not exists a rational number" should be "There does not exist".
- Page 1: "We can assume m and n does not have a common factor" should be "do not have".
- Page 1: "and therefore $2 m_1 = n$" is missing both squares: from $4 m_1^2 = 2 n^2$ what follows is $2 m_1^2 = n^2$. (On the board Colding first says "is equal to n" and corrects himself to "n squared", transcript ≈14:59.)
- Page 1: "This show that there is no rational number" should be "This shows".
- Page 1: "The real numbers $\mathbf{R}$ is a complete ordered Field" has a plural subject with a singular verb ("The real numbers $\mathbf{R}$ are", or "The real number system $\mathbf{R}$ is").
- Page 3: "This contradict that $x$ is the least upper bound" should be "This contradicts".
- Page 3: the display $(x + h)^2 \lt x^2 + 2 - x^2 \lt 2$ has a wrong final sign: $x^2 + 2 - x^2$ equals $2$, so the last symbol should be an equals sign (the strict inequality already sits in the first step, $(x + h)^2 \lt x^2 + 2 - x^2$).
- Page 3: "This is the desired contradiction and show that $x^2 \geq 2$" should be "shows".

Not a slip, but worth knowing: the notes leave some steps unstated. They are reproduced as printed.

- Page 1: "so 2 is a factor in $m^2$ and therefore in $m$ itself" gives no reason for the second half, and "so $n$ is also even" is likewise stated without the step from $n^2$ to $n$.
- Page 2: $A$ is written $(0, \sqrt{2}) \cap \mathbf{Q}$, using the number whose existence the theorem is about; the next sentence restates $A$ as the positive rational numbers $a$ with $a^2 \lt 2$, which does not mention $\sqrt{2}$.
- Page 3: after $(x - h)^2 \gt 2$ the notes say "therefore $x - h$ is also an upper bound for $A$" without showing why. After $(x + h)^2 \lt 2$ they call it "the desired contradiction" without saying what it contradicts; since $A$ consists of rational numbers, the notes do not say whether $x + h$ is rational or how it relates to $A$.
- Page 3: the second half takes $0 \lt h \lt 1$ and then chooses $h$ positive with $h \lt \frac{2 - x^2}{2 x + 1}$, without saying in so many words that $h$ must satisfy both. A student asks about exactly this at the end of the lecture (transcript ≈1:13:42).
- Page 4: "let $m - 1$ be the largest integer so that $m - 1 \leq x n$" does not say why a largest such integer exists, and "It follows that $\frac{m}{n}$ has the desired property" leaves both inequalities to the reader.

---

## Page 1

SPRING 2025 - 18.100B/18.1002

TOBIAS HOLCK COLDING

**Lecture 2**

The real numbers $\mathbf{R}$ is a complete ordered Field that contains $\mathbf{Q}$.

**Question**: What is the difference between $\mathbf{R}$ and $\mathbf{Q}$?
One difference is that $\mathbf{R}$ contains $\sqrt{2}$ and $\mathbf{Q}$ does not.

$\sqrt{2}$ is a number $x$ so that $x \gt 0$ and $x^2 = 2$.

**Theorem**: There does not exists a rational number $x$ so that $x^2 = 2$.

*Proof.* We will argue by contradiction. So suppose that there exists a rational number $x = \frac{m}{n}$, where $m \in \mathbf{Z}$ and $n \in \mathbf{N}$, so that $x^2 = \frac{m^2}{n^2} = 2$. We can assume $m$ and $n$ does not have a common factor (other than one). We have that $m^2 = 2 n^2$ and so 2 is a factor in $m^2$ and therefore in $m$ itself. This means that $m = 2 m_1$, where $m_1$ is also an integer. It follows that $m^2 = 4 m_1^2 = 2 n^2$ and therefore $2 m_1 = n$ and so $n$ is also even. We have now that both $m$ and $n$ are even and so have 2 as a common factor. This is the desired contradiction. This show that there is no rational number $x$ with the property that $x^2 = 2$. □

How do we add $\sqrt{2}$ to the number system?

$\sqrt{2} = 1.4142136 \cdots$

So 1, 1.4, 1.41, 1.414, 1.4142, 1.41421, $\to \sqrt{2}$.

$\sqrt{2}$ is the limit of a sequence of numbers.

1

## Page 2

2 — TOBIAS HOLCK COLDING

Completeness of $\mathbf{R}$. (Least upper bound property.)

Completeness is: If a subset $A$ of $\mathbf{R}$ has an upper bound, then $A$ has a least upper bound.

Suppose that $\mathbf{S}$ is an ordered set and $A$ is a subset of $\mathbf{S}$, then $M$ is an upper bound for $A$ if for all $a \in A$ we have that $a \leq M$.

Example: If $A = \lbrace 1, 2, 3 \rbrace \subset \mathbf{Z}$, then 4 is an upper bound, whereas 2 is not an upper bound.

Example: If $\mathbf{S} = \mathbf{Q}$, then $\mathbf{N}$ as a subset does not have an upper bound (we will return to this shortly).

Least upper bound: Suppose that $\mathbf{S}$ is an ordered set and $A$ is a subset that has an upper bound. We say that $M$ is a least upper bound for $A$ if $M$ is an upper bound for $A$ and for any other upper bound $M_1$ we have that $M \leq M_1$.

Complete ordered set: We say that an ordered set is complete if any subset that has an upper bound has a least upper bound.

**Theorem**: There exists a complete ordered Field that contains $\mathbf{Q}$.

This Field is denoted by $\mathbf{R}$.

We will not prove this, as a proof would take us too far a field, rather we will take it for granted.

**Theorem**: $\sqrt{2} \in \mathbf{R}$.

*Proof.* Let $A = (0, \sqrt{2}) \cap \mathbf{Q}$. That is $A$ consists of all the positive rational numbers $a$ so that $a^2 \lt 2$. Let $x$ be the least upper bound for $A$. Note that $A$ is nonempty (since $1 \in A$) and that 2 is an upper bound for $A$. Note also that $x \geq 1 \gt 0$ since it is an upper bound. We need to show that $x^2 = 2$.

We will first show that $x^2 \leq 2$. Suppose not; so assume that $x^2 \gt 2$. We will show that this leads to a contradiction. Consider

$$
(x - h)^2 = x^2 - 2 x h + h^2 \gt x^2 - 2 h x .
$$

As long as $h \gt 0$ is chosen so that

$$
2 h x \lt x^2 - 2
$$

## Page 3

SPRING 2025 - 18.100B/18.1002 — 3

or, equivalently, that

$$
h \lt \frac{x^2 - 2}{2 x}
$$

then

$$
(x - h)^2 \gt 2
$$

and therefore $x - h$ is also an upper bound for $A$. This contradict that $x$ is the least upper bound. We therefore have that if $x$ is the least upper bound for $A$, then $x^2 \leq 2$.

To show the reverse inequality (that $x^2 \geq 2$) we argue similarly. Assume that for the least upper bound $x$ we have that $x^2 \lt 2$. Consider $x + h$, where $0 \lt h \lt 1$. We have that

$$
(x + h)^2 = x^2 + 2 x h + h^2 \lt x^2 + 2 x h + h = x^2 + h (2 x + 1) .
$$

Since we are assuming that $x^2 \lt 2$ we can choose $h$ positive so that

$$
h \lt \frac{2 - x^2}{2 x + 1} .
$$

We therefore have that

$$
(x + h)^2 \lt x^2 + 2 - x^2 \lt 2 .
$$

This is the desired contradiction and show that $x^2 \geq 2$. Together with the first step we have that $x^2 = 2$. □

**Corollary: $\mathbf{Q}$ is not complete.**

*Proof.* If $\mathbf{Q}$ was complete, then $\sqrt{2} \in \mathbf{Q}$ but we have already proven that there is no rational number with the property that $x^2 = 2$. □

**Archimedean property**: For all $x \in \mathbf{R}$, there exists a natural $n \in \mathbf{N}$ so that $x \lt n$.

*Proof.* If this was not the case, then $\mathbf{N}$ would be bounded. To see that $\mathbf{N}$ is not bounded we argue as follows. Assume it is bounded and let $\alpha$ be the least upper bound for $\mathbf{N}$. We would now have that for all $n \in \mathbf{N}$ that $n \leq \alpha$. Since $n + 1$ is also a natural number we would have that $n + 1 \leq \alpha$ as well. So, in fact, $n \leq \alpha - 1$ or in other words, since $n$ was any natural number, $\alpha - 1$ would be an upper bound contradicting that $\alpha$ was the least upper bound. □

As a corollary of the Archimedean property we get the following:

**Corollary**: If $x \lt y$, then there exists a rational number $\frac{m}{n}$ such that

$$
x \lt \frac{m}{n} \lt y .
$$

## Page 4

4 — TOBIAS HOLCK COLDING

*Proof.* Set $\beta = \frac{1}{y - x}$. From the Archimedean property we have that there exists a natural number $n$ with $n \gt \beta$. It follows that

$$
0 \lt \frac{1}{n} \lt \frac{1}{\beta} .
$$

Now let $m - 1$ be the largest integer so that

$$
m - 1 \leq x n .
$$

It follows that $\frac{m}{n}$ has the desired property. □

REFERENCES

[TBB] B.S. Thomson, J.B. Bruckner, and A.M. Bruckner, *Elementary Real Analysis, 2nd edition*
TBB can be downloaded at:
https://classicalrealanalysis.info/com/documents/TBB-AllChapters-Landscape.pdf
(screen-optimized)
https://classicalrealanalysis.info/com/documents/TBB-AllChapters-Portrait.pdf
(print-optimized)

MIT, Dept. of Math., 77 Massachusetts Avenue, Cambridge, MA 02139-4307.

## Page 5

MIT OpenCourseWare back page (not lecture content): "MIT OpenCourseWare https://ocw.mit.edu — 18.100B Real Analysis — Spring 2025 — For information about citing these materials or our Terms of Use, visit: https://ocw.mit.edu/terms."
