---
title: Lecture 3 — How to Write a Proof; Archimedean Property (lecture notes)
lecture: 3
pages: 6
source_pdf: https://ocw.mit.edu/courses/18-100b-real-analysis-spring-2025/mit18_100b_s25_lec03.pdf
resource_page: https://ocw.mit.edu/courses/18-100b-real-analysis-spring-2025/resources/mit18_100b_s25_lec03_pdf/
numbering: PDF page N = printed page N (page 1 prints its number at the bottom, pages 2–5 in the running head; page 6 is the MIT OpenCourseWare back page, not lecture content). The notes have no equation numbers.
figures: There are no figures. The small vector objects on pages 2–5 are fraction bars, not drawings.
---

# Lecture 3 — How to Write a Proof; Archimedean Property: lecture notes

Full text of the course's written notes for Lecture 3 (MIT 18.100B/18.1002 Real Analysis, Spring 2025, Tobias Holck Colding), transcribed from the PDF. Cite as "notes p. N". The notes set the number sets in bold type, not blackboard bold, so they are written $\mathbf{N}$, $\mathbf{Q}$, $\mathbf{R}$ here; the ordered set is likewise the bold $\mathbf{S}$. The notes print no equation numbers. Page 6 is the OpenCourseWare citation page and is summarized, not transcribed as lecture content.

[wiki page for this lecture](../../wiki/03-how-to-write-a-proof-archimedean-property.md) · [transcript](../transcripts/03-how-to-write-a-proof-archimedean-property.md)

## Contents

| Section | Page(s) |
| --- | --- |
| Theorem: $\mathbf{R}$ is a complete ordered Field that contains $\mathbf{Q}$; upper bound, completeness, $\sup A$, lower bound, $\inf A$ | 1 |
| How to write a mathematical proof: theorem that there exists $\alpha \gt 0$ with $\alpha^2 = 2$; the set $A$ and $\alpha = \sup A$ | 2 |
| Part 1: $\alpha^2 \leq 2$ (with $h = \frac{\alpha^2 - 2}{4 \alpha}$, $\alpha_0 = \alpha - h$) | 2–3 |
| Part 2: $\alpha^2 \geq 2$ (with $h = \frac{2 - \alpha^2}{4 \alpha}$, $\alpha_1 = \alpha + h$) | 3 |
| Archimedean property: theorem that the natural numbers are not bounded from above | 4 |
| Corollary: for any $\epsilon \gt 0$ there is $n \in \mathbf{N}$ with $\frac{1}{n} \lt \epsilon$ | 4 |
| Sequences: definition, Examples 1–3, limit of a sequence | 5 |
| References | 5 |
| OpenCourseWare back page | 6 |

## Printed slips

These are in the PDF as printed; the body below keeps them as printed.

- Page 1: "From now on we will concentrate of the case of $\mathbf{R}$" should be "concentrate on".
- Page 2: "we will show that that if this was the case" repeats "that" ("show that if this was the case").
- Page 2: "we will see that this lead to a contradiction" should be "this leads to". The same sentence recurs on page 3 in Part 2 ("we will see that this lead to a contradiction").
- Page 2: "Note that since we are assuming that $\alpha \gt 2$, then we have that $h \gt 0$" is missing the exponent: the page image shows $\alpha \gt 2$ (no square), but the assumption in Part 1 is $\alpha^2 \gt 2$ (that is what makes $h = \frac{\alpha^2 - 2}{4 \alpha} \gt 0$). Not an OCR effect: the text layer has a plain "α > 2" there too.
- Page 3: "This is the desired contradiction and show that $\alpha^2 \leq 2$" should be "shows".
- Page 4: "The set of natural number is not bounded from above" should be "natural numbers".
- Page 4: in the proof the least upper bound is first named $M$ ("we can let $M$ be the least upper bound") and from the next line on it is called $\alpha$ (the display $n \leq \alpha$, and "contradicting that $\alpha$ was the least upper bound"). The variable is renamed mid-proof; $M$ should be $\alpha$.
- Page 4: in the corollary's proof, "Set $\alpha = \frac{1}{\epsilon}$, By the Archimedean property" has a capital "By" after a comma (should be a period or a lowercase "by").
- Page 5: "can be thought of a limit of a sequence", said of $\sqrt{2}$, should be "thought of as a limit".
- Page 5: "The $a_n$'s alternates between $-1$ and 1" should be "alternate".

Not a slip, but worth knowing: the notes leave some steps unstated and a heading has no text under it. They are reproduced as printed.

