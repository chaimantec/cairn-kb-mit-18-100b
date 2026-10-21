---
title: Lecture 4 — Sequences; Convergence (lecture notes)
lecture: 4
pages: 7
source_pdf: https://ocw.mit.edu/courses/18-100b-real-analysis-spring-2025/mit18_100b_s25_lec04.pdf
resource_page: https://ocw.mit.edu/courses/18-100b-real-analysis-spring-2025/resources/mit18_100b_s25_lec04_pdf/
numbering: PDF page N = printed page N (page 1 prints its number at the bottom, pages 2–6 in the running head; page 7 is the MIT OpenCourseWare back page, not lecture content). The notes have no equation numbers; the four algebraic properties of limits are numbered (1)–(4) in the notes.
figures: There are no figures. The small vector objects on pages 2–6 are fraction bars and absolute-value or radical rules, not drawings.
---

# Lecture 4 — Sequences; Convergence: lecture notes

Full text of the course's written notes for Lecture 4 (MIT 18.100B/18.1002 Real Analysis, Spring 2025, Tobias Holck Colding), transcribed from the PDF. Cite as "notes p. N". The notes set the number sets in bold type, not blackboard bold, so they are written $\mathbf{N}$, $\mathbf{Q}$, $\mathbf{R}$ here; the ordered set is likewise the bold $\mathbf{S}$. The notes print no equation numbers. Page 7 is the OpenCourseWare citation page and is summarized, not transcribed as lecture content.

[wiki page for this lecture](../../wiki/04-sequences-convergence.md) · [transcript](../transcripts/04-sequences-convergence.md)

## Contents

| Section | Page(s) |
| --- | --- |
| Theorem: $\mathbf{R}$ is a complete ordered Field that contains $\mathbf{Q}$; upper bound, completeness, $\sup A$, lower bound, greatest lower bound | 1 |
| Sequences: $\sqrt{2}$ as a limit of decimals; a sequence as a function $f : \mathbf{N} \to \mathbf{R}$ | 1–2 |
| Examples 1–3 of sequences ($\sqrt{2}$, $(-1)^n$, $\frac{1}{n}$) | 2 |
| Limit: definition of convergence, convergent, divergent | 2 |
| Example: $0.999999999 \cdots = 1$ and the claim $\lim_{n \to \infty} a_n = 1$ with proof | 2–3 |
| Theorem: a convergent sequence is bounded | 3 |
| Basic algebraic properties of limits: statement of (1)–(4) | 3 |
| Proofs of (1) and (2); outlines for (3) and (4) | 4 |
| Subsequence: Examples 1 and 2, formal definition | 5 |
| Theorem: $a_n$ converges to $a$ if and only if all subsequences converge to $a$; proof | 5–6 |
| References | 6 |
| OpenCourseWare back page | 7 |

## Printed slips

These are in the PDF as printed; the body below keeps them as printed.

- Page 1: "We denote by $\sup A$ the greatest lower bound of $A$" should be "the smallest upper bound of $A$", as the Lecture 3 notes (p. 1) have it. The line above states completeness in terms of a least upper bound, and $\inf A$ is not named on this page.
- Page 1: "can be thought of a limit of a sequence" should be "thought of as a limit".
- Page 2: "The $a_n$'s alternates between $-1$ and 1" should be "alternate".
- Page 2: "the sequence is convergenet" should be "convergent".
- Page 2: "A sequence that is not covergent" should be "convergent".
- Page 3: "Suppose that $a_n$ and $b_n$ are convergenet sequences" should be "convergent".
- Page 3: item (1) says that $c_n = C \thinspace a_n$ "is convergenet", which should be "convergent".
- Page 4: the proof of the first property begins "If $c = 0$" with a lower-case $c$; the statement and the rest of the proof use the capital constant $C$ ("for $C \neq 0$").
- Page 4: "This show the first property" should be "shows".
- Page 4: "We now set $N = \max\lbrace Na, N_b \rbrace$" prints the first entry as "Na" in ordinary type; the page image shows no subscript there (the two lines above use $N_a$).
- Page 4: "combine it with the theorem above that show that the set" should be "shows".
- Page 4: "There are the details to fill in" should be "There are details to fill in" (compare "there are details to fill in" a few lines later).
- Page 4: in the outline of the fourth property, the displayed identity $\frac{1}{b_n} - \frac{1}{b} = \frac{\vert b - b_n \vert}{\vert b \vert \thinspace \vert b_n \vert}$ has no absolute value on the left side as printed (the page image shows plain $\frac{1}{b_n} - \frac{1}{b}$), while the right side is an absolute value quotient.
- Page 5: "is NOT s subsequence" should be "a subsequence".
- Page 5: "Formel definition" should be "Formal definition".
- Page 5: "Sometimes a subsequence of the sequence $a_n$ also denoted by $a_{n_k}$" is missing "is" ("is also denoted by").
- Page 5: "First we need to show that is all subsequences of $a_n$ are convergent" should be "that if all subsequences".
- Page 5: "choose $N$ so large so that for" should be "so large that" (or "so large, so that").

