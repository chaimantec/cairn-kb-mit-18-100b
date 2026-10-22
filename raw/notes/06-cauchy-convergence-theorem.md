---
title: Lecture 6 — Cauchy Convergence Theorem (lecture notes)
lecture: 6
pages: 5
source_pdf: https://ocw.mit.edu/courses/18-100b-real-analysis-spring-2025/mit18_100b_s25_lec06.pdf
resource_page: https://ocw.mit.edu/courses/18-100b-real-analysis-spring-2025/resources/mit18_100b_s25_lec06_pdf/
numbering: PDF page N = printed page N (page 1 prints its number at the bottom, pages 2–4 in the running head; page 5 is the MIT OpenCourseWare back page, not lecture content). The notes have no equation numbers and no numbered lists.
figures: There are no figures. The small vector objects on pages 2 and 3 are fraction bars, not drawings; pages 1 and 4 have none; page 5's belong to the OCW back page.
---

# Lecture 6 — Cauchy Convergence Theorem: lecture notes

Full text of the course's written notes for Lecture 6 (MIT 18.100B/18.1002 Real Analysis, Spring 2025, Tobias Holck Colding), transcribed from the PDF. Cite as "notes p. N". The notes set the number sets in bold type, not blackboard bold, so they are written $\mathbf{R}$ here. The notes print no equation numbers. Page 5 is the OpenCourseWare citation page and is summarized, not transcribed as lecture content.

[wiki page for this lecture](../../wiki/06-cauchy-convergence-theorem.md) · [transcript](../transcripts/06-cauchy-convergence-theorem.md)

## Contents

| Section | Page(s) |
| --- | --- |
| Last time (recap list); Cauchy sequence: definition | 1 |
| Cauchy convergence theorem (statement); fixed point of a map $T : \mathbf{R} \to \mathbf{R}$ | 1 |
| Contracting map: definition; contracting mapping theorem (statement) | 1 |
| Uniqueness of the fixed point | 2 |
| Existence of the fixed point via the sequence $a_{n+1} = T(a_n)$ (uses Pset 3 and the Cauchy theorem) | 2 |
| Applications: ODEs (deferred) and Newton's method | 2–3 |
| Bolzano-Weierstrass theorem (statement); proof of the Cauchy theorem (Cauchy implies convergent) | 3 |
| Continuity at a point, continuous function; theorem on $f(x_n) \to f(x_0)$ with proof | 4 |
| Extreme value theorem with proof | 4 |
| References | 4 |
| OpenCourseWare back page | 5 |

## Printed slips

These are in the PDF as printed; the body below keeps them as printed.

- Page 1: "(Tail of the sequence bunch together.)" should be "bunches" (or "Tails of the sequence").
- Page 1: "Existence of fixed points for a maps" should be "a map" (or "for maps").
- Page 2: "For a contracting map the fix point is unique." should be "fixed point".
- Page 2: "Suppose that $x$ and $y$ are two fixed point" should be "points".
- Page 2: "We need therefore show" is missing "to" ("We therefore need to show").
- Page 2: "Finding a zeroth of a function" should be "a zero".
- Page 3: "So as long as $x$ stay close to the initial guess" should be "stays".
- Page 3: "Bolzano -Weirstrass theorem" (bold label), "Once we have the Bolzano-Weirstrass theorem", "From the Bolzano-Weirstrass theorem it follows" and "Another application of the Bolzano-Weirstrass theorem": "Weirstrass" should be "Weierstrass" (four places on page 3).
- Page 3: "there exist an $N_2$" should be "exists".
- Page 3: "This show that $a_n \to a$ as claimed." should be "shows".
- Page 4: "This show that $f(x_n) \to f(x_0)$ as claimed." should be "shows".
- Page 4: "Let $f$ be a continues function" should be "continuous".
- Page 4: "there exist $x \in [a, b]$ such that" should be "exists".
- Page 4: "The proof that the infimum is the same with obvious modification" is missing words ("The proof that the infimum is achieved is the same, with obvious modifications").
- Page 4: "by the Bolzano - Weirstrass theorem": "Weirstrass" should be "Weierstrass".

