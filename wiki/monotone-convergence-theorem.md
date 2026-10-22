# The monotone convergence theorem

**Monotone increasing and decreasing sequences, the theorem that a bounded monotone sequence converges (to the $\sup$ or the $\inf$ of its terms), its proof from the least upper bound, the two monotone sequences built from any bounded sequence, and the application to $\sqrt{2}$ as the limit of its decimals. From Lecture 5.**

Notation: $\mathbf{N} = \lbrace 1, 2, 3, \cdots \rbrace$ and $\mathbf{R}$ are the natural and the real numbers, set in bold as in the notes. A sequence is written $a_n$, and $\sup \lbrace a_n \rbrace$ and $\inf \lbrace a_n \rbrace$ are the least upper bound and the greatest lower bound of the set of its terms (see [supremum and infimum](supremum-and-infimum.md)).

## Why the course needs it

By the end of Lecture 4 the course had a definition of convergence and only a *necessary* condition for it: a convergent sequence is bounded, but a bounded sequence such as $(-1)^n$ need not converge (Lecture 4, ≈17:00). The monotone convergence theorem is the first *sufficient* condition, and the first result in the course that proves a limit exists without being told in advance what the limit is. Colding introduces it to make precise the picture of $\sqrt{2}$ as $1.4$, $1.414$ and so on: "to make this more precise, we want to look at particular sequences, what's called monotone sequences" (Lecture 5, ≈15:20). The notes: to show that $\sqrt{2}$ is the limit of $a_1 = 1$, $a_2 = 1.4$, $a_3 = 1.41$, $a_4 = 1.414$, …, "we need something else. We need the monotone convergence theorem" (Lecture 5 notes p. 2).

## Monotone sequences

**Definition** (Lecture 5 notes p. 2; Lecture 5, ≈16:07–16:54). A sequence $a_n$ is **monotone increasing** if $a_n \leq a_{n+1}$ for all $n$, that is,

$$a_1 \leq a_2 \leq a_3 \leq \cdots ,$$

and **monotone decreasing** if $a_{n+1} \leq a_n$ for all $n$. A *strictly* monotone increasing sequence is one where the inequality is strict (≈16:07–16:54). A monotone increasing sequence is automatically bounded from below, by its first term: "already the first element is a lower bound" (≈19:21). Likewise a decreasing sequence is bounded from above by its first term.

## The theorem

**Monotone convergence theorem** (Lecture 5 notes p. 2; Lecture 5, ≈17:43–21:51).

- **Increasing version.** If $a_n$ is monotone increasing and bounded from above, so that there exists $A$ with $a_n \leq A$ for all $n$, then $a_n$ is convergent and

$$\lim_{n \to \infty} a_n = \sup \lbrace a_n \rbrace .$$

- **Decreasing version.** If $a_n$ is monotone decreasing and bounded from below, then $a_n$ converges and

$$\lim_{n \to \infty} a_n = \inf \lbrace a_n \rbrace .$$

In Colding's words, "if you have a monotone increasing sequence that is bounded, then it's also convergent. And likewise, if you have a monotone decreasing sequence that is bounded from below, then it is also convergent" (≈20:14). The theorem names the limit as well as asserting that it exists. Colding remarks later that for a monotone sequence "you could write down explicitly what the limit was", in contrast with Cauchy sequences, where in general you cannot (≈1:08:56; see [Cauchy sequences](cauchy-sequences.md)).

## The proof

The course proves the increasing version; the decreasing version "is just the same with obvious modifications" (Lecture 5, ≈34:28; notes p. 5: "The decreasing version is proven similarly").

**Proof** (Lecture 5 notes p. 5; Lecture 5, ≈34:28–41:49). Suppose $a_n \leq a_{n+1} \leq A$ for all $n$, and set $a = \sup \lbrace a_n \rbrace$. Given $\epsilon \gt 0$:

1. Because $a$ is an upper bound, $a_n \leq a$ for every $n$, so $a - a_n \geq 0$ and the absolute value in the definition of convergence can be dropped (≈37:00–38:32).
2. Because $a$ is the *least* upper bound and $a - \epsilon \lt a$, the number $a - \epsilon$ is not an upper bound. So some term exceeds it: there is an $N$ with $a_N \gt a - \epsilon$ (≈38:32–39:32).
3. Because the sequence is increasing, every later term is at least $a_N$. So for $n \geq N$,

$$a - \epsilon \lt a_N \leq a_n \leq a ,$$

and therefore $0 \leq a - a_n \lt \epsilon$ (≈40:17–41:03). □

Each half of the definition of $\sup$ is used once: being an upper bound gives $a_n \leq a$, and being the least one gives the $N$. "Now I'm going to use that as the least upper bound" (≈38:32). The picture: all the $a_n$ from $a_N$ on are "squished in this little interval" between $a - \epsilon$ and $a$ (≈40:17–41:03).

The proof needs $\sup \lbrace a_n \rbrace$ to exist. Neither the lecture nor the notes say so at this point, but that is the [least upper bound property](least-upper-bound-property.md) of $\mathbf{R}$: the set of terms is non-empty and bounded from above, so it has a least upper bound.

## Two monotone sequences from any bounded sequence

