# Algebraic properties of limits

**Limits of sequences respect constant multiples, sums, products and quotients: the theorem as the Lecture 4 notes state it, the proofs of all four parts, the trick of comparing through a term halfway between, and how Lecture 5 uses them.**

Notation: $a_n$ and $b_n$ are sequences of real numbers, $\vert x \vert$ is the absolute value of $x$ (Colding often says "norm"), $\mathbf{N} = \lbrace 1, 2, 3, \cdots \rbrace$ and $\mathbf{R}$ are set in bold as in the notes. A sequence $a_n$ converges to $a$ if for every $\epsilon \gt 0$ there is an $N \in \mathbf{N}$ with $\vert a_n - a \vert \lt \epsilon$ for all $n \geq N$; see [sequences and limits](sequences-and-limits.md).

## The theorem

**Theorem** (Lecture 4 notes p. 3, "Basic algebraic properties of limits"; Lecture 4, ≈27:14–30:25). Suppose that $a_n$ and $b_n$ are convergent sequences with $\lim a_n = a$ and $\lim b_n = b$, and let $C \in \mathbf{R}$. Then:

1. $c_n = C a_n$ is convergent and $\lim_{n \to \infty} c_n = C a$.
2. $c_n = a_n + b_n$ is convergent and $\lim_{n \to \infty} c_n = a + b$.
3. $c_n = a_n b_n$ is convergent with $\lim_{n \to \infty} c_n = a b$.
4. If $b_n \neq 0$, $b \neq 0$ and $c_n = \frac{a_n}{b_n}$, then $c_n$ is convergent and $\lim_{n \to \infty} c_n = \frac{a}{b}$.

On the board the fourth property is stated for reciprocals: if every $a_n \neq 0$ and $a \neq 0$, then $\frac{1}{a_n} \to \frac{1}{a}$ (Lecture 4, ≈29:33). The notes prove the case $\frac{1}{b_n}$ and say that the general case follows from it together with the third property (notes p. 4), without spelling out how.

Colding proves the first two formally and presents the last two as something "very, very close to a formal proof but it's more like what you would have on a piece of scrap paper" (≈30:25). In the event the board proof of the third is complete (≈51:53). The notes give full proofs of (1) and (2) and outlines of (3) and (4), with details "to fill in" (notes p. 4).

## The common pattern

Each proof is handed an $\epsilon \gt 0$ and must produce an $N$. It does not feed that $\epsilon$ straight into the hypotheses. Since $a_n \to a$ holds for every positive number, the proof applies it to whatever positive number makes the final inequality come out: $\frac{\epsilon}{\vert C \vert}$, $\frac{\epsilon}{2}$, $\frac{\epsilon}{2 (\vert b \vert + 1)}$ or $\frac{\vert a \vert}{2}$ (≈32:03, ≈35:27, ≈48:34, ≈58:56). "I'm basically using that for all epsilon, that it wasn't just for a fixed epsilon" (≈42:08). When two hypotheses each give an $N$, the proof takes the larger of the two.

## Property 1: $C a_n \to C a$

(Lecture 4 notes p. 4; ≈31:10–33:35.) If $C = 0$ the claim is obviously true, so assume $C \neq 0$. Given $\epsilon \gt 0$, there is an $N$ such that for $n \geq N$,

$$\vert a - a_n \vert \lt \frac{\epsilon}{\vert C \vert} .$$

Multiplying both sides by $\vert C \vert$ gives $\vert C a - C a_n \vert \lt \epsilon$ for $n \geq N$. □

## Property 2: $a_n + b_n \to a + b$

(Lecture 4 notes p. 4; ≈35:27–40:34.) Observe that

$$\vert c_n - (a + b) \vert = \vert (a_n - a) + (b_n - b) \vert \leq \vert a_n - a \vert + \vert b_n - b \vert .$$

