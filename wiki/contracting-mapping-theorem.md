# The contracting mapping theorem

**Fixed points, contracting maps $T : \mathbf{R} \to \mathbf{R}$, and the theorem that a contracting map has exactly one fixed point: stated in Lecture 5, proved in Lecture 6 from the Cauchy convergence theorem and a Problem Set 3 exercise; the iteration $a_{n+1} = T(a_n)$ that finds the fixed point; Newton's method as an application; and why the course cares: the same theorem in other spaces gives solutions to differential equations.**

Notation: $\mathbf{R}$ is the real numbers, set in bold as in the notes, and $\vert x \vert$ is the absolute value of $x$. Colding calls it the "contracting mapping theorem", and once the "contraction mapping theorem" (Lecture 5, ≈1:13:39).

## Fixed points

**Definition** (Lecture 5 notes p. 6; Lecture 6 notes p. 1; Lecture 5, ≈1:17:08; Lecture 6, ≈12:58–13:52). If $T : \mathbf{R} \to \mathbf{R}$ is a map, then $x_0 \in \mathbf{R}$ is a **fixed point** of $T$ if

$$T(x_0) = x_0 .$$

"For a map T, if it is under the map, the point remain unchanged" (Lecture 6, ≈12:58).

## Contracting maps

**Definition** (Lecture 5 notes p. 6; Lecture 6 notes p. 1; Lecture 5, ≈1:13:39–1:15:25; Lecture 6, ≈11:07–12:58). A **contracting map** is a map $T : \mathbf{R} \to \mathbf{R}$ for which there exists a constant $c \lt 1$ such that for all $x, y \in \mathbf{R}$,

$$\vert T(x) - T(y) \vert \leq c \thinspace \vert x - y \vert .$$

The images of two points are closer together than the points themselves, by at least the factor $c$: "So they have to come closer" (Lecture 5, ≈1:15:25); "under the map, the images are squeezed more together" (Lecture 6, ≈12:58). The notes: "(Points are squeezed together under the map.)" (Lecture 5 notes p. 6; Lecture 6 notes p. 1).

What Colding stresses is that $c$ is *strictly* less than $1$: "the important point is that c has to be strictly less than 1. That's a crucial point" (Lecture 5, ≈1:14:35); "the key point is that this constant has to be strictly less than 1" (Lecture 6, ≈12:11). On the board he also says, in both lectures, that $c$ is positive (Lecture 5, ≈1:14:35; Lecture 6, ≈12:11); the notes state only $c \lt 1$.

**The same $c$ for all $x$ and $y$** (Lecture 6, ≈13:52, ≈37:31). A student asked whether $c$ is the same for all $x$ and $y$. "It is the same c", Colding said; "You can weaken that a little bit", but "Just think about it, that it's a requirement that it's the same c for all" (≈13:52). Later: "you could have some kind of local statement where, it was true for x and y in some small range. And that would be enough to guarantee you a fixed point. But in general, it's the same" (≈37:31). The local version is not stated or proved.

## At most one fixed point

**Lemma** (Lecture 6 notes p. 2; Lecture 6, ≈14:41–18:02). A contracting map has at most one fixed point. If $x$ and $y$ are fixed points, then

$$\vert x - y \vert = \vert T(x) - T(y) \vert \leq c \thinspace \vert x - y \vert ,$$

and since $c \lt 1$ this is only possible if $\vert x - y \vert = 0$, so $x = y$ (≈16:30–17:16). □

## Iterating the map: the Problem Set 3 exercise