- Page 4: the heading "Archimedean property:" stands alone; no statement of the property is printed under it. The next heading "Formal proof:" is followed by the theorem that the set of natural numbers is not bounded from above, and the corollary on $\frac{1}{n} \lt \epsilon$ is proved "by the Archimedean property" without the property being stated in this form.
- Page 2: the page says "2 is an upper bound for $A$" without a reason.
- Page 2: "Since $1 \in A$ it follows that $0 \lt 1 \lt \alpha$" writes a strict inequality $1 \lt \alpha$; the rest of the proof uses $1 \leq \alpha$ ("since $1 \leq \alpha \leq 2$" on page 2, "from that $1 \leq \alpha$" on page 3).
- Page 2: "such that $\alpha_0^2 \gt 2$ so $\alpha_0$ is an upper bound" does not say why a positive number whose square is greater than $2$ is an upper bound for $A$.
- Page 2: the upper half of "since $1 \leq \alpha \leq 2$" is used without saying where the upper half comes from (the page earlier says only that $2$ is an upper bound for $A$ and $\alpha = \sup A$).
- Page 3: "In particular, $0 \lt \alpha_0$" is stated without the step from $h \leq \frac{1}{2}$ and $1 \leq \alpha$ to $\alpha_0 = \alpha - h \gt 0$. The chain after "Next" drops $h^2$ and uses $\alpha^2 \gt 2$ for the last inequality without saying so; Part 2 likewise uses $h \lt 1$ and $\alpha^2 \lt 2$ without comment.
- Page 3: Part 1 concludes with "the desired contradiction" without restating which statement it contradicts (that $\alpha_0$ is an upper bound smaller than $\alpha$ is set up on page 2, and the last display shows $\alpha_0^2 \gt 2$ but the page does not repeat that this contradicts $\alpha = \sup A$).
- Page 4: the corollary's "It follows that $\frac{1}{n} \lt \epsilon$" leaves the step from $n \gt \frac{1}{\epsilon}$ to the inequality to the reader.
- Page 5: "When does a limit exist?" is asked and not answered on the page; the definition of "converges" is given under "Limit:".

---

## Page 1

SPRING 2025 - 18.100B/18.1002

TOBIAS HOLCK COLDING

**Lecture 3**

**Theorem**: $\mathbf{R}$ is a complete ordered Field that contains $\mathbf{Q}$.

$\mathbf{S}$ is an ordered set. A non-empty subset $A$ of $\mathbf{S}$ is said to have an upper bound if there exists an $M \in \mathbf{S}$ such that for all $a \in A$ we have that $a \leq M$.

Completeness is the property that every bounded non-empty subset has a least upper bound.

We denote by $\sup A$ the smallest upper bound of $A$.

Lower bound: A non-empty subset $A$ is said to have a lower bound if there exists $m \in \mathbf{S}$ such that for all $a \in A$ we have that $m \leq a$.

The greatest lower bound is a lower bound that is greater or equal to all other lower bounds.

The greatest lower bound is denoted by $\inf A$.

From now on we will concentrate of the case of $\mathbf{R}$.

1

## Page 2

2 — TOBIAS HOLCK COLDING

How to write a mathematical proof?

This lecture we will look at how to write a mathematical proof.
We will explain this in two results that we talked about last time.

Let us return to the example of showing that $\sqrt{2} \in \mathbf{R}$.

We already showed this but we did not write it as a ”proper proof”. That is what we will do next.

**Theorem:** There exists $\alpha \gt 0$ such that $\alpha^2 = 2$.

*Proof.* Define a set $A$ by

$$
A = \lbrace x \in \mathbf{R} \vert x \gt 0 \text{ and } x^2 \leq 2 \rbrace .
$$

We will show that $A$ is a non-empty bounded subset and that $\alpha = \sup A$ has the property that $\alpha \gt 0$ and $\alpha^2 = 2$.

Observe first that $1 \in A$, so $A$ is non-empty. Moreover, 2 is an upper bound for $A$ so $A$ is bounded from above. Let $\alpha = \sup A$, we need to show that $\alpha \gt 0$ and that $\alpha^2 = 2$. Since $1 \in A$ it follows that $0 \lt 1 \lt \alpha$. To show that $\alpha^2 = 2$ we divide the proof into two parts.

**Part 1**: We will show that $\alpha^2 \leq 2$. Suppose not; we will see that this lead to a contradiction. Indeed, we will show that that if this was the case, then there exists an $0 \lt \alpha_0 \lt \alpha$ such that $\alpha_0^2 \gt 2$ so $\alpha_0$ is an upper bound that is smaller than $\alpha$. To show this we set

$$
h = \frac{\alpha^2 - 2}{4 \alpha}
$$

and set

$$
\alpha_0 = \alpha - h .
$$