Not a slip, but worth knowing: the notes leave some steps unstated. They are reproduced as printed.

- Page 1: the Cauchy convergence theorem is stated as an if and only if; page 3 proves only that a Cauchy sequence is convergent. The converse (a convergent sequence is Cauchy) is not proved in the notes.
- Page 1: the contracting map definition says only that $c \lt 1$ and does not say that $c$ is non-negative.
- Page 2: the proof that the sequence $a_{n+1} = T(a_n)$ is Cauchy is deferred to Pset 3 ("On Pset 3 you will be asked to show"). The contracting mapping theorem is thus proved on page 2 only modulo that exercise, the Cauchy theorem and the Bolzano-Weierstrass theorem.
- Page 2: the notes say "Cauchy theorem" for what page 1 calls the Cauchy convergence theorem.
- Page 2: the application to ODEs is not carried out; the notes say it needs a version of the theorem on a more general space than the real numbers.
- Page 2: for Newton's method the derivative of $T$ is printed as $T'(x) = 1 - \frac{f'}{f'} + \frac{f \thinspace f''}{(f')^2} = f \frac{f''}{(f')^2}$, with $f$, $f'$, $f''$ written without the argument $x$; the notes then say, on page 3, that $T$ is a contracting map "as long as $x$ stay close to the initial guess and for the initial guess $f(x)$ is small compared with $\frac{f''}{(f')^2}$". The notes do not state a precise condition, and do not say why a bound on $T'$ makes $T$ satisfy $\vert T(x) - T(y) \vert \leq c \vert x - y \vert$, nor that $T$ is defined only near the initial guess and not on all of $\mathbf{R}$ as in the definition.
- Page 3: the Bolzano-Weierstrass theorem is stated without proof.
- Page 3: in the proof of the Cauchy theorem, the bound $\vert a_n \vert \leq \max \lbrace \vert a_N \vert + 1, \vert a_1 \vert, \cdots, \vert a_{N-1} \vert \rbrace$ is stated after $\vert a_n \vert \leq 1 + \vert a_N \vert$ for $n \geq N$; the terms with $n \lt N$ are covered by the other entries of the maximum without comment. Also the final estimate is stated "if $n \geq N$ and $k \geq N$" and uses $\vert a_n - a_{n_k} \vert \lt \frac{\epsilon}{2}$ without saying that $n_k \geq N_1$.
- Page 4: the theorem that $f(x_n) \to f(x_0)$ is stated for $f : \mathbf{R} \to \mathbf{R}$ continuous, and is then applied to a function on $[a, b]$ in the extreme value theorem.
- Page 4: in the extreme value theorem proof, the existence of a sequence with $f(x_n) \to \sup f$, the finiteness of $\sup f$, and the claim "Note that $x \in [a, b]$" are stated without reasons.

---

## Page 1

SPRING 2025 - 18.100B/18.1002

TOBIAS HOLCK COLDING

**Lecture 6**

**Last time:**

Basic algebraic properties of limits.

Monotone convergence theorem.

Cauchy sequence.

**Cauchy sequence:** A sequence $a_n$ is said to be a Cauchy sequence if for all $\epsilon \gt 0$, there exists an $N$ such that if $m, n \geq N$, then

$$
\vert a_n - a_m \vert \lt \epsilon .
$$

(Tail of the sequence bunch together.)

**Theorem (Cauchy convergence theorem)**: A sequence is convergent if and only if it is a Cauchy sequence.

Application: Existence of fixed points for a maps.

If $T : \mathbf{R} \to \mathbf{R}$ is a map, then $x_0 \in \mathbf{R}$ is a fixed point if

$$
T(x_0) = x_0 .
$$

**Definition** A contracting map is a map $T : \mathbf{R} \to \mathbf{R}$ such that there exists $c \lt 1$ so for all $x, y \in \mathbf{R}$ we have that

