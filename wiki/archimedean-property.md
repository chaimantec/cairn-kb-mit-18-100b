# The Archimedean property

**Every real number is exceeded by some natural number; equivalently, $\mathbf{N}$ is not bounded from above. The course proves it from completeness in Lecture 2, uses it to find a rational number between any two reals, and writes the proof out formally in Lecture 3. Lecture 4 uses it to prove that $0.999 \cdots = 1$.**

## Statement

**Archimedean property** (Lecture 2 notes p. 3; ≈54:54–56:28). For every $x \in \mathbf{R}$ there is a natural number $n \in \mathbf{N}$ with $x \lt n$.

Here $\mathbf{N} = \lbrace 1, 2, 3, \cdots \rbrace$ and $\mathbf{R}$ is the real numbers, set in bold as in the notes. Colding notes that it "seems like a kind of trivial fact", but proves it rigorously (≈56:28). Equivalently, as the notes frame the proof, $\mathbf{N}$ is not bounded in $\mathbf{R}$. That is the example of $\mathbf{N}$ having no upper bound, which the lecture raised when it defined upper bounds and promised to return to (≈23:58; notes p. 2). Lecture 3 makes this the statement of the theorem: **the set of natural numbers is not bounded from above** (Lecture 3 notes p. 4; ≈1:09:15). Colding calls it one way of formulating the Archimedean property; the other, that for every real number there is a larger natural number, is "the same" (Lecture 3, ≈1:09:15–1:10:01).

## Proof from completeness

The proof is by contradiction and uses the [least upper bound property](least-upper-bound-property.md) (Lecture 2 notes p. 3; ≈56:28–1:00:49).

If the property failed, there would be an $x$ with $n \leq x$ for every $n \in \mathbf{N}$ (≈57:17). Then $\mathbf{N}$ has an upper bound, so it has a least upper bound $\alpha$ (the board calls it $y$). So $n \leq \alpha$ for all $n \in \mathbf{N}$. Since $n + 1$ is also a natural number, $n + 1 \leq \alpha$ as well, that is, $n \leq \alpha - 1$. As $n$ was arbitrary, $\alpha - 1$ is an upper bound for $\mathbf{N}$, smaller than $\alpha$. That contradicts $\alpha$ being the least upper bound. □

## The formal proof (Lecture 3)

Lecture 3 writes the same argument as a formal proof (Lecture 3 notes p. 4; ≈1:10:01–1:14:20). Suppose $\mathbf{N}$ is bounded from above, and let $\alpha$ be its least upper bound; on the board Colding takes an upper bound $\alpha$ and replaces it by the supremum (≈1:10:49). Then, before any computation, the proof says where the contradiction will come from: $\alpha - 1$ will turn out to be an upper bound too, contradicting that $\alpha$ was the least one (≈1:11:43–1:12:33). For any $n \in \mathbf{N}$, $n + 1$ is also a natural number, so $n + 1 \leq \alpha$, and subtracting $1$, $n \leq \alpha - 1$. So $\alpha - 1$ is an upper bound: the desired contradiction. □

The notes start this proof "let $M$ be the least upper bound" and call it $\alpha$ from the next line on, a [printed slip](../raw/notes/03-how-to-write-a-proof-archimedean-property.md#printed-slips). What Lecture 3 adds is not a new argument but the writing; see [writing proofs](writing-proofs.md).

## Corollary: some $\frac{1}{n}$ is smaller than any given $\epsilon \gt 0$

**Corollary** (Lecture 3 notes p. 4). For any $\epsilon \gt 0$, there exists an $n \in \mathbf{N}$ such that $\frac{1}{n} \lt \epsilon$.

**Proof** (notes p. 4). Set $\alpha = \frac{1}{\epsilon}$. By the Archimedean property there exists an $n \in \mathbf{N}$ with $n \gt \alpha$. It follows that $\frac{1}{n} \lt \epsilon$. □

This corollary is in the notes only; the Lecture 3 video does not reach it. The notes leave the last step to the reader. The same notes go on to define convergence of a sequence; see [sequences and limits](sequences-and-limits.md).

**First use** (Lecture 4 notes p. 3; Lecture 4, ≈12:54). In the proof that the sequence $0.9$, $0.99$, $0.999$, … converges to $1$, the Archimedean property is what lets one "choose $N$ such that $\frac{1}{N} \lt \epsilon$". Then for $n \geq N$, $\vert a_n - 1 \vert = 10^{-n} \lt \frac{1}{n} \leq \frac{1}{N} \lt \epsilon$. See the [Lecture 4 page](04-sequences-convergence.md).

## Corollary: a rational number between any two reals

**Corollary** (Lecture 2 notes pp. 3–4; ≈1:00:49–1:08:14). If $x \lt y$ are real numbers, there is a rational number $\frac{m}{n}$ with

$$x \lt \frac{m}{n} \lt y .$$

The idea is to take steps of length $\frac{1}{n}$ that are shorter than the gap $y - x$, and stop at the first step past $x$. By the Archimedean property there is a natural number $n$ with $n \gt \frac{1}{y - x}$, so $\frac{1}{n} \lt y - x$. (The notes call $\frac{1}{y - x}$ by the name $\beta$; the board uses $\beta$ for $y - x$ itself.) Let $m - 1$ be the largest integer with $m - 1 \leq x n$. Then $\frac{m - 1}{n} \leq x \lt \frac{m}{n}$, and since one step is shorter than the gap,

$$\frac{m}{n} \leq x + \frac{1}{n} \lt y .$$

The notes leave both final inequalities to the reader, and neither the notes nor the board say why a largest such integer exists. Colding said something along these lines would appear on the homework (≈1:08:14). The step-by-step version is on the [Lecture 2 page](02-introduction-to-real-numbers-cont.md).

## Lectures

- [Lecture 2 — Introduction to Real Numbers (cont.)](02-introduction-to-real-numbers-cont.md): the statement, the proof and the rational number between two reals.
- [Lecture 3 — How to Write a Proof; Archimedean Property](03-how-to-write-a-proof-archimedean-property.md): the formal proof, and in the notes the corollary that $\frac{1}{n} \lt \epsilon$ for some $n$.
- [Lecture 4 — Sequences; Convergence](04-sequences-convergence.md): the property used to choose $N$ in the proof that $0.999 \cdots = 1$.
