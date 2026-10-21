# Writing proofs

**What 18.100B expects a proof to look like, as stated so far, with the course's worked examples from Lectures 1 and 2.**

Learning to write a mathematical proof is one of the course's two stated goals; the other is proving the theorems of calculus (Lecture 1, ≈4:44; notes p. 1). Lecture 3 is titled "How to Write a Proof; Archimedean Property" on the OCW lecture list, but this knowledge base does not yet cover it. What follows is what Lectures 1 and 2 say and show.

## Why rigor

Colding's case for rigor is practical, not pedantic. If the foundation is not completely rigorous, you quickly reach statements that seem to be true but might not be, and soon you cannot even tell whether something should be true. Building up "step to step, where each step is totally rigorous" both guarantees that results are right and makes it easier to predict what should be true (≈9:29). The motivating example is the [intermediate value theorem](intermediate-value-theorem.md): obvious from a picture, but not proved until we know exactly which properties of $\mathbf{R}$ it uses.

## How detailed

The well-definedness proof for multiplication of rationals is offered explicitly as a calibration: "this is also supposed to illustrate how detailed a proof is" (≈31:22). The notes say the same: "This illustrate how detailed a proof should be" (p. 3). In that proof, every equation is justified either by the definition of equality of quotients or by a hypothesis.

Lecture 1's three proofs show the pattern:

- **Multiplication on $\mathbf{Q}$ is well defined** (≈24:49–31:22; notes p. 2). Unwind the definitions until the claim becomes an equation between integers, then derive it from the hypotheses by rearranging and substituting.
- **A field has only one zero** (≈44:19–48:18; notes p. 3). Suppose there are two, apply the defining property of each to their sum, and conclude that they are equal. The board version cites commutativity at the step where the notes leave it implicit.
- **In an ordered field, $x \lt y$ and $z \gt 0$ give $x z \lt y z$** (≈58:14–1:04:35; notes p. 4). Reduce the goal through a chain of equivalences until it is exactly one of the axioms. On the board, every step names the axiom that licenses it: "This is this law here that is chaining the ordering together with addition" (≈1:01:31).

All three are on the [Lecture 1 page](01-introduction-to-real-numbers.md).

## Proof by contradiction, and equalities as two inequalities

Most of Lecture 2's proofs are by contradiction: that no rational number squares to $2$, both halves of $\sqrt{2} \in \mathbf{R}$, that $\mathbf{Q}$ is not complete, and the Archimedean property. Only the last result, a rational number between any two reals, is proved directly. Colding comments on this himself (Lecture 2, ≈37:28). It may seem the class will always argue by contradiction, "and we won't". A direct proof is generally thought of as better style, but sometimes contradiction is more logical, and easier the first time, "and there's nothing wrong with proving it by contradiction."

Lecture 2 also models two habits worth copying.

- **Prove an equality as two inequalities.** To show that the least upper bound $x$ satisfies $x^2 = 2$, the proof shows $x^2 \leq 2$ and $x^2 \geq 2$ separately (≈36:41). Colding adds a colleague's joke that mathematics is three steps: locate a problem, prove whichever of the two inequalities is easier, and ask Raghu, his collaborator, to prove the other (≈45:15).
- **Do not name an object by what you hope to prove about it.** The least upper bound is called $x$, not $\sqrt{2}$, because "if I denote it by square root of 2, then it's going to be confusing", and you would automatically use what you think $\sqrt{2}$ should satisfy (≈34:20–35:07).

A further lesson came from the students. In step 2 of the proof the number $h$ had to satisfy two bounds at once, $h \lt 1$ and $h \lt \frac{2 - x^2}{2 x + 1}$, and the board had not said so. A student caught it, and Colding agreed (≈1:13:42–1:15:17). The full proofs are on the [Lecture 2 page](02-introduction-to-real-numbers-cont.md).

## Board versus notes

Colding says the posted notes are written "slightly more rigorous", with "a little bit more meat", than the shorter board versions, and asks students to read them too (≈47:33–48:18). For Lecture 1, the notes and the board do differ in places. The board names the axiom behind each step of the ordered-field proof, while the notes compress it into three sentences. The board makes the commutativity step in the zero proof explicit, while the notes do not. In Lecture 2 the differences are of a different kind: the board and the notes define the set in the proof of $\sqrt{2} \in \mathbf{R}$ over different number systems, and label the steps of the last corollary differently. The [Lecture 2 page](02-introduction-to-real-numbers-cont.md#board-versus-notes) lists them.

## Expect it to take time

Colding says students need patience: learning to write proofs takes a little time (≈45:55). In his experience, a few weeks or months in, "things will really turn around, and it will all make sense. And then it will be more fun also" (≈1:05:20).

## Lectures

- [Lecture 1 — Introduction to Real Numbers](01-introduction-to-real-numbers.md): the case for rigor and three model proofs.
- [Lecture 2 — Introduction to Real Numbers (cont.)](02-introduction-to-real-numbers-cont.md): proofs by contradiction, an equality proved as two inequalities, and Colding's remarks on method.
