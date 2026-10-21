# Sequences and limits

**What a sequence of real numbers is, the course's first examples, and the definition of convergence as the Lecture 3 notes give it. The lectures on convergence itself are not yet in this knowledge base.**

Notation: $\mathbf{N} = \lbrace 1, 2, 3, \cdots \rbrace$ is the natural numbers and $\mathbf{R}$ the real numbers, set in bold as in the notes.

## Why the course needs them

Sequences first come up as a way to place $\sqrt{2}$ on the real line. As a decimal, $\sqrt{2}$ begins $1.4142136$, and it can be thought of as the limit of the increasing sequence $1$, $1.4$, $1.41$, $1.414$, … (Lecture 2, ≈16:47–18:30; Lecture 2 notes p. 1). Lecture 2 calls this a preview: sequences and limits are "another really important concept that we will talk much more about later" (≈17:40). Lecture 3 starts them, saying "this will be a big topic" (≈1:14:20), and notes that to use this picture of $\sqrt{2}$ the course must make precise both what a sequence is and what its limit is (≈1:16:02).

## Sequences

**Definition** (Lecture 3 notes p. 5; Lecture 3, ≈1:16:48). A sequence of real numbers is a function

$$f : \mathbf{N} \to \mathbf{R} .$$

For each natural number you get a real number. Rather than writing the argument in brackets, it is usual to write it as a subscript, $a_n = f(n)$ (≈1:17:35).

**Example 1** (notes p. 5; ≈1:17:35–1:19:05). $a_1 = 1$, $a_2 = 1.4$, $a_3 = 1.41$, $a_4 = 1.414$, and so on, where $a_n$ keeps the first $n$ digits of $\sqrt{2}$. This sequence is increasing, $a_n \lt a_{n+1}$, and $\sqrt{2}$ is its limit, written $\lim_{n \to \infty} a_n$.

The notes give two more examples, which the Lecture 3 video does not reach (notes p. 5):

- **Example 2.** $a_n = (-1)^n$. "This sequence has NO limit": its terms alternate between $-1$ and $1$.
- **Example 3.** The sequence $a_n = \frac{1}{n}$ has zero as its limit.

## Convergence

**Definition** (Lecture 3 notes p. 5). Let $a_n$ be a sequence and $a$ a real number. The sequence $a_n$ **converges** to $a$ if for all $\epsilon \gt 0$ there exists an $N \in \mathbf{N}$ such that if $n \geq N$, then

$$\vert a_n - a \vert \lt \epsilon .$$

This is printed in the Lecture 3 notes, but in the video Colding stops before it and says what a limit means is for next time (≈1:19:05). The notes also pose the question "When does a limit exist?" and leave it open on that page.

A related fact is proved in the same notes, as a corollary of the [Archimedean property](archimedean-property.md): for any $\epsilon \gt 0$ there exists an $n \in \mathbf{N}$ such that $\frac{1}{n} \lt \epsilon$ (Lecture 3 notes p. 4).

## Not yet in this knowledge base

On the OCW lecture list, sequences continue in Lecture 4, "Sequences; Convergence" (TBB Sections 2.1–2.2 and 2.4–2.7), Lecture 5, "Monotone Convergence Theorem" (TBB Sections 2.8, 2.9 and 2.11), and Lecture 6, "Cauchy Convergence Theorem" (TBB Section 2.12). None of them is covered here yet, so the course's treatment of limits, beyond the definition above, is not in this knowledge base.

## Lectures

- [Lecture 2 — Introduction to Real Numbers (cont.)](02-introduction-to-real-numbers-cont.md): $\sqrt{2}$ as the limit of its decimals, as a preview.
- [Lecture 3 — How to Write a Proof; Archimedean Property](03-how-to-write-a-proof-archimedean-property.md): the definition of a sequence, and in the notes, the examples and the definition of convergence.
