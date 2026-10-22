# Cauchy sequences

**The definition of a Cauchy sequence and how it differs from convergence (Lecture 5); the theorem that a Cauchy sequence is bounded, and the proof that every Cauchy sequence of real numbers converges, from the Bolzano–Weierstrass theorem (Lecture 6), which Lecture 7 proves; the theorem's uses for series in Lectures 7 and 8, and Lecture 8's answer to why Cauchy sequences are convenient; and what is still missing: the converse, that a convergent sequence is Cauchy, is stated and used but not proved in the material here.**

Notation: $\mathbf{N}$ and $\mathbf{R}$ are the natural and the real numbers, set in bold as in the notes, $\vert x \vert$ is the absolute value of $x$, and a subsequence of $a_n$ is written $a_{n_k}$ (see [subsequences](subsequences.md)). On the board in Lecture 6 the sequence is called $x_n$; the notes call it $a_n$, as here.

## Why the course needs them

Colding's motivation (Lecture 5, ≈1:08:10–1:08:56): for a monotone sequence you can write the limit down explicitly, as the $\sup$ or the $\inf$ of the terms, and in all the examples so far it was easy to write down the limits. "But in general, you might not be able to write down the limit, but you want to prove that the limit exists" (≈1:08:56). A Cauchy sequence is defined by a condition on its terms alone, with no candidate limit in it. See [the monotone convergence theorem](monotone-convergence-theorem.md).

## Definition

**Definition** (Lecture 5 notes p. 6; Lecture 6 notes p. 1; Lecture 5, ≈1:08:56–1:09:45; Lecture 6, ≈1:37–3:24). A sequence $a_n$ is a **Cauchy sequence** if for all $\epsilon \gt 0$ there exists an $N$ such that if $m, n \geq N$, then

$$\vert a_n - a_m \vert \lt \epsilon .$$

On the board in Lecture 5 the condition is stated for $n$ and $m$ bigger than $N$ (≈1:09:45). Compare the definition of convergence to $a$, which asks for $\vert a_n - a \vert \lt \epsilon$ for $n \geq N$ (see [sequences and limits](sequences-and-limits.md)).

## How it differs from convergence

"This is a different notion than convergence" (Lecture 5, ≈1:09:45). Convergence says that everything far out in the sequence "accumulates around the limit"; the Cauchy condition says that if you are far out, "things bunch together, basically" (≈1:10:32). Lecture 6 recalls it the same way: "the Cauchy sequence just meant that the tail of the sequence bunched together" (Lecture 6, ≈3:24). The notes put it as "(Tail of the sequence bunch together.)" (Lecture 5 notes p. 6; Lecture 6 notes p. 1).

## A Cauchy sequence is bounded

**Theorem** (Lecture 6, ≈3:24–8:26; Lecture 6 notes p. 3). If $a_n$ is a Cauchy sequence, then $a_n$ is bounded. On the board this is a separate "little theorem"; in the notes it is the first step of the proof below.

**Proof.** Apply the definition with $\epsilon = 1$: there is an $N$ with $\vert a_n - a_m \vert \lt 1$ for $m, n \geq N$ (≈4:16–5:10). Fix $m = N$: "I'm only applying this now and just choosing just one single m" (≈6:00). Then for $n \geq N$,

$$\vert a_n \vert = \vert (a_n - a_N) + a_N \vert \leq 1 + \vert a_N \vert ,$$

so for every $n$,

$$\vert a_n \vert \leq \max \lbrace \vert a_N \vert + 1, \vert a_1 \vert, \cdots, \vert a_{N-1} \vert \rbrace$$

