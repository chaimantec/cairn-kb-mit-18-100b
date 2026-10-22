# The Bolzano–Weierstrass theorem

**Every bounded sequence of real numbers has a convergent subsequence: the statement, Lecture 7's proof by halving intervals and squeezing the subsequence between two monotone sequences, and the theorem's two uses in Lecture 6, for the Cauchy convergence theorem and the extreme value theorem, where it was assumed.**

Notation: $\mathbf{R}$ is the real numbers, set in bold as in the notes, $\vert x \vert$ is the absolute value of $x$, and a subsequence of $a_n$ is written $a_{n_k}$ (see [subsequences](subsequences.md)). The notes spell the name "Bolzano-Weirstrass", a printed slip for Weierstrass.

## The statement

**Bolzano–Weierstrass theorem** (Lecture 6 notes p. 3; Lecture 7 notes p. 1; Lecture 6, ≈51:05; Lecture 7, ≈1:39). Any bounded sequence has a convergent subsequence.

On the board: "So the Bolzano-Weierstrass theorem says that every bounded sequence has a convergent subsequence" (Lecture 6, ≈51:05). A sequence is bounded when the set of its terms is bounded from above and from below (Lecture 4; see [sequences and limits](sequences-and-limits.md)). The theorem does not say that the sequence itself converges, only that some subsequence does. Colding makes the point in the proof of the extreme value theorem: "It's a good exercise to see that this sequence in itself-- you can just draw a little picture, and you convince yourself that this sequence in itself may not be convergent" (Lecture 6, ≈1:11:40). Lecture 4's example $(-1)^n$ shows the difference: it is bounded and does not converge (Lecture 4, ≈17:00), but its even-numbered terms form the constant subsequence $1, 1, 1, \cdots$ (Lecture 4, ≈1:04:28–1:06:05; see [subsequences](subsequences.md)).

Lecture 6 used the theorem without proving it: "But we're going to cheat just a little bit, because we are going to deduce it from another theorem that I will prove next time" (Lecture 6, ≈50:17). Lecture 7 opens with the proof: "But we didn't prove the Bolzano-Weierstrass Theorem. So let's try to prove it now" (Lecture 7, ≈2:25).

## The proof (Lecture 7)

(Lecture 7, ≈3:13–22:12; Lecture 7 notes pp. 1–2.) Assume, "for simplicity", that every $a_n$ lies in $[0, 1]$ (notes p. 1). "It could be any other bounded interval. But let's just say 0 to 1" (≈3:13); "the same argument works for any other interval" (≈9:27). How the general case follows is not shown.

**The idea** (≈3:13–7:54). Find a subsequence $a_{n_k}$ and two sequences with $b_k \leq a_{n_k} \leq c_k$, where the $b_k$ increase and the $c_k$ decrease, so that the subsequence "is going to be squeezed between two other sequences" (≈4:50) and "that's going to force it to converge" (≈7:07). The two outer sequences "are much nicer" (≈4:50): they are monotone, so they converge, and if they come together they have the same limit.

**The construction** (≈9:27–19:01; notes p. 1).

1. Set $b_1 = 0$, $c_1 = 1$ and $a_{n_1} = a_1$ (≈10:13).
2. Halve the interval. One of the halves, $[0, \frac{1}{2}]$ or $[\frac{1}{2}, 1]$, contains infinitely many terms of the sequence, "either infinitely many here or infinitely many there" (≈11:02); possibly both, and then pick one (≈17:26). Say $[0, \frac{1}{2}]$.
3. Let $a_{n_2}$ be the next term after $a_{n_1}$ in that half, so that $n_2 \gt n_1$; it "could be the same value. But it will have to come from a different subscript" (≈13:27). Set $b_2 = 0$ and $c_2 = \frac{1}{2}$, the endpoints of the half (≈13:27).
4. From now on look only at the infinitely many terms in that half (≈14:15). Halve again, keep a half with infinitely many of them, say $[\frac{1}{4}, \frac{1}{2}]$, take as $a_{n_3}$ the next term after $a_{n_2}$ in it, and set $b_3 = \frac{1}{4}$, $c_3 = \frac{1}{2}$ (≈15:04–16:41; notes p. 1).
5. Continue: at each step $b_k$ and $c_k$ are the left and right endpoints of the current interval (≈17:26).

**The endpoints** (≈19:01–21:22). Each new interval is a half of the previous one, so the $b_k$ increase, the $c_k$ decrease, and the length halves: $c_{k+1} - b_{k+1} = \frac{1}{2} (c_k - b_k)$, with $c_1 - b_1 = 1$, so

$$c_k - b_k = 2^{1-k}$$

(≈19:47–20:36). The monotone sequences are bounded, each $b_k$ by the first $c$ and each $c_k$ by the first $b$ (≈7:07), so by the [monotone convergence theorem](monotone-convergence-theorem.md) $b_k \to b$ and $c_k \to c$. Since the difference goes to $0$, $b = c$ (≈21:22).

