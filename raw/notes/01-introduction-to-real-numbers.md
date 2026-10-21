---
title: Lecture 1 — Introduction to Real Numbers (lecture notes)
lecture: 1
pages: 5
source_pdf: https://ocw.mit.edu/courses/18-100b-real-analysis-spring-2025/mit18_100b_s25_lec01.pdf
resource_page: https://ocw.mit.edu/courses/18-100b-real-analysis-spring-2025/resources/mit18_100b_s25_lec01_pdf/
numbering: PDF page N = printed page N (page 1 prints its number at the bottom, pages 2–4 in the running head; page 5 is the MIT OpenCourseWare back page, not lecture content). The notes have no equation numbers; list items keep their own numbering (1)–(5).
figures: There are no figures. The small vector objects on pages 1 and 3 are square-root bars, not drawings; the notes mention a picture of the intermediate value theorem (page 1) but do not draw one.
---

# Lecture 1 — Introduction to Real Numbers: lecture notes

Full text of the course's written notes for Lecture 1 (MIT 18.100B/18.1002 Real Analysis, Spring 2025, Tobias Holck Colding), transcribed from the PDF. Cite as "notes p. N". The notes set the number sets in bold type, not blackboard bold, so they are written $\mathbf{N}$, $\mathbf{Z}$, $\mathbf{Q}$, $\mathbf{R}$ here; the field is likewise the bold $\mathbf{F}$ and the ordered set the bold $\mathbf{S}$. The notes print no equation numbers. Page 5 is the OpenCourseWare citation page and is summarized, not transcribed as lecture content.

[wiki page for this lecture](../../wiki/01-introduction-to-real-numbers.md) · [transcript](../transcripts/01-introduction-to-real-numbers.md)

## Contents

| Section | Page(s) |
| --- | --- |
| Two key topics; intermediate value theorem; questions Q1–Q3 | 1 |
| Notation for $\mathbf{N}$, $\mathbf{Z}$, $\mathbf{Q}$ | 2 |
| Rational numbers: equality, addition, multiplication, order | 2 |
| Multiplication is well-defined (proof) | 2 |
| A field: definition, additive and multiplicative axioms, distributive axiom | 3 |
| Theorem: zero is unique | 3 |
| Examples; ordered set; ordered field | 4 |
| Theorem: $x \lt y$ and $z \gt 0$ imply $x z \lt y z$ | 4 |
| References | 4 |
| OpenCourseWare back page | 5 |

## Printed slips

These are in the PDF as printed; the body below keeps them as printed.

- Page 1: "is a continuous functions" should be "is a continuous function".
- Page 1: "but how to we actually prove this?" should be "how do we actually prove this?".
- Page 1: a stray full stop sits alone on its own line after that bullet list.
- Page 3: "This illustrate how detailed a proof should be" should be "illustrates".
- Page 3: "Those two operations satisfies the following axioms" should be "satisfy".
- Page 3: "The final axion that we need" should be "axiom".
- Page 3: an empty bullet precedes the displayed distributive law.
- Page 4: "For an x, y ∈ S" should read "For any x, y ∈ S".
- Page 4: "an ordered set that is also Field" is missing "a" ("also a Field").

Not a slip, but worth knowing: the page 2 proof stops at $m_1 p_1 n_2 q_2 = m_2 n_1 p_2 q_1$ and leaves the last step to the reader. Read as $(m_1 p_1)(n_2 q_2) = (m_2 p_2)(n_1 q_1)$, that is exactly the equality test of item 1 applied to $\frac{m_1 p_1}{n_1 q_1}$ and $\frac{m_2 p_2}{n_2 q_2}$, which is what the proof set out to show.

---

## Page 1

SPRING 2025 - 18.100B/18.1002

TOBIAS HOLCK COLDING

**Lecture 1**

Two key topics for this class:

- How to write a mathematical proof.
- How to prove theorems.

Here is an example:

**Intermediate value theorem:**

- Suppose that $f : [a, b] \to \mathbf{R}$ is a continuous functions.
- Assume that $f(a) \lt 0$ and $f(b) \gt 0$.

The intermediate value theorem says that there exists a $c$ between $a$ and $b$ where $f(c) = 0$.

- How do we prove this?
- If we draw a picture, then it seems obvious, but how to we actually prove this?

.

That a function is continuous basically means that when you draw the graph of the function the pencil is not allowed to leave the paper.

- How do we make this into a proper proof?
- What properties of the real values are needed for a proof?

This leads to several questions:

- Q1: What is a real number?
- Q2: Why is $\sqrt{2}$ a real number?
- Q3: What is $\sqrt{2}$?

**The answer to these questions**: $\mathbf{R}$ is a complete ordered field that contains the rational numbers $\mathbf{Q}$.

1

## Page 2

2 — TOBIAS HOLCK COLDING

Here is some notation:

1. $\mathbf{N}$ is the natural numbers. This means that $\mathbf{N} = \lbrace 1, 2, 3, \cdots \rbrace$.
2. $\mathbf{Z}$ is the integers. This means that $\mathbf{Z} = \lbrace 0, \pm 1, \pm 2, \pm 3, \cdots \rbrace$.
3. $\mathbf{Q}$ is the rational numbers. So all numbers of the form $\frac{m}{n}$, where $m \in \mathbf{Z}$ and $n \in \mathbf{N}$.

**Properties:**

**Rational numbers**:

Rational numbers $\mathbf{Q}$ are numbers of the form $\frac{m}{n}$, where $m \in \mathbf{Z}$ and $n \in \mathbf{N}$.

1. When are two numbers the same?

$$
\frac{m_1}{n_1} = \frac{m_2}{n_2} \iff m_1 n_2 = m_2 n_1 .
$$

2. How do we add two numbers?

$$
\frac{m_1}{n_1} + \frac{m_2}{n_2} = \frac{m_1 n_2 + m_2 n_1}{n_1 n_2} .
$$

3. How do we multiply two numbers?

$$
\frac{m_1}{n_1} \frac{m_2}{n_2} = \frac{m_1 m_2}{n_1 n_2} .
$$

4. When is one number less than another?

$$
\frac{m_1}{n_1} \lt \frac{m_2}{n_2} \iff m_1 n_2 \lt m_2 n_1 .
$$

For this to make sense we need (for instance) to show that multiplication is well-defined:

This means that if we have two representations of the same rational number

$$
\frac{m_1}{n_1} = \frac{m_2}{n_2}
$$

and likewise

$$
\frac{p_1}{q_1} = \frac{p_2}{q_2} ,
$$

then

$$
\frac{m_1}{n_1} \frac{p_1}{q_1} = \frac{m_2}{n_2} \frac{p_2}{q_2} .
$$

*Proof.* We have that $m_1 n_2 = m_2 n_1$ and $p_1 q_2 = p_2 q_1$. Therefore,

$$
m_1 p_1 n_2 q_2 = m_1 n_2 p_1 q_2 = m_2 n_1 p_2 q_1 .
$$

□

## Page 3

SPRING 2025 - 18.100B/18.1002 — 3

This illustrate how detailed a proof should be.

**A Field:**

**Definition:**
A Field $\mathbf{F}$ is a set with two operations that we are denoting suggestively by "+" and " $\cdot$ ". Those two operations satisfies the following axioms:

Additive properties:

1. $x, y \in \mathbf{F}$, then $x + y \in \mathbf{F}$.
2. $x + y = y + x$.
3. $(x + y) + z = x + (y + z)$.
4. There exists an element $0 \in \mathbf{F}$ such that $0 + x = x$ for all $x \in \mathbf{F}$.
5. For all $x \in \mathbf{F}$ there exists an element, suggestively, denoted by $(-x)$ such that $x + (-x) = 0$.

Multiplicative properties:

1. $x, y \in \mathbf{F}$, then $x y \in \mathbf{F}$.
2. $x y = y x$.
3. $(x y) z = x (y z)$.
4. There exists an element, suggestively, denoted by 1 such that $1 x = x$ for all $x \in \mathbf{F}$.
5. For all $x \in \mathbf{F} \setminus \lbrace 0 \rbrace$ there exists an element, suggestively, denoted by $\frac{1}{x}$ such that $x \frac{1}{x} = 1$.

The final axion that we need is an axiom that chains addition and multiplication together:

-

$$
(x + y) z = x z + y z .
$$

**Theorem**: For any field 'zero' is unique.

*Proof.* Suppose there are two. Let us denote them by $0_ {1}$ and $0_ {2}$. Then

$$
0_ {1} + 0_ {2} = 0_ {2}
$$

since $0_ {1}$ is a 'zero' and

$$
0_ {1} + 0_ {2} = 0_ {1}
$$

since $0_ {2}$ is a 'zero' so $0_ {1} = 0_ {2}$.

□

## Page 4

4 — TOBIAS HOLCK COLDING

**Examples:** $\mathbf{Q}$ is a Field, whereas $\mathbf{N}$ and $\mathbf{Z}$ are not Fields.

**Ordered set:** An ordered set $\mathbf{S}$ is a set with a relation $\lt$ with the following properties:

1. For an $x, y \in \mathbf{S}$, one of the following holds: $x \lt y$ or $y \lt x$ or $x = y$.
2. If $x, y, z \in \mathbf{S}$ with $x \lt y$ and $y \lt z$, then $x \lt z$.

**Ordered Field:**
An ordered Field is an ordered set that is also Field and has the following two additional properties that chains the operations in the Field together with the ordering:

1. If $x \lt y$, then $x + z \lt y + z$.
2. If $x \gt 0$ and $y \gt 0$, then $x y \gt 0$.

Example: $\mathbf{Q}$ is an ordered Field.

**Theorem**: If $x \lt y$ and $z \gt 0$, then $x z \lt y z$.

*Proof.* We need to show that $x z \lt y z$ or equivalently $y z - x z \gt 0$. The latter can be rewritten as $y z - x z = (y - x) z$. Since $y \gt x$ we have that $y - x \gt 0$ and the claim therefore follows since $z \gt 0$. □

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