This is on the board only (Lecture 5, ≈21:51–33:39); the notes do not have it.

A random sequence is not monotone (≈21:51). But if $a_n$ is bounded, the suprema and infima of its tails,

$$b_n = \sup \lbrace a_n, a_{n+1}, a_{n+2}, \cdots \rbrace , \qquad c_n = \inf \lbrace a_n, a_{n+1}, a_{n+2}, \cdots \rbrace ,$$

are two monotone sequences (≈23:24–24:10). $b_{n+1}$ is a sup over a smaller set than $b_n$, so $b_n \geq b_{n+1}$ and $b_n$ is decreasing (≈24:10–25:48). $c_{n+1}$ is an inf over fewer elements than $c_n$, so $c_{n+1} \geq c_n$ and $c_n$ is increasing (≈28:08–28:56). For each $n$ both are taken over the same set, so $c_n \leq b_n$ (≈29:46). Both sequences are bounded, so by the theorem $b_n$ decreases to a limit $b$ and $c_n$ increases to a limit $c$, and Colding adds that "we'll prove this later, but it seems probably pretty obvious that the limit here, c is less than or equal to b" (≈32:08–32:54).

He says this construction "will play an important role when we prove the basic theorem about Cauchy sequences" (≈32:54; in Lecture 6 that proof goes through the [Bolzano–Weierstrass theorem](bolzano-weierstrass-theorem.md) instead, and the construction does not appear) and that "this is how one defines limsup and liminf", which the course has not yet defined (≈1:07:23–1:08:10). For a monotone increasing sequence it is "almost like too simple": a student asked about that case, and Colding answered that every $b_n$ is then the limit, so $b_n$ is constant (≈25:48–27:19). The full passage, with his picture of the $c_n$ always lying to the left of the $b_n$, is on the [Lecture 5 page](05-monotone-convergence-theorem.md).

## Application: $\sqrt{2}$ as the limit of its decimals

(Lecture 5 notes pp. 3–4; Lecture 5, ≈41:49–1:05:47.) Let $b_n$ be the largest integer with $b_n^2 \leq 2 \cdot 10^{2n-2}$, and set $a_n = \frac{b_n}{10^{n-1}}$. Then $a_1 = 1$, and the notes describe the sequence as $1$, $1.4$, $1.41$, $1.414$, …: "the n is referring to the number of digits, but including the digits that is before the point" (≈53:26).

- **Increasing.** $(10 \thinspace b_n)^2 = 100 \thinspace b_n^2 \leq 2 \cdot 10^{2(n+1)-2}$, and $b_{n+1}$ is the largest integer with that property, so $b_{n+1} \geq 10 \thinspace b_n$, which is $a_{n+1} \geq a_n$ (≈47:46–53:26).
- **Bounded.** $(2 \cdot 10^{n-1})^2 = 4 \cdot 10^{2n-2}$ is too big, so $b_n \leq 2 \cdot 10^{n-1}$ and $a_n \leq 2$ (≈54:12–55:47).
- **So it converges**, to some $a$, by the monotone convergence theorem (≈56:56).
- **$a^2 = 2$.** Each $a_n^2 \leq 2$, so $a^2 \leq 2$; and because $b_n$ is the largest, $(b_n + 1)^2 \gt 2 \cdot 10^{2n-2}$, which gives $(a_n + 10^{1-n})^2 \gt 2$ and, in the limit, $a^2 \geq 2$. Both limits use the algebraic properties of limits (≈56:56–1:04:58).

"This is one more proof that square root of 2 is a real number. But this is in a way how you think about it, in terms of the decimals" (≈59:33). The step-by-step proof, and where the board and the notes differ, are on the [Lecture 5 page](05-monotone-convergence-theorem.md); the course's other proofs that $\sqrt{2}$ is real are on [the square root of 2](square-root-of-2.md).

## What is used without proof

Two facts that the application relies on are asserted in Lecture 5 rather than proved. One is that a limit keeps an inequality that every term satisfies, with a strict inequality becoming non-strict in the limit (≈58:38, ≈1:04:58–1:07:23); the related claim that $c \leq b$ for the tails construction is promised: "we'll prove this later" (≈32:54). The other is that $\frac{1}{n^2}$ and $10^{1-n}$ tend to $0$ (≈9:00, ≈1:04:13).

## Not yet in this knowledge base

Lecture 6 opens by recalling the theorem (Lecture 6, ≈0:00–1:37) and is covered on [its own page](06-cauchy-convergence-theorem.md). On the OCW lecture list, Lecture 7 is "Bolzano–Weierstrass Theorem; Cauchy Sequences; Series" (TBB Sections 2.11–2.12 and 3.4), and Lecture 9 is "Limsup and Liminf; Power Series; Continuous Functions; Exponential Function". Neither is covered here yet. The OCW readings for Lecture 5 are TBB Sections 2.8, 2.9 and 2.11.

## Lectures

- [Lecture 5 — Monotone Convergence Theorem](05-monotone-convergence-theorem.md): the definition, the theorem, its proof, the tails construction and the $\sqrt{2}$ application.
- [Lecture 4 — Sequences; Convergence](04-sequences-convergence.md): convergence, and the boundedness theorem that the monotone convergence theorem complements.