Given $\epsilon \gt 0$, find $N_a$ with $\vert a_n - a \vert \lt \frac{\epsilon}{2}$ for $n \geq N_a$, and $N_b$ with $\vert b_n - b \vert \lt \frac{\epsilon}{2}$ for $n \geq N_b$. Set $N = \max\lbrace N_a, N_b \rbrace$. For $n \geq N$,

$$\vert c_n - (a + b) \vert \leq \vert a_n - a \vert + \vert b_n - b \vert \lt \frac{\epsilon}{2} + \frac{\epsilon}{2} = \epsilon .$$

□

A student asked what justifies using $\frac{\epsilon}{2}$. The convergence of $a_n$ and $b_n$ holds for every $\epsilon$, in particular for $\frac{\epsilon}{2}$. The cost is that the $N$ obtained is probably much larger than for $\epsilon$ itself (≈40:34–42:08).

## Property 3: $a_n b_n \to a b$, and the halfway trick

(Lecture 4 notes p. 4; ≈42:08–53:24.) Comparing $a_n b_n$ with $a b$ directly is awkward. Instead compare each with $a_n b$, "something that is halfway between this and that" (≈43:44): subtract it and add it straight back. This gives (notes p. 4)

$$\vert a b - a_n b_n \vert \leq \vert a b - a_n b \vert + \vert a_n b - a_n b_n \vert = \vert b \vert \thinspace \vert a - a_n \vert + \vert a_n \vert \thinspace \vert b - b_n \vert .$$

