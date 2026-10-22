# Lecture 5 — Monotone Convergence Theorem

**18.100B Real Analysis, Spring 2025 · Tobias Holck Colding · [video](https://www.youtube.com/watch?v=EjXtpzysDL4) (79 min)**

Sources for this page: the [edited transcript](../raw/transcripts/05-monotone-convergence-theorem.md) (timestamps below are written ≈M:SS and point into it), the course's typed [lecture notes](../raw/notes/05-monotone-convergence-theorem.md) for this lecture (cited "notes p. N"; [PDF on OCW](https://ocw.mit.edu/courses/18-100b-real-analysis-spring-2025/mit18_100b_s25_lec05.pdf)), and the OCW readings list, which assigns Sections 2.8, 2.9 and 2.11 of Thomson, Bruckner and Bruckner, *Elementary Real Analysis* (TBB) to this lecture. Colding teaches from the blackboard; there are no slides.

## What this lecture establishes

Lecture 4 proved that a convergent sequence is bounded, which is only a necessary condition for convergence. This lecture gives the first condition that guarantees a limit exists. A sequence is **monotone increasing** if each term is at least the one before it, and **monotone decreasing** if each term is at most the one before it (≈16:07–16:54; notes p. 2). The **monotone convergence theorem** says that a monotone increasing sequence that is bounded from above converges, and its limit is the supremum of its terms; a monotone decreasing sequence that is bounded from below converges to the infimum of its terms (≈17:43–21:51; notes p. 2). The proof uses that the supremum is the *least* upper bound (≈34:28–41:49; notes p. 5).

The theorem is then used to make precise the old picture of $\sqrt{2}$ as the limit of $1$, $1.4$, $1.41$, $1.414$, …: Colding defines the sequence of decimal approximations exactly, shows that it is increasing and bounded by $2$, and proves that the square of its limit is $2$, using the algebraic rules for limits (≈41:49–1:06:36; notes pp. 3–4). Along the way he shows how to build two monotone sequences out of *any* bounded sequence, by taking the supremum and the infimum of its tails, which he says is how limsup and liminf are defined and which will be used for Cauchy sequences (≈21:51–33:39, ≈1:07:23–1:08:10; on the board only). The lecture ends by defining **Cauchy sequences** and **contracting maps** and stating, without proof, that a sequence of real numbers converges if and only if it is Cauchy, and that a contracting map has a fixed point (≈1:08:10–1:17:53; notes p. 6). Both proofs are promised for next time.

Notation: as in the earlier lectures, the notes set the number systems in bold, $\mathbf{N}$ and $\mathbf{R}$, and this page follows them. In this course $\mathbf{N} = \lbrace 1, 2, 3, \cdots \rbrace$ starts at $1$. A sequence is written $a_n$, $\vert x \vert$ is the absolute value of $x$, and $\sup$ and $\inf$ are the least upper bound and the greatest lower bound (see [supremum and infimum](supremum-and-infimum.md)). The letter $b_n$ is used for three different sequences in this lecture: the numerator in the first example, the suprema of the tails of a bounded sequence, and the integers in the $\sqrt{2}$ construction. Each section below says which one it means.

## Review: sequences, subsequences, convergence, the algebraic rules (≈0:00–7:20)

Colding opens by recalling Lecture 4's definitions (notes p. 1 repeats them). A **sequence** is a map from $\mathbf{N}$ into $\mathbf{R}$, and the image of $n$ is usually written $a_n$ (≈0:00). A **subsequence** comes from a second map $g : \mathbf{N} \to \mathbf{N}$, which has to be strictly increasing, and is the composition of the two maps, written $a_{n_k}$ (≈0:47–2:21). He says why the map must be strictly increasing: the subsequence should keep the terms "in the same order than it was in the original sequence", and no term should be "picked more times than it was in the original sequence" (≈2:21–3:10). And he says what $n_k$ is: "n k, really, you should think about it as g of k" (≈2:21). The notes write the subsequence as $b_k = f(g(k))$, where $f$ is the sequence, and say "We often write $a_{n_k}$ for $b_k$" (notes p. 1). See [subsequences](subsequences.md).

**Convergence** (≈3:10–4:50; notes p. 1). The sequence $a_n$ converges to $a$ if for all $\epsilon \gt 0$ there exists an $N$ such that if $n \geq N$, then

$$\vert a_n - a \vert \lt \epsilon .$$

The limit $a$ "is another real number. It's not infinity" (≈3:10). A sequence that is not convergent is divergent (≈4:50). The notes also restate, without proof, that a convergent sequence is bounded (notes p. 1). See [sequences and limits](sequences-and-limits.md).

**The algebraic rules** (≈4:50–7:20; notes p. 1). If $a_n \to a$ and $b_n \to b$, then the sum, a constant multiple and the product converge to the sum, the constant multiple and the product of the limits; and if $a_n \neq 0$ for all $n$ and $a \neq 0$, then $\frac{1}{a_n} \to \frac{1}{a}$ (≈6:29–7:20). On the board the sum is rule 1 and the constant multiple rule 2, and Colding says "I think I might have exchanged the order of 1 and 2 last time" and that there is no particular convention (≈7:20). The notes keep Lecture 4's order, constant multiple first, and state the fourth rule for a reciprocal: if $b_n \neq 0$, $b \neq 0$ and $c_n = \frac{1}{b_n}$, then $c_n \to \frac{1}{b}$ (notes p. 1). The Lecture 4 notes had stated it for a quotient $\frac{a_n}{b_n}$. See [algebraic properties of limits](algebraic-properties-of-limits.md).

## Example: a sequence of quotients (≈7:20–13:46)

**Claim** (notes p. 2; ≈7:20). The sequence

$$a_n = \frac{n^2 + 1}{n^2 + n + 1}$$

converges with limit $1$. For each $n$ the term is a rational number, "but it's a real number" (≈8:10).

**Proof on the board** (≈8:10–13:00). Factor $n^2$ out of the numerator and the denominator and cancel it (≈8:10), so that

$$a_n = \frac{1 + \frac{1}{n^2}}{1 + \frac{1}{n} + \frac{1}{n^2}}$$

(notes p. 2). Colding then names the pieces: $x_n = \frac{1}{n}$, $y_n = \frac{1}{n^2}$, and $z_n = 1$, the constant sequence (≈9:00–9:48).

1. $\frac{1}{n} \to 0$, which "essentially just follows from the Archimedean property. But we've already seen this" (≈9:00). The same holds for $\frac{1}{n^2}$ (≈9:00); this is asserted, not proved. The constant sequence $z_n = 1$ obviously converges to $1$ (≈9:48). See [the Archimedean property](archimedean-property.md).
2. The numerator $b_n = z_n + y_n$ converges to $1 + 0 = 1$ by the rule for sums (≈9:48–10:36).
3. The denominator $c_n = z_n + x_n + y_n$ converges to $1 + 0 + 0 = 1$, again by the rule for sums (≈10:36–11:24).
4. Every $c_n$ is strictly positive, so none is $0$, and the limit $1$ is not $0$ either. So the fourth rule applies, and $\frac{1}{c_n} \to \frac{1}{1} = 1$ (≈11:24–12:10).
5. Finally $a_n = b_n \cdot \frac{1}{c_n}$, and by the third rule, for products, it converges to $1 \cdot 1 = 1$ (≈12:10–13:00). □

The notes compress steps 1 to 5 into "Since $\frac{1}{n} \to 0$ and $\frac{1}{n^2} \to 0$", the two limits $1 + \frac{1}{n^2} \to 1$ and $1 + \frac{1}{n} + \frac{1}{n^2} \to 1$, and "It now follows from the algebraic properties of limits that" $a_n \to 1$ (notes p. 2). A sequence is often expressed through functions like this, Colding says, and "you do this reduction"; it is the first time students see it, "but you know in a couple of weeks this will feel too easy" (≈13:00–13:46).

## Why monotone sequences (≈13:46–16:07)

The course has already defined $\sqrt{2}$ and shown it is a real number, from the completeness of the reals (≈14:33; see [the square root of 2](square-root-of-2.md)). "But we also, in the back of our mind", already had a picture of it: "when you think about square root of 2, at least I think about square root of 2, I think about it as 1.4", then $1.414$ and so on, because it cannot be expressed as a fraction (≈14:33–15:20). To make that picture precise, "we want to look at particular sequences, what's called monotone sequences" (≈15:20). The notes put the same point this way: to show that $\sqrt{2}$ is the limit of $a_1 = 1$, $a_2 = 1.4$, $a_3 = 1.41$, $a_4 = 1.414$, …, "we need something else. We need the monotone convergence theorem" (notes p. 2).

## Monotone sequences (≈16:07–17:43)

**Definition** (notes p. 2; ≈16:07–16:54). A sequence $a_n$ is **monotone increasing** if for all $n$

$$a_n \leq a_{n+1} ,$$

that is, $a_1 \leq a_2 \leq a_3 \leq \cdots$: "the next element is larger or equal to the previous element" (≈16:07). It is **monotone decreasing** if for all $n$

$$a_{n+1} \leq a_n$$

(≈16:54; notes p. 2). Some people also speak of a *strictly* monotone increasing sequence, where the inequality has to be strict (≈16:07–16:54).

## The monotone convergence theorem (≈17:43–21:51)

**Theorem** (notes p. 2; ≈17:43–21:51). There are two versions.

- **Increasing version.** Let $a_n$ be a monotone increasing sequence that is bounded from above, so that there exists $A$ with $a_n \leq A$ for all $n$. Then $a_n$ is convergent, with limit

$$\lim_{n \to \infty} a_n = \sup \lbrace a_n \rbrace .$$

- **Decreasing version.** Let $a_n$ be a monotone decreasing sequence that is bounded from below. Then $a_n$ converges, and

$$\lim_{n \to \infty} a_n = \inf \lbrace a_n \rbrace .$$

Colding states the increasing version and calls the decreasing one "kind of obviously a parallel" (≈18:29). For an increasing sequence only the upper bound has to be assumed: "Any monotone increasing sequence is clearly bounded from below because already the first element is a lower bound" (≈19:21). He sums it up as "if you have a monotone increasing sequence that is bounded, then it's also convergent. And likewise, if you have a monotone decreasing sequence that is bounded from below, then it is also convergent" (≈20:14). The notes call the bound $A$ and say "bounded" in the decreasing version (notes p. 2); on the board the captions write the bound as "a", which cannot be told apart from the limit in speech, and in the proof Colding sets "little a" equal to the sup (≈35:17).

## Two monotone sequences from any bounded sequence (≈21:51–33:39)

This part is on the board only; the notes have nothing corresponding to it.

"you may say that this seems rather special. If you take a random sequence, obviously, it's not going to be monotone" (≈21:51). But any bounded sequence produces two monotone ones (≈22:36). Let $a_n$ be bounded, that is, bounded from above and from below. For each $n$, take the supremum and the infimum of the terms from $a_n$ onwards:

$$b_n = \sup \lbrace a_n, a_{n+1}, a_{n+2}, \cdots \rbrace , \qquad c_n = \inf \lbrace a_n, a_{n+1}, a_{n+2}, \cdots \rbrace$$

(≈23:24–24:10). These are real numbers because the set of all the $a_n$ is bounded (≈23:24).

**$b_n$ is decreasing** (≈24:10–25:48). For example $b_3 = \sup \lbrace a_3, a_4, \cdots \rbrace$ and $b_2 = \sup \lbrace a_2, a_3, a_4, \cdots \rbrace$. Colding first says $b_3$ is bigger than or equal to $b_2$ and corrects himself: $b_2$ is the sup over a larger set, since it also includes $a_2$, so $b_2 \geq b_3$ (≈24:10–25:03). The same argument gives $b_n \geq b_{n+1}$ for every $n$ (≈25:48). So $b_n$ is a monotone decreasing sequence that is bounded (≈27:19–28:08); Colding writes this with a standard shorthand that the captions do not record (≈27:19).

**$c_n$ is increasing** (≈28:08–28:56). $c_{n+1}$ is the infimum over the same terms except $a_n$, so over fewer elements, and it cannot be smaller: $c_{n+1} \geq c_n$. So $c_n$ is monotone increasing and bounded.

**$c_n \leq b_n$** (≈29:46–31:21). For the same $n$, both are taken over the same set, one as the sup and one as the inf, "so of course b n is bigger or equal to c n" (≈29:46). Comparing a term of one sequence with a term of the other at a different index is "a priori" less clear (≈28:56–29:46). Colding draws the picture: $c_1$ to the left of $b_1$ on the line, the $c_n$ moving right and the $b_n$ moving left, with $c_2$ to the right of $c_1$ but to the left of $b_2$, so that "the c n will always lie to the left of the b n's" (≈30:31–31:21). The captions of this passage include a false start (≈30:31), so how he compared different indices is not fully recoverable.

**The limits** (≈32:08–33:39). By the monotone convergence theorem, which at that point had not yet been proved, $b_n$ converges downwards to a limit $b$ and $c_n$ converges upwards to a limit $c$ (≈32:08). "And we'll prove this later, but it seems probably pretty obvious that the limit here, c is less than or equal to b" (≈32:54). This construction "will play an important role when we prove the basic theorem about Cauchy sequences" (≈32:54). Near the end of the lecture he adds that "this is how one defines limsup and liminf", which the course has not yet talked about (≈1:07:23–1:08:10). On the OCW lecture list those come in Lecture 9, "Limsup and Liminf; Power Series; Continuous Functions; Exponential Function", which is not yet in this knowledge base.

**Question** (≈25:48–27:19). A student asked what happens if the sequence is monotone increasing. Then, Colding said, the construction "becomes very special": every $b_n$ would just be the limit $a$ from before, so the sequence of $b_n$ "would be a constant sequence. And it would be just the limit" (≈26:33). The student added that the inequality still holds then, and he agreed: "Yeah, definitely, because it's just constant, exactly". It is a good example, "but it's just kind of almost like too simple" (≈26:33–27:19).

**The takeaway** (≈32:54–33:39). There is the concept of a monotone increasing or decreasing sequence; if such a sequence is bounded, it is convergent; and for any bounded sequence there is "a very natural monotone increasing sequence and a very natural monotone decreasing sequence" (≈33:39).

## Proof of the monotone convergence theorem (≈33:39–41:49)

Colding proves the increasing version only, "because the other one is just the same with obvious modifications" (≈34:28). The notes do the same: "The decreasing version is proven similarly" (notes p. 5).

**Proof** (notes p. 5; ≈34:28–41:49). Suppose

$$a_n \leq a_{n+1} \leq A$$

for all $n$, and set

$$a = \sup \lbrace a_n \rbrace .$$

We want to show that $a_n \to a$ (≈35:17).

1. **$a$ is an upper bound.** The sup of a set is its smallest upper bound, so in particular it is an upper bound, and $a_n \leq a$ for all $n$ (≈36:10–37:00). "It's actually the smallest upper bound. But for this you just need it's an upper bound" (≈37:00). So $a - a_n \geq 0$, and no absolute value is needed: given $\epsilon \gt 0$, it is enough to find an $N$ such that $a - a_n \lt \epsilon$ for $n \geq N$ (≈37:47–38:32).
2. **$a$ is the least upper bound.** "Now I'm going to use that as the least upper bound" (≈38:32). Since $a - \epsilon \lt a$, the number $a - \epsilon$ is not an upper bound for the sequence. So there exists an $N$ with

$$a_N \gt a - \epsilon$$

(≈39:32; notes p. 5). On the board Colding first says "bigger or equal" and then writes it strictly (≈39:32).

3. **The tail.** Since the sequence is increasing, for $n \geq N$,

$$a - \epsilon \lt a_N \leq a_n \leq a ,$$

where the last inequality uses that $a$ is an upper bound (≈40:17; notes p. 5). On the line, all the $a_n$ from $a_N$ outwards lie between $a - \epsilon$ and $a$: "they're squished in this little interval" (≈40:17–41:03). So for $n \geq N$,

$$0 \leq a - a_n \lt \epsilon ,$$

and the sequence converges with limit $a$ (≈41:03; notes p. 5). □

For a decreasing sequence that is bounded from below, "the proof with obvious changes is the same", with the inf in place of the sup (≈41:03–41:49). The proof takes for granted that $\sup \lbrace a_n \rbrace$ exists; neither the board nor the notes name the property that guarantees it. It is the completeness of $\mathbf{R}$ from Lecture 2, every bounded non-empty subset has a least upper bound, which the Lecture 4 notes restate (Lecture 4 notes p. 1). See [completeness and the least upper bound property](least-upper-bound-property.md).

## $\sqrt{2}$ as the limit of its decimals (≈41:49–1:07:23)

"The way to just get an idea about how large it is, you think about it as 1 and then a number of digits afterwards. That's a kind of approximation. So let's try to make this more precise" (≈41:49).

### The two sequences (≈42:47–47:46)

Here $b_n$ is a sequence of integers and $a_n$ the sequence of real numbers built from it (notes p. 3; ≈42:47–47:00). Let $b_n$ be the largest integer such that

$$b_n^2 \leq 2 \cdot 10^{2n-2} ,$$

and let

$$a_n = \frac{b_n}{10^{n-1}} .$$

On the board $b_n$ is "the largest natural number" with this property (≈45:14); the notes say "the largest integer" (notes p. 3). The natural numbers whose squares are at most $2 \cdot 10^{2n-2}$ form a finite set, Colding says, so $b_n$ is just its maximum (≈46:08). It is really $a_n$ that we are interested in, "But b n is going to be a useful tool here", and it is simple because it is just a natural number (≈44:28–45:14).

For $n = 1$ the exponent is $0$, and $10^0 = 1$ "by definition" (≈43:34). So $b_1$ is the largest natural number whose square is at most $2$, which is $1$, and $a_1 = b_1 = 1$ (≈47:00). The notes describe the sequence as $a_1 = 1$, $a_2 = 1.4$, $a_3 = 1.41$, $a_4 = 1.414$, … (notes p. 3). Colding explains the idea behind the definition: "the n is referring to the number of digits, but including the digits that is before the point" (≈53:26), so that $a_n$ takes "the number of digits in square root of 2, including the 1, the starting 1" (≈55:47). Neither the board nor the notes check $a_2$, $a_3$, $a_4$ against the definition.

The plan (notes p. 3): show that $a_n$ is increasing and bounded, so that it converges by the monotone convergence theorem, and that its limit $a$ has $a^2 = 2$.

### $a_n$ is increasing (≈47:46–53:26)

**Scrap paper first** (≈47:46–51:05). To show $a_n \leq a_{n+1}$, write out what it says:

$$\frac{b_n}{10^{n-1}} \leq \frac{b_{n+1}}{10^{n}} .$$

Multiplying both sides by $10^n$ turns it into

$$10 \thinspace b_n \leq b_{n+1} ,$$

and that is what has to be proved (≈48:32–50:18). Colding misspeaks the exponent of $a_n$'s denominator once, as "n minus 2" (≈48:32). He uses this to make a point about writing: "if I was to write it down, I would probably have some of this on scrap paper. And then I would instead establish this here first, and then say, therefore, and then I'll conclude why. But of course, that's not the way you're thinking about it. You first try to analyze what you have to prove. And then once you know that, then you try to write it down nicely" (≈50:18–51:05). See [writing proofs](writing-proofs.md).

**The proof** (notes p. 3; ≈51:05–53:26). By the definition of $b_n$, $b_n^2 \leq 2 \cdot 10^{2n-2}$. The number $10 \thinspace b_n$ is still an integer, and

$$(10 \thinspace b_n)^2 = 100 \thinspace b_n^2 \leq 2 \cdot 10^{2n} = 2 \cdot 10^{2(n+1)-2}$$

(≈51:50; the captions garble the last form). So $10 \thinspace b_n$ is an integer whose square is at most $2 \cdot 10^{2(n+1)-2}$, and $b_{n+1}$ is the largest such integer. Therefore $b_{n+1} \geq 10 \thinspace b_n$ (≈52:36–53:26), so $a_{n+1} \geq a_n$ and the sequence is increasing (notes p. 3). The notes give the middle inequality with "obviously".

### $a_n$ is bounded (≈54:12–55:47)

To bound $a_n$, bound $b_n$ (≈54:12). Take the integer $2 \cdot 10^{n-1}$ and square it:

$$(2 \cdot 10^{n-1})^2 = 4 \cdot 10^{2n-2} \gt 2 \cdot 10^{2n-2} .$$

So this number "would not be allowed as a b n. In fact, it would be larger than b n" (≈54:57). Hence $b_n \leq 2 \cdot 10^{n-1}$, and

$$a_n = \frac{b_n}{10^{n-1}} \leq 2$$

(≈54:57; notes p. 3). Neither the board nor the notes say why an integer whose square is too large must be larger than $b_n$. The notes print the reason as $(2 \cdot 10^{2n-2})^2 \gt 2 \cdot 10^{2n-2}$, with the exponent of the claim on the same line replaced; it is listed as a [printed slip](../raw/notes/05-monotone-convergence-theorem.md#printed-slips). So $a_n$ is increasing and bounded, and by the monotone convergence theorem it converges to some $a$ (≈56:56; notes p. 3).

### $a^2 \leq 2$ (≈56:56–1:00:19)

For each $n$,

$$a_n^2 = \frac{b_n^2}{10^{2n-2}} \leq 2$$

(≈57:51; notes p. 4 writes it as $a_n^2 \thinspace 10^{2n-2} = b_n^2 \leq 2 \cdot 10^{2n-2}$). By the rule for products, the sequence $a_n \cdot a_n$ converges to $a^2$ (≈58:38; notes p. 4). "And this thing here, because each of these squares here, each of them is less than or equal to 2, then the limit must be less than or equal to 2" (≈58:38). So $a^2 \leq 2$. That a limit keeps an inequality satisfied by every term is used here without proof, in the lecture and in the notes alike; earlier in the lecture Colding says of a similar fact, "we'll prove this later" (≈32:54).

"This is one more proof that square root of 2 is a real number. But this is in a way how you think about it, in terms of the decimals" (≈59:33).

### $a^2 \geq 2$ (≈1:00:19–1:05:47)

Since $a^2 \leq 2$ is proved, it is enough to show $a^2 \geq 2$ (≈1:00:19). The first half did not use the definition fully: "I didn't really use that ... b n was the largest such number" (≈1:01:05). Now it is used. Because $b_n$ is the largest integer with $b_n^2 \leq 2 \cdot 10^{2n-2}$, the next integer fails:

$$(b_n + 1)^2 \gt 2 \cdot 10^{2n-2}$$

(≈1:01:05; notes p. 4). Divide by $10^{2n-2}$, written as $10^{n-1} \cdot 10^{n-1}$, and split the fraction (≈1:01:54–1:03:28):

$$\left( a_n + 10^{1-n} \right)^2 = \frac{(b_n + 1)^2}{10^{2n-2}} \gt 2$$

(notes p. 4). On the board the extra term is written $\frac{1}{10^{n-1}}$ (≈1:02:42), and once, a little later, it is spoken as "1 over 10 to the n" (≈1:04:13). This sequence goes to $0$, so by the rule for sums $a_n + 10^{1-n}$ goes to $a + 0 = a$, and by the rule for products its square goes to $a^2$ (≈1:04:13–1:04:58). That $10^{1-n} \to 0$ is asserted, not proved. Since the inequality holds for each term, it holds for the limit, "except you have to be a little bit careful-- it may not be strict inequality, but just bigger or equal to" (≈1:04:58):

$$2 \leq \lim_{n \to \infty} \left( a_n + 10^{1-n} \right)^2 = \lim_{n \to \infty} a_n^2 = a^2$$

(notes p. 4). Together with $a^2 \leq 2$, this gives $a^2 = 2$ (≈1:04:58). □

"It sounds maybe a little bit convoluted. But it's really writing down precisely what you think about when you're thinking about a square root of 2 because you're thinking about the number of digits" (≈1:04:58–1:05:47). It was "a little illustration of how the monotone convergence theorem works" (≈1:05:47). See [the square root of 2](square-root-of-2.md) for the course's other proofs that $\sqrt{2}$ is real.

### Question: strict and non-strict (≈1:06:36–1:07:23)

A student asked whether the inequality is strict, $\gt 2$, for each term but only $\geq 2$ at the end because $a$ and $a^2$ are limits. Colding agreed: each element of the product sequence is strictly bigger than $2$, "But it doesn't necessarily mean that the limit is strictly", because the terms "could kind of approach 2. And that's exactly what happened, of course" (≈1:07:23). In this answer he twice misspeaks: he says the sum $a_n + 10^{1-n}$ "converges to 0" where he means $a$ (≈1:06:36), and that the limit "has to be bigger than 2" where he means bigger than or equal to (≈1:07:23).

## Looking ahead: limsup and liminf (≈1:07:23–1:08:10)

Colding comes back to the construction of $b_n$ and $c_n$ from a bounded sequence: "This is how one defines limsup and liminf. We haven't talked about those yet. It's also going to be used to prove an important theorem, really important theorem", which he states next (≈1:07:23–1:08:10). The lecture does not define limsup or liminf.

## Cauchy sequences (≈1:08:10–1:12:08)

**Why** (≈1:08:10–1:08:56). For a monotone sequence the limit can be written down explicitly, and in the examples so far it was easy to write down the limits. "But in general, you might not be able to write down the limit, but you want to prove that the limit exists" (≈1:08:56). That is where the next notion becomes handy.

**Definition** (notes p. 6; ≈1:08:56–1:09:45). A sequence $a_n$ is a **Cauchy sequence** if for all $\epsilon \gt 0$ there exists an $N$ such that if $m, n \geq N$, then

$$\vert a_n - a_m \vert \lt \epsilon .$$

On the board the condition is that $n$ and $m$ are bigger than $N$ (≈1:09:45).

**How it differs from convergence** (≈1:09:45–1:10:32). "This is a different notion than convergence." Convergence says that everything far out "accumulates around the limit"; a Cauchy sequence is one where, if you are far out, "things bunch together, basically" (≈1:10:32). The definition mentions no limit at all, only the terms. The notes' gloss is "(Tail of the sequence bunch together.)" (notes p. 6).

**Theorem** (notes p. 6; ≈1:10:32–1:12:08). A sequence of real numbers is convergent if and only if it is a Cauchy sequence. "For now, everything is in R at the moment" (≈1:11:21). Colding does not prove it in this lecture: "I won't prove this now, but I'll prove this next time", and the proof will use the two monotone sequences built from a bounded sequence (≈1:11:21–1:12:08). [Lecture 6](06-cauchy-convergence-theorem.md) proves that a Cauchy sequence converges, from the Bolzano–Weierstrass theorem rather than from this construction. See [Cauchy sequences](cauchy-sequences.md).

### From the notes only: Cauchy

The notes follow the definition with a short biography quoted "From Wikipedia": Baron Augustin-Louis Cauchy (1789–1857) was a French mathematician, engineer and physicist, "one of the first to rigorously state and prove the key theorems of calculus (thereby creating real analysis)", who pioneered complex analysis and the study of permutation groups and contributed to mathematical physics, notably continuum mechanics (notes p. 6). The lecture does not mention it.

## Contracting maps and fixed points (≈1:12:08–1:17:53)

**Where this is going** (≈1:12:08–1:13:39). Everything so far is in $\mathbf{R}$, but "a lot of these concepts work much more general", and the generalization can be used to find solutions to differential equations. For that the concepts have to be abstracted "to where sequences are not any more real numbers, but they are of some other space", and that "often goes over using what's called the contracting mapping theorem" (≈1:12:53). The theorem has all kinds of forms, but "it's just a matter of what space you're looking at" (≈1:13:39). Here the space is $\mathbf{R}$.

**Fixed point** (notes p. 6; ≈1:17:08). If $T : \mathbf{R} \to \mathbf{R}$ is a map, then $x_0 \in \mathbf{R}$ is a **fixed point** of $T$ if

$$T(x_0) = x_0 .$$

**Definition** (notes p. 6; ≈1:13:39–1:15:25). A **contracting map** is a map $T : \mathbf{R} \to \mathbf{R}$ for which there exists a constant $c \lt 1$ such that for all $x, y \in \mathbf{R}$,

$$\vert T(x) - T(y) \vert \leq c \thinspace \vert x - y \vert .$$

The images of two points are closer together than the points were, by the factor $c$: "So they have to come closer" (≈1:15:25). The notes: "(Points are squeezed together under the map.)" (notes p. 6). On the board Colding also says that $c$ is positive; his remark about it is hard to read from the captions ("c is positive. I mean, that's not important. It had to be positive", ≈1:14:35). What he stresses is the other end: "the important point is that c has to be strictly less than 1. That's a crucial point" (≈1:14:35). The notes state only $c \lt 1$.

**Contracting mapping theorem** (notes p. 6; ≈1:15:25–1:17:53). Any contracting map $T : \mathbf{R} \to \mathbf{R}$ has a fixed point: there is an $x$ with $T(x) = x$ (≈1:16:16–1:17:08). Again "it's crucial that this c is less than 1. That's what makes everything go. If it was equal to 1, you wouldn't get anything" (≈1:17:08). The proof is for next time: "once you know the more abstract concepts, then it's quite easy" (≈1:15:25–1:16:16). It is given in [Lecture 6](06-cauchy-convergence-theorem.md).

**Application** (notes p. 6; ≈1:17:08–1:17:53). Set up in more general spaces than $\mathbf{R}$, the fixed point can be a solution to a differential equation; this is "a standard application to get solutions to differential equations" (≈1:17:53). The notes: "Application of contracting mapping theorem: Existence of solutions to ODEs. More on all of this next time......" (notes p. 6). Colding closes: next time "We'll talk about the contracting mapping theorem. We won't talk quite yet about the applications" (≈1:17:53). On the OCW lecture list, Lectures 22 and 23 cover ordinary differential equations and the Picard–Lindelöf theorem; this knowledge base does not yet cover them. See [the contracting mapping theorem](contracting-mapping-theorem.md).

## Board versus notes

Where they differ, this page follows the notes and gives the board's version with its timestamp. Collected here:

- **The order of the algebraic rules.** Board: the sum is rule 1 and the constant multiple rule 2 (≈5:40–6:29). Notes: constant multiple (1), sum (2), as in Lecture 4 (p. 1).
- **The fourth rule.** Board: $\frac{1}{a_n} \to \frac{1}{a}$ when every $a_n \neq 0$ and $a \neq 0$ (≈6:29–7:20). Notes: $\frac{1}{b_n} \to \frac{1}{b}$ when $b_n \neq 0$ and $b \neq 0$ (p. 1). Both are now reciprocals; the Lecture 4 notes had the quotient $\frac{a_n}{b_n}$.
- **The quotient example.** Board: names $\frac{1}{n}$, $\frac{1}{n^2}$ and $1$ as three sequences and applies the rules for sums, reciprocals and products one at a time (≈9:00–13:00). Notes: cite "the algebraic properties of limits" for the whole step (p. 2).
- **The monotone convergence theorem.** Board: the bound is spoken as "a" and the limit set to "little a" (≈18:29, ≈35:17); the two versions are called "part 1" and "Part B" (≈21:03). Notes: bound $A$, limit $\sup \lbrace a_n \rbrace$; "Increasing version" and "Decreasing version" (p. 2).
- **Monotone sequences from a bounded sequence.** Board only: $b_n$ and $c_n$, the sup and inf of the tails (≈21:51–33:39). Not in the notes.
- **The first step of the proof.** Board: "a n is less than a for all n" (≈37:00). Notes: $a_n \leq a$ as the last link of the chain (p. 5).
- **$b_n$ in the $\sqrt{2}$ construction.** Board: "the largest natural number" (≈45:14). Notes: "the largest integer" (p. 3).
- **Increasing.** Board: reduces $a_n \leq a_{n+1}$ to $10 \thinspace b_n \leq b_{n+1}$ on scrap paper, then computes $(10 \thinspace b_n)^2 = 100 \thinspace b_n^2$ (≈48:32–53:26). Notes: "then obviously" $(10 \thinspace b_n)^2 \leq 2 \cdot 10^{2(n+1)-2}$ (p. 3).
- **Bounded.** Board: squares $2 \cdot 10^{n-1}$ to get $4 \cdot 10^{2n-2}$ (≈54:12–54:57). Notes: print the reason with $10^{2n-2}$ inside the parenthesis, a slip (p. 3).
- **The extra term in $a^2 \geq 2$.** Board: $\frac{1}{10^{n-1}}$ (≈1:02:42), once spoken "1 over 10 to the n" (≈1:04:13). Notes: $10^{1-n}$ (p. 4).
- **The Cauchy condition.** Board: $n$ and $m$ bigger than $N$ (≈1:09:45). Notes: $m, n \geq N$ (p. 6).
- **The contraction constant.** Board: $c$ positive and strictly less than $1$ (≈1:14:35). Notes: $c \lt 1$ (p. 6).
- **Cauchy's biography.** Notes only (p. 6).

## Where the lecture stops

The course now has a condition that guarantees convergence, the monotone convergence theorem, and has used it to give the decimal picture of $\sqrt{2}$ a precise meaning. Several facts were used without proof and are promised or simply asserted: that $\frac{1}{n^2}$ and $10^{1-n}$ tend to $0$; that a limit keeps an inequality ($\leq$ or $\geq$) satisfied by every term, and the related claim that $c \leq b$ for the limits of the inf and sup sequences ("we'll prove this later", ≈32:54). The Cauchy convergence theorem and the contracting mapping theorem are stated, with proofs promised for next time (≈1:11:21, ≈1:17:53). [Lecture 6](06-cauchy-convergence-theorem.md), "Cauchy Convergence Theorem" (TBB Section 2.12), proves that a Cauchy sequence converges, assuming the Bolzano–Weierstrass theorem, and proves the contracting mapping theorem from it.

## Related pages

- [The monotone convergence theorem](monotone-convergence-theorem.md): monotone sequences, the theorem and its proof, the sup and inf of the tails, and the $\sqrt{2}$ application.
- [Sequences and limits](sequences-and-limits.md): sequences, convergence and divergence across Lectures 2 to 6.
- [Algebraic properties of limits](algebraic-properties-of-limits.md): the four rules, used here for the quotient example and for $a^2 = 2$.
- [The square root of 2](square-root-of-2.md): the course's proofs that $\sqrt{2}$ is not rational and is real, including this lecture's decimal construction.
- [Supremum and infimum](supremum-and-infimum.md): the $\sup$ and $\inf$ in the theorem and in the tails construction.
- [Completeness and the least upper bound property](least-upper-bound-property.md): what guarantees that the $\sup$ in the proof exists.
- [Cauchy sequences](cauchy-sequences.md): the definition and the theorem stated in this lecture.
- [The contracting mapping theorem](contracting-mapping-theorem.md): fixed points, contracting maps and the theorem stated in this lecture.
- [Subsequences](subsequences.md): the review at the start of the lecture.
- [Writing proofs](writing-proofs.md): scrap paper first, then the written proof, as in the proof that $a_n$ is increasing.
- [Lecture 4 — Sequences; Convergence](04-sequences-convergence.md): the previous lecture.
- [Lecture 6 — Cauchy Convergence Theorem](06-cauchy-convergence-theorem.md): the next lecture.
