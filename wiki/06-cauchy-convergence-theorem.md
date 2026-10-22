# Lecture 6 — Cauchy Convergence Theorem

**18.100B Real Analysis, Spring 2025 · Tobias Holck Colding · [video](https://www.youtube.com/watch?v=WCCpss6udNs) (77 min)**

Sources for this page: the [edited transcript](../raw/transcripts/06-cauchy-convergence-theorem.md) (timestamps below are written ≈M:SS and point into it), the course's typed [lecture notes](../raw/notes/06-cauchy-convergence-theorem.md) for this lecture (cited "notes p. N"; [PDF on OCW](https://ocw.mit.edu/courses/18-100b-real-analysis-spring-2025/mit18_100b_s25_lec06.pdf)), and the OCW readings list, which assigns Section 2.12 of Thomson, Bruckner and Bruckner, *Elementary Real Analysis* (TBB) to this lecture. Colding teaches from the blackboard; there are no slides.

## What this lecture establishes

Lecture 5 defined Cauchy sequences and stated, without proof, that a sequence of real numbers converges if and only if it is Cauchy. This lecture proves the direction that matters for applications: **every Cauchy sequence is convergent**. The proof has two steps. A Cauchy sequence is bounded (≈3:24–8:26; notes p. 3), and by the **Bolzano–Weierstrass theorem**, which says that every bounded sequence has a convergent subsequence, it then has a convergent subsequence, whose limit turns out to be the limit of the whole sequence (≈50:17–58:28; notes p. 3). The Bolzano–Weierstrass theorem itself is assumed here and promised for next time: "we're going to cheat just a little bit" (≈50:17).

The theorem is put to work twice. With it Colding proves the **contracting mapping theorem**: a contracting map $T : \mathbf{R} \to \mathbf{R}$ has a fixed point, and it has at most one (≈11:07–36:43; notes pp. 1–2). He then uses the fixed-point idea to explain **Newton's method** for finding a zero of a function (≈37:31–49:32; notes pp. 2–3). Finally he gives the rigorous **definition of a continuous function**, with $\epsilon$ and $\delta$, proves that a continuous function takes convergent sequences to convergent sequences, and proves the **extreme value theorem**: a continuous function on a closed interval $[a, b]$ attains its supremum and its infimum (≈58:28–1:16:18; notes pp. 3–4).

Notation: as in the earlier lectures, the notes set the real numbers in bold, $\mathbf{R}$, and this page follows them. $\vert x \vert$ is the absolute value of $x$, which Colding often calls "the norm"; $\sup$ and $\inf$ are the least upper bound and the greatest lower bound (see [supremum and infimum](supremum-and-infimum.md)). On the board the sequences in the first half are called $x_n$; the notes call them $a_n$, and this page follows the notes in the formal statements. A subsequence is written $a_{n_k}$, as in [subsequences](subsequences.md). The letter $a$ is used both for the limit of a sequence and for the left endpoint of the interval $[a, b]$; each section says which.

## Review (≈0:00–3:24)

Colding opens with what Lecture 5 covered: "Last time we talked about the basic algebraic operation for limit of sequences. We talked about the monotone convergence theorem" (≈0:00). An increasing sequence that is bounded converges to the sup of its terms, and a decreasing sequence that is bounded from below converges to the inf (≈0:49–1:37; see [the monotone convergence theorem](monotone-convergence-theorem.md)). "And the third thing we talked about, and that's where we will continue today, is Cauchy sequence" (≈1:37). The notes open with the same three items under "Last time:" (notes p. 1).

**Cauchy sequence** (notes p. 1; ≈1:37–3:24). A sequence $a_n$ is a Cauchy sequence if for all $\epsilon \gt 0$ there exists an $N$ such that if $m, n \geq N$, then

$$\vert a_n - a_m \vert \lt \epsilon .$$

On the board Colding first says only "if little n is bigger or equal to the capital N" and corrects himself to "little n and little m" (≈2:38). The captions garble the end of the condition, "is a distribution" (≈3:24); the notes have the inequality above. In words: "the Cauchy sequence just meant that the tail of the sequence bunched together" (≈3:24). The notes: "(Tail of the sequence bunch together.)" (notes p. 1). See [Cauchy sequences](cauchy-sequences.md).

## A Cauchy sequence is bounded (≈3:24–8:26)

On the board this is a separate "little theorem" at the start of the lecture: "If x n is a Cauchy sequence, then x n is bounded" (≈3:24). In the notes it is the first step of the proof of the Cauchy convergence theorem (notes p. 3).

**Proof** (notes p. 3; ≈4:16–8:26).

1. **Take $\epsilon = 1$.** In the definition "you can take epsilon to be equal to 1" (≈4:16). So there exists $N$ such that for $m, n \geq N$,

$$\vert a_n - a_m \vert \lt 1$$

(notes p. 3; on the board, "bigger than this N", ≈5:10).

2. **Fix one $m$.** Set $m = N$: "I'm only applying this now and just choosing just one single m. And I'm choosing it to be equal to that capital" (≈6:00). So for all $n \geq N$,

$$\vert a_n - a_N \vert \lt 1 .$$

3. **Subtract and add $a_N$.** "You can subtract it first and then add it again" (≈6:51). Splitting into two numbers and using the triangle inequality, for $n \geq N$,

$$\vert a_n \vert = \vert (a_n - a_N) + a_N \vert \leq 1 + \vert a_N \vert$$

(notes p. 3; ≈6:51–7:37). For all these $n$ "there is a uniform bound" (≈7:37).

4. **Take the maximum with the first terms.** Only finitely many terms come before $a_N$, so

$$\vert a_n \vert \leq \max \lbrace \vert a_N \vert + 1, \vert a_1 \vert, \cdots, \vert a_{N-1} \vert \rbrace$$

for every $n$ (notes p. 3). On the board the maximum is called $M$, and for $n \geq N$ the bound holds "because it's a maximum in particular of this and all the other ones. That's obvious. So it means that if you have a Cauchy sequence, it's automatically bounded" (≈7:37–8:26). Colding misspeaks twice in this step, saying "x n minus 1" for the term with index $N - 1$ and "less than or equal to n" for $M$ (marked in the transcript). □

Lecture 4 proved that a convergent sequence is bounded in the same way, with $\epsilon = 1$ and the limit $a$ in the place of $a_N$ (see [sequences and limits](sequences-and-limits.md#a-convergent-sequence-is-bounded)).

## The Cauchy convergence theorem (≈8:26–11:07)

**Theorem** (notes p. 1; ≈8:26–10:14). A sequence of real numbers is convergent if and only if it is a Cauchy sequence. The notes call it "Theorem (Cauchy convergence theorem)" on p. 1 and "the Cauchy theorem" on pp. 2–3.

The lecture proves one direction: "So this is the following that any Cauchy sequence is convergent" (≈9:27). For the other direction Colding says "So recall that last time we showed the converse", and "We proved that any convergent sequence is a Cauchy sequence. And so the Cauchy convergence theorem is just a converse" (≈9:27–10:14). The Lecture 5 material in this knowledge base does not contain that proof: Lecture 5 states the equivalence and says "I won't prove this now, but I'll prove this next time" (Lecture 5, ≈1:11:21). Lecture 6 does not prove it either, on the board or in the notes, so **this knowledge base has no proof that a convergent sequence is Cauchy**. The notes print the "if and only if" and prove only the other direction (notes pp. 1, 3).

Before proving the theorem, Colding uses it: "we'll come back to the proof in just a little bit. But before that, let me talk about some applications" (≈10:14).

## Contracting maps and fixed points (≈11:07–14:41)

**Contracting map** (notes p. 1; ≈11:07–12:58). A map $T : \mathbf{R} \to \mathbf{R}$ is a contracting map if there exists a constant $c \lt 1$ such that for all $x, y \in \mathbf{R}$,

$$\vert T(x) - T(y) \vert \leq c \thinspace \vert x - y \vert .$$

On the board the constant is "some constant c positive. And the key point is it will have to be positive. But the key point is that this constant has to be strictly less than 1" (≈12:11); the notes state only $c \lt 1$. The images of two points are "strictly closer together than the point that they are images of" (≈12:11): "under the map, the images are squeezed more together" (≈12:58). The notes: "(Points are squeezed together under the map.)" (notes p. 1).

**Fixed point** (notes p. 1; ≈12:58–13:52). A point $x_0 \in \mathbf{R}$ is a fixed point of $T$ if

$$T(x_0) = x_0 .$$

"For a map T, if it is under the map, the point remain unchanged" (≈12:58).

**Question: the same $c$?** (≈13:52). A student said, "But for that, it's not the same c for all x and y." Colding: "It is the same c." "You can weaken that a little bit", but "Just think about it, that it's a requirement that it's the same c for all. And the key point is that this c is strictly less than 1" (≈13:52). He comes back to this before Newton's method: "you could have some kind of local statement where, it was true for x and y in some small range. And that would be enough to guarantee you a fixed point. But in general, it's the same" (≈37:31). The lecture does not state or prove the local version.

## A contracting map has at most one fixed point (≈14:41–18:02)

**Lemma** (notes p. 2; ≈14:41). "If T here is a contracting map, then there's at most one fixed point." The notes: "For a contracting map the fix point is unique" (notes p. 2; "fix point" is a printed slip for "fixed point").

**Proof** (notes p. 2; ≈15:32–17:16). Suppose $x$ and $y$ are fixed points. Then, using first that they are fixed and then that $T$ is contracting,

$$\vert x - y \vert = \vert T(x) - T(y) \vert \leq c \thinspace \vert x - y \vert$$

(≈16:30; notes p. 2). Since $c \lt 1$, "you can only have an inequality like this, right, if this number here is 0" (≈17:16), so $\vert x - y \vert = 0$ and $x = y$. □ A student then pointed something out on the board; the remark is inaudible in the captions, and Colding's correction ("It should have been this sequence because otherwise it wouldn't be-- if x is equal to y equal to z") cannot be matched to the board from the captions (≈17:16). "So our contracting maps have at most one fixed point" (≈18:02).

## Iterating a contracting map: the Problem Set 3 exercise (≈18:02–27:41)

Colding says he has "harassed the graders to give you back the homework" and that next week's assignment is posted (≈18:02). He first says "here's something on P set 4", then "I forget which one it is. But anyway, on the third P set, you will be asked to prove the following" (≈18:49). The notes: "On Pset 3 you will be asked to show that for a contracting map $T$ and any $a_1 \in \mathbf{R}$ the sequence $a_{n+1} = T(a_n)$ is a Cauchy sequence" (notes p. 2). The problem set is [on OCW](https://ocw.mit.edu/courses/18-100b-real-analysis-spring-2025/mit18_100b_s25_pset03.pdf); this knowledge base does not transcribe it.

**The sequence** (≈18:49–21:17). Start with any point $x$. On the board the sequence starts at index $0$:

$$a_0 = x, \quad a_1 = T(x), \quad a_2 = T(a_1) = T(T(x)), \quad a_3 = T(a_2) = T(T(T(x))), \quad \ldots$$

written $T^2(x)$, $T^3(x)$ and so on, so that $a_{n+1} = T(a_n) = T^{n+1}(x)$ (≈19:34–20:27). The $n$-th element "is just where you have applied the map n times to the original point" (≈21:17). The notes start the sequence at $a_1 \in \mathbf{R}$ instead (notes p. 2).

**The key starting point** (≈22:07–27:41). Proving that $a_n$ is Cauchy is the homework: "But on P set 3, you prove that this a n is a Cauchy sequence" (≈22:07). On the board Colding does only "a special case that is a key starting point" (≈22:52): "I'm looking at two consecutive elements in the sequence. And I'm estimating the distance between them". That alone is "not enough to prove that's a Cauchy sequence, right, because I need to prove that for all n and m sufficiently large" (≈22:52). Since $a_{n+1} = T(a_n)$ and $a_n = T(a_{n-1})$, the contracting property gives

$$\vert a_{n+1} - a_n \vert = \vert T(a_n) - T(a_{n-1}) \vert \leq c \thinspace \vert a_n - a_{n-1} \vert$$

(≈23:39–25:22; at ≈24:31 he leaves the $c$ out when he says it, and has it in the next line). Each step the distance "has decreased with some factor" (≈24:31). Iterating, with "c here I just have to carry along for the ride" and "another c that pops out" each time (≈25:22–26:08),

$$\vert a_{n+1} - a_n \vert \leq c \thinspace \vert a_n - a_{n-1} \vert \leq c^2 \thinspace \vert a_{n-1} - a_{n-2} \vert \leq \cdots$$

down to the first two terms $a_0$ and $a_1$ (≈26:08–26:55). So the distance "is bounded by something like c to the n times a1 minus a0, something like that" (≈26:55); he does not pin down the exact power. Because $c \lt 1$, this "will become incredibly small when n is large" (≈26:55). "And I leave the rest for the homework" (≈27:41). How to get from consecutive terms to all $m, n \geq N$ is not shown in the lecture or the notes.

## Proof of the contracting mapping theorem (≈27:41–36:43)

**Contracting mapping theorem** (notes p. 1; ≈28:27). If $T : \mathbf{R} \to \mathbf{R}$ is a contracting map, then $T$ has a fixed point. "We already know that such a fixed point is unique" (≈29:23).

**Proof** (notes p. 2; ≈29:23–36:43). The proof uses the problem-set result and the Cauchy convergence theorem.

1. **The sequence converges.** Start with any point $x$ and form $a_n$ by applying $T$ repeatedly (≈29:23–30:12). By the Problem Set 3 exercise $a_n$ is a Cauchy sequence (Colding says "P set 2" here, meaning 3, ≈30:12), and by the Cauchy convergence theorem it converges to some $a$ (≈31:05; notes p. 2).
2. **$T(a_n)$ converges to $a$.** "Well, T of a n, that was a n plus 1. It was just 1 further out of the sequence" (≈32:41). Since $a_n \to a$, also $a_{n+1} \to a$, so $T(a_n) = a_{n+1} \to a$ (≈32:41–33:27; notes p. 2).
3. **$T(a_n)$ converges to $T(a)$.** Because $T$ is contracting,

$$\vert T(a_n) - T(a) \vert \leq c \thinspace \vert a_n - a \vert ,$$

and the left side is $\vert a_{n+1} - T(a) \vert$ (≈34:18). Since $a_n \to a$, the right side goes to $0$, so the left side does too, and $a_{n+1} \to T(a)$ (≈34:18–35:07). That a quantity squeezed between $0$ and a sequence tending to $0$ also tends to $0$ is used here without comment, on the board and in the notes.
4. **So $T(a) = a$.** The sequence $a_{n+1}$ converges both to $a$ and to $T(a)$. "There can only be one limit", so $a = T(a)$ (≈35:56). □ That a sequence has only one limit is used here; the lectures so far in this knowledge base do not prove it.

"So from the Cauchy convergence theorem, then you get the contracting mapping theorem" (≈35:56).

The notes organize steps 2 to 4 differently (notes p. 2). They first observe that $T(a_n) = a_{n+1} \to a$, then prove a general statement: if $x_n \to x$, then $T(x_n) \to T(x)$, because

$$\vert T(x_n) - T(x) \vert \leq c \thinspace \vert x_n - x \vert$$

and the right side tends to $0$. Applied to $a_n$ this gives $T(a_n) \to T(a)$, and so $T(a) = a$. The theorem about continuous functions later in the lecture has the same shape.

**Why it matters** (≈31:53, ≈36:43). "The contracting mapping theorem is actually extremely powerful." It can be used to solve ordinary differential equations, which the course will come back to, "But it can also be used to solve PDEs, which is more complicated, Partial Differential Equations, and in all kinds of other areas of math" (≈31:53). The notes list "Existence of solutions to ODEs" as the first application and defer it, "as this needs a version of the contracting mapping theorem where $T$ is defined on a more general space than the real numbers" (notes p. 2). The proof also gives a method: "for many things, it's almost impossible to find the actual fixed point", but you can start anywhere "And then you just apply the map enough times", or start from "something pretty close to the fixed point. And then you iterate from there" (≈36:43). See [the contracting mapping theorem](contracting-mapping-theorem.md).

## Newton's method (≈37:31–49:32)

Colding illustrates the last point with Newton's method (≈37:31–38:16). Given a function $f$, the goal is a point where it vanishes, that is, a solution of $f(x) = 0$; "the method is a numerical method to find such a point" (≈38:16). For a linear or a quadratic function the point is easy to find, but for a complicated function you may not be able to say exactly what it is (≈39:03). "Newton's methods require that you start with a good guess" (≈39:03). The notes: "Finding a zeroth of a function $f : \mathbf{R} \to \mathbf{R}$. (So find a solution $x$ to $f(x) = 0$.)" (notes p. 2; "zeroth" is a printed slip for "zero").

This section uses derivatives, the quotient rule and the mean value theorem, none of which the course has defined or proved yet. On the OCW lecture list derivatives come in Lecture 15 ("Derivatives; Laws for Differentiation") and the mean value theorem in Lecture 16 ("Rolle's Theorem; Mean Theorem; L'Hôpital's Rule; Taylor Expansion"); this knowledge base does not yet cover either.

**The assumption** (≈39:03–39:52; notes p. 2). Assume $f' \neq 0$. On the board: "I'm assuming that there's nowhere where the differential vanishes", so that "it's actually monotone. It's either increasing or decreasing" (≈39:52). The notes also suppose that $x_1$ is a good initial guess, "so $f(x_1)$ is sufficiently small" (notes p. 2).

**The map** (notes p. 2; ≈39:52). Define

$$T(x) = x - \frac{f(x)}{f'(x)} .$$

"This seems maybe far away from contracting now" (≈39:52).

**Its derivative** (notes p. 2; ≈40:38–41:26). The derivative of $x$ is $1$, and the second term is a quotient. The captions garble the quotient-rule step (≈40:38). Colding then splits the result into two fractions: one is $f'$ squared over $f'$ squared, which cancels the $1$, and the other is $f$ times $f''$ over $(f')^2$ (≈40:38–41:26). The notes:

$$T'(x) = 1 - \frac{f'}{f'} + \frac{f \thinspace f''}{(f')^2} = f \frac{f''}{(f')^2} .$$

So $T'(x)$ is $f(x) f''(x)$ divided by $f'(x)^2$ (≈41:26, ≈45:38).

**Why a small derivative makes $T$ contracting** (≈41:26–43:55; board only). By the mean value theorem, $T(x) - T(y)$ is "a derivative at somewhere in between x and y times the difference between x and y" (≈42:17). Colding first gives the theorem another name that the captions render as "Wallis theorem" and that is probably misheard (≈42:17). So if the derivative of $T$ were bounded everywhere by some $c \lt 1$, then

$$\vert T(x) - T(y) \vert \leq c \thinspace \vert x - y \vert ,$$

and "if we knew that the derivative of T was strictly less than 1 everywhere, then we would know that this map is a contracting map" (≈43:07–43:55). The notes do not mention the mean value theorem; they go straight from the formula for $T'$ to "then $T$ is a contracting map" (notes pp. 2–3).

**What "good guess" means** (≈43:55–47:12). "I'm not going to make that too precise, as I'm putting it in quotation marks" (≈44:49). A good guess is not a point where $f$ vanishes, but one "where the value is really small" (≈44:49). Precisely enough for the argument, it means that the derivative of $T$, which is $f$ times $f''$ over $(f')^2$, is really small at that point: "And, in fact, I want it to be small compared with this. So if this here is really small compared with that, then I can guarantee that the absolute value of this is smaller than 1" (≈45:38–46:24). The captions do not say what "this" and "that" are on the board. The notes put it as: $T$ is a contracting map "as long as $x$ stay close to the initial guess and for the initial guess $f(x)$ is small compared with" $\frac{f''}{(f')^2}$ (notes p. 3). Neither gives a precise condition.

**What the method does not say** (≈46:24–47:59). Starting from a good guess, you form the sequence $x$, $T(x)$, $T^2(x)$, …, and "you need to be able to say that once you form the sequence, the next thing that it's spitting out is also a good guess, so that you stay in this range of good guess" (≈46:24). Only then is $T$ a contracting map along the way, with a fixed point as the limit (≈47:12–47:59). "But the Newton method doesn't tell you anything about that. But it require that to be applied" (≈47:12). The notes: "By the contracting mapping theorem the sequence $x_{n+1} = T(x_n)$ is a Cauchy sequence that converges to a fixed point of $T$" (notes p. 3). Note that $T$ here is considered only near the initial guess, while the contracting mapping theorem was stated for maps on all of $\mathbf{R}$; the local version Colding mentioned (≈37:31) is what this needs, and it is not stated or proved.

**A fixed point is a zero** (notes p. 3; ≈48:44–49:32). If $x_0$ is a fixed point, then

$$x_0 = x_0 - \frac{f(x_0)}{f'(x_0)} ,$$

so subtracting $x_0$ on both sides leaves $\frac{f(x_0)}{f'(x_0)} = 0$, and the numerator must be $0$ (Colding says "denominator" here, ≈49:32). "So a fixed point is indeed a point where f of x0 is equal to 0" (≈49:32).

## The Bolzano–Weierstrass theorem (≈49:32–51:51)

"So now we want to prove the Cauchy convergence theorem. But we're going to cheat just a little bit, because we are going to deduce it from another theorem that I will prove next time" (≈49:32–50:17).

**Bolzano–Weierstrass theorem** (notes p. 3; ≈51:05). "So the Bolzano-Weierstrass theorem says that every bounded sequence has a convergent subsequence" (≈51:05). The notes: "Any bounded sequence has a convergent subsequence", and "Once we have the Bolzano-Weirstrass theorem we can prove the Cauchy theorem" (notes p. 3; "Weirstrass" is a printed slip, repeated throughout the notes). It is not proved in this lecture: "Again, I'll prove this next time" (≈51:05). On the OCW lecture list Lecture 7 is "Bolzano–Weierstrass Theorem; Cauchy Sequences; Series" (TBB Sections 2.11–2.12 and 3.4), which is not yet in this knowledge base. See [the Bolzano–Weierstrass theorem](bolzano-weierstrass-theorem.md).

In Lecture 5 Colding had said that the proof of the Cauchy theorem would use the two monotone sequences built from the sup and the inf of the tails of a bounded sequence (Lecture 5, ≈32:54, ≈1:11:21). The proof given here goes through the Bolzano–Weierstrass theorem instead, and the tails construction does not appear in this lecture.

## Proof of the Cauchy convergence theorem (≈51:51–58:28)

**Claim** (notes p. 3; ≈52:38). If $a_n$ is a Cauchy sequence, then it is convergent.

**Proof** (notes p. 3; ≈52:38–58:28).

1. **Bounded.** "But we already showed that any Cauchy sequence is bounded" (≈52:38), by the theorem at the start of the lecture.
2. **A convergent subsequence.** By the Bolzano–Weierstrass theorem, $a_n$ has a convergent subsequence $a_{n_k}$, with some limit $a$ (≈53:24–54:23; notes p. 3; on the board the limit is $x$). It remains to show that the whole sequence converges to $a$ (≈54:23).
3. **Two choices of $N$.** Let $\epsilon \gt 0$. Since $a_n$ is Cauchy, there exists $N_1$ such that if $m, n \geq N_1$, then

$$\vert a_n - a_m \vert \lt \frac{\epsilon}{2}$$

(≈55:14; notes p. 3). Since $a_{n_k} \to a$, there exists $N_2$ such that if $k \geq N_2$, then $\vert a_{n_k} - a \vert \lt \frac{\epsilon}{2}$ (≈55:59; notes p. 3). On the board both conditions are spoken as "bigger than".
4. **Compare through a term of the subsequence.** Set $N = \max \lbrace N_1, N_2 \rbrace$ (≈56:45; notes p. 3). For $n \geq N$, insert a term $a_{n_k}$ of the subsequence and use the triangle inequality:

$$\vert a_n - a \vert \leq \vert a_n - a_{n_k} \vert + \vert a_{n_k} - a \vert \lt \frac{\epsilon}{2} + \frac{\epsilon}{2}$$

(notes p. 3). The notes take this "if $n \geq N$ and $k \geq N$". On the board, "this is where k is taking equal to this N2" (≈56:45); the captions garble the line where he splits the difference (≈56:45–57:43). Each piece is less than $\frac{\epsilon}{2}$, "And so you get that this difference here was less than epsilon" (≈57:43). □

For the first piece to be less than $\frac{\epsilon}{2}$, both $n$ and $n_k$ have to be at least $N_1$; neither the board nor the notes say why $n_k \geq N_1$. (Lecture 4 noted the related fact $n_k \geq k$, also without proof; see [subsequences](subsequences.md).) "So this is why the Bolzano-Weierstrass theorem implies the Cauchy convergence theorem" (≈58:28). The step of comparing through something in between is the trick Lecture 4 used for the product of limits; see [algebraic properties of limits](algebraic-properties-of-limits.md).

## Continuous functions (≈58:28–1:06:48)

The lecture's second application is the extreme value theorem, and it needs a definition first: "let me introduce this notion of a function being continuous in a rigorous way" (≈59:17). Lecture 1 had described continuity only informally, as drawing a graph without lifting the chalk (see [the intermediate value theorem](intermediate-value-theorem.md)).

**Definition** (notes p. 4; ≈59:17–1:01:53). A function $f : \mathbf{R} \to \mathbf{R}$ is **continuous at a point** $x_0 \in \mathbf{R}$ if for all $\epsilon \gt 0$ there exists a $\delta \gt 0$ such that

$$\vert x - x_0 \vert \lt \delta \implies \vert f(x) - f(x_0) \vert \lt \epsilon .$$

A function is **continuous** if it is continuous at all points in its domain (notes p. 4; ≈1:01:06–1:01:53). On the board the domain "could be a subset of R, could be all of R" (≈59:17–1:00:13), and the condition is that "the images are within epsilon region" (≈1:00:13). Colding draws the picture: around $f(x_0)$ on the vertical axis take "a little interval around here-- this is a epsilon interval", "then there should be some delta interval around here so that if you're looking at images here, then it will map into here" (≈1:01:06).

**Theorem** (notes p. 4; ≈1:02:42–1:03:29). If $f : \mathbf{R} \to \mathbf{R}$ is continuous and $x_n$ is a sequence with $x_n \to x_0$, then $f(x_n) \to f(x_0)$. "And this is often useful way of thinking about continuity" (≈1:02:42). The domain does not have to be all of $\mathbf{R}$, "but you just have to be careful that everything that you talk about is in the domain" (≈1:02:42). On the board the limit point is called $x$.

**Proof** (notes p. 4; ≈1:03:29–1:06:48). "you only need that is continuous at each x" (≈1:04:18), in fact at the one limit point. Given $\epsilon \gt 0$, continuity gives a $\delta \gt 0$ such that if $\vert x - x_0 \vert \lt \delta$, then $\vert f(x) - f(x_0) \vert \lt \epsilon$ (≈1:04:18; notes p. 4). Since $x_n \to x_0$, apply the definition of convergence with this $\delta$ in the place of $\epsilon$: there exists $N$ such that if $n \geq N$, then $\vert x_n - x_0 \vert \lt \delta$ (≈1:05:08; on the board "bigger than capital N"). Therefore $\vert f(x_n) - f(x_0) \vert \lt \epsilon$ for $n \geq N$, which is $f(x_n) \to f(x_0)$ (≈1:05:54; notes p. 4). □ See [continuous functions](continuous-functions.md).

## The extreme value theorem (≈1:06:48–1:16:18)

**Theorem** (notes p. 4; ≈1:06:48–1:08:22). Let $a \lt b$ be real numbers and let $f$ be continuous on the interval $[a, b]$, which includes both endpoints. Then the sup and the inf of $f$ are achieved: there exists $x \in [a, b]$ with $f(x) = \sup f$, and likewise for $\inf f$ (notes p. 4). The board stresses both hypotheses, "It needs to be continuous at all points. And this interval needs to contain the endpoints also" (≈1:06:48), and names the points: the sup is the value at a point $x_M$, "capital M for Max", and the inf the value at a point $x_m$ (≈1:07:37–1:08:22). "In particular, the sup is finite. And it's not really a sup. It's a max" (≈1:07:37). The inf part can be obtained from the sup part "by looking at the function minus f if you wanted", or by the same proof (≈1:08:22). The notes call it "Another application of the Bolzano-Weirstrass theorem" (notes p. 3); on the board Colding first calls it an application of the Cauchy convergence theorem (≈58:28) and then, in the proof, says "So then I'm using not Cauchy convergence theorem. I'm using the Bolzano-Weierstrass theorem, which implies the Cauchy convergence theorem" (≈1:11:40).

**Proof for the sup** (notes p. 4; ≈1:09:09–1:14:44). "The proof that the infimum is the same with obvious modification" (notes p. 4; ≈1:09:56). Here $a$ and $b$ are the endpoints of the interval.

1. **A sequence approaching the sup.** "A priori, the sup could be infinity" (≈1:09:56): Colding allows the value $\infty$ when $f$ has no upper bound, though "we don't usually like this" (≈1:10:43). In either case there is a sequence $x_n \in [a, b]$ with $f(x_n) \to \sup f$; when the sup is infinite this means "there's a sequence where the value of these become larger and larger without bound" (≈1:09:56–1:10:43; notes p. 4). The notes take the sequence as given; on the board a student asked about it (below).
2. **A convergent subsequence.** The $x_n$ lie in $[a, b]$, so they form a bounded sequence (≈1:10:43), and by the Bolzano–Weierstrass theorem there is a convergent subsequence $x_{n_k} \to x$ (≈1:11:40–1:12:26; notes p. 4; on the board the limit is $x_M$). "It's a good exercise to see that this sequence in itself-- you can just draw a little picture, and you convince yourself that this sequence in itself may not be convergent" (≈1:11:40).
3. **The limit is in the interval.** "And it converges to something in this interval. And that's important" (≈1:12:26), because $f$ is defined there. If the interval did not include its endpoints, the subsequence could converge to an endpoint, "but the function would not be defined there. So you wouldn't be able to conclude the extreme value theorem" (≈1:12:26–1:13:11). The notes say only "Note that $x \in [a, b]$." (notes p. 4). Why the limit of points of $[a, b]$ lies in $[a, b]$ is not proved; it is the fact, used without proof in Lecture 5, that a limit keeps an inequality satisfied by every term.
4. **Two limits of $f(x_{n_k})$.** By the theorem on continuous functions, $f(x_{n_k}) \to f(x)$ (≈1:13:11; notes p. 4). And $f(x_{n_k})$ is a subsequence of $f(x_n)$, which converges to $\sup f$: "But if you take a sequence that converges to whatever number, then any subsequence will converge to the same number" (≈1:13:57), the theorem of Lecture 4 (see [subsequences](subsequences.md)). So $\sup f = f(x)$ (≈1:13:57; notes p. 4). □

If the sup was a priori infinite, "that is still fine. But that should only take a minute, to convince yourself about that" (≈1:13:57); the argument for that case is not given. In the notes, the existence of the sequence in step 1 and the finiteness of $\sup f$ are not discussed, and the theorem on continuous functions, stated there for $f : \mathbf{R} \to \mathbf{R}$, is applied to a function on $[a, b]$ (notes p. 4). The conclusion: "So the sup is really a max", and by a very similar proof the infimum is achieved too, "so both the min and max" (≈1:14:44). See [the extreme value theorem](extreme-value-theorem.md).

**Question: where does the sequence come from?** (≈1:14:44–1:16:18). A student's question is partly inaudible; Colding asks, "Are you asking why such a bounded sequence exists?" (≈1:15:32). His answer: take the sup of $f$ over the interval. For any $\epsilon$, there must be a point $x$ where the value of $f$ is larger than the sup minus $\epsilon$ (≈1:15:32–1:16:18). "And so you could imagine, instead of epsilon here, looking at a sequence like this", and that gives the sequence (≈1:16:18); the captions do not record which sequence of $\epsilon$'s he wrote. It is bounded because it lies between $a$ and $b$; the Bolzano–Weierstrass theorem, "that we'll prove next time", gives the convergent subsequence, and the theorem on continuous functions gives the maximum, and likewise the minimum (≈1:16:18). This answer uses that the sup is the *least* upper bound, so the sup minus $\epsilon$ is not an upper bound; see [supremum and infimum](supremum-and-infimum.md). The lecture ends with "Any questions?" (≈1:16:18).

## Board versus notes

Where they differ, this page follows the notes and gives the board's version with its timestamp. Collected here:

- **Names.** Board: the Cauchy sequence is $x_n$ and the subsequence's limit $x$ (≈1:37–58:28). Notes: $a_n$ and $a$ (pp. 1, 3).
- **Boundedness of a Cauchy sequence.** Board: a separate "little theorem" at the start of the lecture, with the maximum called $M$ (≈3:24–8:26). Notes: the first step of the proof of the Cauchy theorem (p. 3).
- **The converse.** Board: "last time we showed the converse", that a convergent sequence is Cauchy (≈9:27–10:14). Notes: state the "if and only if" (p. 1) and prove only that a Cauchy sequence converges (p. 3). Neither this lecture nor Lecture 5, as recorded here, contains a proof of the converse.
- **The contraction constant.** Board: $c$ positive and strictly less than $1$ (≈12:11). Notes: $c \lt 1$ (p. 1).
- **Uniqueness of the fixed point.** Board: called a Lemma (≈14:41). Notes: "For a contracting map the fix point is unique" (p. 2).
- **The iterated sequence.** Board: starts at $a_0 = x$, writes $a_{n+1} = T^{n+1}(x)$, and shows the estimate for consecutive terms as the key starting point of the homework (≈19:34–27:41). Notes: start at any $a_1 \in \mathbf{R}$ and leave the whole proof to Pset 3 (p. 2).
- **$T(a) = a$.** Board: estimates $\vert a_{n+1} - T(a) \vert \leq c \thinspace \vert a_n - a \vert$ directly (≈34:18–35:56). Notes: first prove that $x_n \to x$ implies $T(x_n) \to T(x)$ for a contracting map, then apply it (p. 2).
- **Newton's method.** Board: assumes the derivative vanishes nowhere, so $f$ is monotone (≈39:52); derives $T'$ by the quotient rule, splitting off $f'$ squared over $f'$ squared (≈40:38–41:26); uses the mean value theorem to explain why a bound on $T'$ makes $T$ contracting (≈42:17–43:55); and says that the method does not guarantee that the iterates stay good guesses (≈46:24–47:12). Notes: assume $f' \neq 0$, print the middle term as $\frac{f'}{f'}$, do not mention the mean value theorem, and say $T$ is contracting "as long as $x$ stay close to the initial guess" (pp. 2–3).
- **The extreme value theorem.** Board: introduced as an application of the Cauchy convergence theorem (≈58:28), proved with the Bolzano–Weierstrass theorem (≈1:11:40); allows the sup to be infinite a priori (≈1:09:56); explains why the endpoints must be included (≈1:12:26–1:13:11); names the points $x_M$ and $x_m$ and gets the inf from $-f$ (≈1:07:37–1:08:22). Notes: an application of the Bolzano–Weierstrass theorem (p. 3); "Note that $x \in [a, b]$" without comment; "Likewise for $\inf f$" (p. 4).
- **Continuity.** Board: the domain may be a subset of $\mathbf{R}$ (≈59:17–1:00:13), with a picture of the $\epsilon$ and $\delta$ intervals (≈1:01:06). Notes: $f : \mathbf{R} \to \mathbf{R}$ (p. 4).
- **The theorem on continuous functions.** Board: only continuity at the limit point is needed (≈1:04:18). Notes: "since $f$ is continuous" (p. 4).
- **Spoken inequalities.** Board: several conditions $n \geq N$ are spoken as "bigger than" (≈5:10, ≈55:14, ≈55:59, ≈1:05:08). Notes: $\geq$ throughout (pp. 3–4).

## Where the lecture stops

The course now has a criterion for convergence that needs no candidate limit: a Cauchy sequence of real numbers converges. Its proof rests on the Bolzano–Weierstrass theorem, which is stated and promised for next time (≈50:17, ≈51:05). With the Cauchy convergence theorem, a contracting map on $\mathbf{R}$ has a unique fixed point, provided the Problem Set 3 exercise that the iterates form a Cauchy sequence; with the Bolzano–Weierstrass theorem, a continuous function on $[a, b]$ attains its maximum and its minimum. Several things are used without proof or left open: that a convergent sequence is Cauchy (said to have been proved "last time", ≈9:27); that a limit is unique (≈35:56); that a limit of points of $[a, b]$ lies in $[a, b]$; derivatives and the mean value theorem in the Newton's method discussion; the local version of the contracting mapping theorem that Newton's method needs (≈37:31); and the case of an infinite sup in the extreme value theorem (≈1:13:57). On the OCW lecture list, Lecture 7 is "Bolzano–Weierstrass Theorem; Cauchy Sequences; Series" (TBB Sections 2.11–2.12 and 3.4), which is not yet in this knowledge base.

## Related pages

- [Cauchy sequences](cauchy-sequences.md): the definition, boundedness, and the proof of the Cauchy convergence theorem.
- [The Bolzano–Weierstrass theorem](bolzano-weierstrass-theorem.md): the statement, assumed here, and its two uses in this lecture.
- [The contracting mapping theorem](contracting-mapping-theorem.md): fixed points, uniqueness, the proof from the Cauchy theorem, and Newton's method.
- [Continuous functions](continuous-functions.md): the definition with $\epsilon$ and $\delta$, and the theorem that continuous functions preserve limits of sequences.
- [The extreme value theorem](extreme-value-theorem.md): the statement and proof given here.
- [Sequences and limits](sequences-and-limits.md): convergence, boundedness and the course's conditions for convergence.
- [Subsequences](subsequences.md): the subsequences used in both proofs, and the theorem that a subsequence of a convergent sequence has the same limit.
- [The monotone convergence theorem](monotone-convergence-theorem.md): the review at the start of the lecture.
- [Supremum and infimum](supremum-and-infimum.md): the sup and inf in the extreme value theorem.
- [The intermediate value theorem](intermediate-value-theorem.md): the course's other theorem about continuous functions on $[a, b]$, not yet proved.
- [Lecture 5 — Monotone Convergence Theorem](05-monotone-convergence-theorem.md): the previous lecture, where the Cauchy and contracting mapping theorems were stated.