$$
\vert T(x) - T(y) \vert \leq c \thinspace \vert x - y \vert .
$$

(Points are squeezed together under the map.)

**Contracting mapping theorem:** Any contracting map has a fixed point.

1

## Page 2

2 — TOBIAS HOLCK COLDING

For a contracting map the fix point is unique.

Suppose that $x$ and $y$ are two fixed point we want to show that $x = y$. We have

$$
\vert x - y \vert = \vert T(x) - T(y) \vert \leq c \thinspace \vert x - y \vert .
$$

Since $c \lt 1$ this implies that $\vert x - y \vert = 0$ and so $x = y$.

On Pset 3 you will be asked to show that for a contracting map $T$ and any $a_1 \in \mathbf{R}$ the sequence $a_{n+1} = T(a_n)$ is a Cauchy sequence. By the Cauchy theorem we then have that $a_n$ is convergent.

Let $a$ denote the limit. We claim that $T(a) = a$. Observe that $T(a_n) = a_{n+1} \to a$. If we can show that if $x_n \to x$, then $T(x_n) \to T(x)$, then

$$
T(a_n) \to T(a)
$$

but we already have that $T(a_n) = a_{n+1} \to a$ so we would have that $T(a) = a$ and thus $a$ is a fixed point.

We need therefore show that if $x_n \to x$, then $T(x_n) \to T(x)$. To do that observe that

$$
\vert T(x_n) - T(x) \vert \leq c \thinspace \vert x_n - x \vert .
$$

Since $x_n \to x$ we have that $\vert x_n - x \vert \to 0$ and so $\vert T(x_n) - T(x) \vert \to 0$. It follows that $T(x_n) \to T(x)$. Applying this to the sequence $a_n$ shows that $a$ is a fixed point for $T$.

Applications of contracting mapping theorem:

Existence of solutions to ODEs. We will return to this later as this needs a version of the contracting mapping theorem where $T$ is defined on a more general space than the real numbers.

Newton's method: Finding a zeroth of a function $f : \mathbf{R} \to \mathbf{R}$. (So find a solution $x$ to $f(x) = 0$.)

Suppose that $x_1$ is a "good" initial guess, so $f(x_1)$ is sufficiently small. Assume also that $f' \neq 0$. Define a map

