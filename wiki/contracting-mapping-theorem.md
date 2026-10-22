# The contracting mapping theorem

**Fixed points, contracting maps $T : \mathbf{R} \to \mathbf{R}$, and the theorem, stated in Lecture 5 with the proof promised for next time, that a contracting map has a fixed point; and why the course cares: the same theorem in other spaces gives solutions to differential equations. The proof is not yet in this knowledge base.**

Notation: $\mathbf{R}$ is the real numbers, set in bold as in the notes, and $\vert x \vert$ is the absolute value of $x$. Colding calls it the "contracting mapping theorem", and once the "contraction mapping theorem" (Lecture 5, ≈1:13:39).

## Fixed points

**Definition** (Lecture 5 notes p. 6; Lecture 5, ≈1:17:08). If $T : \mathbf{R} \to \mathbf{R}$ is a map, then $x_0 \in \mathbf{R}$ is a **fixed point** of $T$ if

$$T(x_0) = x_0 .$$

## Contracting maps

**Definition** (Lecture 5 notes p. 6; Lecture 5, ≈1:13:39–1:15:25). A **contracting map** is a map $T : \mathbf{R} \to \mathbf{R}$ for which there exists a constant $c \lt 1$ such that for all $x, y \in \mathbf{R}$,

$$\vert T(x) - T(y) \vert \leq c \thinspace \vert x - y \vert .$$

The images of two points are closer together than the points themselves, by at least the factor $c$: "So they have to come closer" (≈1:15:25). The notes: "(Points are squeezed together under the map.)" (Lecture 5 notes p. 6).

What Colding stresses is that $c$ is *strictly* less than $1$: "the important point is that c has to be strictly less than 1. That's a crucial point" (≈1:14:35). On the board he also says that $c$ is positive, in a remark that is hard to read from the captions (≈1:14:35); the notes state only $c \lt 1$.

## The theorem

**Contracting mapping theorem** (Lecture 5 notes p. 6; Lecture 5, ≈1:15:25–1:17:53). If $T : \mathbf{R} \to \mathbf{R}$ is a contracting map, then $T$ has a fixed point: there is an $x$ with $T(x) = x$.

"It's crucial that this c is less than 1. That's what makes everything go. If it was equal to 1, you wouldn't get anything" (≈1:17:08). Lecture 5 does not prove the theorem: "we'll talk about the proof next time", and "once you know the more abstract concepts, then it's quite easy" (≈1:15:25–1:16:16). The notes end the section with "More on all of this next time......" (Lecture 5 notes p. 6).

## Why it matters: differential equations

Colding introduces the theorem as the first instance of something more general (Lecture 5, ≈1:12:08–1:13:39). Many of the course's concepts "work much more general", and to use them on differential equations they have to be abstracted "to where sequences are not any more real numbers, but they are of some other space" (≈1:12:53). Showing that a differential equation has a solution "often goes over using what's called the contracting mapping theorem", which has "all kinds of forms", depending only on "what space you're looking at" (≈1:12:53–1:13:39). In such a space the fixed point can be a solution to a differential equation; this is "a standard application to get solutions to differential equations" (≈1:17:53). The notes: "Application of contracting mapping theorem: Existence of solutions to ODEs" (Lecture 5 notes p. 6). In the notes, fixed points are introduced under the heading "Application: Existence of fixed points for a maps", directly after the Cauchy theorem; the notes do not say what it is an application of (Lecture 5 notes p. 6).

## Not yet in this knowledge base

Colding says the next lecture will discuss the contracting mapping theorem but "won't talk quite yet about the applications" (Lecture 5, ≈1:17:53). On the OCW lecture list, Lecture 6 is "Cauchy Convergence Theorem" (TBB Section 2.12); Lecture 22 is "Differentiating and Integrating Power Series; Ordinary Differential Equations (ODEs)" and Lecture 23 is "Existence and Uniqueness for ODEs: Picard–Lindelöf Theorem". None of them is covered here yet.

## Lectures

- [Lecture 5 — Monotone Convergence Theorem](05-monotone-convergence-theorem.md): the definitions and the statement of the theorem.
- [Cauchy sequences](cauchy-sequences.md): the theorem stated just before it in the notes.