**The squeeze** (≈21:22–22:12). For $l \geq k$ the term $a_{n_l}$ lies in the $k$-th interval, between $b_k$ and $c_k$ (≈22:12). So the subsequence, squeezed between two sequences that converge to $b$, also converges to $b$: "So that's a Bolzano-Weierstrass Theorem" (≈22:12). □ That a sequence squeezed between two sequences with the same limit has that limit is used without proof, on the board and in the notes.

**Questions** (≈7:54–9:27). Asked "Do they need to be strictly monotonic?", Colding said no: $b_k \leq b_{k+1}$ and $c_k \geq c_{k+1}$, "So it's not strict" (≈7:54–8:40). To a partly inaudible question about the two sequences not coming together he answered: "So you're right that if they didn't come together, we couldn't conclude things. But they will come together. This I will guarantee" (≈9:27).

**The notes' version** (notes pp. 1–2) makes the same choices but defines $b_k$ and $c_k$ after the subsequence. It first observes that for $k_1, k_2 \geq k$,

$$\vert a_{n_{k_1}} - a_{n_{k_2}} \vert \leq 2^{1-k} ,$$

so the subsequence is a Cauchy sequence, "However, more is true" (notes p. 1): the proof goes on to the squeeze between $b_k$ and $c_k$, "the left endpoint of the interval of length $2^{1-k}$ that all the element $a_{n_i}$ will lie in when $i \geq k$" and the right endpoint of the same interval (notes p. 1). The full walk-through is on the [Lecture 7 page](07-bolzano-weierstrass-theorem-cauchy-sequences-series.md).

**Where the proof sits.** Lecture 6 proved the Cauchy convergence theorem from this theorem, so with Lecture 7's proof that chain is complete. The proof itself uses the monotone convergence theorem (Lecture 5), and through it the least upper bound property of $\mathbf{R}$. In Lecture 5 Colding had built two monotone sequences from any bounded sequence, the $\sup$ and the $\inf$ of its tails, and said they would "play an important role when we prove the basic theorem about Cauchy sequences" (Lecture 5, ≈32:54); Lecture 7's monotone sequences are the endpoints of the halved intervals instead.

## Use 1: the Cauchy convergence theorem

A Cauchy sequence is bounded, so by the Bolzano–Weierstrass theorem it has a convergent subsequence $a_{n_k} \to a$. Because the terms of a Cauchy sequence bunch together, the whole sequence then converges to $a$: for $n$ large, $\vert a_n - a \vert \leq \vert a_n - a_{n_k} \vert + \vert a_{n_k} - a \vert$, and each piece is less than $\frac{\epsilon}{2}$ (Lecture 6, ≈51:51–58:28; Lecture 6 notes p. 3). "So this is why the Bolzano-Weierstrass theorem implies the Cauchy convergence theorem" (Lecture 6, ≈58:28). Lecture 7 recalls the argument (Lecture 7, ≈1:39–2:25). The full proof is on [Cauchy sequences](cauchy-sequences.md#proof-that-a-cauchy-sequence-converges) and the [Lecture 6 page](06-cauchy-convergence-theorem.md).

## Use 2: the extreme value theorem

A continuous function $f$ on $[a, b]$ attains its supremum. Take $x_n \in [a, b]$ with $f(x_n) \to \sup f$. The sequence $x_n$ is bounded because it lies in $[a, b]$, so it has a convergent subsequence $x_{n_k} \to x$, with $x \in [a, b]$, and continuity gives $f(x_{n_k}) \to f(x)$, so $f(x) = \sup f$ (Lecture 6, ≈1:09:56–1:14:44; Lecture 6 notes p. 4). The notes call the extreme value theorem "Another application of the Bolzano-Weirstrass theorem" (Lecture 6 notes p. 3). On the board Colding first calls it an application of the Cauchy convergence theorem (Lecture 6, ≈58:28), and then corrects the emphasis: "So then I'm using not Cauchy convergence theorem. I'm using the Bolzano-Weierstrass theorem, which implies the Cauchy convergence theorem. But I will use the Bolzano-Weierstrass theorem" (Lecture 6, ≈1:11:40). See [the extreme value theorem](extreme-value-theorem.md).

The Lecture 7 notes quote a biography of Weierstrass "From Wikipedia", which says that he "used the latter to study the properties of continuous functions on closed bounded intervals" (Lecture 7 notes p. 2).

## Not yet in this knowledge base

On the OCW lecture list, Lecture 14 is "Sequential Compactness; Bolzano–Weierstrass Theorem in a Metric Space", which is not covered here yet.

## Lectures

- [Lecture 6 — Cauchy Convergence Theorem](06-cauchy-convergence-theorem.md): the statement, assumed, and its use for the Cauchy convergence theorem and the extreme value theorem.
- [Lecture 7 — Bolzano–Weierstrass Theorem; Cauchy Sequences; Series](07-bolzano-weierstrass-theorem-cauchy-sequences-series.md): the proof.
- [Subsequences](subsequences.md): what a subsequence is, and the theorem that a subsequence of a convergent sequence has the same limit.
- [The monotone convergence theorem](monotone-convergence-theorem.md): used in the proof.