The first term is a fixed constant times a difference that goes to $0$, "no problem at all". The second has the factor $\vert a_n \vert$, which is not constant (≈45:16). Here the theorem that a [convergent sequence is bounded](sequences-and-limits.md#a-convergent-sequence-is-bounded) comes in: $\vert a_n \vert \leq C$ for all $n$, for some $C$ (≈46:04–46:51). So

$$\vert a_n b_n - a b \vert \leq C \vert b_n - b \vert + \vert b \vert \thinspace \vert a_n - a \vert .$$

The notes stop here: "This is the main idea of the proof of the third property." On the board Colding finishes (≈48:34–51:53). Given $\epsilon \gt 0$, choose $N_a$ with

$$\vert a_n - a \vert \lt \frac{\epsilon}{2 (\vert b \vert + 1)}$$

for $n$ beyond $N_a$, and $N_b$ with

$$\vert b_n - b \vert \lt \frac{\epsilon}{2 (1 + C)}$$

for $n$ beyond $N_b$. The $+1$ in each denominator keeps the expression meaningful if $b$ is $0$ (≈49:24, ≈50:17). For $n$ beyond both,

$$\vert a_n b_n - a b \vert \leq C \frac{\epsilon}{2 (1 + C)} + \vert b \vert \frac{\epsilon}{2 (\vert b \vert + 1)} ,$$

and since $\frac{C}{1 + C}$ and $\frac{\vert b \vert}{\vert b \vert + 1}$ are bounded by $1$, each term is bounded by $\frac{\epsilon}{2}$ and the whole by $\epsilon$ (≈51:04–51:53). □

**Why the trick matters.** Colding's main takeaway from the third property is "this little idea about inserting something that was halfway between the two things you were comparing" (≈53:24). The same trick proves the Leibniz rule for the derivative of a product of two functions (≈54:10). On the OCW lecture list, derivatives come in Lecture 15, "Derivatives; Laws for Differentiation", which this knowledge base does not yet cover.

## Property 4: quotients and reciprocals

(Lecture 4 notes p. 4; ≈54:10–1:03:38.) Take the reciprocal case, $c_n = \frac{1}{a_n}$ with every $a_n \neq 0$ and $a \neq 0$, as on the board. Then

$$\left\vert \frac{1}{a_n} - \frac{1}{a} \right\vert = \frac{\vert a - a_n \vert}{\vert a_n \vert \thinspace \vert a \vert} .$$

The numerator goes to $0$. The denominator has to be bounded from below, which, since $a$ is fixed and not $0$, means bounding $\vert a_n \vert$ from below for $n$ sufficiently large (≈55:42–56:33). Writing $a = (a - a_n) + a_n$ gives

$$\vert a \vert - \vert a - a_n \vert \leq \vert a_n \vert$$

(≈57:20–58:05). Apply the definition of $a_n \to a$ to the positive number $\frac{\vert a \vert}{2}$: there is an $N_1$ such that $\vert a - a_n \vert \lt \frac{\vert a \vert}{2}$ for $n$ bigger than $N_1$, and then $\vert a_n \vert \gt \frac{\vert a \vert}{2}$ (≈58:56–1:00:36). So for $n$ bigger than $N_1$,

$$\left\vert \frac{1}{a_n} - \frac{1}{a} \right\vert \leq \frac{2 \vert a - a_n \vert}{\vert a \vert^2} ,$$

and since $a$ is a constant, going further out than $N_1$ makes this smaller than any given $\epsilon$ (≈1:02:08–1:02:53). "At this point, that's not very much to fill in" (≈1:02:53).

The notes' outline is the same argument with $b_n$ and $b$: it uses $\frac{1}{b_n} - \frac{1}{b} = \frac{\vert b - b_n \vert}{\vert b \vert \thinspace \vert b_n \vert}$ (printed without absolute value bars on the left, a [printed slip](../raw/notes/04-sequences-convergence.md#printed-slips)) and $\vert b_n \vert \geq \vert b \vert - \vert b_n - b \vert$ to bound the denominator from below, and leaves the details (notes p. 4).

## The rules at work (Lecture 5)

Lecture 5 reviews the four rules with the sum first and the constant multiple second; Colding says "I think I might have exchanged the order of 1 and 2 last time", and that there is no particular convention (Lecture 5, ≈4:50–7:20). He states the fourth rule for reciprocals: if $a_n \neq 0$ for all $n$ and $a \neq 0$, then $\frac{1}{a_n} \to \frac{1}{a}$ (≈6:29–7:20). The Lecture 5 notes keep Lecture 4's order and also state the fourth rule for a reciprocal, $c_n = \frac{1}{b_n}$ with limit $\frac{1}{b}$ (Lecture 5 notes p. 1).

**A worked example** (Lecture 5 notes p. 2; Lecture 5, ≈7:20–13:46). To show $a_n = \frac{n^2 + 1}{n^2 + n + 1} \to 1$, divide the numerator and the denominator by $n^2$:

$$a_n = \frac{1 + \frac{1}{n^2}}{1 + \frac{1}{n} + \frac{1}{n^2}} .$$

On the board each rule is applied in turn. Since $\frac{1}{n} \to 0$, $\frac{1}{n^2} \to 0$ and the constant sequence $1$ converges to $1$, the rule for sums gives that the numerator and the denominator both converge to $1$. The denominator is never $0$ and its limit is not $0$, so the rule for reciprocals gives that $1$ over the denominator converges to $1$. Then the rule for products gives $a_n \to 1 \cdot 1 = 1$ (≈9:00–13:00). The notes say only "It now follows from the algebraic properties of limits that" $a_n \to 1$. Colding's comment: "This is the first time you see it, but you know in a couple of weeks this will feel too easy" (≈13:46).

**In the proof that the decimals of $\sqrt{2}$ converge** (Lecture 5 notes p. 4; ≈56:56–1:04:58). The rule for products gives $a_n^2 \to a^2$ from $a_n \to a$, and the rules for sums and products give $\left( a_n + 10^{1-n} \right)^2 \to a^2$ from $10^{1-n} \to 0$. The step from an inequality for every term to the same inequality for the limit is used there without proof. See [the monotone convergence theorem](monotone-convergence-theorem.md).

## Lectures

- [Lecture 4 — Sequences; Convergence](04-sequences-convergence.md): the statement, the proofs on the board, the students' questions, and where the board and the notes differ.
- [Lecture 5 — Monotone Convergence Theorem](05-monotone-convergence-theorem.md): the review, the worked example, and the rules used in the proof about $\sqrt{2}$.