$$
T(x) = x - \frac{f(x)}{f'(x)} .
$$

We have

$$
T'(x) = 1 - \frac{f'}{f'} + \frac{f \thinspace f''}{(f')^2} = f \frac{f''}{(f')^2} .
$$

## Page 3

SPRING 2025 - 18.100B/18.1002 — 3

So as long as $x$ stay close to the initial guess and for the initial guess $f(x)$ is small compared with $\frac{f''}{(f')^2}$, then $T$ is a contracting map. By the contracting mapping theorem the sequence $x_{n+1} = T(x_n)$ is a Cauchy sequence that converges to a fixed point of $T$.

For a fixed point for $T$ we have $T(x) = x$ so $x - \frac{f(x)}{f'(x)} = x$ and therefore $f(x) = 0$.

Back to Cauchy sequences.

**Bolzano -Weirstrass theorem**: Any bounded sequence has a convergent subsequence.

Once we have the Bolzano-Weirstrass theorem we can prove the Cauchy theorem.

*Proof.* (of the Cauchy theorem.) So suppose that $a_n$ is a Cauchy sequence. We will first show that $a_n$ is bounded. From the definition of a Cauchy sequence we have that there exists $N$ such that for $m, n \geq N$, then

$$
\vert a_n - a_m \vert \lt 1 .
$$

It follows, in particular, that for all $n \geq N$, we have that

$$
\vert a_n - a_N \vert \lt 1 ,
$$

and so

$$
\vert a_n \vert = \vert (a_n - a_N) + a_N \vert \leq 1 + \vert a_N \vert .
$$

Therefore,

$$
\vert a_n \vert \leq \max \lbrace \vert a_N \vert + 1, \vert a_1 \vert, \cdots, \vert a_{N-1} \vert \rbrace .
$$

So the sequence is bounded.

From the Bolzano-Weirstrass theorem it follows that $a_n$ has a convergent subsequence $a_{n_k}$ with limit $a$. We want to show that $a_n$ is convergent with limit $a$. Given $\epsilon \gt 0$, there exists an $N_1$ such that if $m, n \geq N_1$, then

$$
\vert a_n - a_m \vert \lt \frac{\epsilon}{2} .
$$

Moreover, there exist an $N_2$ such that if $k \geq N_2$, then $\vert a_{n_k} - a \vert \lt \frac{\epsilon}{2}$. Set $N = \max \lbrace N_1, N_2 \rbrace$. It follows that if $n \geq N$ and $k \geq N$, then

$$
\vert a_n - a \vert \leq \vert a_n - a_{n_k} \vert + \vert a_{n_k} - a \vert \lt \frac{\epsilon}{2} + \frac{\epsilon}{2} .
$$

This show that $a_n \to a$ as claimed. $\square$

Another application of the Bolzano-Weirstrass theorem is the Extreme value theorem.

## Page 4

4 — TOBIAS HOLCK COLDING

Before stating this we need another key notion:

A function $f : \mathbf{R} \to \mathbf{R}$ is said to be continuous at a point $x_0 \in \mathbf{R}$, if for all $\epsilon \gt 0$, there exists a $\delta \gt 0$ such that if

$$
\vert x - x_0 \vert \lt \delta \implies \vert f(x) - f(x_0) \vert \lt \epsilon .
$$

A function is said to be continuous if it is continuous at all points in the domain.

**Theorem**: If $f : \mathbf{R} \to \mathbf{R}$ is continuous and $x_n$ is a sequence with $x_n \to x_0$, then $f(x_n) \to f(x_0)$.

*Proof.* Given $\epsilon \gt 0$, since $f$ is continuous, there exists a $\delta \gt 0$, such that if $\vert x - x_0 \vert \lt \delta$, then $\vert f(x) - f(x_0) \vert \lt \epsilon$. Since $x_n \to x_0$, there exists $N$ such that if $n \geq N$, then $\vert x_n - x_0 \vert \lt \delta$ and therefore $\vert f(x_n) - f(x_0) \vert \lt \epsilon$. This show that $f(x_n) \to f(x_0)$ as claimed. $\square$

**Extreme value theorem**: Let $f$ be a continues function on an interval $[a, b]$. The extreme value theorem says that the sup and inf are achieved. That is, there exist $x \in [a, b]$ such that $f(x) = \sup f$. Likewise for $\inf f$.

*Proof.* We will show that the supremum is achieved. The proof that the infimum is the same with obvious modification. Let $x_n \in [a, b]$ be a sequence where $f(x_n) \to \sup f$. Since the sequence is contained in $[a, b]$ it is bounded and therefore by the Bolzano - Weirstrass theorem has a convergent subsequence $x_{n_k} \to x$. Note that $x \in [a, b]$. By the theorem above $f(x_{n_k}) \to f(x)$ and since we also have that $f(x_{n_k}) \to \sup f$ it follows that $\sup f = f(x)$. This proves that the supremum is achieved. $\square$

REFERENCES

[TBB] B.S. Thomson, J.B. Bruckner, and A.M. Bruckner, *Elementary Real Analysis, 2nd edition*
TBB can be downloaded at:
https://classicalrealanalysis.info/com/documents/TBB-AllChapters-Landscape.pdf
(screen-optimized)
https://classicalrealanalysis.info/com/documents/TBB-AllChapters-Portrait.pdf
(print-optimized)

MIT, Dept. of Math., 77 Massachusetts Avenue, Cambridge, MA 02139-4307.

## Page 5

MIT OpenCourseWare back page (not lecture content): "MIT OpenCourseWare https://ocw.mit.edu — 18.100B Real Analysis — Spring 2025 — For information about citing these materials or our Terms of Use, visit: https://ocw.mit.edu/terms."
