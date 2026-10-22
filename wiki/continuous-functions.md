# Continuous functions

**The course's rigorous definition of continuity at a point, with $\epsilon$ and $\delta$ (Lecture 6), the picture behind it, and the theorem that a continuous function takes a convergent sequence to a convergent sequence, with its proof; and where continuity has appeared before, informally, in Lecture 1.**

Notation: $\mathbf{R}$ is the real numbers, set in bold as in the notes, $\vert x \vert$ is the absolute value of $x$, and $\epsilon$ and $\delta$ are positive real numbers.

## Before Lecture 6: the informal picture

Continuity first appears in Lecture 1, in the statement of the [intermediate value theorem](intermediate-value-theorem.md), and only informally: when you draw the graph, the chalk never leaves the blackboard, and a function that jumps is not continuous (Lecture 1, ≈7:55–8:40). Lecture 6 introduces "this notion of a function being continuous in a rigorous way" (Lecture 6, ≈59:17), because the extreme value theorem needs it.

## The definition

**Definition** (Lecture 6 notes p. 4; Lecture 6, ≈59:17–1:01:53). A function $f : \mathbf{R} \to \mathbf{R}$ is **continuous at a point** $x_0 \in \mathbf{R}$ if for all $\epsilon \gt 0$ there exists a $\delta \gt 0$ such that

$$\vert x - x_0 \vert \lt \delta \implies \vert f(x) - f(x_0) \vert \lt \epsilon .$$

A function is **continuous** if it is continuous at all points in its domain (notes p. 4; ≈1:01:53).

On the board the domain "could be a subset of R, could be all of R" (≈59:17–1:00:13); the notes state the definition for $f : \mathbf{R} \to \mathbf{R}$. In words, if $x$ is within $\delta$ of $x_0$, "then the images are within epsilon region" (≈1:00:13). As in the definition of convergence, $\epsilon$ comes first and $\delta$ is chosen after it, so $\delta$ may depend on $\epsilon$.

**The picture** (≈1:01:06). Draw the graph and mark $f(x_0)$ on the vertical axis. Around it take "a little interval around here-- this is a epsilon interval", and "then there should be some delta interval around here so that if you're looking at images here, then it will map into here" (≈1:01:06). Every point within $\delta$ of $x_0$ is sent within $\epsilon$ of $f(x_0)$.

## Continuous functions preserve limits of sequences

**Theorem** (Lecture 6 notes p. 4; Lecture 6, ≈1:02:42–1:03:29). If $f : \mathbf{R} \to \mathbf{R}$ is continuous and $x_n$ is a sequence with $x_n \to x_0$, then $f(x_n) \to f(x_0)$.

"And this is often useful way of thinking about continuity" (≈1:02:42). The domain need not be all of $\mathbf{R}$, "but you just have to be careful that everything that you talk about is in the domain" (≈1:02:42).

**Proof** (notes p. 4; ≈1:03:29–1:05:54). Only continuity at the limit point is needed: "you only need that is continuous at each x" (≈1:04:18). Let $\epsilon \gt 0$.

1. By continuity at $x_0$ there exists a $\delta \gt 0$ such that if $\vert x - x_0 \vert \lt \delta$, then $\vert f(x) - f(x_0) \vert \lt \epsilon$ (≈1:04:18).
2. Since $x_n \to x_0$, apply the definition of convergence with $\delta$ in the place of $\epsilon$: there exists $N$ such that if $n \geq N$, then $\vert x_n - x_0 \vert \lt \delta$ (≈1:05:08).
3. So for $n \geq N$, $\vert f(x_n) - f(x_0) \vert \lt \epsilon$, which is the definition of $f(x_n) \to f(x_0)$ (≈1:05:54). □

Earlier in the same lecture, before continuity is defined, the notes prove a statement of the same shape for a contracting map $T$: if $x_n \to x$, then $T(x_n) \to T(x)$, since $\vert T(x_n) - T(x) \vert \leq c \thinspace \vert x_n - x \vert$ (Lecture 6 notes p. 2). See [the contracting mapping theorem](contracting-mapping-theorem.md).

## Where it is used

- **The extreme value theorem** (Lecture 6, ≈1:13:11; notes p. 4). A continuous function on $[a, b]$ attains its supremum: a subsequence $x_{n_k} \to x$ of points where $f$ approaches its supremum gives $f(x_{n_k}) \to f(x)$ by the theorem above. In the notes the theorem is stated for $f : \mathbf{R} \to \mathbf{R}$ and applied to a function on $[a, b]$. See [the extreme value theorem](extreme-value-theorem.md).

## Not yet in this knowledge base

On the OCW lecture list, continuous functions are the subject of Lecture 9, "Limsup and Liminf; Power Series; Continuous Functions; Exponential Function", and Lecture 10, "Continuous Functions; Exponential Function (cont.)", and Lecture 11 is "Extreme and Intermediate Value Theorem; Metric Spaces". None of them is covered here yet.

## Lectures

- [Lecture 1 — Introduction to Real Numbers](01-introduction-to-real-numbers.md): the informal picture of continuity, in the intermediate value theorem.
- [Lecture 6 — Cauchy Convergence Theorem](06-cauchy-convergence-theorem.md): the definition, the picture, the theorem on sequences and its use in the extreme value theorem.
