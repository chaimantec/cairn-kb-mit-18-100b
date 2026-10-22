# The intermediate value theorem

**The course's opening example: a statement every calculus student believes, used to show why the real numbers must be defined precisely before anything can be proved.**

## Statement as given in Lecture 1

Let $a \lt b$ be real numbers and let $f : [a, b] \to \mathbf{R}$ be continuous, with $f(a) \lt 0$ and $f(b) \gt 0$. Then there is a $c$ between $a$ and $b$ with $f(c) = 0$ (Lecture 1, ≈5:29–7:09; notes p. 1). Colding also states the general form informally: a continuous function on an interval "takes all values in between" (≈7:09).

## Why it seems obvious

"Continuous" is first explained informally: when you draw the graph, the chalk is not allowed to leave the blackboard, and a function that jumps is not continuous (≈7:55–8:40). The notes say the same with a pencil and paper (p. 1). On that picture the theorem is clear: a graph drawn in one motion that starts below the axis and ends above it must cross the axis.

## Why that is not a proof

The course's point is that the picture is intuition, not proof, and the question "how do we make this into a proper proof?" is not merely semantic. Without a fully rigorous foundation one soon meets statements that seem true but are not, and can no longer tell what should be true (≈8:40–9:29). A proof has to use some property of the real numbers, so the first question is **which one** (≈10:18). The answer given is that $\mathbf{R}$ is a complete ordered field containing $\mathbf{Q}$ (≈12:45–13:39). The rest of Lecture 1 explains what "ordered field" means, and Lecture 2 explains "complete": every subset of $\mathbf{R}$ with an upper bound has a least upper bound. See [the real numbers](real-numbers.md) and [completeness and the least upper bound property](least-upper-bound-property.md).

Lecture 2 opens by recalling this example and the question it raised (Lecture 2, ≈0:00–2:27). Neither lecture defines continuity formally, and neither proves the theorem. Lecture 6 gives the rigorous definition, with $\epsilon$ and $\delta$, and proves the extreme value theorem for continuous functions on $[a, b]$, but not this theorem (see [continuous functions](continuous-functions.md) and [the extreme value theorem](extreme-value-theorem.md)).

## Where it is proved

On the OCW lecture list, Lecture 11 is "Extreme and Intermediate Value Theorem; Metric Spaces", with readings TBB Sections 5.4 and 13.1–13.2. **This knowledge base does not yet cover that lecture**, so it does not contain the course's proof.

## Lectures

- [Lecture 1 — Introduction to Real Numbers](01-introduction-to-real-numbers.md): the statement and its role as motivation.
- [Lecture 2 — Introduction to Real Numbers (cont.)](02-introduction-to-real-numbers-cont.md): recalls it as the motivating example, then defines completeness.
- [Continuous functions](continuous-functions.md): the rigorous definition of continuity, from Lecture 6.