Not a slip, but worth knowing: the notes leave some steps unstated or reuse a symbol. They are reproduced as printed.

- Page 4: "we will assume that $a_n = 1$" in the outline of the fourth property is printed without "for all $n$"; the page says "The general case indeed will follow from this together with the third property" and does not spell out how.
- Page 4: the outlines of the third and fourth properties end with "there are details to fill in"; the page does not supply them. The third-property outline refers to "the theorem above" (the boundedness theorem on page 3).
- Page 3: in the proof of the claim, the step from $\vert a_n - 1 \vert = 10^{-n}$ to $10^{-n} \lt \frac{1}{n}$ is stated without a reason; the page also gives no proof of the formula $\vert a_n - 1 \vert = 10^{-n}$ beyond stating it.
- Page 3: in the boundedness proof, the page does not say why $\lbrace a_1, \cdots, a_{N-1} \rbrace$ is bounded.
- Page 2: Example 2 says the sequence has NO limit and Example 3 says $\frac{1}{n}$ has zero as its limit, both without proof; the definition of the limit follows them.
- Page 5: in Example 1 the symbol $c_n$ is used twice, first for the constant sequence $c_n = -1$ and then for $c_n = (-1)^{n+1}$.
- Page 5: Example 1 on page 5 (subsequences) is a different example from Example 1 on page 2 (sequences); both are numbered "Example 1" in the notes.
- Page 5: the formal definition says a subsequence is $f \circ g$ with $g : \mathbf{N} \to \mathbf{N}$ strictly increasing; the proof on page 6 uses $n_k \geq k$ without justifying it, and the page does not say that $n_k$ stands for $g(k)$ (it says only that a subsequence is "sometimes" denoted $a_{n_k}$).

---

## Page 1

SPRING 2025 - 18.100B/18.1002

TOBIAS HOLCK COLDING

**Lecture 4**

**Theorem**: $\mathbf{R}$ is a complete ordered Field that contains $\mathbf{Q}$.

$\mathbf{S}$ is an ordered set. A non-empty subset $A$ of $\mathbf{S}$ is said to have an upper bound if there exists an $M \in \mathbf{S}$ such that for all $a \in A$ we have that $a \leq M$.

Completeness is the property that every bounded non-empty subset has a least upper bound.

We denote by $\sup A$ the greatest lower bound of $A$.

Lower bound: A non-empty subset $A$ is said to have a lower bound if there exists $m \in \mathbf{S}$ such that for all $a \in A$ we have that $m \leq a$.

The greatest lower bound is a lower bound that is greater or equal to all other lower bounds.

Sequences:

$\sqrt{2}$ can be thought of a limit of a sequence of decimal numbers as follows.

$$
1 \lt 1.4 \lt 1.41 \lt 1.414 \cdots .
$$

A sequence of real numbers is a function $f : \mathbf{N} \to \mathbf{R}$.

1

## Page 2

2 — TOBIAS HOLCK COLDING

We usually use the notation $a_n = f(n)$.

**Example 1:** $\sqrt{2}$ is the limit of $a_1 = 1$, $a_2 = 1.4$, $a_3 = 1.41$, $a_4 = 1.414$ etc.

**Example 2:** $a_n = (-1)^n$. This sequence has NO limit. The $a_n$'s alternates between $-1$ and 1.

**Example 3:** The sequence $a_n = \frac{1}{n}$ has zero as its limit.

Limit: Let $a_n$ be a sequence and $a$ a real number. We say that $a_n$ converges to $a$ if for all $\epsilon \gt 0$, there exists an $N \in \mathbf{N}$ such that if $n \geq N$, then

$$
\vert a_n - a \vert \lt \epsilon .
$$

If this is the case, then we also say that $a$ is the limit of the sequence and we say that the sequence is convergenet.

A sequence that is not covergent is said to be divergent.

**Example**:

$$
0.999999999 \cdots = 1 .
$$

What does the left hand side mean?

Define a sequence $a_n$ as follows: Set

