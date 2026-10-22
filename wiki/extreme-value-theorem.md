# The extreme value theorem

**A continuous function on a closed interval $[a, b]$ attains its supremum and its infimum, so they are a maximum and a minimum: the statement and proof as given in Lecture 6, from the Bolzano–Weierstrass theorem, why the endpoints must be included, and what the proof leaves to the reader.**

Notation: $a \lt b$ are real numbers, $[a, b]$ is the interval of real numbers $x$ with $a \leq x \leq b$, which includes both endpoints, and $\sup f$ and $\inf f$ are the supremum and the infimum of the values of $f$ on $[a, b]$ (see [supremum and infimum](supremum-and-infimum.md)).

## The statement

**Extreme value theorem** (Lecture 6 notes p. 4; Lecture 6, ≈1:06:48–1:08:22). Let $f$ be a continuous function on an interval $[a, b]$. Then the sup and the inf of $f$ are achieved: there exists $x \in [a, b]$ with $f(x) = \sup f$, and likewise for $\inf f$.

Colding stresses both hypotheses: "It needs to be continuous at all points. And this interval needs to contain the endpoints also" (Lecture 6, ≈1:06:48). He names the points: the sup is the value at a point $x_M$, "capital M for Max", and the inf is the value at a point $x_m$ (≈1:07:37–1:08:22). "In particular, the sup is finite. And it's not really a sup. It's a max" (≈1:07:37). The infimum part follows from the supremum part "by looking at the function minus f if you wanted", or from the same proof (≈1:08:22).

## The proof

The proof is for the supremum; "The proof that the infimum is the same with obvious modification" (Lecture 6 notes p. 4; ≈1:09:56). It needs three results: the [Bolzano–Weierstrass theorem](bolzano-weierstrass-theorem.md), assumed in Lecture 6 and proved in Lecture 7; the theorem that a continuous function takes a convergent sequence to a convergent sequence (see [continuous functions](continuous-functions.md)); and Lecture 4's theorem that a subsequence of a convergent sequence has the same limit (see [subsequences](subsequences.md)).

1. **A sequence approaching the sup** (≈1:09:56–1:10:43). Choose $x_n \in [a, b]$ with $f(x_n) \to \sup f$ (notes p. 4). Colding allows the sup to be infinite a priori, "if there is no upper bound, then I will write infinity" (≈1:09:56); then the sequence is one where "the value of these become larger and larger without bound" (≈1:10:43).
2. **A convergent subsequence** (≈1:10:43–1:12:26). The $x_n$ lie in $[a, b]$, so the sequence is bounded, and by the Bolzano–Weierstrass theorem it has a convergent subsequence $x_{n_k} \to x$ (notes p. 4; on the board the limit is called $x_M$). The sequence $x_n$ itself need not converge (≈1:11:40).
3. **The limit lies in $[a, b]$** (≈1:12:26–1:13:11). "And it converges to something in this interval. And that's important", because $f$ is defined there (≈1:12:26). The notes: "Note that $x \in [a, b]$." (notes p. 4).
4. **Two limits** (≈1:13:11–1:13:57). By continuity, $f(x_{n_k}) \to f(x)$. And $f(x_{n_k})$ is a subsequence of $f(x_n)$, which converges to $\sup f$: "But if you take a sequence that converges to whatever number, then any subsequence will converge to the same number" (≈1:13:57). So $\sup f = f(x)$ (notes p. 4). □

"So the sup is really a max", and by a very similar proof the infimum is achieved too (≈1:14:44).

## Why the endpoints matter

If the interval did not include its endpoints, the subsequence could converge to an endpoint, "but the function would not be defined there. So you wouldn't be able to conclude the extreme value theorem" (Lecture 6, ≈1:12:26–1:13:11). The lecture gives no example of a function for which the conclusion then fails.

## The student's question: where does the sequence come from?

After the proof a student asked, in a question that is partly inaudible, about step 1; Colding asked, "Are you asking why such a bounded sequence exists?" (Lecture 6, ≈1:15:32). His answer uses that the sup is the *least* upper bound: for any $\epsilon$, the sup minus $\epsilon$ is not an upper bound, so there must be a point $x$ of the interval where the value of $f$ is larger than it (≈1:15:32–1:16:18). "And so you could imagine, instead of epsilon here, looking at a sequence like this", and that gives the sequence (≈1:16:18); the captions do not record which values of $\epsilon$ he wrote. The same use of the least upper bound appears in the proof of the [monotone convergence theorem](monotone-convergence-theorem.md).

## What the proof leaves to the reader

- **An infinite supremum.** If the sup was a priori infinite, "that is still fine. But that should only take a minute, to convince yourself about that" (≈1:13:57). The argument is not given.
- **Why the limit is in $[a, b]$.** That a limit of points satisfying $a \leq x_{n_k} \leq b$ also satisfies these inequalities is used without proof, here and in Lecture 5 (see [the monotone convergence theorem](monotone-convergence-theorem.md#what-is-used-without-proof)).
- **The domain.** The theorem on continuous functions is stated in the notes for $f : \mathbf{R} \to \mathbf{R}$ and applied to a function on $[a, b]$ (notes p. 4); on the board Colding says the domain may be a subset of $\mathbf{R}$ if you are careful that everything is in the domain (≈1:02:42).

## Not yet in this knowledge base

On the OCW lecture list, Lecture 11 is "Extreme and Intermediate Value Theorem; Metric Spaces" (TBB Sections 5.4 and 13.1–13.2), which is not covered here yet. The proof of the Bolzano–Weierstrass theorem, which the proof above uses, is on [its own page](bolzano-weierstrass-theorem.md) (Lecture 7).

## Lectures

- [Lecture 6 — Cauchy Convergence Theorem](06-cauchy-convergence-theorem.md): the statement and the proof, and the question about the sequence.
- [The intermediate value theorem](intermediate-value-theorem.md): the course's other theorem about continuous functions on $[a, b]$, stated in Lecture 1 and not yet proved.
