# The square root of 2

**The course's running example of the difference between $\mathbf{Q}$ and $\mathbf{R}$: Lecture 1 asks what $\sqrt{2}$ is, Lecture 2 proves that it is not rational and that it is real, and Lecture 3 writes the second proof out formally.**

## The questions

Lecture 1 opens with the [intermediate value theorem](intermediate-value-theorem.md) and asks which properties of the real numbers its proof needs. That leads to three questions (Lecture 1, ≈11:12–11:58; notes p. 1): What is a real number? Why is $\sqrt{2}$ a real number? What is $\sqrt{2}$? The answer given is that $\mathbf{R}$ is a complete ordered field containing $\mathbf{Q}$ (≈12:45), but Lecture 1 does not return to $\sqrt{2}$. Lecture 2 does.

## Definition

$\sqrt{2}$ is **a number $x$ such that $x \gt 0$ and $x^2 = 2$** (Lecture 2 notes p. 1; ≈9:13).

## It is not rational

**Theorem** (Lecture 2 notes p. 1; ≈10:04–15:44). There is no rational number $x$ with $x^2 = 2$.

The proof is by contradiction. Write $x = \frac{m}{n}$ with $m \in \mathbf{Z}$, $n \in \mathbf{N}$ and, after reducing, no common factor of $m$ and $n$ other than one. From $x^2 = 2$ we get $m^2 = 2 n^2$, so $2$ is a factor of $m$; writing $m = 2 m_1$ gives $4 m_1^2 = 2 n^2$, so $2 m_1^2 = n^2$ and $2$ is a factor of $n$ too. That contradicts the choice of $m$ and $n$. The notes misprint $2 m_1^2 = n^2$ as $2 m_1 = n$ (a [printed slip](../raw/notes/02-introduction-to-real-numbers-cont.md#printed-slips)). Step-by-step proof on the [Lecture 2 page](02-introduction-to-real-numbers-cont.md).

So $\mathbf{R}$, if it contains $\sqrt{2}$, is strictly larger than $\mathbf{Q}$ (≈19:16).

## A limit of decimals

As a decimal, $\sqrt{2} = 1.4142136 \cdots$ (Lecture 2 notes p. 1; ≈16:47). One way to think of it is as the limit of the increasing sequence $1$, $1.4$, $1.41$, $1.414$, $1.4142$, $1.41421$, … (≈17:40–18:30). Colding presents this as motivation for sequences and limits, which the course treats later (≈17:40–19:16). Lecture 3 takes the first step: a sequence is a function from $\mathbf{N}$ to $\mathbf{R}$, and here $a_1 = 1$, $a_2 = 1.4$, $a_3 = 1.41$, $a_4 = 1.414$, … keeps the first $n$ digits of $\sqrt{2}$, an increasing sequence whose limit will be $\sqrt{2}$ (Lecture 3, ≈1:15:06–1:19:05; Lecture 3 notes p. 5). What a limit is comes in Lecture 4, "Sequences; Convergence", which is not yet in this knowledge base. See [sequences and limits](sequences-and-limits.md).

## It is real

**Theorem** (Lecture 2 notes pp. 2–3; ≈30:11–52:20). $\sqrt{2} \in \mathbf{R}$.

The proof uses [completeness](least-upper-bound-property.md). Take the set $A$ of positive numbers whose square is less than $2$. It contains $1$, and $2$ is an upper bound for it, so it has a least upper bound, and Lecture 2 *defines* $\sqrt{2}$ to be that least upper bound (≈33:25). Colding calls it $x$ during the proof, so as not to use, without noticing, what we expect $\sqrt{2}$ to satisfy (≈34:20–35:07). Then:

- $x \geq 1 \gt 0$, because $1 \in A$ and $x$ is an upper bound.
- If $x^2 \gt 2$, then for $0 \lt h \lt \frac{x^2 - 2}{2 x}$ the smaller number $x - h$ still satisfies $(x - h)^2 \gt 2$ and is an upper bound. That contradicts $x$ being least.
- If $x^2 \lt 2$, then for $h$ with $0 \lt h \lt 1$ and $h \lt \frac{2 - x^2}{2 x + 1}$ the larger number $x + h$ satisfies $(x + h)^2 \lt 2$, so it lies in $A$. That contradicts $x$ being an upper bound.

So $x^2 = 2$. On the board $A$ is a set of real numbers; in the notes it is a set of rationals, written $(0, \sqrt{2}) \cap \mathbf{Q}$. Full proof, with the board's and the notes' versions side by side, on the [Lecture 2 page](02-introduction-to-real-numbers-cont.md).

## The formal proof (Lecture 3)

Lecture 3 proves the same theorem again, this time written as a formal proof, to show what one looks like (Lecture 3 notes pp. 2–3; ≈22:52–1:06:09). The statement becomes: **there exists $\alpha \gt 0$ such that $\alpha^2 = 2$.** The set is now

$$A = \lbrace x \in \mathbf{R} \vert x \gt 0 \text{ and } x^2 \leq 2 \rbrace ,$$

with $x^2 \leq 2$ in place of Lecture 2's $x^2 \lt 2$, and $\alpha = \sup A$. Since $1 \in A$ and $2$ is an upper bound, $1 \leq \alpha \leq 2$. The two inequalities are proved by contradiction as before, but with $h$ chosen up front:

- If $\alpha^2 \gt 2$, set $h = \frac{\alpha^2 - 2}{4 \alpha}$ and $\alpha_0 = \alpha - h$. Then $0 \lt \alpha_0 \lt \alpha$ and $\alpha_0^2 \gt \frac{\alpha^2}{2} + 1 \geq 2$, so $\alpha_0$ is an upper bound smaller than $\alpha$.
- If $\alpha^2 \lt 2$, set $h = \frac{2 - \alpha^2}{4 \alpha}$ and $\alpha_1 = \alpha + h$. Then $0 \lt h \lt 1$ and $\alpha_1^2 \lt 2$, so $\alpha_1$ is in $A$ and larger than $\alpha$.

On the board the two auxiliary numbers are called $\alpha_1$ and $\alpha_2$. The full computation, with the board's detour and the notes' printed slip ($\alpha \gt 2$ for $\alpha^2 \gt 2$), is on the [Lecture 3 page](03-how-to-write-a-proof-archimedean-property.md). Asked which properties of $\mathbf{R}$ the proof uses, Colding named the ordering, the ordered-field structure (multiplication, to define a square root at all, and $1 \gt 0$), and completeness, to define the least upper bound (≈1:06:55).

## What follows

The same argument works in any complete ordered field containing $\mathbf{Q}$, so such a field contains $\sqrt{2}$ (≈53:07–54:08). Since $\sqrt{2}$ is not rational, **$\mathbf{Q}$ is not complete** (notes p. 3). See [the rational numbers](rational-numbers.md) and [the real numbers](real-numbers.md).

## Lectures

- [Lecture 1 — Introduction to Real Numbers](01-introduction-to-real-numbers.md): the questions about $\sqrt{2}$.
- [Lecture 2 — Introduction to Real Numbers (cont.)](02-introduction-to-real-numbers-cont.md): the definition, both theorems, and the corollary that $\mathbf{Q}$ is not complete.
- [Lecture 3 — How to Write a Proof; Archimedean Property](03-how-to-write-a-proof-archimedean-property.md): the formal proof that a positive $\alpha$ with $\alpha^2 = 2$ exists, and $\sqrt{2}$ as the limit of a sequence.