Note that since we are assuming that $\alpha \gt 2$, then we have that $h \gt 0$ and therefore $\alpha_0 \lt \alpha$. Note also that since $1 \leq \alpha \leq 2$ we have that

$$
h \leq \frac{1}{2 \alpha} \leq \frac{1}{2} .
$$

## Page 3

SPRING 2025 - 18.100B/18.1002 — 3

In particular, $0 \lt \alpha_0$. Next

$$
\alpha_0^2 = \alpha^2 + h^2 - 2 h \alpha \gt \alpha^2 - \frac{\alpha^2 - 2}{2} = \frac{\alpha^2}{2} + 1 \geq 2 .
$$

This is the desired contradiction and show that $\alpha^2 \leq 2$.

**Part 2**: We will next show that $\alpha^2 \geq 2$. Suppose not; we will see that this lead to a contradiction. Indeed, we will show that if this was the case, then there exists an $\alpha_1 \gt \alpha$ such that $\alpha_1^2 \lt 2$ contradicting that $\alpha$ was an upper bound for $A$. So assume that $\alpha^2 \lt 2$. This time we will set

$$
h = \frac{2 - \alpha^2}{4 \alpha} .
$$

Note that $1 \gt h \gt 0$ (the first inequality follows from that $1 \leq \alpha$). Set $\alpha_1 = \alpha + h$. It follows that

$$
\alpha_1^2 = \alpha^2 + h^2 + 2 h \alpha \lt \alpha^2 + h + \frac{2 - \alpha^2}{2} \leq \alpha^2 + 2 \frac{2 - \alpha^2}{2} = 2 .
$$

Together parts 1 and 2 show that $\alpha^2 = 2$; completing the proof. □

## Page 4

4 — TOBIAS HOLCK COLDING

Archimedean property:

Formal proof:

**Theorem**: The set of natural number is not bounded from above.

*Proof.* If $\mathbf{N}$ is bounded from above, then we can let $M$ be the least upper bound. We now have that for all $n \in \mathbf{N}$

$$
n \leq \alpha
$$

We claim that also $\alpha - 1$ is an upper bound contradicting that $\alpha$ was the least upper bound. Namely, for a given $n$ since $\alpha$ is an upper bound for all natural numbers we have that

$$
n + 1 \leq \alpha
$$

but this implies that

$$
n \leq \alpha - 1
$$

showing that $\alpha - 1$ is an upper bound. That is the desired contradiction. □

**Corollary**: For any $\epsilon \gt 0$, there exists an $n \in \mathbf{N}$ such that $\frac{1}{n} \lt \epsilon$.

*Proof.* Set $\alpha = \frac{1}{\epsilon}$, By the Archimedean property we know that there exists an $n \in \mathbf{N}$ with $n \gt \alpha$. It follows that $\frac{1}{n} \lt \epsilon$. □

## Page 5

SPRING 2025 - 18.100B/18.1002 — 5

Sequences:

$\sqrt{2}$ can be thought of a limit of a sequence of decimal numbers as follows.

$$
1 \lt 1.4 \lt 1.41 \lt 1.414 \cdots .
$$

When does a limit exist?

A sequence of real numbers is a function $f : \mathbf{N} \to \mathbf{R}$.

We usually use the notation $a_n = f(n)$.

**Example 1:** $\sqrt{2}$ is the limit of $a_1 = 1$, $a_2 = 1.4$, $a_3 = 1.41$, $a_4 = 1.414$ etc.

**Example 2:** $a_n = (-1)^n$. This sequence has NO limit. The $a_n$'s alternates between $-1$ and 1.

**Example 3:** The sequence $a_n = \frac{1}{n}$ has zero as its limit.

Limit: Let $a_n$ be a sequence and $a$ a real number. We say that $a_n$ converges to $a$ if for all $\epsilon \gt 0$, there exists an $N \in \mathbf{N}$ such that if $n \geq N$, then

$$
\vert a_n - a \vert \lt \epsilon .
$$

REFERENCES

[TBB] B.S. Thomson, J.B. Bruckner, and A.M. Bruckner, *Elementary Real Analysis, 2nd edition*
TBB can be downloaded at:
https://classicalrealanalysis.info/com/documents/TBB-AllChapters-Landscape.pdf
(screen-optimized)
https://classicalrealanalysis.info/com/documents/TBB-AllChapters-Portrait.pdf
(print-optimized)

MIT, Dept. of Math., 77 Massachusetts Avenue, Cambridge, MA 02139-4307.

## Page 6

MIT OpenCourseWare back page (not lecture content): "MIT OpenCourseWare https://ocw.mit.edu — 18.100B Real Analysis — Spring 2025 — For information about citing these materials or our Terms of Use, visit: https://ocw.mit.edu/terms."
