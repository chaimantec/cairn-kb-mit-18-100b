# Fields and ordered fields

**The axioms 18.100B uses to say what the real numbers are, as stated in Lecture 1, with the consequences proved so far, the course's examples and non-examples, and where completeness (Lecture 2) fits in.**

## Field

A **field** $\mathbf{F}$ is a set with two operations, written suggestively as $+$ and $\cdot$. The symbols are only suggestive: the operations are abstract and are characterized by the axioms alone (Lecture 1, ≈33:05; notes p. 3). There are eleven axioms: five for addition, five for multiplication that mirror them, and one that ties the two together (≈33:52). In the statements below, $x$, $y$ and $z$ are arbitrary elements of $\mathbf{F}$.

| | Addition | Multiplication | Name used in lecture |
| --- | --- | --- | --- |
| 1 | $x + y \in \mathbf{F}$ | $x y \in \mathbf{F}$ | it is an operation |
| 2 | $x + y = y + x$ | $x y = y x$ | commutative, or abelian |
| 3 | $(x + y) + z = x + (y + z)$ | $(x y) z = x (y z)$ | associative |
| 4 | some $0 \in \mathbf{F}$ has $0 + x = x$ for all $x$ | some $1$ has $1 x = x$ for all $x$ | neutral element |
| 5 | each $x$ has a $(-x)$ with $x + (-x) = 0$ | each $x \neq 0$ has a $\frac{1}{x}$ with $x \frac{1}{x} = 1$ | inverse element |

The eleventh axiom is the **distributive law**,

$$(x + y) z = x z + y z ,$$

as printed in the notes (p. 3). On the board it is written $x(y + z) = xy + xz$ (≈43:32), the same statement by commutativity, and Colding later calls it "the 11th law" (≈1:02:19).

Two points the lecture stresses. Multiplicative axiom 5 has a twist: $0$ is excluded, so $0$ has no multiplicative inverse (≈41:57). And apart from that mention of $0$, the first ten axioms say nothing about how the operations interact; the distributive law is the only axiom "chaining" them (≈42:43). The notes use "chains" in the same sense for the ordered-field axioms below.

**Consequence proved: the zero is unique.** Axiom 4 asserts that *a* zero exists. If $0_ {1}$ and $0_ {2}$ are both zeros, then $0_ {1} + 0_ {2} = 0_ {2}$, because $0_ {1}$ is a zero. By commutativity $0_ {1} + 0_ {2} = 0_ {2} + 0_ {1}$, and that equals $0_ {1}$, because $0_ {2}$ is a zero. So $0_ {1} = 0_ {2}$ (≈45:55–47:33; notes p. 3). The board version uses commutativity explicitly; the notes leave it implicit. Full proof on the [Lecture 1 page](01-introduction-to-real-numbers.md).

**Examples** (≈48:18–50:37; notes p. 4):

- $\mathbf{Q}$ is a field.
- $\mathbf{N}$ is not: among other failures, it has no zero element.
- $\mathbf{Z}$ is not, though it is closer. Multiplicative axiom 5 fails, because $2$ would need an inverse, one half, which is not an integer.

## Ordered set

An **ordered set** $\mathbf{S}$ is a set with a relation $\lt$ such that (notes p. 4):

1. for any $x, y \in \mathbf{S}$, one of $x \lt y$, $y \lt x$, $x = y$ holds;
2. if $x \lt y$ and $y \lt z$, then $x \lt z$.

The first property means any two elements can be compared: if they are different, one is smaller (≈53:26). The second, transitivity, is in the Lecture 1 notes but is not stated aloud in that lecture; Lecture 2's recap states it (Lecture 2, ≈4:57–5:42).

## Ordered field

An **ordered field** is a field that is also an ordered set, in which the order is compatible with the operations (≈54:15–56:33; notes p. 4):

1. if $x \lt y$, then $x + z \lt y + z$, for every $z$;
2. if $x \gt 0$ and $y \gt 0$, then $x y \gt 0$.

The first says you may add the same element to both sides of an inequality. The second says a product of positives is positive.

**Consequence proved: multiplying by a positive element preserves order.** If $x \lt y$ and $z \gt 0$, then $x z \lt y z$ (≈58:14–1:04:35; notes p. 4). Adding $-(x z)$ to both sides (axiom 1) turns the goal into $0 \lt y z - x z$. The distributive law rewrites this as $(y - x) z$. Adding $-x$ to both sides of $x \lt y$ (axiom 1 again) gives $y - x \gt 0$, and then axiom 2 makes $(y - x) z$ positive. Step-by-step proof on the [Lecture 1 page](01-introduction-to-real-numbers.md).

**Example:** $\mathbf{Q}$, with the order defined by cross-multiplying, is an ordered field (≈56:33–58:14).

**The element $1$ is unique too, and $-1$ is defined from it.** Asked at the end of Lecture 2 how $-1$ is defined, Colding answered that $1$ is the neutral element for multiplication, that the argument that proved the zero unique also proves $1$ unique, so "1" is a well-defined notion, and that $-1$ is the inverse of $1$ with respect to addition (Lecture 2, ≈1:09:46–1:10:32).

## Complete ordered field

The course's description of $\mathbf{R}$ is "a complete ordered field that contains $\mathbf{Q}$" (Lecture 1, ≈12:45). Lecture 2 defines the last word. An ordered set is **complete** if every subset that has an upper bound has a least upper bound (Lecture 2 notes p. 2). On the board, a complete ordered field is an ordered field in which any bounded subset has a least upper bound (Lecture 2, ≈27:25–28:35). $\mathbf{Q}$ is an ordered field but not a complete one. The course takes for granted that a complete ordered field containing $\mathbf{Q}$ exists, and calls it $\mathbf{R}$. See [completeness and the least upper bound property](least-upper-bound-property.md) and [the real numbers](real-numbers.md).

## Lectures

- [Lecture 1 — Introduction to Real Numbers](01-introduction-to-real-numbers.md): all of the field and ordered-field definitions and both theorems above.
- [Lecture 2 — Introduction to Real Numbers (cont.)](02-introduction-to-real-numbers-cont.md): a recap of the axioms, the uniqueness of $1$ (in answer to a question), and complete ordered fields.
