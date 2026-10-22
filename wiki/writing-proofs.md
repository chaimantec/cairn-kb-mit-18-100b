# Writing proofs

**What 18.100B expects a proof to look like, as stated so far: the worked examples of Lectures 1 and 2, Lecture 3's advice on writing a formal proof, Lecture 4's first proofs with $\epsilon$ and $N$, Lecture 5's advice to analyse what has to be proved before writing it down, and Lecture 6's proofs from results not yet proved.**

Learning to write a mathematical proof is one of the course's two stated goals; the other is proving the theorems of calculus (Lecture 1, ≈4:44; notes p. 1). Lecture 3, "How to Write a Proof; Archimedean Property", is given over to it: it rewrites two of Lecture 2's proofs as formal proofs and says what that means. What follows is what Lectures 1 to 6 say and show.

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

## Scrap paper and the formal proof (Lecture 3)

Lecture 3 separates two activities: working out *why* something is true, and writing a proof of it (≈0:00). Lecture 2's proof that $\sqrt{2}$ is real was the first kind, "what you would be writing on the scrap paper". If you were handing a proof in or showing it to somebody, you would write it as Lecture 3 does (≈23:41–24:27). Writing proofs this way "may seem like a formal thing. Why bother with that? But it's really, really useful. And the more complicated things become, the more useful it is" (≈22:52). To keep attention on the writing, Colding reuses two results the class has already seen, the existence of a positive $\alpha$ with $\alpha^2 = 2$ and the Archimedean property (≈1:08:27–1:09:15). Both proofs are on the [Lecture 3 page](03-how-to-write-a-proof-archimedean-property.md).

His summary of the structure, for a proof like the one for $\alpha^2 = 2$ (≈1:04:36–1:06:09):

1. **Divide the proof into its steps** and write each step separately. Here there were two, $\alpha^2 \leq 2$ and $\alpha^2 \geq 2$.
2. **Say up front how each step is proved.** Both were by contradiction, so say so, and then assume the negation of what you want to prove.
3. **Say where the contradiction will come from**, "if you can, and it doesn't feel too much". For the second step: there will be a number larger than $\alpha$ whose square is still less than $2$, contradicting that $\alpha$ is an upper bound (≈54:06–55:49). The written Archimedean proof does the same: "we will get the desired contradiction by showing that alpha minus 1 is also an upper bound" (≈1:11:43–1:12:33).
4. **Define the objects you need, with no motivation.** The number $h = \frac{\alpha^2 - 2}{4 \alpha}$ is simply set, though "obviously, if this was the first time you would do it, you wouldn't just come up with this sort of thing": "This is coming from the scrap paper that you had" (≈35:02). In the formal proof "that seems to come out of nowhere" (≈1:06:09). In Lecture 2, by contrast, the calculation came first and $h$ appeared at the end (≈50:02–50:50).
5. **Establish the property that gives the contradiction**, and end with a line tying the steps together: "Together parts 1 and 2 show that $\alpha^2 = 2$; completing the proof" (notes p. 3; ≈1:04:36).

Two smaller habits from the same lecture. Establish only the properties you need, because establishing others "just makes it confusing" (≈27:43–28:28). And "it's always good to err on more details than fewer details", even when some steps come to feel almost too trivial (≈33:29–34:16).

**Write down what you want to show.** Colding's own board proof went wrong in a way that makes the point. Partway through the first step he began bounding the square of the smaller number from above, which is what the second step needs, before stopping to ask "what am I trying to prove here?" (≈39:04–46:54). His diagnosis: "I fell into the trap. I was doing it so formally that I lost track of what I was doing" (≈50:02). And a few minutes later: "if I really had written that before, then I wouldn't have been in trouble, because I was trying to prove something else" (≈58:08). The formal proof, he adds, is still "much easier to read afterwards" (≈50:02).

## Proofs with $\epsilon$ and $N$ (Lecture 4)