(Lecture 6 notes p. 3; ≈6:51–8:26). "So it means that if you have a Cauchy sequence, it's automatically bounded" (≈8:26). □ This is the argument Lecture 4 used to show that a convergent sequence is bounded, with $a_N$ in the place of the limit (see [sequences and limits](sequences-and-limits.md#a-convergent-sequence-is-bounded)).

## The Cauchy convergence theorem

**Theorem** (Lecture 5 notes p. 6; Lecture 6 notes p. 1; Lecture 5, ≈1:10:32–1:12:08; Lecture 6, ≈8:26–10:14). A sequence of real numbers is convergent if and only if it is a Cauchy sequence.

Lecture 5 states it without proof, "for now, everything is in R at the moment", and promises it: "I won't prove this now, but I'll prove this next time" (Lecture 5, ≈1:11:21). Lecture 6 proves that a Cauchy sequence converges. For the other direction Colding says "So recall that last time we showed the converse", that any convergent sequence is a Cauchy sequence (Lecture 6, ≈9:27–10:14). The Lecture 5 transcript and notes here do not contain that proof, and Lecture 6 does not give it either; the Lecture 6 notes print the "if and only if" and prove only one direction (pp. 1, 3). **This knowledge base therefore has no proof that a convergent sequence is Cauchy.**

## Proof that a Cauchy sequence converges

(Lecture 6, ≈49:32–58:28; Lecture 6 notes p. 3.) The proof uses the [Bolzano–Weierstrass theorem](bolzano-weierstrass-theorem.md), that every bounded sequence has a convergent subsequence, which Lecture 6 assumes and promises for the next lecture: "we're going to cheat just a little bit, because we are going to deduce it from another theorem that I will prove next time" (≈50:17). Lecture 7 proves it, by halving intervals (Lecture 7, ≈2:25–22:12; Lecture 7 notes pp. 1–2), and opens by recalling this argument: "you would then want to prove that the limit is actually a limit for the whole sequence. That's what we did, right?" (Lecture 7, ≈2:25).

1. A Cauchy sequence $a_n$ is bounded, so by the Bolzano–Weierstrass theorem it has a convergent subsequence $a_{n_k}$, with limit $a$ (≈52:38–54:23).
2. Let $\epsilon \gt 0$. There is an $N_1$ such that $\vert a_n - a_m \vert \lt \frac{\epsilon}{2}$ for $m, n \geq N_1$, because $a_n$ is Cauchy, and an $N_2$ such that $\vert a_{n_k} - a \vert \lt \frac{\epsilon}{2}$ for $k \geq N_2$, because the subsequence converges (≈55:14–55:59).
3. Let $N = \max \lbrace N_1, N_2 \rbrace$. For $n \geq N$, compare through a term of the subsequence:

$$\vert a_n - a \vert \leq \vert a_n - a_{n_k} \vert + \vert a_{n_k} - a \vert \lt \frac{\epsilon}{2} + \frac{\epsilon}{2} ,$$

so $a_n \to a$ (≈56:45–57:43; notes p. 3). □

The notes take the last step "if $n \geq N$ and $k \geq N$"; on the board the captions garble the line (≈56:45–57:43). For the first piece both $n$ and $n_k$ must be at least $N_1$, and neither the board nor the notes say why $n_k \geq N_1$. The idea of comparing through a term in between is Lecture 4's trick from the product of limits (see [algebraic properties of limits](algebraic-properties-of-limits.md)). In Lecture 5 Colding had said the proof would use the two monotone sequences formed from the $\sup$ and the $\inf$ of the tails of a bounded sequence (Lecture 5, ≈32:54, ≈1:11:21; see [the monotone convergence theorem](monotone-convergence-theorem.md#two-monotone-sequences-from-any-bounded-sequence)); the proof Lecture 6 gives goes through the Bolzano–Weierstrass theorem instead.

## What it is used for

- **The contracting mapping theorem** (Lecture 6, ≈27:41–36:43; notes p. 2). Iterating a contracting map from any starting point gives a Cauchy sequence (an exercise on Problem Set 3), so it converges, and its limit is a fixed point. "So from the Cauchy convergence theorem, then you get the contracting mapping theorem" (≈35:56). See [the contracting mapping theorem](contracting-mapping-theorem.md).
- **Newton's method** (Lecture 6, ≈37:31–49:32; notes pp. 2–3), through the contracting mapping theorem.
- **The extreme value theorem.** Colding introduces it as "another application of the Cauchy convergence theorem" (Lecture 6, ≈58:28), but the proof uses the Bolzano–Weierstrass theorem directly (≈1:11:40). See [the extreme value theorem](extreme-value-theorem.md).
- **Absolute convergence implies convergence** (Lecture 7, ≈1:02:21–1:05:31; Lecture 7 notes pp. 3–4). If $\sum \vert a_i \vert$ converges, its partial sums form a Cauchy sequence; the partial sums of $\sum a_i$ differ by no more, so they are Cauchy too, and they converge by the Cauchy convergence theorem. See [series](series.md#absolute-convergence).
- **The comparison test** (Lecture 8, ≈24:38–29:17). If $0 \leq a_n \leq b_n$, the difference of two partial sums of the $a_n$ is at most the corresponding difference for the $b_n$. So when the series of the $b_n$ converges, the partial sums of the $a_n$ form a Cauchy sequence and converge. See [convergence tests for series](convergence-tests-for-series.md).

**Why use Cauchy sequences here?** A student asked this in Lecture 8, recalling the original definition of convergence. Colding: "So if you went all the way back to the definition, then you would have to determine what the limit was" (Lecture 8, ≈27:45), and knowing the sum of one series does not give the sum of the other. "So the advantage with Cauchy sequence is that you don't have to figure out what the limit is" (≈28:31). The same test also has a proof by the monotone convergence theorem, which he gives next (≈29:17–30:48).

Lecture 7 also uses the other direction, that a convergent sequence is a Cauchy sequence, three times: in the absolute-convergence proof above, for the partial sums of $\sum \vert a_i \vert$ (≈1:04:44); to show that the geometric series diverges when $\vert c \vert \geq 1$, because consecutive partial sums stay at least $1$ apart, "Remember that if a sequence is convergent, if a sequence is convergent, then it is a Cauchy sequence" (≈43:16); and to show that a series whose terms do not go to $0$ diverges (≈55:11). See [the geometric series](geometric-series.md) and [series](series.md#first-check-do-the-terms-go-to-zero). Lecture 8 uses it twice more: for the same check on the terms, now by taking $m = n - 1$ in the Cauchy condition for the partial sums (Lecture 8, ≈2:27–5:46), and in the first proof of the comparison test, for the partial sums of the $b_n$ (≈29:17). The proof of that direction is still not in the material here; the Lecture 7 notes' recap states only "Every Cauchy sequence is convergent" (Lecture 7 notes p. 1).

## From the notes: Cauchy

The Lecture 5 notes quote a short biography "From Wikipedia": Baron Augustin-Louis Cauchy (1789–1857) was a French mathematician, engineer and physicist, one of the first to state and prove the key theorems of calculus rigorously, "thereby creating real analysis" (Lecture 5 notes p. 6). The lecture does not mention it.

## Not yet in this knowledge base

On the OCW lecture list, Lecture 12 is "Convergence in Metric Spaces; Operations on Sets", which is not yet in this knowledge base.

## Lectures

- [Lecture 5 — Monotone Convergence Theorem](05-monotone-convergence-theorem.md): the definition and the statement of the theorem.
- [Lecture 6 — Cauchy Convergence Theorem](06-cauchy-convergence-theorem.md): boundedness, the proof that a Cauchy sequence converges, and the applications.
- [Lecture 7 — Bolzano–Weierstrass Theorem; Cauchy Sequences; Series](07-bolzano-weierstrass-theorem-cauchy-sequences-series.md): the proof of the Bolzano–Weierstrass theorem, and both directions of the Cauchy convergence theorem used for series.
- [Lecture 8 — Convergence Tests for Series; Power Series](08-convergence-tests-for-series-power-series.md): the check on the terms and the first proof of the comparison test, and why Cauchy sequences avoid naming the limit.
