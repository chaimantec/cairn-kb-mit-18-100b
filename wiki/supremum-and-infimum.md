# Supremum and infimum

**Upper and lower bounds, the least upper bound $\sup A$ and the greatest lower bound $\inf A$, as the course defines them in Lectures 2 and 3, why a bound depends on the set it is taken in, and where they are used through Lecture 8.**

Throughout, $\mathbf{S}$ is an ordered set, $A$ is a subset of $\mathbf{S}$, and $\mathbf{N} = \lbrace 1, 2, 3, \cdots \rbrace$, $\mathbf{Q}$ and $\mathbf{R}$ are the natural, rational and real numbers, set in bold as in the notes. When a problem does not say what the larger set is, it is $\mathbf{R}$ (Lecture 3, ≈14:56).

## Upper and lower bounds

**Bounded from above.** $A$ is bounded from above if there is an $M \in \mathbf{S}$ such that $a \leq M$ for all $a \in A$. Such an $M$ is an **upper bound** for $A$ (Lecture 2 notes p. 2; Lecture 3 notes p. 1; Lecture 3, ≈4:48–5:43).

**Bounded from below.** $A$ is bounded from below if there is an $m \in \mathbf{S}$ such that $m \leq a$ for all $a \in A$. Such an $m$ is a **lower bound** for $A$ (Lecture 3 notes p. 1; ≈5:43–6:39).

**Bounded**, said without qualification, means bounded from above and from below (Lecture 3, ≈8:12). The Lecture 3 notes state both definitions for non-empty subsets.

Lecture 2 defined only upper bounds, and a student asked why (Lecture 2, ≈1:10:32–1:11:17). Lecture 3 defines lower bounds directly, and Colding calls the two notions "a symmetric property" (≈19:42).

## A bound lives in the larger set

An upper bound **does not need to be in $A$**; it only has to be in the larger set (Lecture 3, ≈7:26–9:48, ≈10:45). The open interval $(0, 1)$, as a subset of $\mathbf{R}$, is bounded, since every $x$ in it is less than $1$. But no element of the interval is an upper bound for it: "The upper bound is outside the set. But it is in all of R. And that's fine" (≈9:01).

The flip side is that **whether $A$ is bounded depends on the ordered set it is taken in** (≈11:32–14:08). Let $\mathbf{S}$ be the half line of real numbers greater than $0$, and let $A$ be the interval from $0$ to $1$ inside it. Then $A$ is bounded from above in $\mathbf{S}$, by $1$. But it is not bounded from below as a subset of $\mathbf{S}$, because a lower bound would have to be in $\mathbf{S}$, and "0 is not in this set, and no negative numbers in this set" (≈13:10). As a subset of $\mathbf{R}$ the same $A$ is bounded from below. Colding warns that this may seem counterintuitive.

Infinity and minus infinity are not real numbers, so they are never bounds in $\mathbf{R}$ (≈14:08).

## Least upper bound: $\sup A$

Suppose $A$ is bounded from above. $M$ is the **least upper bound** of $A$ if (Lecture 2 notes p. 2; Lecture 3, ≈17:24–18:11)

1. $M$ is an upper bound for $A$: $a \leq M$ for all $a \in A$, and
2. $M \leq M_1$ for every other upper bound $M_1$ of $A$.

It is written $\sup A$; the Lecture 3 notes call it "the smallest upper bound of $A$" (p. 1). In Lecture 2 the same notion appears without the notation, as the least upper bound $x$ of a set whose square is to be $2$.

## Greatest lower bound: $\inf A$

Suppose $A$ is bounded from below. $m$ is the **greatest lower bound** of $A$ if (Lecture 3 notes p. 1; ≈18:11–19:42)

1. $m$ is a lower bound for $A$: $m \leq a$ for all $a \in A$, and
2. $m_1 \leq m$ for every other lower bound $m_1$ of $A$.

The notes define it as "a lower bound that is greater or equal to all other lower bounds" and write it $\inf A$.

## Existence, and whether they belong to $A$

An ordered set is **complete** when every subset that is bounded from above has a least upper bound (Lecture 2 notes p. 2; Lecture 3, ≈15:42–17:24). The course takes for granted that $\mathbf{R}$ is complete; see [completeness and the least upper bound property](least-upper-bound-property.md). On the board, Colding concludes that every bounded subset of $\mathbf{R}$ has both a least upper bound and a greatest lower bound (Lecture 3, ≈19:42). The course has so far presented the existence of $\inf A$ as the symmetric counterpart of the least upper bound property, without deriving it.

In general, $\sup A$ and $\inf A$ are not elements of $A$: "they could be. But in general, they wouldn't be" (Lecture 3, ≈19:42).

Asked whether the half line above is complete, Colding answered that a subset of it which is bounded from below cannot have numbers approaching $0$, and so would have a greatest lower bound; "it's pretty convincing that it is actually complete, in this sense", though in another sense, to come later in the course, it is not (Lecture 3, ≈20:29–22:07). He did not prove it, and the question is mostly inaudible in the captions.

## Where $\sup$ is used so far

