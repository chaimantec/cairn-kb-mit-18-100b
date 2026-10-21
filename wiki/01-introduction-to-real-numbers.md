# Lecture 1 — Introduction to Real Numbers

**18.100B Real Analysis, Spring 2025 · Tobias Holck Colding · [video](https://www.youtube.com/watch?v=BWvjy0a1Ffg) (66 min)**

Sources for this page: the [edited transcript](../raw/transcripts/01-introduction-to-real-numbers.md) (timestamps below are written ≈M:SS and point into it), the course's typed [lecture notes](../raw/notes/01-introduction-to-real-numbers.md) for this lecture (cited "notes p. N"; [PDF on OCW](https://ocw.mit.edu/courses/18-100b-real-analysis-spring-2025/mit18_100b_s25_lec01.pdf)), and the OCW readings list, which assigns Sections 1.1–1.4 of Thomson, Bruckner and Bruckner, *Elementary Real Analysis* (TBB) to this lecture. Colding teaches from the blackboard; there are no slides.

## What this lecture establishes

The course has two goals: learning **how to write a mathematical proof**, and **proving the theorems of calculus** rigorously (≈4:44; notes p. 1). Colding motivates both with the intermediate value theorem, which looks obvious from a picture but cannot be proved until we know exactly which properties of the real numbers it uses. The answer, stated in this lecture and unpacked over the next ones, is that **$\mathbf{R}$ is a complete ordered field that contains the rational numbers $\mathbf{Q}$** (≈12:45; notes p. 1). This lecture explains everything in that sentence except *complete*, which is deferred to a later lecture (≈13:39–14:27). On the way it defines the rational numbers and their operations, proves that multiplication of rationals is well defined, states the eleven field axioms, defines ordered sets and ordered fields, and proves two small theorems from the axioms: a field has only one zero, and in an ordered field multiplying an inequality by a positive element preserves it.

Notation: the notes set the number systems in bold, $\mathbf{N}$, $\mathbf{Z}$, $\mathbf{Q}$, $\mathbf{R}$, and write a field as $\mathbf{F}$; this page follows them. On the board Colding calls them "capital R", "Q" and "capital F" (≈13:39, ≈32:08).

## Course logistics (≈0:00–4:44)

These are as announced in the first lecture of Spring 2025. There are ten weekly problem sets; the first was due two weeks after this lecture rather than one (≈1:32). There is one midterm, announced for March 20, and one final exam (≈2:18). Homework counts for 50% of the grade, the midterm 20% and the final 30% (≈2:18), which matches the OCW syllabus; the syllabus adds that the lowest problem-set score is dropped, that the midterm is 1.5 hours and the final 3 hours, and that one page of notes is allowed in each exam. Collaboration on problem sets is encouraged, but everyone hands in their own; Colding enabled the "pset partners" tool to help students find collaborators (≈3:54). He typed lecture notes for this class specifically, which he says he does not usually do (≈0:46). The class is listed as both 18.100B and 18.1002 (≈0:00; notes p. 1).

## The motivating example: the intermediate value theorem (≈5:29–10:18)

Suppose $a$ and $b$ are real numbers with $a \lt b$, and $f : [a, b] \to \mathbf{R}$ is a continuous function with $f(a) \lt 0$ and $f(b) \gt 0$. The **intermediate value theorem** says there is a $c$ between $a$ and $b$ with $f(c) = 0$ (≈7:09; notes p. 1). More generally, Colding says, a continuous function on an interval "takes all values in between" (≈7:09).

The informal meaning of *continuous* is that when you draw the graph, the chalk never leaves the blackboard: the graph is drawn in one motion, and a function that jumps is not continuous (≈7:55–8:40; notes p. 1 says the same with a pencil and paper). With that picture the theorem seems obvious: a graph that starts below the axis and ends above it must cross it. The point of the course is that this intuition is not a proof. Colding insists this is not a semantic quibble: without a completely rigorous foundation one quickly reaches statements that *seem* true but are not, and then one cannot even tell what *should* be true. Building up step by step, each step rigorous, both guarantees correctness and makes it easier to predict what is true (≈9:29).

So the first question a proof raises is: **which property of the real numbers does it use?** (≈10:18). That leads to three questions (≈11:12–11:58; notes p. 1):

- **Q1.** What is a real number?
- **Q2.** Why is $\sqrt{2}$ a real number?
- **Q3.** What is $\sqrt{2}$?

The answer: $\mathbf{R}$ is a complete ordered field containing $\mathbf{Q}$, and this is exactly what the proof of the intermediate value theorem uses (≈12:45–13:39). The theorem itself is proved later in the course; the OCW lecture list puts it in Lecture 11, "Extreme and Intermediate Value Theorem; Metric Spaces". See [the intermediate value theorem](intermediate-value-theorem.md) and [the real numbers](real-numbers.md).

## Notation: $\mathbf{N}$, $\mathbf{Z}$, $\mathbf{Q}$ (≈14:27–16:10)

- $\mathbf{N} = \lbrace 1, 2, 3, \cdots \rbrace$ is the **natural numbers**. Note that $0 \notin \mathbf{N}$ in this course's convention.
- $\mathbf{Z} = \lbrace 0, \pm 1, \pm 2, \pm 3, \cdots \rbrace$ is the **integers**: the natural numbers, their negatives, and $0$.
- $\mathbf{Q}$ is the **rational numbers**: all numbers of the form $\frac{m}{n}$ with $m \in \mathbf{Z}$ and $n \in \mathbf{N}$ (notes p. 2).

The convention that the denominator is a *natural* number, so always positive, matters below: it is what makes the definition of order on $\mathbf{Q}$ work (≈23:10–24:01).

## The rational numbers and their operations (≈16:10–24:01)

A rational number is written as a quotient, but not uniquely: many quotients represent the same number (≈16:56). So the first thing to define is when two quotients are equal. With $m_1, m_2 \in \mathbf{Z}$ and $n_1, n_2 \in \mathbf{N}$ (notes p. 2):

$$\frac{m_1}{n_1} = \frac{m_2}{n_2} \iff m_1 n_2 = m_2 n_1 .$$

That is, two quotients are the same exactly when cross-multiplying gives the same integer (≈17:47). Then come two operations and an order. **Addition** puts the quotients over a common denominator (≈19:21):

$$\frac{m_1}{n_1} + \frac{m_2}{n_2} = \frac{m_1 n_2 + m_2 n_1}{n_1 n_2} ,$$

and the result is again a rational number, because the numerator is an integer and the denominator a natural number. **Multiplication** multiplies numerators and denominators (≈21:37):

$$\frac{m_1}{n_1} \frac{m_2}{n_2} = \frac{m_1 m_2}{n_1 n_2} .$$

**Order** compares by cross-multiplying (≈23:10):

$$\frac{m_1}{n_1} \lt \frac{m_2}{n_2} \iff m_1 n_2 \lt m_2 n_1 .$$

This step is legitimate only because $n_1$ and $n_2$ are positive: multiplying both sides of an inequality by them keeps its direction (≈24:01). Colding's summary is that $\mathbf{Q}$ comes with addition, multiplication and an ordering, and the definitions of field and ordered field below abstract exactly these three structures (≈32:08). More in [the rational numbers](rational-numbers.md).

## Proof: multiplication on $\mathbf{Q}$ is well defined (≈24:01–31:22)

Because a rational number has many representations, an operation on quotients only makes sense if the answer does not depend on which representation you started from. For addition and multiplication this has to be checked (≈20:06–20:52, ≈24:01). Colding checks multiplication. He picks it because it is less messy on the blackboard; addition is "exactly the same" but messier (≈30:35–31:22). Neither the lecture nor the notes write out the addition case.

**Claim** (notes p. 2). If

$$\frac{m_1}{n_1} = \frac{m_2}{n_2} \quad\text{and}\quad \frac{p_1}{q_1} = \frac{p_2}{q_2} ,$$

then

$$\frac{m_1}{n_1} \frac{p_1}{q_1} = \frac{m_2}{n_2} \frac{p_2}{q_2} .$$

**Proof.** By the definition of equality of quotients, the hypotheses say $m_1 n_2 = m_2 n_1$ and $p_1 q_2 = p_2 q_1$ (≈27:26). The two products are $\frac{m_1 p_1}{n_1 q_1}$ and $\frac{m_2 p_2}{n_2 q_2}$ (≈28:12–28:59), and again by the definition of equality, they are equal exactly when

$$m_1 p_1 n_2 q_2 = m_2 p_2 n_1 q_1$$

(≈28:59–29:50). Rearranging the left side and substituting the two hypotheses gives it:

$$m_1 p_1 n_2 q_2 = m_1 n_2 p_1 q_2 = m_2 n_1 p_2 q_1 ,$$

and the right-hand end has the same four factors as $m_2 p_2 n_1 q_1$ (≈29:50–30:35). □

The notes stop at the displayed chain and leave that last comparison to the reader. Colding presents the argument as a model of **how detailed a proof should be**: every step is justified by a definition or a hypothesis (≈31:22; notes p. 3, "This illustrate how detailed a proof should be"). See [writing proofs](writing-proofs.md).

## Fields (≈32:08–44:19)

Abstracting from $\mathbf{Q}$: a **field** $\mathbf{F}$ is a set with two operations, denoted "suggestively" by $+$ and $\cdot$. The symbols are only suggestive; the operations are abstract and are characterized entirely by the axioms (≈33:05; notes p. 3). There are five axioms for each operation and one more that ties them together, eleven in all (≈33:52).

**Additive properties** (≈33:52–37:52; notes p. 3):

1. If $x, y \in \mathbf{F}$, then $x + y \in \mathbf{F}$. Addition really is an operation on $\mathbf{F}$.
2. $x + y = y + x$. This is the *commutative* or *abelian* property (≈35:28).
3. $(x + y) + z = x + (y + z)$. This is the *associative* property (≈41:57).
4. There exists an element $0 \in \mathbf{F}$ such that $0 + x = x$ for all $x \in \mathbf{F}$. This is a *neutral element* for addition (≈36:17).
5. For every $x \in \mathbf{F}$ there exists an element, denoted suggestively by $(-x)$, such that $x + (-x) = 0$. This is the *inverse element* (≈42:43).

**Multiplicative properties** (≈38:41–41:12; notes p. 3), which mirror the additive ones:

1. If $x, y \in \mathbf{F}$, then $x y \in \mathbf{F}$.
2. $x y = y x$.
3. $(x y) z = x (y z)$.
4. There exists an element, denoted suggestively by $1$, such that $1 x = x$ for all $x \in \mathbf{F}$.
5. For every $x \in \mathbf{F} \setminus \lbrace 0 \rbrace$ there exists an element, denoted suggestively by $\frac{1}{x}$, such that $x \frac{1}{x} = 1$.

The one twist in the mirror is in property 5: $0$ has to be excluded, so there is no inverse of $0$ (≈41:57). Colding points out that, apart from that reference to $0$, the ten axioms say nothing about how the two operations interact (≈42:43). The eleventh does:

**Distributive law** (≈42:43–44:19; notes p. 3):

$$(x + y) z = x z + y z .$$

On the board Colding states it with the multiplication on the left, $x(y + z) = xy + xz$ (≈43:32). By the commutativity of multiplication the two forms say the same thing. When he uses it later in the lecture he calls it "the 11th law" (≈1:02:19).

### Theorem: a field has only one zero (≈44:19–48:18)

Axiom 4 says *some* element behaves like zero; it does not say only one does. The first theorem settles it (notes p. 3): **in any field, the zero is unique.**

**Proof.** Suppose $0_ {1}$ and $0_ {2}$ are both zero elements, meaning $0_ {1} + x = x$ and $0_ {2} + x = x$ for every $x \in \mathbf{F}$ (≈46:45). Take $x = 0_ {2}$ in the first: $0_ {1} + 0_ {2} = 0_ {2}$. Now use commutativity to write $0_ {1} + 0_ {2} = 0_ {2} + 0_ {1}$, and take $x = 0_ {1}$ in the second: $0_ {2} + 0_ {1} = 0_ {1}$. Both equal $0_ {1} + 0_ {2}$, so $0_ {1} = 0_ {2}$ (≈46:45–47:33). □

The commutativity step is explicit on the board (≈47:33: "the ordering I know already is irrelevant"). The notes' version, $0_ {1} + 0_ {2} = 0_ {1}$ "since $0_ {2}$ is a 'zero'", uses it silently, because axiom 4 is written with the zero on the left. Colding says the posted notes are "slightly more rigorous" than what he wrote on the board, and tells students to read them too (≈47:33–48:18).

### Examples (≈48:18–50:37)

- $\mathbf{Q}$ **is a field**, with all eleven properties (≈49:04; notes p. 4).
- $\mathbf{N}$ **is not a field.** It fails many of the axioms, starting with the most basic: it has no zero element at all (≈49:04).
- $\mathbf{Z}$ **is not a field**, though it is "slightly closer". It fails multiplicative property 5: the multiplicative identity is the usual $1$, and $2$ would need an inverse, an element whose product with $2$ is $1$. That element would be one half, which is not in $\mathbf{Z}$ (≈49:52–50:37).

More in [fields and ordered fields](fields-and-ordered-fields.md).

## Ordered sets and ordered fields (≈50:37–58:14)

An **ordered set** $\mathbf{S}$ is a set with a relation $\lt$, again chosen only because it is suggestive (≈52:23), with two properties (notes p. 4):

1. For any $x, y \in \mathbf{S}$, one of the following holds: $x \lt y$, or $y \lt x$, or $x = y$.
2. If $x \lt y$ and $y \lt z$, then $x \lt z$.

The first property says any two elements can be compared: if they are not the same element, one is smaller than the other (≈53:26). The lecture does not state the second property, transitivity, aloud; it is in the notes.

An **ordered field** is a field that is also an ordered set, in which the ordering and the operations "speak to each other" through two more properties (≈54:15–56:33; notes p. 4):

1. If $x \lt y$, then $x + z \lt y + z$ (for every $z$ in the field). This is how the order interacts with addition: you can add the same thing to both sides.
2. If $x \gt 0$ and $y \gt 0$, then $x y \gt 0$. This is how the order interacts with multiplication: a product of positives is positive.

$\mathbf{Q}$ **is an ordered field**: it is a field, its order (defined by cross-multiplying, above) compares any two rationals, and the order interacts with addition and multiplication in exactly these two ways (≈56:33–58:14; notes p. 4).

### Theorem: multiplying by a positive element preserves an inequality (≈58:14–1:04:35)

**Theorem** (notes p. 4). In an ordered field, if $x \lt y$ and $z \gt 0$, then $x z \lt y z$.

Colding introduces it as a property "you know so well", which now follows from the axioms (≈59:09–59:55).

**Proof** (≈59:55–1:04:35). We want $x z \lt y z$. Adding $-(x z)$ to both sides, which is ordered-field property 1, shows this is equivalent to $0 \lt y z - x z$. On the left, $x z + (-(x z)) = 0$ by additive property 5, since $-(x z)$ is the inverse element of the product $x z$ (≈1:00:42–1:01:31). On the right, the distributive law lets us factor:

$$y z - x z = (y - x) z$$

(≈1:02:19). Colding remarks in passing that writing $y z + (-(x z))$ as $y z - x z$ "maybe we need to show", but that it is "not hard to believe". Next, $y \gt x$ is equivalent to $y - x \gt 0$, by adding $-x$ to both sides, again ordered-field property 1 (≈1:03:04). So we need to show that $(y - x) z \gt 0$, where both $y - x$ and $z$ are positive. That is exactly ordered-field property 2: a product of positives is positive (≈1:03:49). □

The notes give the same argument in three sentences (notes p. 4). The board version names the axiom behind every step, which is the level of detail the course is asking for.

## Where the lecture stops

In the statement that $\mathbf{R}$ is a complete ordered field containing $\mathbf{Q}$, the one word still unexplained is **complete**. Colding says he will define it in a later lecture (≈13:39–14:27, ≈51:29). The course's Lecture 2 is titled "Introduction to Real Numbers (cont.)" and its reading is TBB Sections 1.5–1.6, but this knowledge base does not yet cover it. He closes by asking for patience. In his experience, writing proofs takes students some time to get the hang of; a few weeks or months in, "things will really turn around", and it becomes more fun (≈1:05:20).

## Related pages

- [The real numbers](real-numbers.md): what it means that $\mathbf{R}$ is a complete ordered field containing $\mathbf{Q}$, and what is still to come.
- [The rational numbers](rational-numbers.md): quotients, equality, the operations, the order, and well-definedness.
- [Fields and ordered fields](fields-and-ordered-fields.md): the eleven field axioms, ordered sets and ordered fields, and the consequences proved so far.
- [The intermediate value theorem](intermediate-value-theorem.md): the course's motivating example.
- [Writing proofs](writing-proofs.md): what the course expects a proof to look like.