$$
a_1 = 0.9 ,
$$

$$
a_2 = 0.99 ,
$$

$$
a_3 = 0.999 ,
$$

$$
a_4 = 0.9999 ,
$$

etc.

The left hand side above is then defined as the limit of the sequence $a_n$.

## Page 3

SPRING 2025 - 18.100B/18.1002 — 3

**Claim**:

$$
\lim_{n \to \infty} a_n = 1 .
$$

*Proof.* We need to show that for all $\epsilon \gt 0$, there exists an $N \in \mathbf{N}$ such that for $n \geq N$ we have that

$$
\vert a_n - 1 \vert \lt \epsilon .
$$

By the Archimedean property we can choose $N$ such that $\frac{1}{N} \lt \epsilon$. We also have that

$$
\vert a_n - 1 \vert = 10^{-n} .
$$

Therefore, for $n \geq N$ we have that

$$
\vert a_n - 1 \vert = 10^{-n} \lt \frac{1}{n} \leq \frac{1}{N} \lt \epsilon .
$$

This proves the claim. □

**Theorem** If $a_n$ is a convergent sequence, then the set $\lbrace a_n \rbrace$ is a bounded subset of $\mathbf{R}$.

*Proof.* Since $a_n$ is convergent to $a$ we can find $N$ such that for $n \geq N$ we have that

$$
\vert a - a_n \vert \lt 1 .
$$

Note also that the set $\lbrace a_1, \cdots, a_{N-1} \rbrace$ is bounded so there exists $C \in \mathbf{R}$ such that for $n = 1, \cdots, N-1$ we have that

$$
\vert a_n \vert \leq C .
$$

To see that the larger set $\lbrace a_n \rbrace$ is bounded we will use that for $n \geq N$

$$
\vert a_n \vert \leq \vert a \vert + \vert a_n - a \vert \leq \vert a \vert + 1 .
$$

From this we have that for all $n$

$$
\vert a_n \vert \leq \max\lbrace C, \vert a \vert + 1 \rbrace .
$$

□

Basic algebraic properties of limits:

**Theorem** Suppose that $a_n$ and $b_n$ are convergenet sequences with $\lim a_n = a$, $\lim b_n = b$ and $C \in \mathbf{R}$, then

(1) $c_n = C \thinspace a_n$ is convergenet and $\lim_{n \to \infty} c_n = C \thinspace a$.

(2) $c_n = a_n + b_n$ is convergent and $\lim_{n \to \infty} c_n = a + b$.

(3) $c_n = a_n \thinspace b_n$ is convergent with $\lim_{n \to \infty} c_n = a \thinspace b$.

(4) If $b_n \neq 0$, $b \neq 0$ and $c_n = \frac{a_n}{b_n}$, then $c_n$ is convergent and $\lim_{n \to \infty} c_n = \frac{a}{b}$.

## Page 4

4 — TOBIAS HOLCK COLDING

*Proof.* (of the first property.) If $c = 0$, then the claim is obviously true so we need only show the claim for $C \neq 0$. Given $\epsilon \gt 0$, there exists an $N$ such that if $n \geq N$, then

$$
\vert a - a_n \vert \lt \frac{\epsilon}{\vert C \vert} .
$$

Multiplying both sides by $\vert C \vert$ gives that

$$
\vert C \thinspace a - C \thinspace a_n \vert \lt \epsilon .
$$

for $n \geq N$. This show the first property.

(Of the second of these properties.) Observe that

$$
\vert c_n - (a + b) \vert = \vert a_n + b_n - (a + b) \vert = \vert (a_n - a) + (b_n - b) \vert \leq \vert a_n - a \vert + \vert b_n - b \vert .
$$

Since $a_n \to a$, given $\epsilon \gt 0$ we can find a $N_a$ such that if $n \geq N_a$, then

$$
\vert a_n - a \vert \lt \frac{\epsilon}{2} .
$$

Likewise since $b_n \to b$ we can find $N_b$ such that if $n \geq N_b$, then

$$
\vert b_n - b \vert \lt \frac{\epsilon}{2} .
$$

We now set $N = \max\lbrace Na, N_b \rbrace$ and observe that if $n \geq N$, then

$$
\vert c_n - (a + b) \vert \leq \vert a_n - a \vert + \vert b_n - b \vert \lt \frac{\epsilon}{2} + \frac{\epsilon}{2} = \epsilon .
$$

This proves the second property.

(Outline of how to show the third property.) To prove the third property we will use that

