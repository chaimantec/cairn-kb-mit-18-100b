# The Archimedean property

**Every real number is exceeded by some natural number. The course proves it from completeness in Lecture 2 and uses it to find a rational number between any two reals. Lecture 3 carries it in its title and is not yet covered here.**

## Statement

**Archimedean property** (Lecture 2 notes p. 3; ≈54:54–56:28). For every $x \in \mathbf{R}$ there is a natural number $n \in \mathbf{N}$ with $x \lt n$.

Here $\mathbf{N} = \lbrace 1, 2, 3, \cdots \rbrace$ and $\mathbf{R}$ is the real numbers, set in bold as in the notes. Colding notes that it "seems like a kind of trivial fact", but proves it rigorously (≈56:28). Equivalently, as the notes frame the proof, $\mathbf{N}$ is not bounded in $\mathbf{R}$. That is the example of $\mathbf{N}$ having no upper bound, which the lecture raised when it defined upper bounds and promised to return to (≈23:58; notes p. 2).

## Proof from completeness

The proof is by contradiction and uses the [least upper bound property](least-upper-bound-property.md) (Lecture 2 notes p. 3; ≈56:28–1:00:49).

If the property failed, there would be an $x$ with $n \leq x$ for every $n \in \mathbf{N}$ (≈57:17). Then $\mathbf{N}$ has an upper bound, so it has a least upper bound $\alpha$ (the board calls it $y$). So $n \leq \alpha$ for all $n \in \mathbf{N}$. Since $n + 1$ is also a natural number, $n + 1 \leq \alpha$ as well, that is, $n \leq \alpha - 1$. As $n$ was arbitrary, $\alpha - 1$ is an upper bound for $\mathbf{N}$, smaller than $\alpha$. That contradicts $\alpha$ being the least upper bound. □

## Corollary: a rational number between any two reals

**Corollary** (Lecture 2 notes pp. 3–4; ≈1:00:49–1:08:14). If $x \lt y$ are real numbers, there is a rational number $\frac{m}{n}$ with

$$x \lt \frac{m}{n} \lt y .$$

The idea is to take steps of length $\frac{1}{n}$ that are shorter than the gap $y - x$, and stop at the first step past $x$. By the Archimedean property there is a natural number $n$ with $n \gt \frac{1}{y - x}$, so $\frac{1}{n} \lt y - x$. (The notes call $\frac{1}{y - x}$ by the name $\beta$; the board uses $\beta$ for $y - x$ itself.) Let $m - 1$ be the largest integer with $m - 1 \leq x n$. Then $\frac{m - 1}{n} \leq x \lt \frac{m}{n}$, and since one step is shorter than the gap,

$$\frac{m}{n} \leq x + \frac{1}{n} \lt y .$$

The notes leave both final inequalities to the reader, and neither the notes nor the board say why a largest such integer exists. Colding said something along these lines would appear on the homework (≈1:08:14). The step-by-step version is on the [Lecture 2 page](02-introduction-to-real-numbers-cont.md).

## Where this goes next

Lecture 3 on the OCW list is "How to Write a Proof; Archimedean Property", with reading TBB Section 1.7. **This knowledge base does not yet cover it**, so what that lecture adds is not here.

## Lectures

- [Lecture 2 — Introduction to Real Numbers (cont.)](02-introduction-to-real-numbers-cont.md): the statement, the proof and the corollary.
