# Lecture 7 — Bolzano–Weierstrass Theorem; Cauchy Sequences; Series

**18.100B Real Analysis, Spring 2025 · Tobias Holck Colding · [video](https://www.youtube.com/watch?v=qeDewaJ4n24) (83 min)**

Sources for this page: the [edited transcript](../raw/transcripts/07-bolzano-weierstrass-theorem-cauchy-sequences-series.md) (timestamps below are written ≈M:SS and point into it), the course's typed [lecture notes](../raw/notes/07-bolzano-weierstrass-theorem-cauchy-sequences-series.md) for this lecture (cited "notes p. N"; [PDF on OCW](https://ocw.mit.edu/courses/18-100b-real-analysis-spring-2025/mit18_100b_s25_lec07.pdf)), and the OCW readings list, which assigns Sections 2.11–2.12 and 3.4 of Thomson, Bruckner and Bruckner, *Elementary Real Analysis* (TBB) to this lecture. Colding teaches from the blackboard; there are no slides.

## What this lecture establishes

Lecture 6 proved that every Cauchy sequence converges, assuming the **Bolzano–Weierstrass theorem**: every bounded sequence has a convergent subsequence. This lecture proves it (≈2:25–22:12; notes pp. 1–2). The idea is to halve an interval again and again, each time keeping a half that contains infinitely many terms of the sequence, and to pick one term from each half. The chosen terms form a subsequence that is squeezed between the left endpoints $b_k$, which increase, and the right endpoints $c_k$, which decrease. Both converge by the monotone convergence theorem, and since $c_k - b_k = 2^{1-k}$ they have the same limit, which the subsequence is forced to share.

The rest of the lecture starts the theory of **series** (≈23:00–1:20:42; notes pp. 2–5). A series is the sequence $s_n$ of partial sums of a sequence $a_n$, and it converges when $s_n$ does. Colding proves that the **geometric series** $\sum_{i=0}^{\infty} c^i$ converges to $\frac{1}{1-c}$ when $\vert c \vert \lt 1$ and diverges otherwise, and that the **harmonic series** $\sum \frac{1}{n}$ diverges, by showing $s_{2^n - 1} \geq \frac{n}{2}$. He gives a first check for any series (if $a_n$ does not tend to $0$, the series diverges), observes that a series of non-negative terms converges exactly when its partial sums are bounded, defines **absolute convergence** and proves that it implies convergence, and proves that $\sum \frac{1}{n^2}$ converges by comparing it with a geometric series. The lecture ends with the list of convergence tests and the simplest **comparison test**. The notes go further, with a second comparison test and the ratio test (notes pp. 5–7); they are given below under their own heading.

Notation: the notes set the real numbers in bold, $\mathbf{R}$, and this page follows them. $\vert x \vert$ is the absolute value of $x$, which Colding often calls "the norm". A sequence is written $a_n$ and a subsequence $a_{n_k}$, as in [subsequences](subsequences.md). In the series part, $s_n$ is the $n$-th partial sum; where the summation starts ($i = 0$ or $i = 1$) varies, and each section says which. The notes spell the name "Bolzano-Weirstrass" throughout page 1, a printed slip for Weierstrass.

## Review (≈0:00–3:13)

"So the Cauchy Convergence Theorem says that any Cauchy sequence is convergent" (≈0:00). Lecture 6 proved it, "But we proved it assuming another theorem", the Bolzano–Weierstrass theorem (≈0:51): any bounded sequence has a convergent subsequence (≈1:39). Colding recalls the shape of that proof. A Cauchy sequence is bounded, so the Bolzano–Weierstrass theorem gives it a convergent subsequence, and "you would then want to prove that the limit is actually a limit for the whole sequence. That's what we did, right? But we didn't prove the Bolzano-Weierstrass Theorem. So let's try to prove it now" (≈2:25). The notes open the same way: "Last time we showed that the Bolzano-Weirstrass implies the Cauchy theorem" (notes p. 1). See [Cauchy sequences](cauchy-sequences.md).

## The Bolzano–Weierstrass theorem (≈2:25–23:00)

**Bolzano–Weierstrass theorem** (notes p. 1; ≈1:39). Any bounded sequence has a convergent subsequence.

### The idea: squeeze the subsequence (≈3:13–7:54)

Take a bounded sequence $a_n$. To keep the picture simple, assume every $a_n$ lies in the interval $[0, 1]$: "It could be any other bounded interval. But let's just say 0 to 1" (≈3:13). The notes make the same assumption, "For simplicity assume that $a_n \in [0, 1]$" (notes p. 1). Neither shows how the general case follows; Colding says only that "the same argument works for any other interval" and that "there's nothing essential I'm using about it" (≈9:27).

The plan is to find a subsequence $a_{n_k}$ and two other sequences $b_k$ and $c_k$ with

$$b_k \leq a_{n_k} \leq c_k ,$$

so that the subsequence "is going to be squeezed between two other sequences" (≈4:50). "And the thing about the other sequences is that they are much nicer": the $b_k$ are monotone increasing and the $c_k$ monotone decreasing (≈4:50). In Colding's picture the $b_k$ move to the right as $k$ grows and the $c_k$ move to the left, and every later term of the subsequence lies between them, so "the subsequence is going to be squeezed in smaller and smaller interval. And that's going to force it to converge" (≈5:35–7:07).

Why the endpoints converge (≈7:07–7:54): every $b_k$ lies below the first $c$, so the $b_k$ form an increasing sequence that is bounded, and it has a limit; likewise the $c_k$ decrease and are bounded below by the first $b$, so they converge too. This is the [monotone convergence theorem](monotone-convergence-theorem.md) of Lecture 5. Because the two sequences come closer and closer together, their limits are equal: "So that's going to imply that b is equal to c. That's the idea" (≈7:54).

**Questions** (≈7:54–9:27). A student asked, "Do they need to be strictly monotonic?" Colding: no, $b_k \leq b_{k+1}$ and $c_k \geq c_{k+1}$, "So it's not strict" (≈7:54–8:40). A second question is partly inaudible in the captions; it seems to ask what happens if the endpoints stayed a constant distance apart, and Colding answered "Yeah that's right" (≈8:40). The point, he said, is that the difference $c_k - b_k$ is positive and goes to $0$: "So you're right that if they didn't come together, we couldn't conclude things. But they will come together. This I will guarantee" (≈9:27). What he says the difference equals is garbled in the captions at this point (≈8:40); the formula is derived later in the lecture, $c_k - b_k = 2^{1-k}$ (≈20:36).

### The construction (≈9:27–19:01)

1. **Start.** Set $b_1 = 0$ and $c_1 = 1$, and let the first term of the subsequence be the first term of the sequence, $a_{n_1} = a_1$ (≈10:13). Trivially $b_1 \leq a_1 \leq c_1$ (≈11:02). The notes: "Set $a_{n_1} = a_1$" (notes p. 1).
2. **Halve.** Divide $[0, 1]$ into $[0, \frac{1}{2}]$ and $[\frac{1}{2}, 1]$. The whole sequence lies in $[0, 1]$, "So this means that there are either infinitely many here or infinitely many there, right?" (≈11:02). Possibly both; then pick one (≈17:26). Say infinitely many $a_n$ lie in $[0, \frac{1}{2}]$ (≈11:02; notes p. 1).
3. **Pick the next term.** Let $a_{n_2}$ be the next term after $a_1$ that lies in $[0, \frac{1}{2}]$ (≈11:51–12:39). It must be a later term, not $a_1$ again, "because otherwise it's not going to be a subsequence" (≈12:39); "I mean, it could be the same value. But it will have to come from a different subscript" (≈13:27). The new endpoints are those of the interval now in focus: $b_2 = 0$ and $c_2 = \frac{1}{2}$ (≈13:27). The notes record $n_2 \gt n_1 = 1$, $a_{n_1} \in [0, 1]$ and $a_{n_2} \in [0, \frac{1}{2}]$ (notes p. 1).
4. **Only look at the infinitely many.** "And here you have to be a little bit careful" (≈13:27): from now on only the infinitely many terms in $[0, \frac{1}{2}]$ matter, "You're not going to worry about what lies here" (≈14:15). Halve $[0, \frac{1}{2}]$ into $[0, \frac{1}{4}]$ and $[\frac{1}{4}, \frac{1}{2}]$. Of the infinitely many terms, infinitely many lie in one of the two halves; say in $[\frac{1}{4}, \frac{1}{2}]$ (≈15:04). Let $a_{n_3}$ be the next term after $a_{n_2}$ in that interval, and set $b_3 = \frac{1}{4}$ and $c_3 = \frac{1}{2}$ (≈15:52–16:41). The notes make the same choice: "Pick an $n \gt n_2$ such that $a_n \in [\frac{1}{4}, \frac{1}{2}]$ and set $a_{n_3} = a_n$. We continue this way" (notes p. 1).
5. **Continue.** At each step halve the current interval, keep a half that contains infinitely many of the terms still in play, take as the next term of the subsequence the next term of the sequence in that half, and let $b_k$ and $c_k$ be its left and right endpoints: "The b's will always be the left endpoint of the interval. The c's will be the right endpoint of the interval" (≈17:26). Colding repeats the whole recipe slowly at ≈16:41–18:15.

### The endpoints (≈19:01–21:22)

"If you do that, you see each time you're halving it" (≈19:01). The new interval is one of the two halves of the previous one, so its left endpoint is at least the previous left endpoint and its right endpoint at most the previous right endpoint: the $b_k$ are increasing and the $c_k$ decreasing (≈19:01). Each interval is half as long as the previous one,

$$c_{k+1} - b_{k+1} = \frac{1}{2} (c_k - b_k) ,$$

(≈19:47; the captions garble the spoken formula), and the first interval has length $c_1 - b_1 = 1$ (≈20:36). Together these give

$$c_k - b_k = 2^{1-k}$$

(≈20:36). "And so you see that the length of this interval becomes smaller and smaller" (≈20:36).

### The subsequence converges (≈21:22–23:00)

The $b_k$ increase, so they converge to some $b$; the $c_k$ decrease, so they converge to some $c$; "And because the difference between these goes to 0, then the b must be equal to c" (≈21:22). By construction $a_{n_k}$ lies between $b_k$ and $c_k$, and so does every later term $a_{n_l}$ with $l \geq k$ (≈21:22–22:12). Since $b_k$ and $c_k$ converge to the same number $b$, the terms squeezed between them "will also converge to b. So that's a Bolzano-Weierstrass Theorem" (≈22:12). □

That a sequence squeezed between two sequences with the same limit converges to that limit is used here without proof, on the board and in the notes. So is the bound on the $b_k$ and $c_k$ that the monotone convergence theorem needs: on the board it is that every $b_k$ lies below the first $c$ and every $c_k$ above the first $b$ (≈7:07); the notes say only "(as it is also bounded)" (notes p. 1).

### The notes' version (notes pp. 1–2)

The notes choose the same halves as the board ($[0, \frac{1}{2}]$, then $[\frac{1}{4}, \frac{1}{2}]$) but define $b_k$ and $c_k$ only after the subsequence. Before that they note that for $k_1, k_2 \geq k$,

$$\vert a_{n_{k_1}} - a_{n_{k_2}} \vert \leq 2^{1-k} ,$$

and "Since $2^{-k} \to 0$ as $k \to \infty$ this shows that the subsequence $a_{n_k}$ is a Cauchy sequence. However, more is true" (notes p. 1). They do not use the Cauchy property; the proof continues with the squeeze. "The sequence $b_k$ will be the left endpoint of the interval of length $2^{1-k}$ that all the element $a_{n_i}$ will lie in when $i \geq k$ and $c_k$ will be the right end point of the same interval" (notes p. 1). Then $b_k$ is increasing, $c_k$ decreasing, both converge, and "Since $c_k - b_k = 2^{1-k}$ it follows that $b_k$ and $c_k$ converges to the … same number and since the later $a_{n_k}$ are all squeezed between the two they also converges to that same number" (notes pp. 1–2; "converges" is a printed slip, twice).

See [the Bolzano–Weierstrass theorem](bolzano-weierstrass-theorem.md) for the statement, this proof and its uses.

### From the notes only: Weierstrass

The notes quote a short biography "From Wikipedia" (notes p. 2): Karl Theodor Wilhelm Weierstrass (1815–1897) was a German mathematician often cited as the "father of modern analysis". He left university without a degree, trained as a school teacher and taught mathematics, physics, botany and gymnastics. Among other contributions he "formalized the definition of the continuity of a function", proved the intermediate value theorem and the Bolzano–Weierstrass theorem, "and used the latter to study the properties of continuous functions on closed bounded intervals". The lecture does not mention it. The use of the theorem for continuous functions on $[a, b]$ is the course's extreme value theorem of Lecture 6 (see [the extreme value theorem](extreme-value-theorem.md)).

## Series (≈23:00–25:21, ≈33:22–36:38)

"OK, another key concept in this class is the concept of a series" (≈23:00).

**Definition** (notes p. 2; ≈23:00–25:21). Given a sequence $a_n$, form a new sequence $s_n$:

$$s_1 = a_1 , \quad s_2 = a_1 + a_2 , \quad s_3 = a_1 + a_2 + a_3 ,$$

and in general

$$s_n = a_1 + \cdots + a_n = \sum_{i=1}^{n} a_i$$

(notes p. 2; ≈23:45–24:36). A sequence of this form is called a **series** (≈25:21). The series $\sum_{i=1}^{\infty} a_i$ **converges** if the sequence $s_n$ converges, and then the limit is also written $\sum_{i=1}^{\infty} a_i$ (notes p. 2; ≈34:14–35:05).

**One symbol, two meanings** (≈33:22–35:52). "But really, what you're thinking about is this sequence here. But you, with a slight abuse of notation, you write this here for series" (≈34:14). "And so a series is convergent. It just means that the sequence" of partial sums is convergent (≈34:14). "So in a way, this symbol here is used for two different things. It's used for the series. And if the series is convergent, it's also used for the limit. This is like standard" (≈35:52). The infinite sum is the limit of the partial sums (≈35:05).

**Where the sum starts** (≈33:22, ≈36:38, ≈53:37–54:24). The geometric series below starts at $i = 0$, so its $s_n$ has $n + 1$ terms (≈33:22). "It's, of course, important where you start. I mean, the convergence is not important. But what the limit is depends on where you start" (≈36:38): the starting point never decides whether a series converges, "because this is just adding something to it. It will matter where you start for the limit, but not whether or not the series is convergent" (≈54:24). The notes switch between starting at $0$ and at $1$ without comment (notes pp. 2–5).

**Achilles and the turtle** (≈25:21–26:56; board only). Colding connects series to "one of the famous Greek paradoxes", in the form with "Achilles and the turtle" (≈25:21). The turtle has a head start, and to catch up Achilles must first cover half the distance, then half of what remains, and so on; "And so this goes on infinitely long, and therefore, he can never catch up with the turtle" (≈26:07). "And that's exactly a series" (≈26:07). He does not work out the sum.

See [series](series.md).

## The geometric series (≈26:56–44:03)

"So this is the most important series" (≈26:56). For a number $c$, the **geometric series** is

$$s_n = \sum_{i=0}^{n} c^i ,$$

so $s_0 = 1$ (since $c^0 = 1$), $s_1 = 1 + c$, $s_2 = 1 + c + c^2$, and so on (notes p. 2; ≈26:56–28:32). It matters because it is "a non-trivial series that can be used to determine whether other series" converge: "you can compare other series with the geometric series. And the geometric series is easier … to determine whether it is convergent or not" (≈26:56–29:17).

**The formula** (notes p. 2; ≈29:17–32:27). Multiplying $1 + c + c^2 + \cdots + c^n$ by $c$ gives $c + c^2 + \cdots + c^{n+1}$ (≈29:17–30:05). So when the sum is multiplied by $1 - c$, "there's a lot of cancelation" (≈30:53), and only the first and the last term survive:

$$(1 - c) \sum_{i=0}^{n} c^i = 1 - c^{n+1}$$

(notes p. 2; ≈30:53–31:40). If $c \neq 1$, divide by $1 - c$:

$$s_n = \sum_{i=0}^{n} c^i = \frac{1 - c^{n+1}}{1 - c}$$

(notes p. 2; ≈31:40–32:27).

**Theorem** (notes pp. 2–3; ≈36:38–38:29). The geometric series converges if $\vert c \vert \lt 1$ and diverges otherwise. When $\vert c \vert \lt 1$,

$$\sum_{i=0}^{\infty} c^i = \frac{1}{1 - c} .$$

When Colding states the limit he says "the limit is 1 minus c" (≈38:29), and later "1 minus c over 1" (≈40:55); both times the board and the notes have $\frac{1}{1-c}$ (marked in the transcript). He first states the divergence for $\vert c \vert \gt 1$ (≈37:35) and then proves it for $\vert c \vert \geq 1$ (≈41:43).

**Proof when $\vert c \vert \lt 1$** (≈39:21–41:43). Then $c \neq 1$, so the formula for $s_n$ applies (≈39:21). The absolute value of a product is the product of the absolute values, so $\vert c^{n+1} \vert = \vert c \vert^{n+1}$, and because $\vert c \vert \lt 1$ this "converges to 0" as $n$ goes to infinity (≈40:10). "So just by the algebraic rules for limits", $s_n \to \frac{1}{1-c}$ (≈40:55; see [algebraic properties of limits](algebraic-properties-of-limits.md)). That $\vert c \vert^{n+1} \to 0$ when $\vert c \vert \lt 1$ is used without proof. Colding points out how unusual this is: "And in fact, we have even, which is really nice, and unusual for a series. I mean, usually you cannot actually determine what the limit is. But in this case, we could" (≈40:55).

**Proof when $\vert c \vert \geq 1$** (≈41:43–44:03; board only). Two consecutive partial sums differ by one term:

$$s_{n+1} - s_n = c^{n+1} , \qquad \vert s_{n+1} - s_n \vert = \vert c \vert^{n+1} \geq 1$$

(≈42:28–43:16). "Remember that if a sequence is convergent, if a sequence is convergent, then it is a Cauchy sequence" (≈43:16). Here the terms do not bunch together: "not even two consecutive is bunching together, because independent on how far, how large n is, the difference is always at least 1" (≈43:16). So $s_n$ is not a Cauchy sequence and does not converge. □ This step uses the direction "convergent implies Cauchy" of the Cauchy convergence theorem, which Lecture 6 says was proved in Lecture 5 but which this knowledge base has no proof of (see [Cauchy sequences](cauchy-sequences.md)).

The notes argue differently (notes p. 3), from the formula: "Therefore, $s_n$ converges with limit $\frac{1}{1-c}$ if $\vert c \vert \lt 1$ and diverges if $\vert c \vert \gt 1$ or $c = -1$. One easily checks, separately, that it also diverges for $c = 1$." They give no further detail for the divergent cases. The board's argument covers all of them at once, including $c = 1$, where the formula for $s_n$ does not apply.

See [the geometric series](geometric-series.md).

## The harmonic series diverges (≈44:03–53:37)

"Maybe the second most important is what's called the harmonic series", and it "is unfortunately not a series that is convergent" (≈44:03). The **harmonic series** is

$$\sum_{n=1}^{\infty} \frac{1}{n} ,$$

which has to start at $1$ "because I'm dividing by n" (≈44:50). The notes write $a_n = \frac{1}{n}$ and print the series as $\sum_{i=1}^{\infty} \frac{1}{2}$, a slip for $\frac{1}{i}$ (notes p. 3). Writing it as an infinite sum is the abuse of notation again, "but it's not a convergent series, so the infinite sum doesn't really make sense" (≈44:50).

Tests that decide convergence come later. "The test that is particularly useful in this case, it's what's called the integral test. But I won't talk about that today. But instead, I will show you a very simple proof of why this here is not convergent" (≈45:41).

**Theorem** (notes p. 3; ≈45:41–46:30). The harmonic series is divergent.

**Claim** (notes p. 3; ≈46:30–47:16). For every $n$,

$$s_{2^n - 1} = \sum_{i=1}^{2^n - 1} \frac{1}{i} \geq \frac{n}{2} .$$

The $s_{2^n - 1}$ form a subsequence of the partial sums, and the claim makes it unbounded. If the series converged, every subsequence of $s_n$ would converge too (≈47:16; the Lecture 4 theorem in [subsequences](subsequences.md)), and an unbounded sequence cannot converge (Lecture 4; see [sequences and limits](sequences-and-limits.md#a-convergent-sequence-is-bounded)). "So of course, the original harmonic series is not convergent" (≈47:16). The notes: "Since $\frac{n}{2} \to \infty$ it follows that the subsequence $s_{2^n - 1}$ is divergent and therefore so is the original series" (notes p. 3).

**Proof of the claim, by induction** (notes p. 3; ≈48:06–53:37).

1. **$n = 1$.** Then $2^1 - 1 = 1$, and the claim is $s_1 \geq \frac{1}{2}$. "But of course, s1 here, s1 is just 1 over 1. So that's definitely fine" (≈48:51).
2. **From $n$ to $n + 1$.** Assume $s_{2^n - 1} \geq \frac{n}{2}$ (≈50:30). Split the next partial sum into the old one and the new terms:

$$s_{2^{n+1} - 1} = s_{2^n - 1} + \sum_{i=2^n}^{2^{n+1} - 1} \frac{1}{i}$$

(≈50:30–51:20). By assumption the first part is at least $\frac{n}{2}$. The second part has $2^n$ terms, and the smallest of them is the last one, $\frac{1}{2^{n+1} - 1}$; "if I take the smallest of these guys and I multiply it by 2n, then that's definitely a lower bound" (≈52:05; "2n" is the captions' rendering of $2^n$). Dividing by the larger number $2^{n+1}$ makes it smaller still (≈52:51), so

$$s_{2^{n+1} - 1} \geq \frac{n}{2} + 2^n \frac{1}{2^{n+1}} = \frac{n}{2} + \frac{1}{2} = \frac{n+1}{2} .$$

"And that's exactly the claim for n plus 1" (≈52:51). □

The notes write the step as

$$s_{2^{n+1} - 1} \geq s_{2^n - 1} + \sum_{i=2^n}^{2^{n+1} - 1} \frac{1}{i} \geq \frac{n}{2} + 2^n \frac{1}{2^{n+1} - 1} \geq \frac{n}{2} + \frac{1}{2} = \frac{n+1}{2}$$

(notes p. 3), with $\geq$ in the first place where the two sides are equal, and without the board's intermediate $\frac{1}{2^{n+1}}$. "This is just like a simple proof", "very simple-minded proof", and "Once we learn about the integral test and so on, there are other way better ways of doing it" (≈47:16–48:06). "So that's a harmonic series. So you see that the harmonic series is divergent" (≈53:37).

See [the harmonic series](harmonic-series.md).

## First check: do the terms go to zero? (≈53:37–55:58; board only)

"So for a series, always check if" the terms $a_n$ go to $0$ or not (≈54:24; just before, Colding says "if you give me a limit", meaning a series, marked in the transcript). The reason: two consecutive partial sums differ by one term,

$$s_n - s_{n-1} = a_n$$

(≈55:11). If the series converges, the partial sums form a convergent sequence, so they are a Cauchy sequence, and in particular two consecutive ones must bunch together, which is whether $a_n$ goes to $0$ (≈55:11). "So if" $a_n$ "does not go to 0, you're already done, right? There's no reason to continue" (≈55:58): the series diverges, and no test is needed. "So that was just a side remark" (≈55:58). As with the geometric series, the argument uses that a convergent sequence is Cauchy. The notes do not state this check.

Colding adds that the harmonic series "failed this test" (≈55:58). Its terms $\frac{1}{n}$ do tend to $0$ (Lecture 4), so the check cannot detect its divergence; it gives a reason to stop only when the terms do not go to $0$.

## Series of non-negative terms (≈55:58–58:19)

If every $a_n \geq 0$, then each partial sum is the previous one plus a non-negative term,

$$s_{n+1} = s_n + a_{n+1} \geq s_n ,$$

so the partial sums are monotone increasing (≈56:43–57:30). By the [monotone convergence theorem](monotone-convergence-theorem.md), deciding whether such a series converges "it's just a matter of proving whether to determine whether this sequence is bounded or not. So you just need to find a bound" (≈57:30).

**Theorem** (notes p. 4). A series of non-negative numbers $\sum_{i=0}^{\infty} a_i$, where $a_n \geq 0$, is convergent if and only if the sequence $s_n$ is bounded from above. The notes' proof: $s_n$ is monotone nondecreasing, "The claim now follows from the monotone convergence theorem" (notes p. 4). The notes print the step as $s_{n+1} = s_n + a_n \geq s_n$, a slip for $a_{n+1}$ (notes p. 4). The direction from convergent to bounded is Lecture 4's theorem that a convergent sequence is bounded; the notes do not say so.

Colding also says that the harmonic series is "an example of something" in this setting (≈55:58–56:43): its terms are non-negative, so by the claim above its partial sums are increasing and unbounded.

## Absolute convergence (≈58:19–1:05:31)

"So this naturally leads to looking at what's called absolute convergence. So this is something stronger than convergence" (≈58:19).

**Definition** (notes p. 3; ≈59:09). A series $\sum_{n=0}^{\infty} a_n$ is **absolutely convergent** (on the board, "converge absolutely") if the series

$$\sum_{n=0}^{\infty} \vert a_n \vert$$

is convergent: the series "where you slap absolute values on them" (≈59:09).

**Theorem** (notes p. 3; ≈59:55). "So absolute convergence implies convergence. So this is a theorem. But it's not the other way around" (≈59:55). The notes: "Absolutely convergent implies convergent but not the other way around" (notes p. 3).

**The example: the alternating harmonic series** (notes p. 3; ≈1:00:40–1:02:21). The series

$$\sum_{n=1}^{\infty} \frac{(-1)^n}{n}$$

is convergent but not absolutely convergent: with absolute values it becomes the harmonic series, which diverges (≈1:01:34; notes p. 3). "It's called the alternating harmonic series" (≈1:00:40). Alternating "means that the sign of it is alternating": "the first one is negative. The next one is positive" (≈1:01:34). Its convergence is not proved here: "And we haven't yet proved that it's converging, but we'll do that in some later lecture" (≈1:00:40). The notes: "We will see later that the series" converges (notes p. 3). The notes print the sum without an upper limit.

**Proof that absolute convergence implies convergence** (notes pp. 3–4; ≈1:02:21–1:05:31). Take the partial sums of the series and of the series of absolute values. On the board the second is written with a bar, "I denote it with a bar" (≈1:02:21):

$$s_n = \sum_{i=0}^{n} a_i , \qquad \bar{s}_ n = \sum_{i=0}^{n} \vert a_i \vert .$$

For $m$ larger than $n$, the difference $s_m - s_n$ is the sum of the terms from $a_{n+1}$ up to $a_m$ (≈1:03:11; the captions garble the range). By the triangle inequality,

$$\vert s_m - s_n \vert = \vert a_{n+1} + \cdots + a_m \vert \leq \vert a_{n+1} \vert + \cdots + \vert a_m \vert = \vert \bar{s}_ m - \bar{s}_ n \vert$$

(≈1:03:57). "And here, actually, I don't even need to take absolute value" on the right, since $\bar{s}_ m - \bar{s}_ n$ is a sum of non-negative terms (≈1:03:57–1:04:44). If the series is absolutely convergent, $\bar{s}_ n$ converges, so it is a Cauchy sequence: far enough out its terms are within $\epsilon$ of each other (≈1:04:44). The inequality then says the same of $s_n$, so $s_n$ is a Cauchy sequence, and by the Cauchy convergence theorem it converges (≈1:04:44–1:05:31). "So it means that the original series was convergent" (≈1:05:31). □

The notes write the partial sums of $\sum \vert a_i \vert$ as a bold red $\mathbf{s}_ n$ instead of the bar, take $m \lt n$, and write

$$\vert s_n - s_m \vert = \vert a_n + \cdots + a_{m+1} \vert \leq \vert a_n \vert + \cdots + \vert a_{m+1} \vert = \vert \mathbf{s}_ n - \mathbf{s}_ m \vert$$

(notes p. 4). "Since the sequence $\mathbf{s}_ n$ is a Cauchy sequence it now follows that $s_n$ is" (notes p. 4). Both versions use the two directions of the Cauchy convergence theorem: convergent implies Cauchy for $\bar{s}_ n$, which this knowledge base has no proof of, and Cauchy implies convergent for $s_n$, proved in Lecture 6. See [series](series.md#absolute-convergence).

## The series of $\frac{1}{n^2}$ converges (≈1:05:31–1:16:35)

"So maybe the most important series is the geometric series. After that, you can debate a little bit which series is the most important" (≈1:06:20). The next candidate is

$$\sum_{n=1}^{\infty} \frac{1}{n^2} ,$$

the case of power $2$; "you could do it more generally where you raise it to some power", and power $1$ is the harmonic series (≈1:06:20). "I mean, this one doesn't really have a name, but it is a key series" (≈1:07:08). Colding first writes the sum from $n = 0$ and then corrects himself to start at $1$ (≈1:06:20, ≈1:07:55).

**Theorem** (notes p. 4; ≈1:07:08). The series $\sum_{i=1}^{\infty} \frac{1}{i^2}$ is convergent.

**Reduction** (≈1:07:08–1:07:55; notes p. 4). The terms are non-negative, so by the previous section it is enough to show that the partial sums

$$s_n = \sum_{i=1}^{n} \frac{1}{i^2}$$

are bounded: there exists $M$ with $s_n \leq M$ for all $n$ (notes p. 4).

**Claim** (notes p. 4; ≈1:08:40–1:09:29). For every $n$,

$$s_{2^n - 1} \leq \sum_{i=0}^{n-1} \left( \frac{1}{2} \right)^i .$$

The captions garble the spoken claim (≈1:09:29). The right side is a partial sum of the geometric series with $c = \frac{1}{2}$, which converges, so it is bounded (≈1:09:29–1:10:18; notes p. 4). On the board the bound is explicit: the partial sums are at most $\frac{1}{1-c} = 2$ (≈1:11:04). So the subsequence $s_{2^n - 1}$ is bounded, and since $s_n$ is increasing, "if a subsequence is bounded, then the original sequence is bounded and so convergent" (≈1:10:18). Why a bounded subsequence bounds an increasing sequence is not spelled out.

"I mean, again, this is not necessarily how I would do it. But the advantage with this here is that it doesn't use anything fancy" (≈1:08:40); the usual way is the integral test, which has not been covered.

**Proof of the claim, by induction** (notes pp. 4–5; ≈1:11:51–1:16:35).

1. **$n = 1$.** Then $2^1 - 1 = 1$, and $s_1 = 1 = \left( \frac{1}{2} \right)^0$ (≈1:11:51–1:12:37; notes p. 5).
2. **From $n$ to $n + 1$.** Assume $s_{2^n - 1} \leq \sum_{i=0}^{n-1} \left( \frac{1}{2} \right)^i$ (≈1:12:37). Split as for the harmonic series,

$$s_{2^{n+1} - 1} = s_{2^n - 1} + \sum_{i=2^n}^{2^{n+1} - 1} \frac{1}{i^2} .$$

This time the goal is an upper bound, so "instead of what is the smallest, we think about what is the largest of these numbers. But that's the first one" (≈1:14:14–1:15:01). There are $2^n$ terms, each at most $\frac{1}{(2^n)^2}$, so

$$s_{2^{n+1} - 1} \leq \sum_{i=0}^{n-1} \left( \frac{1}{2} \right)^i + 2^n \frac{1}{(2^n)^2} = \sum_{i=0}^{n-1} \left( \frac{1}{2} \right)^i + \frac{1}{2^n} = \sum_{i=0}^{n} \left( \frac{1}{2} \right)^i$$

(notes p. 5; ≈1:15:01–1:15:50). "The square kills" one factor $2^n$ and leaves $\frac{1}{2^n}$, "exactly the next one in the series" (≈1:15:50). "This is what's called the induction step" (≈1:15:50). □

## Tests for convergence (≈1:16:35–1:20:42)

"So now let me-- I have just four minutes left" (≈1:16:35); the lecture notes are posted and have more (≈1:16:35). To decide whether a series converges "there are a number of tests. And then of course, the key point is to use the right test" (≈1:17:33). Colding lists the comparison test, the ratio test, the root test, the integral test, "And then there's even one called the alternate series test" (≈1:17:33–1:18:21). The notes list the comparison test, the ratio test and the root test (notes p. 5). Only the comparison test is stated in the lecture; the notes also state the ratio test (below). The root test is named but not stated in either.

**Comparison test, version 1** (notes p. 5; ≈1:18:21–1:19:10). Suppose $a_n$ and $b_n$ are two sequences with

$$0 \leq a_n \leq b_n .$$

If $\sum_{n=1}^{\infty} b_n$ is convergent, then so is $\sum_{n=1}^{\infty} a_n$ (notes p. 5). "And this is the simplest version of the comparison test" (≈1:19:10). The captions garble the first inequality (≈1:18:21); the notes have $0 \leq a_n \leq b_n$. Neither the lecture nor the notes prove the test.

**How it is used** (≈1:19:10–1:20:42). A complicated series can be compared with a much simpler one whose convergence is already known (≈1:19:56). It works in both directions: "It's used to both determine that a series is convergent. … And it's also used to determine that the series is divergent", by comparing with a series "you already know is divergent" (≈1:19:56–1:20:42). "So there's a little bit more about tests in the lecture notes. But we will, anyway, talk about it more next time" (≈1:20:42).

## Question: where does the claim come from? (≈1:20:42–end)

A student asked about the intuition behind the claim in the $\frac{1}{n^2}$ proof; the question is partly inaudible in the captions (≈1:20:42). Colding: the geometric series is one that "come up often as a kind of comparison" (≈1:20:42). "Obviously you don't start with the claim. You're looking at the first few things and you see a pattern, basically" (≈1:21:28). "Later on, I would never prove any kind of convergence like this" (≈1:21:28). He sketches the integral test instead. For a series of non-negative numbers, think of each term as the area of a rectangle, so that the sum is the sum of the areas; the integral test compares that with "some curve and the area that lies below it, then it's much more clear" (≈1:21:28–1:22:19). The comparison by hand is done "case by case. Here there's a kind of general idea" (≈1:22:19). The test itself is not stated.

## From the notes only: more tests (notes pp. 5–7)

The notes go beyond the lecture with an example of the first comparison test, a second comparison test and the ratio test. The lecture does not reach them; Colding says tests will be discussed more next time (≈1:20:42). On the OCW lecture list, Lecture 8 is "Convergence Tests for Series; Power Series" (TBB Sections 3.5–3.6), which is not yet in this knowledge base. None of the tests below is proved in the notes.

**Example** (notes p. 5). The series

$$\sum_{n=1}^{\infty} \frac{2^{-n}}{n}$$

is convergent: with $a_n = \frac{2^{-n}}{n}$ and $b_n = 2^{-n}$, "then $0 \leq a_n \leq b_n$ and since the series $\sum_{n=1}^{\infty} b_n$ is convergent, then by the comparison test so is the series $\sum_{n=1}^{\infty} a_n$" (notes p. 5). The series of the $b_n$ is a geometric series with $c = \frac{1}{2}$, started at $n = 1$.

**Comparison test, version 2** (notes p. 6). Suppose $a_n$ and $b_n$ are two sequences with $b_n \neq 0$ and

$$\lim_{n \to \infty} \frac{a_n}{b_n} = L \neq 0 .$$

Then $\sum_{n=1}^{\infty} a_n$ is convergent if and only if $\sum_{n=1}^{\infty} b_n$ is.

**Example** (notes p. 6). The series

$$\sum_{n=2}^{\infty} \frac{1}{n^2 - 1}$$

is convergent, since

$$\frac{n^2}{n^2 - 1} \to 1$$

and the series $\sum_{n=2}^{\infty} \frac{1}{n^2}$ is convergent (notes p. 6). Here $a_n = \frac{1}{n^2 - 1}$, $b_n = \frac{1}{n^2}$, and $\frac{a_n}{b_n} = \frac{n^2}{n^2 - 1}$.

**Ratio test** (notes p. 6). Let $a_n \geq 0$ and assume that

$$\frac{a_{n+1}}{a_n} \to a .$$

If $a \lt 1$, then the series $\sum a_n$ is convergent. If $a \gt 1$, then the series $\sum a_n$ is divergent. If $a = 1$, "it is inconclusive" (notes p. 6). The notes do not say that the $a_n$ must be non-zero for the quotient to make sense.

**The ratio test cannot decide either series of this lecture** (notes pp. 6–7). For $a_n = \frac{1}{n}$, $\frac{a_{n+1}}{a_n} \to 1$, "so the test is inconclusive, but the series is divergent" (Example 1). For $a_n = \frac{1}{n^2}$, again $\frac{a_{n+1}}{a_n} \to 1$, "so the test is inconclusive, but the series is convergent" (Example 2). See [convergence tests for series](convergence-tests-for-series.md).

## Board versus notes

Where they differ, this page follows the notes and gives the board's version with its timestamp. Collected here:

- **Bolzano–Weierstrass: order of the construction.** Board: builds $b_k$ and $c_k$ step by step with the subsequence, starting from $b_1 = 0$ and $c_1 = 1$, and derives $c_k - b_k = 2^{1-k}$ from $c_{k+1} - b_{k+1} = \frac{1}{2} (c_k - b_k)$ (≈10:13–20:36). Notes: build the subsequence first, observe $\vert a_{n_{k_1}} - a_{n_{k_2}} \vert \leq 2^{1-k}$ and that the subsequence is Cauchy, then define $b_k$ and $c_k$ as the endpoints of the intervals (p. 1).
- **Bolzano–Weierstrass: why the endpoints are bounded.** Board: every $b_k$ lies below the first $c$, every $c_k$ above the first $b$ (≈7:07). Notes: "(as it is also bounded)" (p. 1).
- **Bolzano–Weierstrass: the questions.** Board only: whether the sequences must be strictly monotone, and what happens if they did not come together (≈7:54–9:27).
- **Series: notation and starting point.** Board only: the remarks on the abuse of notation (≈34:14–35:52) and that the starting point affects the limit but not convergence (≈36:38, ≈54:24); Achilles and the turtle (≈25:21–26:56).
- **The geometric series diverges.** Board: for all $\vert c \vert \geq 1$ at once, because consecutive partial sums differ by at least $1$, so they are not Cauchy (≈41:43–44:03). Notes: from the formula, for $\vert c \vert \gt 1$ and $c = -1$, and "One easily checks, separately" for $c = 1$ (p. 3).
- **The harmonic series.** Board: bounds the smallest term $\frac{1}{2^{n+1} - 1}$ below by $\frac{1}{2^{n+1}}$ (≈52:51). Notes: go straight to $2^n \frac{1}{2^{n+1} - 1} \geq \frac{1}{2}$, and write the first step as $\geq$ (p. 3).
- **The terms must go to zero.** Board only (≈53:37–55:58).
- **Non-negative terms.** Board: the partial sums are increasing, so you only need a bound (≈56:43–57:30). Notes: a theorem, "convergent if and only if the sequence $s_n$ is bounded from above" (p. 4).
- **Absolute convergence.** Board: $\bar{s}_ n$ with a bar, and $m$ larger than $n$ (≈1:02:21–1:03:57). Notes: a bold red $\mathbf{s}_ n$, and $m \lt n$ (p. 4).
- **The series of $\frac{1}{n^2}$.** Board: first written from $n = 0$, then corrected to start at $1$ (≈1:06:20, ≈1:07:55); the explicit bound $2$ (≈1:11:04). Notes: from $i = 1$, bounded by "a convergent geometric series" (p. 4).
- **The tests.** Board: comparison, ratio, root, integral and alternating series tests named, the first version of the comparison test stated, and the integral test sketched in answer to a question (≈1:17:33–1:22:19). Notes: comparison, ratio and root tests listed; both versions of the comparison test with examples and the ratio test with two examples (pp. 5–7).
- **Weierstrass's biography.** Notes only (p. 2).

## Where the lecture stops

With the Bolzano–Weierstrass theorem proved, the Cauchy convergence theorem of Lecture 6 now rests only on results proved in the course, together with the facts used here without proof: that a sequence squeezed between two sequences with the same limit has that limit, and how the general bounded case reduces to $[0, 1]$. The lecture then sets up series: the definition through partial sums, the geometric series as the basic comparison, the divergent harmonic series and the convergent $\sum \frac{1}{n^2}$, the check that the terms tend to $0$, and absolute convergence, which implies convergence. Several things are used without proof or left for later: that $\vert c \vert^{n} \to 0$ when $\vert c \vert \lt 1$; that a convergent sequence is Cauchy, used for the divergence of the geometric series (≈43:16), for the check on the terms (≈55:11) and for absolute convergence (≈1:04:44), and still without a proof in this knowledge base; the convergence of the alternating harmonic series (≈1:00:40); and the comparison test itself. On the OCW lecture list, Lecture 8 is "Convergence Tests for Series; Power Series" (TBB Sections 3.5–3.6), which is not yet in this knowledge base.

## Related pages

- [The Bolzano–Weierstrass theorem](bolzano-weierstrass-theorem.md): the statement, this lecture's proof, and the uses in Lecture 6.
- [Series](series.md): partial sums, convergence, the notation, the check on the terms, series of non-negative terms and absolute convergence.
- [The geometric series](geometric-series.md): the formula for the partial sums, the theorem and both proofs of divergence.
- [The harmonic series](harmonic-series.md): its divergence, the alternating harmonic series, and the convergent series of $\frac{1}{n^2}$.
- [Convergence tests for series](convergence-tests-for-series.md): the list of tests, the comparison test in two versions and the ratio test.
- [Cauchy sequences](cauchy-sequences.md): the Cauchy convergence theorem, which this lecture completes and then uses for series.
- [The monotone convergence theorem](monotone-convergence-theorem.md): used for the endpoints in the Bolzano–Weierstrass proof and for series of non-negative terms.
- [Subsequences](subsequences.md): the subsequence the proof constructs, and the subsequences $s_{2^n - 1}$ of partial sums.
- [Sequences and limits](sequences-and-limits.md): convergence and boundedness.
- [Writing proofs](writing-proofs.md): this lecture's proofs by induction, and Colding's remark that you do not start with the claim.
- [Lecture 6 — Cauchy Convergence Theorem](06-cauchy-convergence-theorem.md): the previous lecture, which assumed the Bolzano–Weierstrass theorem.