(Lecture 6, ≈18:49–27:41; Lecture 6 notes p. 2.) Start with any point and apply $T$ again and again. The notes: "On Pset 3 you will be asked to show that for a contracting map $T$ and any $a_1 \in \mathbf{R}$ the sequence $a_{n+1} = T(a_n)$ is a Cauchy sequence" (notes p. 2). On the board the sequence starts at $a_0 = x$, so $a_1 = T(x)$, $a_2 = T(T(x))$, and in general $a_{n+1} = T(a_n) = T^{n+1}(x)$ (≈19:34–20:27). The problem set is [on OCW](https://ocw.mit.edu/courses/18-100b-real-analysis-spring-2025/mit18_100b_s25_pset03.pdf).

Colding shows only "a special case that is a key starting point" (≈22:52): the distance between consecutive terms shrinks by the factor $c$ at each step,

$$\vert a_{n+1} - a_n \vert = \vert T(a_n) - T(a_{n-1}) \vert \leq c \thinspace \vert a_n - a_{n-1} \vert \leq c^2 \thinspace \vert a_{n-1} - a_{n-2} \vert \leq \cdots$$

(≈23:39–26:55), so that it "is bounded by something like c to the n times a1 minus a0, something like that", which "will become incredibly small when n is large" (≈26:55). That alone does not make the sequence Cauchy, "because I need to prove that for all n and m sufficiently large" (≈22:52), "And I leave the rest for the homework" (≈27:41).

## The theorem and its proof

**Contracting mapping theorem** (Lecture 5 notes p. 6; Lecture 6 notes p. 1; Lecture 5, ≈1:15:25–1:17:53; Lecture 6, ≈28:27). If $T : \mathbf{R} \to \mathbf{R}$ is a contracting map, then $T$ has a fixed point, and by the lemma it has only one.

"It's crucial that this c is less than 1. That's what makes everything go. If it was equal to 1, you wouldn't get anything" (Lecture 5, ≈1:17:08). Lecture 5 states the theorem; Lecture 6 proves it.

**Proof** (Lecture 6, ≈29:23–35:56; Lecture 6 notes p. 2). Start with any point and form the sequence $a_n$ above. By the Problem Set 3 exercise it is a Cauchy sequence, and by the [Cauchy convergence theorem](cauchy-sequences.md) it converges to some $a$ (≈30:12–31:05). Then:

- $T(a_n) = a_{n+1}$, "just 1 further out of the sequence" (≈32:41), so $T(a_n) \to a$.
- $\vert T(a_n) - T(a) \vert \leq c \thinspace \vert a_n - a \vert$, and the right side goes to $0$, so $T(a_n) \to T(a)$ (≈34:18–35:07). The notes prove this as a general statement: if $x_n \to x$, then $T(x_n) \to T(x)$ (notes p. 2).
- "There can only be one limit" (≈35:56), so $T(a) = a$. □

Two facts are used here without proof in the lectures so far: that a sequence has only one limit, and that a sequence squeezed below one that tends to $0$ also tends to $0$. "So from the Cauchy convergence theorem, then you get the contracting mapping theorem" (≈35:56).

**Finding the fixed point.** The proof is also a method: "for many things, it's almost impossible to find the actual fixed point", but you can start anywhere "And then you just apply the map enough times", or start from "something pretty close to the fixed point. And then you iterate from there" (Lecture 6, ≈36:43).

## Application: Newton's method

(Lecture 6, ≈37:31–49:32; Lecture 6 notes pp. 2–3.) To find a zero of a function $f$, that is, a solution of $f(x) = 0$, assume $f' \neq 0$ and start from a good initial guess $x_1$, one where $f(x_1)$ is small (notes p. 2). Define

$$T(x) = x - \frac{f(x)}{f'(x)} .$$

A fixed point of $T$ is a zero of $f$: $T(x) = x$ gives $\frac{f(x)}{f'(x)} = 0$, so $f(x) = 0$ (notes p. 3; ≈48:44–49:32). The derivative of $T$ is

$$T'(x) = 1 - \frac{f'}{f'} + \frac{f \thinspace f''}{(f')^2} = f \frac{f''}{(f')^2}$$

(notes p. 2; ≈40:38–41:26). On the board Colding explains, with the mean value theorem, that if the derivative of $T$ were bounded by some $c \lt 1$ then $\vert T(x) - T(y) \vert \leq c \thinspace \vert x - y \vert$, so $T$ would be contracting (≈42:17–43:55). Starting with a good guess is meant to make this derivative "really, really small" there (≈45:38–46:24); the notes say $T$ is a contracting map "as long as $x$ stay close to the initial guess and for the initial guess $f(x)$ is small compared with" $\frac{f''}{(f')^2}$ (notes p. 3). Colding says he is "not going to make that too precise" (≈44:49), and that the iterates have to stay good guesses: "the Newton method doesn't tell you anything about that. But it require that to be applied" (≈47:12). The iteration $x_{n+1} = T(x_n)$ then converges to a fixed point of $T$ (notes p. 3).

This uses derivatives, the quotient rule and the mean value theorem before the course has defined or proved them (on the OCW list they come in Lectures 15 and 16), and it needs the local version of the theorem, since $T$ is considered only near the initial guess. The full discussion is on the [Lecture 6 page](06-cauchy-convergence-theorem.md).

## Why it matters: differential equations

Colding introduces the theorem as the first instance of something more general (Lecture 5, ≈1:12:08–1:13:39). Many of the course's concepts "work much more general", and to use them on differential equations they have to be abstracted "to where sequences are not any more real numbers, but they are of some other space" (≈1:12:53). Showing that a differential equation has a solution "often goes over using what's called the contracting mapping theorem", which has "all kinds of forms", depending only on "what space you're looking at" (≈1:12:53–1:13:39). In such a space the fixed point can be a solution to a differential equation; this is "a standard application to get solutions to differential equations" (≈1:17:53). In Lecture 6: "The contracting mapping theorem is actually extremely powerful", for ordinary differential equations, later in the course, "But it can also be used to solve PDEs, which is more complicated, Partial Differential Equations, and in all kinds of other areas of math" (Lecture 6, ≈31:53). The Lecture 6 notes defer the application to ODEs, "as this needs a version of the contracting mapping theorem where $T$ is defined on a more general space than the real numbers" (Lecture 6 notes p. 2). In the notes of both lectures, fixed points are introduced under the heading "Application: Existence of fixed points for a maps", directly after the Cauchy theorem (Lecture 5 notes p. 6; Lecture 6 notes p. 1).

## Not yet in this knowledge base

On the OCW lecture list, Lecture 22 is "Differentiating and Integrating Power Series; Ordinary Differential Equations (ODEs)" and Lecture 23 is "Existence and Uniqueness for ODEs: Picard–Lindelöf Theorem", where the application to differential equations belongs. Neither is covered here yet. The Problem Set 3 exercise that the iterates form a Cauchy sequence is only outlined in Lecture 6.

## Lectures

- [Lecture 5 — Monotone Convergence Theorem](05-monotone-convergence-theorem.md): the definitions and the statement of the theorem.
- [Lecture 6 — Cauchy Convergence Theorem](06-cauchy-convergence-theorem.md): uniqueness, the iteration, the proof from the Cauchy convergence theorem, and Newton's method.
- [Cauchy sequences](cauchy-sequences.md): the theorem the proof rests on.