$$
\vert a \thinspace b - a_n \thinspace b_n \vert \leq \vert a \thinspace b - a_n \thinspace b \vert + \vert a_n \thinspace b - a_n \thinspace b_n \vert = \vert b \vert \thinspace \vert a - a_n \vert + \vert a_n \vert \thinspace \vert b - b_n \vert .
$$

We then combine it with the theorem above that show that the set

$$
\lbrace \vert a_n \vert \vert n \in \mathbf{N} \rbrace
$$

is bounded. This is the main idea of the proof of the third property. There are the details to fill in to make it a proof.

(Outline of how to show the fourth property.) To prove the fourth property we will assume that $a_n = 1$. The general case indeed will follow from this together with the third property. We will use that

$$
\frac{1}{b_n} - \frac{1}{b} = \frac{\vert b - b_n \vert}{\vert b \vert \thinspace \vert b_n \vert} ,
$$

together with that

$$
\vert b_n \vert \leq \vert b \vert + \vert b_n - b \vert .
$$

and therefore

$$
\vert b_n \vert \geq \vert b \vert - \vert b_n - b \vert .
$$

We then want to use this to bound the denominator (when $n$ is sufficiently large) from below in

$$
\frac{\vert b - b_n \vert}{\vert b \vert \thinspace \vert b_n \vert} .
$$

Like for the third property there are details to fill in but these are the main ideas. □

## Page 5

SPRING 2025 - 18.100B/18.1002 — 5

Subsequence:

**Example 1**: Suppose that $a_n = (-1)^n$.
This is a sequence of 1's and $-1$'s that is alternating between $-1$ and 1.
The sequence $b_n = 1$ for all $n$ is a subsequence.
Another subsequence is where $c_n = -1$.
Also the sequence $c_n = (-1)^{n+1}$ is a subsequence of $a_n$.
Another example of a subsequence is

$$
1, 1, -1, -1, 1, 1, -1, -1, \cdots .
$$

**Example 2**: Suppose $a_n = n$. So $a_n$ is:

$$
1, 2, 3, 4, 5, 6, \cdots .
$$

The sequence of increasing odd numbers

$$
1, 3, 5, 7, 9, \cdots .
$$

is a subsequence.
The sequence of increasing even numbers

$$
2, 4, 6, 8, 10, \cdots .
$$

is another subsequence.
The sequence

$$
1, 1, 2, 2, 3, 3, 4, 4, 5, 5 \cdots ,
$$

is NOT s subsequence.

**Formel definition:** Recall that a sequence $a_n$ is a function $f : \mathbf{N} \to \mathbf{R}$ where we set $a_n = f(n)$. A subsequence $b_n$ of $a_n$ is a composition of functions $f \circ g$ where $g : \mathbf{N} \to \mathbf{N}$ is a strictly increasing function. So $b_n = f(g(n))$. Sometimes a subsequence of the sequence $a_n$ also denoted by $a_{n_k}$.

**Theorem**: A sequence $a_n$ is convergent with limit $a$ if and only if all subsequences of $a_n$ are also convergent with limit $a$.

*Proof.* We need to show two implications.

First we need to show that is all subsequences of $a_n$ are convergent with limit $a$, then the sequence $a_n$ is convergent with limit $a$. However, this is trivially so since $a_n$ itself is a (trivial) subsequence of $a_n$.

Next we need to show that any subsequence of a convergent sequence is convergent with the same limit. Suppose therefore that $\epsilon \gt 0$ is given and choose $N$ so large so that for

## Page 6

6 — TOBIAS HOLCK COLDING

$n \geq N$

$$
\vert a_n - a \vert \lt \epsilon .
$$

For $k \geq N$ we have that $n_k \geq k \geq N$ and therefore

$$
\vert a_{n_k} - a \vert \lt \epsilon .
$$

This proves the second implication. □

REFERENCES

[TBB] B.S. Thomson, J.B. Bruckner, and A.M. Bruckner, *Elementary Real Analysis, 2nd edition*
TBB can be downloaded at:
https://classicalrealanalysis.info/com/documents/TBB-AllChapters-Landscape.pdf
(screen-optimized)
https://classicalrealanalysis.info/com/documents/TBB-AllChapters-Portrait.pdf
(print-optimized)

MIT, Dept. of Math., 77 Massachusetts Avenue, Cambridge, MA 02139-4307.

## Page 7

MIT OpenCourseWare back page (not lecture content): "MIT OpenCourseWare https://ocw.mit.edu — 18.100B Real Analysis — Spring 2025 — For information about citing these materials or our Terms of Use, visit: https://ocw.mit.edu/terms."
