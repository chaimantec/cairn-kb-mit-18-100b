# Completeness and the least upper bound property

**What "complete" means in the course's description of $\mathbf{R}$: upper bounds, least upper bounds, complete ordered sets and fields, the theorem that $\mathbf{R}$ exists, and the first things completeness proves.**

## Why this is the missing word

Lecture 1 characterized the real numbers by one sentence, that $\mathbf{R}$ is a complete ordered field that contains $\mathbf{Q}$, and explained everything in it except *complete* (Lecture 1, ≈12:45–14:27). Lecture 2 supplies it. The notes head the section "Completeness of $\mathbf{R}$. (Least upper bound property.)" (Lecture 2 notes p. 2). As elsewhere in this knowledge base, $\mathbf{N} = \lbrace 1, 2, 3, \cdots \rbrace$, $\mathbf{Z}$, $\mathbf{Q}$ and $\mathbf{R}$ are the natural numbers, integers, rationals and reals, set in bold as in the notes.

## Upper bound

Let $\mathbf{S}$ be an [ordered set](fields-and-ordered-fields.md) and $A$ a subset of $\mathbf{S}$. An element $M$ is an **upper bound** for $A$ if

$$a \leq M \quad \text{for all } a \in A$$

(Lecture 2 notes p. 2; ≈20:48–22:22). An upper bound must be greater than or equal to every element of $A$, and it may equal one of them (≈22:22).

Examples from the lecture (notes p. 2; ≈22:22–23:58):

- For $A = \lbrace 1, 2, 3 \rbrace$, $4$ is an upper bound and $2$ is not, because $3 \gt 2$. The notes take $A \subset \mathbf{Z}$; the board uses $\mathbf{N}$.
- In $\mathbf{S} = \mathbf{Q}$, the subset $\mathbf{N}$ has no upper bound. The lecture returns to this with the [Archimedean property](archimedean-property.md).

On the board, Colding calls a set that has an upper bound "bounded" (≈25:35, ≈28:35). Lower bounds are not defined in Lecture 2. Asked why, Colding said he would come back to it next time (≈1:10:32–1:11:17); that lecture is not yet in this knowledge base.

## Least upper bound

Suppose $A \subset \mathbf{S}$ has an upper bound. Then $M$ is a **least upper bound** for $A$ if (notes p. 2; ≈24:44–27:25)

1. $M$ is an upper bound for $A$, and
2. $M \leq M_1$ for every upper bound $M_1$ of $A$.

That is, $M$ is the smallest of the upper bounds, "so to speak" (≈27:25).

## Complete

An ordered set is **complete** if every subset that has an upper bound has a least upper bound (notes p. 2). For $\mathbf{R}$, the notes state it as: "If a subset $A$ of $\mathbf{R}$ has an upper bound, then $A$ has a least upper bound." This is the **least upper bound property**. On the board the definition is given for fields: a complete ordered field is an ordered field in which any bounded subset has a least upper bound (≈27:25–28:35).

One point Colding stressed in answer to a question: the least upper bound has to belong to the field itself. "Any bound, including the least upper bound, that always have to be in the fields" (≈1:12:51). That is exactly what fails in $\mathbf{Q}$, below.

## The existence of $\mathbf{R}$

**Theorem** (notes p. 2). There exists a complete ordered field that contains $\mathbf{Q}$. This field is denoted $\mathbf{R}$.

The course does not prove this and takes it for granted. The notes say a proof "would take us too far a field"; on the board it is "outside the scope of this class", though "you can prove this" (≈28:35–30:11). The board version says there is **a smallest** complete ordered field containing the rational numbers (≈29:21). The lecture does not say in what sense smallest, and the notes do not use the word.

## What completeness proves in Lecture 2

All three results below use the least upper bound property directly. Full proofs are on the [Lecture 2 page](02-introduction-to-real-numbers-cont.md).

- **$\sqrt{2} \in \mathbf{R}$** (notes pp. 2–3; ≈30:11–52:20). Let $A$ be the set of positive numbers whose square is less than $2$. It is nonempty, since $1 \in A$, and has an upper bound, $2$. So it has a least upper bound $x$. Two arguments by contradiction show that $x^2 \gt 2$ would make a slightly smaller number an upper bound, and that $x^2 \lt 2$ would put a slightly larger number in $A$. Hence $x^2 = 2$. The board takes $A$ inside $\mathbf{R}$; the notes take it inside $\mathbf{Q}$. See [the square root of 2](square-root-of-2.md).
- **$\mathbf{Q}$ is not complete** (notes p. 3; ≈52:20–54:54). The same argument would place $\sqrt{2}$ in any complete field containing $\mathbf{Q}$, and $\sqrt{2}$ is not rational. Concretely, the rationals whose square is at most $2$ have an upper bound in $\mathbf{Q}$, but no least upper bound in $\mathbf{Q}$ (≈1:12:05–1:12:51). See [the rational numbers](rational-numbers.md).
- **The Archimedean property** (notes p. 3; ≈54:54–1:00:49). If $\mathbf{N}$ had an upper bound in $\mathbf{R}$, it would have a least one, $\alpha$; but then $\alpha - 1$ would also be an upper bound, a contradiction. See [the Archimedean property](archimedean-property.md).

## Lectures

- [Lecture 1 — Introduction to Real Numbers](01-introduction-to-real-numbers.md): states that $\mathbf{R}$ is complete and defers the definition.
- [Lecture 2 — Introduction to Real Numbers (cont.)](02-introduction-to-real-numbers-cont.md): every definition and result above.