- **$\sqrt{2} \in \mathbf{R}$.** The positive $\alpha$ with $\alpha^2 = 2$ is $\sup A$ for $A = \lbrace x \in \mathbf{R} \vert x \gt 0 \text{ and } x^2 \leq 2 \rbrace$ (Lecture 3 notes pp. 2–3). See [the square root of 2](square-root-of-2.md).
- **The Archimedean property.** If $\mathbf{N}$ were bounded from above, its supremum $\alpha$ would have $\alpha - 1$ as a smaller upper bound (Lecture 2 notes p. 3; Lecture 3 notes p. 4). See [the Archimedean property](archimedean-property.md).
- **A convergent sequence is bounded.** On the board, the conclusion is that the $\sup$ of the set of all $\vert a_n \vert$ is at most $\max\lbrace C, \vert a \vert + 1 \rbrace$. Colding writes $\sup$ rather than a maximum because "if it's infinitely many numbers, it's not clear there is a maximum", and the bound need not be the sup itself (Lecture 4, ≈21:33, ≈25:43). See [sequences and limits](sequences-and-limits.md).
- **The monotone convergence theorem.** A monotone increasing sequence that is bounded from above converges to $\sup \lbrace a_n \rbrace$, and a monotone decreasing one bounded from below converges to $\inf \lbrace a_n \rbrace$ (Lecture 5 notes p. 2). The proof uses both halves of the definition of $\sup$: $a_n \leq \sup \lbrace a_n \rbrace$ because it is an upper bound, and some term exceeds $\sup \lbrace a_n \rbrace - \epsilon$ because it is the least one (Lecture 5, ≈37:00–39:32). See [the monotone convergence theorem](monotone-convergence-theorem.md).
- **The tails of a bounded sequence.** On the board, $b_n = \sup \lbrace a_n, a_{n+1}, \cdots \rbrace$ and $c_n = \inf \lbrace a_n, a_{n+1}, \cdots \rbrace$. Since $b_{n+1}$ and $c_{n+1}$ are taken over a smaller set, $b_n$ decreases and $c_n$ increases, and $c_n \leq b_n$ (Lecture 5, ≈23:24–31:21). The argument behind both is that a $\sup$ over a larger set is at least as large, and an $\inf$ over a larger set at most as large (≈25:03, ≈28:56).
- **The extreme value theorem.** A continuous function $f$ on $[a, b]$ attains its $\sup$ and its $\inf$, so they are a maximum and a minimum: "it's not really a sup. It's a max" (Lecture 6, ≈1:07:37; Lecture 6 notes p. 4). The proof starts from a sequence $x_n$ with $f(x_n) \to \sup f$. Asked where it comes from, Colding used that $\sup f$ is the *least* upper bound: for each $\epsilon$ some value of $f$ is larger than $\sup f$ minus $\epsilon$ (≈1:15:32–1:16:18). For the proof he also allows $\sup f$ to be infinite when $f$ has no upper bound, though "we don't usually like this" (≈1:09:56–1:10:43). See [the extreme value theorem](extreme-value-theorem.md).
- **$\mathbf{Q}$ is not complete.** The rationals whose square is at most $2$ have an upper bound in $\mathbf{Q}$ but no least upper bound in $\mathbf{Q}$ (Lecture 2, ≈1:12:05–1:12:51). See [the rational numbers](rational-numbers.md).

- **$\limsup$.** Lecture 5 says that the $\sup$ and $\inf$ of the tails are "how one defines limsup and liminf", without defining either (Lecture 5, ≈1:08:10). The Lecture 8 notes then define $\limsup a_n$ as the limit of $b_n = \sup \lbrace a_n, a_{n+1}, a_{n+2}, \cdots \rbrace$, or $\infty$ if $a_n$ is not bounded from above (Lecture 8 notes p. 6), and use it for the radius of convergence of a power series. See [limsup and liminf](limsup-and-liminf.md).

$\liminf$ is not yet defined. On the OCW lecture list, Lecture 9 is "Limsup and Liminf; Power Series; Continuous Functions; Exponential Function" (TBB Sections 2.13, 10.2, 5.4 and 5.5), which is not yet in this knowledge base.

## Lectures

- [Lecture 2 — Introduction to Real Numbers (cont.)](02-introduction-to-real-numbers-cont.md): upper bounds, least upper bounds and completeness.
- [Lecture 3 — How to Write a Proof; Archimedean Property](03-how-to-write-a-proof-archimedean-property.md): lower bounds, the notation $\sup$ and $\inf$, and the examples about the surrounding set.
- [Lecture 4 — Sequences; Convergence](04-sequences-convergence.md): a $\sup$ in the proof that a convergent sequence is bounded. The Lecture 4 notes repeat the definitions, and call $\sup A$ "the greatest lower bound of $A$", a [printed slip](../raw/notes/04-sequences-convergence.md#printed-slips).
- [Lecture 5 — Monotone Convergence Theorem](05-monotone-convergence-theorem.md): $\sup$ and $\inf$ as the limits of bounded monotone sequences, and the $\sup$ and $\inf$ of the tails of a bounded sequence.
- [Lecture 6 — Cauchy Convergence Theorem](06-cauchy-convergence-theorem.md): the $\sup$ and $\inf$ of a continuous function on $[a, b]$ are attained.
- [Lecture 8 — Convergence Tests for Series; Power Series](08-convergence-tests-for-series-power-series.md): in the notes, $\limsup$ as the limit of the $\sup$ of the tails.
