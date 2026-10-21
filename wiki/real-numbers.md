# The real numbers

**What the course means by $\mathbf{R}$: a complete ordered field containing $\mathbf{Q}$, with each part of that sentence and where it is explained.**

## The course's answer, in one sentence

18.100B characterizes the real numbers by a single sentence, stated in Lecture 1 and taken apart over Lectures 1 and 2:

> $\mathbf{R}$ is a complete ordered field that contains the rational numbers $\mathbf{Q}$.

(Lecture 1, ≈12:45; notes p. 1.) Each word names a structure with precise axioms. A **field** has an addition and a multiplication obeying eleven axioms. An **ordered field** also has an order $\lt$ that is compatible with both operations. **Complete** means every subset with an upper bound has a least upper bound, a property $\mathbf{Q}$ lacks (both shown in Lecture 2). "Contains $\mathbf{Q}$" says the familiar fractions sit inside $\mathbf{R}$. The notes set the number systems in bold, $\mathbf{N}$, $\mathbf{Z}$, $\mathbf{Q}$, $\mathbf{R}$, and this knowledge base follows them.

## Why the course starts here

Colding opens with the [intermediate value theorem](intermediate-value-theorem.md). A continuous function on $[a, b]$ that is negative at $a$ and positive at $b$ must vanish somewhere in between. That is obvious from a picture, but a proof has to use *some* property of the real numbers, and the first job is to say which (Lecture 1, ≈10:18). Asking that leads to three questions (≈11:12–11:58; notes p. 1):

- What is a real number?
- Why is $\sqrt{2}$ a real number?
- What is $\sqrt{2}$?

The sentence above is the answer, and it is exactly what the proof of the intermediate value theorem will use (≈13:39).

## What is explained so far

**In Lecture 1:** everything except *complete*. The lecture defines $\mathbf{N}$, $\mathbf{Z}$ and $\mathbf{Q}$, builds the operations and the order on $\mathbf{Q}$ from quotients of integers, and abstracts them into the axioms for a field and for an ordered field. It proves two consequences of the axioms: the zero of a field is unique, and in an ordered field $x \lt y$ and $z \gt 0$ give $x z \lt y z$. It also checks that $\mathbf{Q}$ is an ordered field while $\mathbf{N}$ and $\mathbf{Z}$ are not even fields. See [Lecture 1](01-introduction-to-real-numbers.md), [the rational numbers](rational-numbers.md) and [fields and ordered fields](fields-and-ordered-fields.md).

**In Lecture 2:** *complete*. An ordered set is complete when every subset that has an upper bound has a least upper bound, the **least upper bound property** (Lecture 2 notes p. 2; ≈20:02–28:35). The course then takes for granted, without proof, the theorem that a complete ordered field containing $\mathbf{Q}$ exists, and that field *is* $\mathbf{R}$ (notes p. 2; ≈29:21–30:11). On the board Colding says there is "a smallest" such field (≈29:21); the notes do not use the word. Lecture 1's questions about $\sqrt{2}$ are answered too. No rational number squares to $2$ (≈10:04–15:44), but in $\mathbf{R}$ the least upper bound of the positive numbers whose square is less than $2$ is a positive number whose square is $2$ (≈30:11–52:20). So $\sqrt{2} \in \mathbf{R}$ and, as a corollary, $\mathbf{Q}$ is not complete. Completeness also gives the **Archimedean property**, that every real number is less than some natural number, and with it a rational number between any two real numbers (≈54:54–1:08:14). See [Lecture 2](02-introduction-to-real-numbers-cont.md), [completeness and the least upper bound property](least-upper-bound-property.md), [the square root of 2](square-root-of-2.md) and [the Archimedean property](archimedean-property.md).

**In Lecture 3:** nothing new about what $\mathbf{R}$ is, but the tools for working in it. Lower bounds and the greatest lower bound join upper bounds, with the notation $\sup A$ and $\inf A$, and Colding stresses that from here on the course concentrates on $\mathbf{R}$: when a problem does not name the larger set, it is $\mathbf{R}$ (Lecture 3, ≈14:56; Lecture 3 notes p. 1). The proofs that $\sqrt{2} \in \mathbf{R}$ and of the Archimedean property are written out again as formal proofs, and asked which properties of $\mathbf{R}$ the first one uses, Colding named the ordering, the ordered-field structure and completeness (≈1:06:55). See [Lecture 3](03-how-to-write-a-proof-archimedean-property.md) and [supremum and infimum](supremum-and-infimum.md).

**Not yet:** Lecture 3 defines a sequence of real numbers and, in the notes, convergence, and leaves limits for the next lecture (≈1:19:05). On the OCW lecture list, Lecture 4 is "Sequences; Convergence" and Lecture 5 is "Monotone Convergence Theorem". **This knowledge base covers Lectures 1 to 3 only.** See [sequences and limits](sequences-and-limits.md).

## Lectures

- [Lecture 1 — Introduction to Real Numbers](01-introduction-to-real-numbers.md): the defining sentence, the motivation, and every part of it except completeness.
- [Lecture 2 — Introduction to Real Numbers (cont.)](02-introduction-to-real-numbers-cont.md): completeness, the existence of $\mathbf{R}$ (taken for granted), $\sqrt{2} \in \mathbf{R}$, and the Archimedean property.
- [Lecture 3 — How to Write a Proof; Archimedean Property](03-how-to-write-a-proof-archimedean-property.md): $\sup$ and $\inf$, and formal proofs of $\sqrt{2} \in \mathbf{R}$ and the Archimedean property.
