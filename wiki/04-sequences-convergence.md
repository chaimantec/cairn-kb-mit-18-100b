# Lecture 4 — Sequences; Convergence

**18.100B Real Analysis, Spring 2025 · Tobias Holck Colding · [video](https://www.youtube.com/watch?v=PzeCGelnheE) (79 min)**

Sources for this page: the [edited transcript](../raw/transcripts/04-sequences-convergence.md) (timestamps below are written ≈M:SS and point into it), the course's typed [lecture notes](../raw/notes/04-sequences-convergence.md) for this lecture (cited "notes p. N"; [PDF on OCW](https://ocw.mit.edu/courses/18-100b-real-analysis-spring-2025/mit18_100b_s25_lec04.pdf)), and the OCW readings list, which assigns Sections 2.1–2.2 and 2.4–2.7 of Thomson, Bruckner and Bruckner, *Elementary Real Analysis* (TBB) to this lecture. Colding teaches from the blackboard; there are no slides.

## What this lecture establishes

Lecture 3 defined a sequence and stopped before saying what its limit is. This lecture gives the **definition of convergence** with $\epsilon$ and $N$, and calls a sequence that does not converge **divergent** (≈4:45–8:46; notes p. 2). Its first worked example makes sense of $0.999 \cdots = 1$: the left side is the limit of the sequence $0.9$, $0.99$, $0.999$, …, and the Archimedean property proves that this limit is $1$ (≈8:46–15:23; notes pp. 2–3). Then come three results that the rest of the course leans on. A **convergent sequence is bounded** (≈15:23–26:28; notes p. 3). Limits respect the **algebraic operations**: multiplying by a constant, sums, products and quotients (≈24:53–1:03:38; notes pp. 3–4). And a sequence converges to $a$ **if and only if every subsequence converges to $a$** (≈1:11:01–1:16:38; notes pp. 5–6), once a **subsequence** has been defined as the composition with a strictly increasing map $g : \mathbf{N} \to \mathbf{N}$ (≈1:03:38–1:11:01; notes p. 5).

Two techniques recur in the proofs. One is choosing the $\epsilon$ to feed into a definition: $\epsilon$ itself, $1$, $\frac{\epsilon}{2}$, $\frac{\epsilon}{\vert C \vert}$ or $\frac{\vert a \vert}{2}$, whichever makes the conclusion come out. The other is to compare two quantities through a third that sits "halfway between" them (≈43:44, ≈53:24). Both are written up on [sequences and limits](sequences-and-limits.md) and [algebraic properties of limits](algebraic-properties-of-limits.md).

Notation: as in the earlier lectures, the notes set the number systems in bold, $\mathbf{N}$ and $\mathbf{R}$, and this page follows them. In this course $\mathbf{N} = \lbrace 1, 2, 3, \cdots \rbrace$ starts at $1$. A sequence is written $a_n$, its terms $a_1, a_2, a_3, \cdots$, and $\vert x \vert$ is the absolute value of $x$, which Colding often calls the "norm" (≈32:03, ≈57:20).

## From Lecture 3: sequences (≈0:00–4:45)

The notes open by repeating Lecture 3's definitions: an upper bound, completeness, $\sup A$, a lower bound and the greatest lower bound (notes p. 1). In this repetition $\sup A$ is called "the greatest lower bound of $A$", a [printed slip](../raw/notes/04-sequences-convergence.md#printed-slips) for the smallest upper bound.

Colding starts from the end of Lecture 3. On the real line, $\sqrt{2}$ lies between $1$ and $2$, and the sequence $1$, $1.4$, $1.41$, $1.414$, … takes more and more of its digits. This sequence is increasing, and "square root of 2 is, in some sense, the limit of the sequence" (≈0:00–0:55; notes pp. 1–2, Example 1). A **sequence** of real numbers is a function $f : \mathbf{N} \to \mathbf{R}$, and its value at $n$ is written with a subscript, $a_n = f(n)$ (≈1:43; notes pp. 1–2).

Two more examples (≈2:28–4:45; notes p. 2, Examples 2 and 3):

- $a_n = (-1)^n$. Then $a_1 = -1$, $a_2 = (-1)(-1) = 1$, $a_3 = -1$, $a_4 = 1$, and the sequence alternates between $-1$ and $1$. "It doesn't really converge. It doesn't really have a limit" (≈3:13). The notes: "This sequence has NO limit."
- $a_n = \frac{1}{n}$, a decaying sequence: $a_1 = 1$, $a_2 = \frac{1}{2}$, $a_3 = \frac{1}{3}$, $a_4 = \frac{1}{4}$. All its terms are positive and they become smaller and smaller, so it seems obvious that this sequence has a limit, and the limit is $0$ (≈3:58–4:45). Colding says "1/2" for $a_3$, a slip of the tongue (≈3:58).

Neither claim is proved in the lecture or the notes; they motivate the definition that follows.

## The definition of convergence (≈4:45–8:46)

**Definition** (notes p. 2; ≈5:30–7:59). Let $a_n$ be a sequence and $a$ a real number. The sequence $a_n$ **converges** to $a$ if for all $\epsilon \gt 0$ there exists an $N \in \mathbf{N}$ such that if $n \geq N$, then

$$\vert a_n - a \vert \lt \epsilon .$$

In that case $a$ is the **limit** of the sequence, written

$$\lim_{n \to \infty} a_n = a ,$$

and the sequence is **convergent** (≈7:59; notes p. 2). A sequence that is not convergent is **divergent** (≈8:46; notes p. 2). On the board Colding states the condition for little $n$ bigger than capital $N$ (≈6:24, ≈7:11); the notes have $n \geq N$.

**The picture** (≈6:24–7:59). Put $a$ on the real line. Given $\epsilon$, look at the interval from $a - \epsilon$ to $a + \epsilon$ around it. The sequence converges to $a$ if there is some $N$ such that every $a_n$ with $n$ beyond $N$ lands in that interval. And this has to hold for every $\epsilon$: "someone else is allowed to pick the epsilon" (≈7:11), and then you have to prove that there exists a capital $N$ such that from there on all the $a_n$ lie in the little interval (≈7:59).

There are several ways of writing that a sequence converges, with the limit or in words (≈10:31). The notes use $\lim_{n \to \infty} a_n = a$ and, later, $a_n \to a$ (notes pp. 3–4).

## Example: $0.999 \cdots = 1$ (≈8:46–15:23)

**What the left side means** (≈8:46–11:20; notes p. 2). Colding says one thinks of $0.99999 \cdots$ as $1$: "This is indistinguishable from 1" (≈9:35). What is really meant is a sequence,

$$a_1 = 0.9, \quad a_2 = 0.99, \quad a_3 = 0.999, \quad a_4 = 0.9999, \quad \cdots$$

where $a_n$ is zero point followed by $n$ nines (≈9:35). The left side of $0.999999999 \cdots = 1$ is defined as the limit of this sequence (notes p. 2), so the statement to prove is the following.

**Claim** (notes p. 3; ≈10:31–11:20). $\lim_{n \to \infty} a_n = 1$.

**Proof** (notes p. 3; ≈12:07–15:23). We need to show that for every $\epsilon \gt 0$ there is an $N \in \mathbf{N}$ with $\vert a_n - 1 \vert \lt \epsilon$ for $n \geq N$. Given $\epsilon$, choose $N$ with $\frac{1}{N} \lt \epsilon$, which the [Archimedean property](archimedean-property.md) allows (≈12:54). Next,

$$\vert a_n - 1 \vert = 10^{-n} .$$

On the board Colding first says $1 - a_n$ is less than $\frac{1}{10^n}$, since $a_1$ is within $\frac{1}{10}$ of $1$, $a_2$ within $\frac{1}{100}$, and so on, then adds "It's actually equality in this case" (≈13:48–14:36). So for $n \geq N$,

$$\vert a_n - 1 \vert = 10^{-n} \lt \frac{1}{n} \leq \frac{1}{N} \lt \epsilon .$$

That is what had to be proved. □

Colding calls the inequality $10^{-n} \lt \frac{1}{n}$ obvious (≈14:36), and neither the board nor the notes prove it. The shape of the argument is the point: "for your given epsilon, I specify a capital N", and then show that every $a_n$ beyond it is within $\epsilon$ of the limit (≈14:36–15:23).

## A convergent sequence is bounded (≈15:23–26:28)

Colding calls this "the first test for whether a sequence is convergent" (≈15:23).

**Theorem** (notes p. 3; ≈15:23–17:00). If $a_n$ is a convergent sequence, then the set $\lbrace a_n \rbrace = \lbrace a_1, a_2, a_3, \cdots \rbrace$ is a bounded subset of $\mathbf{R}$.

Boundedness is necessary for convergence, not sufficient: "It's not enough to be bounded to be convergent, but it is a necessary criterion" (≈17:00). The sequence $(-1)^n$ takes only two values, so it is bounded, and it does not converge (≈17:00).

**Proof** (notes p. 3; ≈17:47–24:53). Let $a$ be the limit.

1. **One $\epsilon$ is enough.** Apply the definition of convergence with $\epsilon = 1$ only. There is an $N$ such that for $n \geq N$, $\vert a - a_n \vert \lt 1$ (≈17:47–18:53).
2. **The first $N - 1$ terms.** The set $\lbrace a_1, \cdots, a_{N-1} \rbrace$ is finite, so it is bounded: there is a $C \in \mathbf{R}$ with $\vert a_n \vert \leq C$ for $n = 1, \cdots, N - 1$ (≈18:53–20:43). Neither the board nor the notes prove that a finite set is bounded; Colding calls it obvious.
3. **The tail.** For $n \geq N$, write $a_n$ "in a stupid way" as $a_n - a + a$ (≈23:15). The absolute value of a sum is at most the sum of the absolute values (≈24:06), so

$$\vert a_n \vert \leq \vert a \vert + \vert a_n - a \vert \leq \vert a \vert + 1 .$$

4. **Together.** For all $n$,

$$\vert a_n \vert \leq \max\lbrace C, \vert a \vert + 1 \rbrace .$$

□

On the board the conclusion is a claim about a supremum: the $\sup$ of the set of all $\vert a_n \vert$ is at most $\max\lbrace C, \vert a \vert + 1 \rbrace$ (≈21:33–22:22). The notes state the bound for every $n$ instead.

**Questions** (≈23:15, ≈25:43–26:28). A student asked where the $\vert a \vert + 1$ in the maximum comes from; that is step 3. Another asked whether the sup had to be found. Colding: no. The maximum is a bound for the sup, and the sup is presumably smaller. He writes $\sup$ rather than a maximum because "if it's infinitely many numbers, it's not clear there is a maximum" (≈25:43). The $1$ came from the choice $\epsilon = 1$, and "the 1 really, to some extent, could be almost anything" (≈25:43). There is a trade-off, though. A smaller $\epsilon$ would push $N$ further out, and since $C$ is the maximum of the first $N - 1$ terms, $C$ would probably jump up (≈26:28). See [supremum and infimum](supremum-and-infimum.md).

## Algebraic properties of limits (≈24:53–1:03:38)

**Theorem** (notes p. 3, "Basic algebraic properties of limits"; ≈27:14–30:25). Suppose that $a_n$ and $b_n$ are convergent sequences with $\lim a_n = a$ and $\lim b_n = b$, and let $C \in \mathbf{R}$. Then:

1. $c_n = C a_n$ is convergent and $\lim_{n \to \infty} c_n = C a$.
2. $c_n = a_n + b_n$ is convergent and $\lim_{n \to \infty} c_n = a + b$.
3. $c_n = a_n b_n$ is convergent with $\lim_{n \to \infty} c_n = a b$.
4. If $b_n \neq 0$, $b \neq 0$ and $c_n = \frac{a_n}{b_n}$, then $c_n$ is convergent and $\lim_{n \to \infty} c_n = \frac{a}{b}$.

On the board the fourth property is about reciprocals: if every $a_n$ is different from $0$ and the limit $a$ is not $0$, then $c_n = \frac{1}{a_n}$ converges to $\frac{1}{a}$ (≈29:33). The notes state the quotient form, and their outline proves it for $\frac{1}{b_n}$ and says that the general case follows together with the third property (notes p. 4).

Colding's plan: prove the first two "formally, as we talked about last time", and for the third and fourth give something "very, very close to a formal proof but it's more like what you would have on a piece of scrap paper" (≈30:25). None of them is complicated, he says, but the third and fourth contain "a very simple but useful idea" (≈34:33). In the event he wrote out the third proof in full (≈51:53). The notes give full proofs of (1) and (2) and outlines of (3) and (4), with "details to fill in" (notes p. 4). The proofs are collected on [algebraic properties of limits](algebraic-properties-of-limits.md).

### Property 1: a constant multiple (≈31:10–33:35)

**Proof** (notes p. 4). If $C = 0$, every $c_n$ is $0$ and the claim is trivially true, so assume $C \neq 0$ (≈31:10–32:03). Given $\epsilon \gt 0$, do not use $\epsilon$ itself in the definition of $a_n \to a$; use "one that is closely related", the positive number $\frac{\epsilon}{\vert C \vert}$ (≈32:03–32:50). There is an $N$ such that for $n \geq N$,

$$\vert a - a_n \vert \lt \frac{\epsilon}{\vert C \vert} .$$

Multiplying both sides by $\vert C \vert$ gives, for $n \geq N$,

$$\vert C a - C a_n \vert \lt \epsilon ,$$

which is the first property (≈33:35). □

The notes open this proof with "If $c = 0$", in lower case, a [printed slip](../raw/notes/04-sequences-convergence.md#printed-slips) for $C$.

### Property 2: a sum (≈34:33–42:08)

**Proof** (notes p. 4; ≈35:27–40:34). First observe, by the same inequality for absolute values as before, that

$$\vert c_n - (a + b) \vert = \vert (a_n - a) + (b_n - b) \vert \leq \vert a_n - a \vert + \vert b_n - b \vert .$$

Given $\epsilon \gt 0$, use $\frac{\epsilon}{2}$ in each of the two definitions. Since $a_n \to a$, there is an $N_a$ such that $\vert a_n - a \vert \lt \frac{\epsilon}{2}$ for $n \geq N_a$. Since $b_n \to b$, there is an $N_b$, possibly different, such that $\vert b_n - b \vert \lt \frac{\epsilon}{2}$ for $n \geq N_b$ (≈36:17–37:16). Only now choose the $N$ that the definition asks for: $N = \max\lbrace N_a, N_b \rbrace$ (≈37:16–38:08). For $n \geq N$ both inequalities hold, so

$$\vert c_n - (a + b) \vert \leq \vert a_n - a \vert + \vert b_n - b \vert \lt \frac{\epsilon}{2} + \frac{\epsilon}{2} = \epsilon .$$

□

On the board Colding first wrote the difference as $c_n$ minus $a$ times $b$ and corrected it to the sum (≈38:08–38:54). The notes print $\max\lbrace Na, N_b \rbrace$ with the first subscript missing.

**Why $\frac{\epsilon}{2}$ is allowed** (≈40:34–42:08). A student asked what justifies making each difference less than $\frac{\epsilon}{2}$. The answer is that convergence is assumed for every $\epsilon$, so in particular for $\frac{\epsilon}{2}$: "I'm basically using that for all epsilon, that it wasn't just for a fixed epsilon" (≈42:08). The price is a larger $N$: "I will have to choose probably an n that is much larger if I'm using epsilon over 2 than if I use directly the epsilon" (≈41:21). As $\epsilon$ gets smaller, presumably $N$ has to be chosen larger (≈41:21). The student then asked whether this assumes the convergence is smooth rather than oscillating about a point. Colding said "That's right" and repeated that the argument uses the definition for every $\epsilon$; the captions do not show him taking up oscillation as such (≈42:08).

### Property 3: a product (≈42:08–53:24)

**The trick** (≈43:44–45:16). Comparing $a_n b_n$ with $a b$ directly is hard. It gets a lot easier if you compare each with "something that is halfway between this and that" (≈43:44), here $a_n b$: subtract it and add it straight back (≈44:30). Then factor:

$$a b - a_n b_n = (a b - a_n b) + (a_n b - a_n b_n) = b (a - a_n) + a_n (b - b_n),$$

and so (notes p. 4)

$$\vert a b - a_n b_n \vert \leq \vert a b - a_n b \vert + \vert a_n b - a_n b_n \vert = \vert b \vert \thinspace \vert a - a_n \vert + \vert a_n \vert \thinspace \vert b - b_n \vert .$$

(The notes go straight to the inequality; the identity before it is the factoring the board describes.) The term with $\vert b \vert$ "looks like no problem at all because this is just some fixed constant times this difference" (≈45:16). The term with $\vert a_n \vert$ "looks like the problematic one", because $\vert a_n \vert$ is not a fixed constant (≈45:16). This is where the previous theorem comes in. Since $a_n$ converges, the set $\lbrace \vert a_n \vert \thinspace \vert \thinspace n \in \mathbf{N} \rbrace$ is bounded, by some $C$ (≈46:04–46:51; notes p. 4). Then

$$\vert c_n - a b \vert \leq C \vert b_n - b \vert + \vert b \vert \thinspace \vert a_n - a \vert$$

(≈47:38; the captions are garbled at the second term, which is read here from the notes' display).

**The proof on the board** (≈47:38–51:53). This part is not in the notes, which stop at the idea (≈52:38). Given $\epsilon \gt 0$, the aim is to make each term less than $\frac{\epsilon}{2}$. Since $a_n \to a$, there is an $N_a$ such that for $n$ beyond $N_a$,

$$\vert a_n - a \vert \lt \frac{\epsilon}{2 (\vert b \vert + 1)} .$$

Colding uses $\vert b \vert + 1$ rather than $\vert b \vert$ because "I don't want to have something where if b was zero, then it really didn't make any sense what I wrote" (≈49:24). Since $b_n \to b$, there is an $N_b$ such that for $n$ beyond $N_b$,

$$\vert b_n - b \vert \lt \frac{\epsilon}{2 (1 + C)} .$$

$C$ is already non-negative, being at least an absolute value, but he adds $1$ "for the same reason" (≈50:17). For $n$ bigger than the maximum of $N_a$ and $N_b$ both inequalities hold (≈50:17–51:04), and

$$\vert c_n - a b \vert \leq C \frac{\epsilon}{2 (1 + C)} + \vert b \vert \frac{\epsilon}{2 (\vert b \vert + 1)} .$$

The factor $\frac{C}{1 + C}$ is bounded by $1$, so the first term is bounded by $\frac{\epsilon}{2}$, and the second is bounded by $\frac{\epsilon}{2}$ for the same reason. So the whole is bounded by $\epsilon$ when $n$ is bigger than the maximum of $N_a$ and $N_b$ (≈51:04–51:53). □

**The takeaway** (≈53:24–54:10). What Colding wants remembered from this proof is "this little idea about inserting something that was halfway between the two things you were comparing", when they are not easy to compare directly (≈53:24). The same trick proves the Leibniz rule for the derivative of a product of two functions, "and it comes up in various other, more fancy ways" (≈54:10). On the OCW lecture list, derivatives come in Lecture 15, "Derivatives; Laws for Differentiation", which this knowledge base does not yet cover.

### Property 4: a reciprocal (≈54:10–1:03:38)

The board proves the reciprocal form: every $a_n \neq 0$, $a \neq 0$ and $c_n = \frac{1}{a_n}$ (≈54:56). Then

$$\left\vert c_n - \frac{1}{a} \right\vert = \left\vert \frac{1}{a_n} - \frac{1}{a} \right\vert = \frac{\vert a - a_n \vert}{\vert a_n \vert \thinspace \vert a \vert}$$

(≈54:56, ≈1:01:22). The numerator looks very promising, because it goes to $0$; Colding says "denominator" at that moment, a slip of the tongue (≈55:42). The worry is the denominator. To bound the fraction from above, the denominator has to be bounded from below, and since $a$ is a fixed number that is not $0$, that means bounding $\vert a_n \vert$ from below. It need not hold for every $n$, only for $n$ sufficiently large (≈55:42–56:33).

**Bounding $\vert a_n \vert$ from below** (≈57:20–1:00:36). Colding first wrote $\vert a_n \vert \leq \vert a_n - a \vert + \vert a \vert$, said "this was not how I wanted to write it", and did "the symmetric thing" (≈57:20): write $a = (a - a_n) + a_n$, so that

$$\vert a \vert \leq \vert a - a_n \vert + \vert a_n \vert , \quad\text{that is,}\quad \vert a \vert - \vert a - a_n \vert \leq \vert a_n \vert$$

(≈58:05). Because $a \neq 0$, the number $\frac{\vert a \vert}{2}$ is positive, so it can be used as the $\epsilon$ in the definition of $a_n \to a$ (≈58:56). There is an $N_1$, "not the final N that we want to use", such that for $n$ bigger than $N_1$, $\vert a - a_n \vert \lt \frac{\vert a \vert}{2}$ (≈59:50). Then the subtracted term is at most half of $\vert a \vert$, and

$$\vert a_n \vert \gt \frac{\vert a \vert}{2}$$

(≈1:00:36). So $\vert a_n \vert$ is bounded away from $0$.

**Finishing** (≈1:01:22–1:02:53). For $n$ bigger than $N_1$,

$$\left\vert c_n - \frac{1}{a} \right\vert \leq \frac{2 \vert a - a_n \vert}{\vert a \vert^2} ,$$

since the denominator is at least $\vert a \vert \cdot \frac{\vert a \vert}{2}$ and "the 2 jumps up" (≈1:02:08). As $a$ is a constant, going even further out than $N_1$ makes the right side smaller than a given $\epsilon$ (≈1:02:53). "At this point, that's not very much to fill in" (≈1:02:53). □

**The notes' outline** (notes p. 4) does the same with $b_n$ and $b$. It assumes $a_n = 1$, uses

$$\frac{1}{b_n} - \frac{1}{b} = \frac{\vert b - b_n \vert}{\vert b \vert \thinspace \vert b_n \vert} ,$$

which is printed without absolute value bars on the left (a [printed slip](../raw/notes/04-sequences-convergence.md#printed-slips)), and goes from $\vert b_n \vert \leq \vert b \vert + \vert b_n - b \vert$ to $\vert b_n \vert \geq \vert b \vert - \vert b_n - b \vert$, which it uses to bound the denominator from below for $n$ sufficiently large. It does not choose $\frac{\vert b \vert}{2}$ or finish the bound: "there are details to fill in but these are the main ideas".

## Subsequences (≈1:03:38–1:11:01)

Colding gives examples first and the formal definition after (≈1:03:38). For the subsequence he uses a new index, $k$, which "plays the same role as n before", so as not to confuse it with the $n$ of the original sequence (≈1:04:28).

**Examples from $a_n = (-1)^n$** (≈1:04:28–1:06:05; notes p. 5, Example 1).

- The sequence that is $1$ for all $k$ is a subsequence: it takes all the even-numbered terms (≈1:05:15).
- Taking all the odd-numbered terms gives another subsequence, constantly $-1$ (≈1:05:15).
- Something more elaborate: take the first two odd-numbered terms, then the next two even-numbered ones, then the next two odd ones, and so on, so that $b_1 = -1$, $b_2 = -1$, then two $1$'s (≈1:05:15–1:06:05).

The notes list $b_n = 1$ for all $n$, $c_n = -1$, $c_n = (-1)^{n+1}$, and the pattern $1, 1, -1, -1, 1, 1, -1, -1, \cdots$ (notes p. 5).

**Examples from $a_n = n$** (≈1:06:53; notes p. 5, Example 2). The odd numbers $1, 3, 5, 7, 9, \cdots$ form a subsequence, and so do the even numbers $2, 4, 6, 8, 10, \cdots$.

**Non-examples** (≈1:07:40–1:08:28).

- Repeating a term. A sequence that starts $1, 1, 2, \cdots$ is not a subsequence of $a_n = n$, "because what you have done here is that you have taken the same number several times", and the value does not appear several times in the original (≈1:07:40). The notes' example is $1, 1, 2, 2, 3, 3, 4, 4, 5, 5 \cdots$, which "is NOT" a subsequence (notes p. 5). The captions are unclear about the board's digits.
- Taking terms out of order. $3, 2, 4, 5, \cdots$ is not a subsequence either, "because things are taken out of order" (≈1:08:28). This example is only on the board.

**Definition** (notes p. 5; ≈1:08:28–1:11:01). A sequence $a_n$ is a function $f : \mathbf{N} \to \mathbf{R}$ with $a_n = f(n)$. A **subsequence** of $a_n$ is the composition $f \circ g$, where $g : \mathbf{N} \to \mathbf{N}$ is strictly increasing. On the board it is written $b_k = f(g(k))$; the notes write $b_n = f(g(n))$. A subsequence of $a_n$ is also denoted $a_{n_k}$ (≈1:11:01; notes p. 5).

Strictly increasing is what rules out the non-examples. The first term of a subsequence can be any term of the original, "but once you have fixed the first one, you can't look back": the next element has to be further out in the sequence, and so on (≈1:10:15).

## Convergence and subsequences (≈1:11:01–1:18:13)

**Theorem** (notes p. 5; ≈1:11:48). A sequence $a_n$ is convergent with limit $a$ if and only if all subsequences of $a_n$ are also convergent with limit $a$.

"It's a very simple fact. But it is sometimes a useful fact" (≈1:11:01).

**Proof** (notes pp. 5–6; ≈1:12:37–1:16:38). It is an "if and only if", so there are two implications (≈1:12:37).

- **First implication.** If every subsequence converges to $a$, so does $a_n$. This one is trivial, because $a_n$ is a subsequence of itself (≈1:12:37–1:14:14). Take $g$ to be the identity, $g(k) = k$, which is strictly increasing. Then the subsequence is just the original sequence (≈1:13:25).
- **Second implication.** If $a_n$ converges to $a$, so does every subsequence $a_{n_k}$ (≈1:14:14–1:16:38). Given $\epsilon \gt 0$, choose $N$ so large that $\vert a_n - a \vert \lt \epsilon$ for $n \geq N$. Here $n_k$ is the value of the strictly increasing function at $k$, and because the function is strictly increasing, $n_k \geq k$ (≈1:15:51). So for $k \geq N$ we have $n_k \geq k \geq N$, and therefore

$$\vert a_{n_k} - a \vert \lt \epsilon .$$

□

Neither the board nor the notes prove that $n_k \geq k$ for a strictly increasing $g$. The board states it as a consequence of strictly increasing (≈1:15:51); the notes use it without comment.

**How it is used** (≈1:16:38–1:17:28). Contrapositively: if a sequence has a subsequence that does not converge, or two subsequences that converge to different limits, then the original sequence does not converge either (≈1:17:28).

**Questions** (≈1:17:28–1:18:13). Could a convergent subsequence be finite, ending before it reaches the point where the terms settle down? Colding's answer has two parts. "Convergence is always something about the tail, about the end": it never cares about what happened in the beginning, so there may be finitely many $n$ at the start "where things are crazy" (≈1:17:28). And every sequence, subsequences included, is infinite, because $g$ has to be a map from all of $\mathbf{N}$ to $\mathbf{N}$, so each $k$ gives a term (≈1:18:13). The lecture ends there.

## Board versus notes

Where they differ, this page follows the notes and gives the board's version with its timestamp. Collected here:

- **The index condition.** Board: for little $n$ bigger than capital $N$ (≈6:24, ≈18:53, ≈1:15:02). Notes: $n \geq N$ throughout (pp. 2–6).
- **$1 - a_n$ for $0.999 \cdots$.** Board: first "less than" $\frac{1}{10^n}$, then corrected to equality (≈13:48–14:36). Notes: $\vert a_n - 1 \vert = 10^{-n}$ (p. 3).
- **Boundedness.** Board: the $\sup$ of all $\vert a_n \vert$ is at most $\max\lbrace C, \vert a \vert + 1 \rbrace$ (≈21:33). Notes: $\vert a_n \vert \leq \max\lbrace C, \vert a \vert + 1 \rbrace$ for all $n$ (p. 3).
- **The fourth property.** Board: $\frac{1}{a_n} \to \frac{1}{a}$ when every $a_n \neq 0$ and $a \neq 0$ (≈29:33). Notes: $\frac{a_n}{b_n} \to \frac{a}{b}$ when $b_n \neq 0$ and $b \neq 0$, outlined for $\frac{1}{b_n}$ (pp. 3–4).
- **How much is proved.** Board: the third property is proved in full, with $\frac{\epsilon}{2(\vert b \vert + 1)}$ and $\frac{\epsilon}{2(1 + C)}$ (≈47:38–51:53), and the fourth is carried as far as $\frac{2 \vert a - a_n \vert}{\vert a \vert^2}$ (≈1:02:08). Notes: outlines of both (p. 4).
- **The lower bound for the denominator.** Board: chooses $\frac{\vert a \vert}{2}$ as $\epsilon$ and gets $\vert a_n \vert \gt \frac{\vert a \vert}{2}$ beyond $N_1$ (≈58:56–1:00:36). Notes: stop at $\vert b_n \vert \geq \vert b \vert - \vert b_n - b \vert$ (p. 4).
- **Subsequence examples.** Board: first two odd-numbered terms, then the next two even ones, starting $-1, -1$ (≈1:05:15–1:06:05); the out-of-order $3, 2, 4, 5, \cdots$ (≈1:08:28). Notes: $1, 1, -1, -1, \cdots$ and $1, 1, 2, 2, 3, 3, \cdots$ (p. 5).
- **The subsequence index.** Board: $b_k = f(g(k))$ (≈1:10:15). Notes: $b_n = f(g(n))$ (p. 5).

## Where the lecture stops

The course now has convergence, its first consequences (boundedness, the algebraic properties, subsequences), and a worked proof with $\epsilon$ and $N$. Lecture 3's notes asked "When does a limit exist?", and so far the course has only a necessary condition: a convergent sequence is bounded. [Lecture 5](05-monotone-convergence-theorem.md), "Monotone Convergence Theorem" (TBB Sections 2.8, 2.9 and 2.11), gives the first sufficient one: a bounded monotone sequence converges. On the OCW lecture list, Lecture 6 is "Cauchy Convergence Theorem" (TBB Section 2.12), which is not in this knowledge base yet.

## Related pages

- [Sequences and limits](sequences-and-limits.md): the definition of a sequence, convergence, divergence and the examples, across Lectures 3 and 4.
- [Algebraic properties of limits](algebraic-properties-of-limits.md): the four properties with their proofs, and the halfway trick.
- [Subsequences](subsequences.md): examples, non-examples, the definition, and the theorem that subsequences of a convergent sequence converge to the same limit.
- [The Archimedean property](archimedean-property.md): used here to choose $N$ with $\frac{1}{N} \lt \epsilon$.
- [Supremum and infimum](supremum-and-infimum.md): the $\sup$ in the boundedness theorem.
- [Writing proofs](writing-proofs.md): formal proofs versus scrap-paper outlines, and how a proof with $\epsilon$ and $N$ is laid out.
- [Lecture 3 — How to Write a Proof; Archimedean Property](03-how-to-write-a-proof-archimedean-property.md): the previous lecture, which defined a sequence.
- [Lecture 5 — Monotone Convergence Theorem](05-monotone-convergence-theorem.md): the next lecture.
