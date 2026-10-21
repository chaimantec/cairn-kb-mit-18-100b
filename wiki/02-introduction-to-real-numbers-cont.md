# Lecture 2 — Introduction to Real Numbers (cont.)

**18.100B Real Analysis, Spring 2025 · Tobias Holck Colding · [video](https://www.youtube.com/watch?v=6i6sV8WIzLc) (76 min)**

Sources for this page: the [edited transcript](../raw/transcripts/02-introduction-to-real-numbers-cont.md) (timestamps below are written ≈M:SS and point into it), the course's typed [lecture notes](../raw/notes/02-introduction-to-real-numbers-cont.md) for this lecture (cited "notes p. N"; [PDF on OCW](https://ocw.mit.edu/courses/18-100b-real-analysis-spring-2025/mit18_100b_s25_lec02.pdf)), and the OCW readings list, which assigns Sections 1.5–1.6 of Thomson, Bruckner and Bruckner, *Elementary Real Analysis* (TBB) to this lecture. Colding teaches from the blackboard; there are no slides.

## What this lecture establishes

Lecture 1 ended with the sentence that $\mathbf{R}$ is a complete ordered field that contains $\mathbf{Q}$, and explained every part of it except *complete*. This lecture supplies that word. It first shows that $\mathbf{R}$ and $\mathbf{Q}$ really are different: **no rational number squares to $2$** (notes p. 1). It then defines **upper bounds**, **least upper bounds** and **completeness**, the property that every subset with an upper bound has a least upper bound (notes p. 2). It takes for granted, without proof, that a complete ordered field containing $\mathbf{Q}$ exists, and calls it $\mathbf{R}$. With that in hand it proves that **$\sqrt{2} \in \mathbf{R}$**, by showing that the least upper bound $x$ of a suitable set satisfies $x^2 = 2$. Two consequences follow at once: **$\mathbf{Q}$ is not complete**, and the **Archimedean property**, that every real number is exceeded by some natural number. A corollary of the Archimedean property closes the lecture: **between any two real numbers there is a rational number** (notes pp. 3–4).

Notation: as in Lecture 1, the notes set the number systems in bold, $\mathbf{N}$, $\mathbf{Z}$, $\mathbf{Q}$, $\mathbf{R}$, and an ordered set as $\mathbf{S}$; this page follows them. In this course $\mathbf{N} = \lbrace 1, 2, 3, \cdots \rbrace$ starts at $1$.

## Recap of Lecture 1 (≈0:00–8:15)

Colding opens by restating the motivating example, the [intermediate value theorem](intermediate-value-theorem.md): a continuous $f$ on an interval $[a, b]$ with $f(a)$ negative and $f(b)$ positive has a $c$ between $a$ and $b$ with $f(c) = 0$. The question it raised was which property of $\mathbf{R}$ is needed to make that rigorous, and the answer was that $\mathbf{R}$ is a complete ordered field (≈0:00–2:27).

He then recalls the pieces already defined (≈2:27–7:22). A **field** is a set with two operations, each with five properties, plus an eleventh, the distributive law, that ties them together. An **ordered set** has an ordering with two properties: any two elements $x$ and $y$ can be compared (either $x = y$, $x \lt y$ or $y \lt x$), and the ordering is **transitive**, so $x \lt y$ and $y \lt z$ give $x \lt z$ (≈4:57–5:42). Lecture 1 left transitivity to the notes; here it is said aloud. An **ordered field** is a field that is also an ordered set, in which adding the same element to both sides preserves the order and a product of positive elements is positive. What remains is the word *complete* (≈7:22). Details are on the [Lecture 1 page](01-introduction-to-real-numbers.md) and in [fields and ordered fields](fields-and-ordered-fields.md).

## $\sqrt{2}$ is not a rational number (≈8:15–16:47)

The question for the lecture is: what is the difference between $\mathbf{R}$ and $\mathbf{Q}$? Recall that $\mathbf{Q}$ consists of the quotients $\frac{m}{n}$ with $m \in \mathbf{Z}$ and $n \in \mathbf{N}$. One difference is that $\sqrt{2}$ is a real number but not a rational one (≈8:15; notes p. 1). The notes define $\sqrt{2}$ as **a number $x$ such that $x \gt 0$ and $x^2 = 2$** (notes p. 1; ≈9:13).

**Theorem** (notes p. 1). There is no rational number $x$ with $x^2 = 2$.

**Proof, by contradiction** (≈10:53–15:44). Suppose $x = \frac{m}{n}$, with $m \in \mathbf{Z}$ and $n \in \mathbf{N}$, satisfies $x^2 = 2$. Then $\frac{m^2}{n^2} = 2$, and multiplying out, $m^2 = 2 n^2$ (≈11:49–12:36). A rational number has many representations, because numerator and denominator can be multiplied by the same natural number, so we may assume that $m$ and $n$ have no common factor (other than one): otherwise, reduce until they do not (≈12:36–13:27). Now $m^2 = 2 n^2$ says $2$ is a factor of $m^2$, and so of $m$ itself (≈13:27–14:13). Write $m = 2 m_1$ with $m_1$ an integer. Then

$$m^2 = 4 m_1^2 = 2 n^2 , \quad\text{so}\quad 2 m_1^2 = n^2 ,$$

and so $2$ is a factor of $n$ as well (≈14:13–14:59). Now $2$ is a common factor of $m$ and $n$, contradicting the assumption that they have none. So no rational number squares to $2$ (≈14:59–15:44). □

Two details. The notes print the middle step as $2 m_1 = n$, with both squares missing; on the board Colding says "is equal to n" and immediately corrects himself to "n squared" (≈14:59; see the [notes' printed slips](../raw/notes/02-introduction-to-real-numbers-cont.md#printed-slips)). And neither the board nor the notes say why a factor of $2$ in $m^2$ must be a factor of $m$, or the corresponding step for $n$; both are stated and used.

## $\sqrt{2}$ as the limit of a sequence (≈15:44–19:16)

How, then, does $\sqrt{2}$ fit into the number system? As a decimal it begins $1.4142136$ and continues (≈16:47; notes p. 1). One way to think of it, Colding says, is as **the limit of a sequence of numbers**: $1$, $1.4$, $1.41$, $1.414$, $1.4142$, $1.41421$, and so on, an increasing sequence whose limit is $\sqrt{2}$ (≈17:40–18:30; notes p. 1). He flags this as a preview. Sequences and limits are "another really important concept that we will talk much more about later", and this is one reason the course needs them (≈17:40–19:16). Lecture 3 defines a sequence, and [Lecture 4](04-sequences-convergence.md) defines convergence (see [sequences and limits](sequences-and-limits.md)).

The irrationality proof shows that $\mathbf{R}$ is larger than $\mathbf{Q}$, since it contains a number, $\sqrt{2}$, that $\mathbf{Q}$ does not. Colding ties this to completeness: it is related to why $\mathbf{Q}$ is not complete, which is what the lecture works towards next (≈19:16–20:02). See [the square root of 2](square-root-of-2.md).

## Upper bounds and least upper bounds (≈20:02–27:25)

The notes head the section "Completeness of $\mathbf{R}$. (Least upper bound property.)" (notes p. 2; ≈20:48). Two definitions come first. Throughout, $\mathbf{S}$ is an ordered set and $A$ is a subset of $\mathbf{S}$.

**Upper bound** (notes p. 2; ≈20:48–22:22). $M$ is an **upper bound** for $A$ if $a \leq M$ for every $a \in A$. An upper bound has to be greater than or equal to every element of the subset; it may equal one of them (≈22:22).

The examples (notes p. 2; ≈22:22–23:58):

- If $A = \lbrace 1, 2, 3 \rbrace$, then $4$ is an upper bound for $A$, but $2$ is not, because $3$ is bigger than $2$. The notes take $A$ as a subset of $\mathbf{Z}$; on the board the ambient set is $\mathbf{N}$ (≈22:22).
- If $\mathbf{S} = \mathbf{Q}$, then $\mathbf{N}$, as a subset, has **no** upper bound. Both the board and the notes promise to return to this example (≈23:58: "I'll return to this second example in just a minute"; notes p. 2: "we will return to this shortly"). The lecture comes back to it with the [Archimedean property](#the-archimedean-property-5454100049) below.

**Least upper bound** (notes p. 2; ≈24:44–27:25). Suppose $A$ has an upper bound. $M$ is a **least upper bound** for $A$ if

1. $M$ is an upper bound for $A$, and
2. $M \leq M_1$ for every other upper bound $M_1$ of $A$.

In words, a least upper bound is the smallest of the upper bounds, "so to speak" (≈27:25). On the board Colding calls a subset with an upper bound "bounded" (≈25:35, ≈28:35). The lecture defines only upper bounds, not lower bounds; a student asks why at the end (see [questions](#questions-at-the-end-1094611517)).

## Completeness (≈27:25–30:58)

**Complete** (notes p. 2). An ordered set is **complete** if every subset that has an upper bound has a least upper bound. For the real numbers the notes put it as: "If a subset $A$ of $\mathbf{R}$ has an upper bound, then $A$ has a least upper bound." This is the **least upper bound property**. On the board Colding states it directly for fields: a complete ordered field is an ordered field in which any bounded subset has a least upper bound (≈27:25–28:35).

**Theorem** (notes p. 2). There exists a complete ordered field that contains $\mathbf{Q}$. This field is denoted $\mathbf{R}$, the real numbers (≈29:21–30:11).

The course **does not prove this theorem**. The notes say a proof "would take us too far a field"; on the board, it "really takes us off field" and is "outside the scope of this class", but "you can prove this" (≈28:35–30:11). It is taken for granted from here on. The board's statement is slightly different from the notes': it says there exists **a smallest** complete ordered field containing the rational numbers (≈29:21). The lecture does not say in what sense smallest, and the notes leave the word out.

This completes the course's characterization of $\mathbf{R}$ from Lecture 1. See [completeness and the least upper bound property](least-upper-bound-property.md).

## Theorem: $\sqrt{2} \in \mathbf{R}$ (≈30:11–52:20)

The point of working in $\mathbf{R}$ rather than $\mathbf{Q}$ is that, in particular, $\sqrt{2}$ is in it (≈30:11–30:58).

**Theorem** (notes p. 2). $\sqrt{2} \in \mathbf{R}$.

### The set and its least upper bound (≈31:45–36:41)

The proof considers a set $A$ of positive numbers whose squares are less than $2$. The board and the notes define it differently. **On the board** (≈31:45), $A$ is a set of real numbers:

$$A = \lbrace x \in \mathbf{R} : x \gt 0 \text{ and } x^2 \lt 2 \rbrace .$$

**In the notes** (p. 2), $A$ is a set of rational numbers. They write $A = (0, \sqrt{2}) \cap \mathbf{Q}$ and continue: "That is $A$ consists of all the positive rational numbers $a$ so that $a^2 \lt 2$." The interval notation uses the number being constructed; the restatement that follows it does not.

Either way, $A$ is **nonempty**, since $1 \in A$: $1$ is positive and $1^2 = 1 \lt 2$ (≈31:45–32:38; notes p. 2). And $A$ **has an upper bound**. The notes simply say $2$ is one. On the board the reason is that every $x \in A$ is positive with $x^2 \lt 2$, so $x$ itself must be less than $2$, "because 2, of course, when you square it, you're getting 4" (≈32:38).

By completeness, $A$ has a least upper bound, and that is the candidate for $\sqrt{2}$ (≈33:25–34:20). Colding deliberately calls it $x$ rather than $\sqrt{2}$: "if I denote it by square root of 2, then it's going to be confusing", because you would automatically use what you think $\sqrt{2}$ should satisfy (≈34:20–35:07). Since $1 \in A$ and $x$ is an upper bound, $x \geq 1 \gt 0$, so $x$ is positive (≈35:07–35:54; notes p. 2). What remains is to show $x^2 = 2$. The proof splits it into two inequalities, each proved by contradiction (≈36:41).

Colding comments on the method (≈37:28). It may seem that the class will always argue by contradiction, and it won't. A direct proof is generally thought better style, but sometimes contradiction is more logical, and easier the first time, "and there's nothing wrong with proving it by contradiction." See [writing proofs](writing-proofs.md).

### Step 1: $x^2 \leq 2$ (≈38:20–44:30)

Suppose not, so $x^2 \gt 2$, which means $x^2 - 2 \gt 0$ (≈39:05, ≈40:38). The idea is to find a small $h \gt 0$ for which $x - h$ is still an upper bound for $A$. Since $x - h$ is smaller than $x$, that contradicts $x$ being the *least* upper bound (≈39:05–42:11). Expanding the square (notes pp. 2–3),

$$(x - h)^2 = x^2 - 2 x h + h^2 \gt x^2 - 2 h x .$$

On the board the inequality is "bigger or equal", since $h^2$ is non-negative (≈39:53). So it is enough to choose $h$ with $x^2 - 2 h x \gt 2$, that is, with $2 h x \lt x^2 - 2$, or equivalently

$$h \lt \frac{x^2 - 2}{2 x} .$$

The right-hand side is strictly positive, because $x \gt 0$ and $x^2 \gt 2$, so such an $h \gt 0$ exists (≈42:59–44:30). For it, $(x - h)^2 \gt 2$, and the notes conclude that $x - h$ is therefore also an upper bound for $A$ (notes p. 3). That contradicts $x$ being the least upper bound. The step from $(x - h)^2 \gt 2$ to the conclusion that $x - h$ is an upper bound is asserted, not argued, both on the board (≈39:05) and in the notes.

### An aside on the two inequalities (≈44:30–46:03)

Here, Colding says, neither inequality is easier than the other. But he recalls a retired colleague who used to say that doing mathematics comes down to three things: you locate a problem, you prove one of the two inequalities, whichever is easier, and you ask Raghu, his collaborator, to prove the other one (≈45:15).

### Step 2: $x^2 \geq 2$ (≈46:03–52:20)

Suppose not, so $x^2 \lt 2$. This time the contradiction is that $x$ is not even an upper bound: for small $h \gt 0$, the number $x + h$ is in $A$ (≈46:50–48:24). Take $0 \lt h \lt 1$. Then $h^2 \lt h$, so (≈49:13; notes p. 3)

$$(x + h)^2 = x^2 + 2 x h + h^2 \lt x^2 + 2 x h + h = x^2 + h (2 x + 1) .$$

So it is enough that $x^2 + h(2 x + 1) \lt 2$, that is, $h(2 x + 1) \lt 2 - x^2$, or

$$h \lt \frac{2 - x^2}{2 x + 1} .$$

The right-hand side is positive, because $x^2 \lt 2$ and $x \gt 0$, so such an $h$ can be chosen (≈50:00–52:20). Then

$$(x + h)^2 \lt x^2 + (2 - x^2) = 2 .$$

On the board, $x + h$ is therefore in $A$, contradicting that $x$ is an upper bound for $A$ (≈52:20). Together, steps 1 and 2 give $x^2 = 2$, so $x$ is a positive real number whose square is $2$. □

Three remarks on this step:

- The notes print the last display as $(x + h)^2 \lt x^2 + 2 - x^2 \lt 2$. The second inequality sign should be an equals sign, since $x^2 + 2 - x^2$ is $2$ (a [printed slip](../raw/notes/02-introduction-to-real-numbers-cont.md#printed-slips)).
- $h$ has to satisfy **both** conditions, $h \lt 1$ and $h \lt \frac{2 - x^2}{2 x + 1}$. The board did not say so, and a student pointed it out at the end of the lecture. Colding agreed: if the second bound were $500$, "I'm not going to choose 500 because it was supposed to be less than 1"; you choose $h$ less than $1$ and also less than that positive number (≈1:13:42–1:15:17).
- The board's $A$ is a set of real numbers, so $x + h$ is in it as soon as $x + h \gt 0$ and $(x + h)^2 \lt 2$. The notes' $A$ is a set of rational numbers, and the notes call $(x + h)^2 \lt 2$ "the desired contradiction" without saying whether $x + h$ is rational or how it relates to $A$.

## Corollary: $\mathbf{Q}$ is not complete (≈52:20–54:54)

**Corollary** (notes p. 3). $\mathbf{Q}$ is not complete.

**Proof.** If $\mathbf{Q}$ were complete, the argument just given would put $\sqrt{2}$ in $\mathbf{Q}$. But no rational number squares to $2$. □

On the board Colding phrases the first half more generally: what has just been proved is that if a field is complete and contains the rationals, then $\sqrt{2}$ is in that field (≈53:07–54:08). Since $\sqrt{2}$ is not rational, $\mathbf{Q}$ itself cannot be complete.

A student later asked how a bounded set of rationals can fail to have a least upper bound (≈1:11:17–1:12:51). Colding's answer: the set of all rational numbers whose square is less than or equal to $2$ has an upper bound in $\mathbf{Q}$ but no least upper bound in $\mathbf{Q}$, because no rational number squares to $2$. Completeness of a field means that every bounded subset of the field has a least upper bound, and "any bound, including the least upper bound, that always have to be in the fields" (≈1:12:51).

## The Archimedean property (≈54:54–1:00:49)

**Archimedean property** (notes p. 3). For every $x \in \mathbf{R}$ there is a natural number $n \in \mathbf{N}$ with $x \lt n$.

Colding notes that it "seems like a kind of trivial fact", and that the lecture has "sort of used it a little bit already", but proves it rigorously here (≈54:54–56:28).

**Proof, by contradiction** (≈56:28–1:00:49; notes p. 3). The negation of the statement is that there is an $x$ with $n \leq x$ for every natural number $n$ (≈57:17). Then $x$ is an upper bound for $\mathbf{N}$, so $\mathbf{N}$ is a bounded subset of $\mathbf{R}$, and by the least upper bound property it has a least upper bound. The board calls it $y$; the notes call it $\alpha$, and this page follows the notes. So $n \leq \alpha$ for every $n \in \mathbf{N}$ (≈58:09–59:10). But $n + 1$ is also a natural number, so $n + 1 \leq \alpha$ too, which says $n \leq \alpha - 1$. Since $n$ was any natural number, $\alpha - 1$ is an upper bound for $\mathbf{N}$, smaller than $\alpha$. That contradicts $\alpha$ being the least upper bound (≈59:10–1:00:49). □

The notes frame the same argument as a proof that $\mathbf{N}$ is not bounded (notes p. 3), which is how the lecture returns to the example of $\mathbf{N}$ from the upper-bound definitions. See [the Archimedean property](archimedean-property.md).

## Corollary: a rational number between any two reals (≈1:00:49–1:08:59)

**Corollary** (notes pp. 3–4). If $x$ and $y$ are real numbers with $x \lt y$, there is a rational number $\frac{m}{n}$ with

$$x \lt \frac{m}{n} \lt y .$$

**Proof** (notes p. 4; ≈1:02:34–1:08:14). The first step is to choose a step size $\frac{1}{n}$ smaller than the gap $y - x$. Here the board and the notes label things differently, but they produce the same $n$:

- **On the board**, $\beta = y - x$, which is positive. The Archimedean property gives a natural number $n \gt \frac{1}{\beta}$, and taking reciprocals, which reverses the inequality, gives $\frac{1}{n} \lt \beta$ (≈1:02:34–1:04:05).
- **In the notes**, $\beta = \frac{1}{y - x}$. The Archimedean property gives a natural number $n \gt \beta$, and so $0 \lt \frac{1}{n} \lt \frac{1}{\beta}$, where $\frac{1}{\beta}$ is the gap $y - x$.

Next, let $m - 1$ be the largest integer with

$$m - 1 \leq x n$$

(notes p. 4). The board version of this step is garbled in the captions (≈1:05:52), but it also chooses "the largest such $m$". Dividing by $n$ gives $\frac{m - 1}{n} \leq x$. Because $m - 1$ was the largest such integer, $m$ itself is not $\leq x n$, so $\frac{m}{n}$ is larger than $x$ (≈1:06:38–1:07:26).

Finally, $\frac{m}{n}$ is less than $y$. Colding gives this step with a picture (≈1:07:26–1:08:14). Mark $x$ and $y$ on a line. The point $\frac{m - 1}{n}$ is at or to the left of $x$, and $\frac{m}{n}$ is one step of $\frac{1}{n}$ further right. Since a step is shorter than the distance from $x$ to $y$, it cannot carry you past $y$. In symbols,

$$\frac{m}{n} = \frac{m - 1}{n} + \frac{1}{n} \leq x + \frac{1}{n} \lt x + (y - x) = y .$$

□

The notes compress all of this into "It follows that $\frac{m}{n}$ has the desired property", and neither the board nor the notes say why a largest such integer exists. Colding adds that there will be "something along these lines" on the homework (≈1:08:14).

## Logistics (≈1:08:59–1:09:46)

As announced in this lecture: there would be at least four office hours the following week, 5:00–6:00 on Mondays and Wednesdays and 1:15–2:15 on the other days, with times already posted and room numbers to follow. The first homework was to be assigned that day or the next, due not the following week but the week after (≈1:08:59).

## Questions at the end (≈1:09:46–1:15:17)

The captions label four student questions in the closing minutes.

- **How is $-1$ defined, if only $+$ was defined?** (≈1:09:46–1:10:32.) A field has two operations, each with five properties that are almost the same. $1$ is the neutral element for multiplication; that is how it is defined. The argument that proved the zero is unique in Lecture 1 also proves that $1$ is unique, so "1" is a well-defined notion. Then $-1$ is the inverse element of $1$ with respect to addition.
- **Why define an upper bound and not a lower bound?** (≈1:10:32–1:11:17.) Colding agrees it would seem more logical to define both, and says he will come back to it next time. His short answer is that lower bounds are "contained in" the upper-bound notion: "you can look at the complement", and the upper bound for the complement "is the same as the lower bound". That is the captions' wording. The lecture does not say how the set is to be transformed or why its upper bounds are the lower bounds, so read this answer as a pointer to the next lecture rather than a definition. [Lecture 3](03-how-to-write-a-proof-archimedean-property.md) defines lower bounds and the greatest lower bound $\inf A$ directly, calls the two notions "a symmetric property" (Lecture 3, ≈19:42), and does not return to the complement remark. See [supremum and infimum](supremum-and-infimum.md).
- **How can a bounded set of rationals have no least upper bound?** (≈1:11:17–1:12:51.) Answered above, under the corollary that $\mathbf{Q}$ is not complete.
- **Does step 2 also need $h \lt 1$?** (≈1:12:51–1:15:17.) Yes, $h$ must satisfy both bounds: answered above, in the remarks after step 2.

## Board versus notes

Where they differ, this page follows the notes and gives the board's version with its timestamp. Collected here:

- **The set $A$ in the proof that $\sqrt{2} \in \mathbf{R}$.** Board: positive *real* numbers with square less than $2$ (≈31:45). Notes: positive *rational* numbers with square less than $2$, written $(0, \sqrt{2}) \cap \mathbf{Q}$ (p. 2).
- **The existence theorem.** Board: there exists a *smallest* complete ordered field containing $\mathbf{Q}$ (≈29:21). Notes: there exists a complete ordered field containing $\mathbf{Q}$ (p. 2).
- **What is called complete.** Board: a complete ordered *field* (≈27:25–28:35). Notes: a complete ordered *set*, and the least upper bound property for subsets of $\mathbf{R}$ (p. 2).
- **The example $A = \lbrace 1, 2, 3 \rbrace$.** Board: inside $\mathbf{N}$ (≈22:22). Notes: inside $\mathbf{Z}$ (p. 2).
- **Why $A$ has an upper bound.** Board: $x^2 \lt 2$ forces $x \lt 2$ (≈32:38). Notes: "2 is an upper bound for $A$" (p. 2).
- **Step 1's expansion.** Board: $(x - h)^2$ is greater than or equal to $x^2 - 2 x h$ (≈39:53). Notes: strictly greater (p. 2).
- **Names.** The least upper bound of $\mathbf{N}$ is $y$ on the board (≈58:09) and $\alpha$ in the notes; in the last corollary $\beta$ is $y - x$ on the board (≈1:02:34) and $\frac{1}{y - x}$ in the notes (p. 4).
- **The irrationality proof.** The notes' $2 m_1 = n$ is a misprint for $2 m_1^2 = n^2$, which Colding corrects himself to on the board (≈14:59).

## Where the lecture stops

With completeness defined, the course's description of $\mathbf{R}$ as a complete ordered field containing $\mathbf{Q}$ is now fully explained, and Lecture 1's questions "Why is $\sqrt{2}$ a real number?" and "What is $\sqrt{2}$?" have answers: it is the least upper bound of the positive numbers whose square is less than $2$, and such a least upper bound exists because $\mathbf{R}$ is complete. Two threads are left open: lower bounds, promised for next time (≈1:11:17), and sequences and limits, promised for later (≈17:40). [Lecture 3](03-how-to-write-a-proof-archimedean-property.md) takes up lower bounds, rewrites the proofs of $\sqrt{2} \in \mathbf{R}$ and of the Archimedean property as formal proofs, and defines a sequence. Limits come in [Lecture 4](04-sequences-convergence.md), "Sequences; Convergence" (TBB Sections 2.1–2.2 and 2.4–2.7).

## Related pages

- [Completeness and the least upper bound property](least-upper-bound-property.md): upper bounds, least upper bounds, complete ordered sets and fields, and the existence of $\mathbf{R}$.
- [The square root of 2](square-root-of-2.md): why it is not rational, and why it is real.
- [The Archimedean property](archimedean-property.md): the statement, its proof from completeness, and the rational number between any two reals.
- [The real numbers](real-numbers.md): the course's one-sentence characterization of $\mathbf{R}$, now complete.
- [The rational numbers](rational-numbers.md): $\mathbf{Q}$, including why it is not complete.
- [Fields and ordered fields](fields-and-ordered-fields.md): the axioms recapped at the start of this lecture.
- [Writing proofs](writing-proofs.md): proof by contradiction, and proving an equality as two inequalities.
- [Lecture 1 — Introduction to Real Numbers](01-introduction-to-real-numbers.md): the previous lecture.
- [Lecture 3 — How to Write a Proof; Archimedean Property](03-how-to-write-a-proof-archimedean-property.md): the next lecture, which writes two of these proofs out formally.