Lecture 4's proofs about limits all have one shape, set by the definition of convergence: for every $\epsilon \gt 0$ there is an $N$ such that $\vert a_n - a \vert \lt \epsilon$ for $n \geq N$. A proof is handed $\epsilon$, must produce $N$, and must then show the inequality for every $n$ past it. For $0.999 \cdots = 1$: "for your given epsilon, I specify a capital N", and then prove that every term beyond it is within $\epsilon$ of the limit (Lecture 4, ≈14:36–15:23). The $\epsilon$ is not yours to choose: "someone else is allowed to pick the epsilon" (≈7:11). The proofs are on the [Lecture 4 page](04-sequences-convergence.md).

Three habits recur.

- **Apply the hypothesis to the number you need.** Because convergence holds for every positive number, a proof may use it for $1$, $\frac{\epsilon}{2}$, $\frac{\epsilon}{\vert C \vert}$ or $\frac{\vert a \vert}{2}$ rather than the given $\epsilon$. Asked about this, Colding answered: "I'm basically using that for all epsilon, that it wasn't just for a fixed epsilon" (≈42:08). In the product proof he adds $1$ to the denominators, $\frac{\epsilon}{2 (\vert b \vert + 1)}$, because "I don't want to have something where if b was zero, then it really didn't make any sense what I wrote" (≈49:24).
- **Choose $N$ last.** When two hypotheses each give an $N$, take the larger. In the proof for sums, $N_a$ and $N_b$ come first, and only then "set capital N equal to the maximum of these two" (≈37:16).
- **Compare through something halfway between.** To compare $a_n b_n$ with $a b$, subtract and add $a_n b$. Colding calls this the main takeaway of the product proof, and a trick that comes back, for instance in the Leibniz rule for derivatives (≈43:44, ≈53:24–54:10). See [algebraic properties of limits](algebraic-properties-of-limits.md).

Lecture 4 also uses the distinction from Lecture 3 between a formal proof and a scrap-paper argument. The first two algebraic properties are written "formally, as we talked about last time"; for the third and fourth Colding gives what is "very, very close to a formal proof but it's more like what you would have on a piece of scrap paper" (≈30:25). The notes keep that split, with outlines that end in "details to fill in" (Lecture 4 notes p. 4); on the board the product proof ended up complete (≈51:53).

## Analyse first, then write (Lecture 5)

In Lecture 5's proof that the decimal approximations $a_n = \frac{b_n}{10^{n-1}}$ of $\sqrt{2}$ increase, Colding first works out on the board what $a_n \leq a_{n+1}$ amounts to: multiplying through by $10^n$, it is $10 \thinspace b_n \leq b_{n+1}$ (Lecture 5, ≈47:46–50:18). He then says how that differs from the proof as written: "if I was to write it down, I would probably have some of this on scrap paper. And then I would instead establish this here first, and then say, therefore, and then I'll conclude why. But of course, that's not the way you're thinking about it. You first try to analyze what you have to prove. And then once you know that, then you try to write it down nicely" (≈50:18–51:05). That is Lecture 3's distinction between scrap paper and the formal proof, seen from the scrap-paper side. The notes give only the written version, in which the needed inequality is reached "obviously" (Lecture 5 notes p. 3). See the [Lecture 5 page](05-monotone-convergence-theorem.md).

The proof of the monotone convergence theorem in the same lecture is a compact instance of Lecture 4's habits: it uses each half of a definition exactly once, that $\sup \lbrace a_n \rbrace$ is an upper bound and that it is the least one, and announces the switch, "Now I'm going to use that as the least upper bound" (≈38:32). See [the monotone convergence theorem](monotone-convergence-theorem.md).

## Proving a theorem from one not yet proved (Lecture 6)

