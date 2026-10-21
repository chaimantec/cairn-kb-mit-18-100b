# The rational numbers

**$\mathbf{Q}$ as the course builds it: quotients of integers, when two quotients are equal, the operations and the order, and why each operation must be checked to be well defined.**

## Definition

$\mathbf{Q}$ is the set of numbers of the form $\frac{m}{n}$ with $m \in \mathbf{Z}$ and $n \in \mathbf{N}$ (Lecture 1, ≈15:21–16:10; notes p. 2). Here $\mathbf{Z} = \lbrace 0, \pm 1, \pm 2, \cdots \rbrace$ is the integers, and $\mathbf{N} = \lbrace 1, 2, 3, \cdots \rbrace$ is the natural numbers, which do not include $0$ in this course. So the numerator may be any integer, but **the denominator is always a positive whole number**. That convention is what makes the order below work.

## Many quotients, one number

A rational number has many representations as a quotient, so the definition begins with equality. For $m_1, m_2 \in \mathbf{Z}$ and $n_1, n_2 \in \mathbf{N}$,

$$\frac{m_1}{n_1} = \frac{m_2}{n_2} \iff m_1 n_2 = m_2 n_1 .$$

(≈16:56–18:33; notes p. 2.) Equality of rationals is thus *defined* by an equation between integers.

## Operations and order

The course defines (≈19:21–24:01; notes p. 2)

$$\frac{m_1}{n_1} + \frac{m_2}{n_2} = \frac{m_1 n_2 + m_2 n_1}{n_1 n_2}, \qquad \frac{m_1}{n_1} \frac{m_2}{n_2} = \frac{m_1 m_2}{n_1 n_2},$$

and

$$\frac{m_1}{n_1} \lt \frac{m_2}{n_2} \iff m_1 n_2 \lt m_2 n_1 .$$

In both operations the result is again an integer over a natural number, so it is a rational number. The order is defined by cross-multiplying, which is legitimate only because $n_1$ and $n_2$ are positive (≈24:01).

## Well-definedness

Since one rational number has many representations, an operation defined on quotients means something only if the answer does not depend on the representation chosen. In Colding's words, the rational number you get has to be "independent on the representation" (≈20:06–20:52). For multiplication this is proved in Lecture 1: if $\frac{m_1}{n_1} = \frac{m_2}{n_2}$ and $\frac{p_1}{q_1} = \frac{p_2}{q_2}$, then $\frac{m_1 p_1}{n_1 q_1} = \frac{m_2 p_2}{n_2 q_2}$. The proof reduces the conclusion to the integer equation $m_1 p_1 n_2 q_2 = m_2 p_2 n_1 q_1$ and gets it by substituting $m_1 n_2 = m_2 n_1$ and $p_1 q_2 = p_2 q_1$ (≈24:49–30:35; notes p. 2). The full argument is on the [Lecture 1 page](01-introduction-to-real-numbers.md). Addition is "exactly the same" but messier and is not written out in the lecture or the notes (≈30:35–31:22).

## $\mathbf{Q}$ is an ordered field

With these operations and this order, $\mathbf{Q}$ satisfies all eleven field axioms and both ordered-field axioms (≈49:04, ≈56:33–58:14; notes p. 4). It is the course's first example of each structure, and the definitions of field and ordered field are abstracted directly from it (≈32:08). See [fields and ordered fields](fields-and-ordered-fields.md).

## What $\mathbf{Q}$ is not

Lecture 1 asked "Why is $\sqrt{2}$ a real number? What is $\sqrt{2}$?" (notes p. 1), and Lecture 2 answers with the main difference between $\mathbf{Q}$ and $\mathbf{R}$:

- **No rational number squares to $2$** (Lecture 2, ≈10:04–15:44; notes p. 1). Suppose $\frac{m}{n}$ did, with $m$ and $n$ having no common factor. Then $m^2 = 2 n^2$, which forces both $m$ and $n$ to be even, a contradiction. See [the square root of 2](square-root-of-2.md).
- **$\mathbf{Q}$ is not complete** (Lecture 2, ≈52:20–54:54; notes p. 3). A complete ordered field containing $\mathbf{Q}$ must contain $\sqrt{2}$, and $\mathbf{Q}$ does not. Concretely, the set of rationals whose square is at most $2$ has an upper bound in $\mathbf{Q}$, but no least upper bound in $\mathbf{Q}$ (≈1:12:05–1:12:51). See [completeness and the least upper bound property](least-upper-bound-property.md).

But $\mathbf{Q}$ sits closely inside $\mathbf{R}$: **between any two real numbers $x \lt y$ there is a rational number** $\frac{m}{n}$ with $x \lt \frac{m}{n} \lt y$. Lecture 2 proves this from the Archimedean property, by choosing $n$ with $\frac{1}{n} \lt y - x$ and stepping in multiples of $\frac{1}{n}$ (≈1:00:49–1:08:14; notes pp. 3–4). See [the Archimedean property](archimedean-property.md).

## Lectures

- [Lecture 1 — Introduction to Real Numbers](01-introduction-to-real-numbers.md): the definitions above, and the well-definedness proof for multiplication.
- [Lecture 2 — Introduction to Real Numbers (cont.)](02-introduction-to-real-numbers-cont.md): $\sqrt{2}$ is not rational, $\mathbf{Q}$ is not complete, and a rational number lies between any two reals.