Lecture 6 proves the Cauchy convergence theorem from the Bolzano–Weierstrass theorem, which it states but leaves for the next lecture, and says so: "But we're going to cheat just a little bit, because we are going to deduce it from another theorem that I will prove next time" (Lecture 6, ≈50:17). The contracting mapping theorem is proved from an exercise on Problem Set 3, of which Colding shows only "a special case that is a key starting point", the estimate for two consecutive terms, and he says why it is not yet a proof: "That's not enough to prove that's a Cauchy sequence, right, because I need to prove that for all n and m sufficiently large" (≈22:52).

The proofs reuse Lecture 4's habits. To show that a Cauchy sequence is bounded he applies the definition with $\epsilon = 1$ and then fixes one index: "I'm only applying this now and just choosing just one single m" (≈6:00). The proof that a Cauchy sequence converges chooses one number for each hypothesis, $N_1$ and $N_2$, each with $\frac{\epsilon}{2}$, and takes $N = \max \lbrace N_1, N_2 \rbrace$ (≈55:14–56:45). The proof that a continuous function preserves limits applies the definition of convergence with $\delta$ in the place of $\epsilon$ (≈1:05:08). See the [Lecture 6 page](06-cauchy-convergence-theorem.md).

## Board versus notes

Colding says the posted notes are written "slightly more rigorous", with "a little bit more meat", than the shorter board versions, and asks students to read them too (≈47:33–48:18). For Lecture 1, the notes and the board do differ in places. The board names the axiom behind each step of the ordered-field proof, while the notes compress it into three sentences. The board makes the commutativity step in the zero proof explicit, while the notes do not. In Lecture 2 the differences are of a different kind: the board and the notes define the set in the proof of $\sqrt{2} \in \mathbf{R}$ over different number systems, and label the steps of the last corollary differently. The [Lecture 2 page](02-introduction-to-real-numbers-cont.md#board-versus-notes) lists them. In Lecture 3 the formal proofs are the same on the board and in the notes in structure, but they name the auxiliary numbers differently and justify some bounds by different routes; the [Lecture 3 page](03-how-to-write-a-proof-archimedean-property.md#board-versus-notes) lists them. In Lecture 4 the board goes further than the notes: it proves the product property in full and carries the reciprocal property almost to the end, where the notes give outlines; the [Lecture 4 page](04-sequences-convergence.md#board-versus-notes) lists the differences. In Lecture 5 the board again spells out what the notes compress, such as each algebraic rule applied in turn in the example $\frac{n^2 + 1}{n^2 + n + 1} \to 1$, and the board's construction of two monotone sequences from any bounded sequence is not in the notes at all; the [Lecture 5 page](05-monotone-convergence-theorem.md#board-versus-notes) lists the differences.

## Expect it to take time

Colding says students need patience: learning to write proofs takes a little time (≈45:55). In his experience, a few weeks or months in, "things will really turn around, and it will all make sense. And then it will be more fun also" (≈1:05:20).

## Lectures

- [Lecture 1 — Introduction to Real Numbers](01-introduction-to-real-numbers.md): the case for rigor and three model proofs.
- [Lecture 2 — Introduction to Real Numbers (cont.)](02-introduction-to-real-numbers-cont.md): proofs by contradiction, an equality proved as two inequalities, and Colding's remarks on method.
- [Lecture 3 — How to Write a Proof; Archimedean Property](03-how-to-write-a-proof-archimedean-property.md): scrap paper versus the formal proof, and two of Lecture 2's proofs written out formally.
- [Lecture 4 — Sequences; Convergence](04-sequences-convergence.md): the first proofs with $\epsilon$ and $N$, formal proofs beside outlines, and the halfway trick.
- [Lecture 5 — Monotone Convergence Theorem](05-monotone-convergence-theorem.md): analysing an inequality on scrap paper before writing the proof.
- [Lecture 6 — Cauchy Convergence Theorem](06-cauchy-convergence-theorem.md): proofs from a theorem promised for later and from a homework exercise, and the habits of Lecture 4 again.
