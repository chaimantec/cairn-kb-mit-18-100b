# Lecture 8 — Convergence Tests for Series; Power Series

**18.100B Real Analysis, Spring 2025 · Tobias Holck Colding · [video](https://www.youtube.com/watch?v=lEMeyFq4-zQ) (81 min)**

Sources for this page: the [edited transcript](../raw/transcripts/08-convergence-tests-for-series-power-series.md) (timestamps below are written ≈M:SS and point into it), the course's typed [lecture notes](../raw/notes/08-convergence-tests-for-series-power-series.md) for this lecture (cited "notes p. N"; [PDF on OCW](https://ocw.mit.edu/courses/18-100b-real-analysis-spring-2025/mit18_100b_s25_lec08.pdf)), and the OCW readings list, which assigns Sections 3.5–3.6 of Thomson, Bruckner and Bruckner, *Elementary Real Analysis* (TBB) to this lecture. Colding teaches from the blackboard; there are no slides.

## What this lecture establishes

The lecture opens with a review of series (≈0:00–21:58; notes pp. 1–2). The Cauchy convergence theorem shows that the terms of a convergent series must go to $0$, which is the first thing to check. The **geometric series** $\sum c^i$ converges exactly when $\vert c \vert \lt 1$. The **harmonic series** belongs to the family $\sum \frac{1}{n^{\alpha}}$ with $\alpha \geq 1$, which diverges for $\alpha = 1$ and converges for $\alpha \gt 1$. **Absolute convergence** implies convergence but not conversely, and Colding explains with a picture why the **alternating harmonic series** converges. A series of non-negative terms converges exactly when its partial sums are bounded from above.

Then come three **convergence tests** (≈21:58–1:07:35; notes pp. 2–4). The **comparison test** has two versions. The first ($0 \leq a_n \leq b_n$, and $\sum b_n$ convergent) is proved on the board in two ways, with the example $\sum \frac{2^{-n}}{n}$. The second compares through the limit of $\frac{a_n}{b_n}$, with the example $\sum \frac{1}{n^2 - 1}$. The **ratio test** looks at the limit $a$ of $\vert \frac{a_{n+1}}{a_n} \vert$, and the **root test** at the limit of $\vert a_n \vert^{\frac{1}{n}}$. Each concludes convergence if the limit is less than $1$ and divergence if it is greater than $1$, and is inconclusive if it equals $1$. Both are proved by comparison with a geometric series, "And so this is explaining why the geometric series is so crucial" (≈41:18).

The last part introduces **power series** $\sum a_n x^n$ (≈1:07:35–1:20:33; notes pp. 4–5). Colding gives the series for $\frac{1}{1-x}$, the exponential function, cosine and sine, and remarks that not every function has one. He asks for which $x$ a power series converges, and uses the ratio test to show that $\sum \frac{x^n}{n!}$ converges for every $x$. The notes go further than the lecture, defining $\limsup$ and the **radius of convergence** (notes pp. 6–7); that material is given below under its own heading.

Notation: $\vert x \vert$ is the absolute value of $x$. $a_n$ and $b_n$ are sequences of real numbers, $\sum a_n$ the series with terms $a_n$, and $s_n$ its $n$-th partial sum; where a sum starts varies, and each section says which. In the proof of the comparison test the board writes $s_n^{a}$ and $s_n^{b}$ for the partial sums of the two series. The limit in the ratio test is $a$, on the board and in the notes. In the root test it is $c$ on the board and $r$ in the notes, and the number chosen between it and $1$ is $c_0$ on the board and $r_0$ in the notes. In the ratio test's proof that number is $\alpha$. $n!$ is $n$ factorial, $1 \cdot 2 \cdots n$.

## Review: series and the first check (≈0:00–5:46)

"One of the things we talked about last time was series. So we'll continue on that today" (≈0:00). From a sequence $a_n$ form the partial sums

$$s_1 = a_1 , \quad s_2 = a_1 + a_2 , \quad s_3 = a_1 + a_2 + a_3 , \quad s_n = \sum_{i=1}^{n} a_i$$

(notes p. 1; ≈0:51–1:37). The series converges when the sequence $s_n$ does, and the infinite sum denotes both the series and its limit, "slight abuse of notation" (≈1:37–2:27; notes p. 1). Where the sum starts does not affect whether it converges (≈35:26, ≈38:04). See [series](series.md).

**The terms must go to zero** (≈2:27–5:46; board only). By the Cauchy convergence theorem, $s_n$ converges if and only if it is a Cauchy sequence: $\vert s_n - s_m \vert$ is small once $m$ and $n$ are larger than some $N$ chosen depending on $\epsilon$ (≈2:27–4:11). Take $m = n - 1$. Then the difference is a single term,

$$s_n - s_{n-1} = a_n ,$$

so if the series converges, $a_n$ has to go to $0$ as $n$ goes to infinity (≈4:11–5:46). "So again, if you see a series", before applying any test, "The first thing that you check is that this element here goes to 0" (≈5:46). This is the argument of Lecture 7 (≈55:11) again. It uses the direction "convergent implies Cauchy" of the Cauchy convergence theorem, of which this knowledge base has no proof (see [Cauchy sequences](cauchy-sequences.md)).

## The geometric series (≈5:46–9:44)

"So the most important is the geometric series" (≈5:46). It matters because it is easy to decide whether it converges, and it can be used, through the tests, to decide whether other series converge (≈5:46–6:34). The series is

$$\sum_{i=0}^{\infty} c^i ,$$

for a real number $c$: "you multiply it with itself i times, where i runs from 0 to infinity. And when i is zero, this is meant to be 1" (≈7:26). It converges if $\vert c \vert \lt 1$, "And when it is, this here is the limit" (≈8:13): the limit is $\frac{1}{1-c}$, derived in Lecture 7. The notes: "Convergent precisely when $\vert c \vert \lt 1$" (notes p. 1; the notes print the summand as $c^{i}n$, a slip for $c^i$).

**Divergence** (≈8:13–8:59; board only). If $c = 1$, every term is $1$, "But that does not go to 0. So that's clearly diverging" (≈8:13). If $c = -1$, the terms alternate between $1$ and $-1$, so again they do not go to $0$ (≈8:13). And if $\vert c \vert \gt 1$ the terms are "even blowing up. It becomes larger and larger in absolute value" (≈8:59). So the series diverges whenever $\vert c \vert \geq 1$, by the first check above. Lecture 7 proved the same with consecutive partial sums.

The formula for the limit came from "this little trick", multiplying by $1 - c$ (Lecture 7), "a trick that goes back, I think, certainly to the ancient Greeks" (≈8:59). See [the geometric series](geometric-series.md).

## The harmonic series and the series of $\frac{1}{n^{\alpha}}$ (≈9:44–12:09)

The harmonic series

$$\sum_{n=1}^{\infty} \frac{1}{n}$$

is divergent, as shown last time (≈10:30; notes p. 1, "This series is divergent"; the notes print the sum over $i$ of $\frac{1}{n}$, an index slip). It "sits inside a larger family of series" (≈9:44):

$$\sum_{n=1}^{\infty} \frac{1}{n^{\alpha}} , \qquad \alpha \geq 1$$

(≈10:30). For $\alpha = 1$ this is the harmonic series, which diverges. Lecture 7 proved that the case $\alpha = 2$ converges, "But in fact, you can prove that for any alpha strictly bigger than 1, it does converge" (≈11:16). The usual tool is "what's called the integral test", which comes in a later lecture (≈11:16). Neither the general statement nor the integral test is proved here, and the notes do not mention the family. See [the harmonic series](harmonic-series.md).

## Absolute convergence and the alternating harmonic series (≈12:09–19:30)

Most tests, "but again, not all", actually "determine really whether the series is what's called absolutely convergent" (≈12:09).

**Definition** (notes pp. 1–2; ≈12:09–12:56). A series $\sum_{n=0}^{\infty} a_n$ is **absolutely convergent** if the series $\sum_{n=0}^{\infty} \vert a_n \vert$ is convergent: the series "where you're slapping on absolute value" (≈12:56).

**Theorem** (notes p. 2; ≈12:56–13:52). "It is easy to see that absolute convergence implies convergence, but not the other way around" (≈13:52). The implication comes from the Cauchy convergence theorem, as proved last time (≈12:56; see [series](series.md#absolute-convergence)).

**The alternating harmonic series** (≈13:52–19:30; board only). The reason the converse fails is "what's called the alternating series" (≈13:52). The series

$$\sum_{n=1}^{\infty} \frac{(-1)^n}{n}$$

starts at $1$, not $0$, "because you're dividing by 0" (≈14:38). Colding first says $0$ and corrects himself. With absolute values its terms become $\frac{1}{n}$, so the series of absolute values is the harmonic series, which is divergent (≈14:38–15:28). It is nevertheless convergent. "We'll probably come back to that in a later lecture in a more general setting, but let me just explain this" (≈15:28).

The explanation is a picture of the partial sums on a line (≈15:28–18:44). Before summing you are at $0$. The first term is $-1$, so $s_1 = -1$ brings you down to $-1$ (≈16:21–17:08). The next term is $+\frac{1}{2}$, so $s_2$ brings you back towards $0$, "But you don't go as far up as you went down, because it's 1 over 2" (≈17:57). Then $s_3 = s_2 - \frac{1}{3}$ goes down again, but not as far down as before (≈17:57–18:44). Each step goes the other way and is shorter than the one before, so the partial sums swing back and forth in a shrinking interval. "And so you could make this more precise. It's quite easy. And this shows you that this series is converging" (≈18:44). This is "the basis for this alternating series test" (≈18:44). In words, the test needs the signs of the $a_n$ to alternate and "the absolute value goes to 0" (≈18:44). The test is not stated precisely, in the lecture or the notes, and the precise version of the argument is left for later. See [the harmonic series](harmonic-series.md#the-alternating-harmonic-series).

## Series of non-negative terms (≈19:30–21:58)

Suppose $a_n \geq 0$ for all $n$ (≈20:16). Then each partial sum is at most the next one, which adds one more non-negative term:

$$s_n \leq s_{n+1}$$

(≈20:16–21:03). So $s_n$ is a monotone non-decreasing sequence, and by the monotone convergence theorem it converges if and only if it is bounded from above (≈21:03). The notes state this as a theorem: a series of non-negative numbers $\sum_{i=0}^{\infty} a_i$ "is convergent if and only if the sequence $s_n$ is bounded from above" (notes p. 2). See [the monotone convergence theorem](monotone-convergence-theorem.md).

## Tests for convergence (≈21:58–22:46)

Once you have checked that $a_n$ goes to $0$ and still need to decide whether the series converges, "there are these number of tests" (≈21:58). This lecture covers the comparison test, the ratio test and the root test, "But there are other tests" (≈22:46). The notes list the same three, plus "Other tests that we will discuss later" (notes p. 2). See [convergence tests for series](convergence-tests-for-series.md).

## The comparison test, version 1 (≈22:46–34:40)

**Comparison test, version 1** (notes p. 2; ≈23:46–24:38). Suppose $a_n$ and $b_n$ are two sequences with

$$0 \leq a_n \leq b_n .$$

If $\sum_{n=1}^{\infty} b_n$ is convergent, then so is $\sum_{n=1}^{\infty} a_n$.

It is also used for divergence, "where you know that this series is divergent", and you conclude something about the other series from "just a negation of this statement" (≈24:38). The captions do not say which series is which. As the negation (contrapositive) of the test, it says that if the series of the $a_n$ diverges, so does the series of the $b_n$.

**Proof with Cauchy sequences** (≈24:38–29:17; board only, the notes give no proof). "So the proof here of that is actually easy" (≈24:38). By the Cauchy convergence theorem it is enough to show that the partial sums of the $a_n$ form a Cauchy sequence (≈25:24). Write

$$s_n^{a} = \sum_{i=1}^{n} a_i , \qquad s_n^{b} = \sum_{i=1}^{n} b_i ,$$

with "the superscript a just to denote that it's coming from the sequence" $a_n$ (≈26:12). For $m \lt n$ the difference is the sum of the terms from $a_{m+1}$ to $a_n$ (≈26:58). They are non-negative, so the absolute value signs "are really irrelevant" (≈28:31–29:17), and each term is at most the corresponding $b$:

$$\vert s_n^{a} - s_m^{a} \vert = a_{m+1} + \cdots + a_n \leq b_{m+1} + \cdots + b_n = s_n^{b} - s_m^{b}$$

(≈26:58–29:17). Since $\sum b_n$ converges, the right side can be made as small as we want by taking $m$ and $n$ large enough (≈29:17). So $s_n^{a}$ is a Cauchy sequence, and it converges. □ Getting from the convergence of $\sum b_n$ to a small right side uses the direction "convergent implies Cauchy" again.

**A student's question: why Cauchy sequences?** (≈27:45–28:31.) A student asked whether Cauchy sequences are used here as motivation, and recalled the original definition of convergence, with the absolute value of $a_n$ minus a limit (≈27:45). Colding: "So if you went all the way back to the definition, then you would have to determine what the limit was", which we do not know. Knowing the limit of the series of the $b_n$ does not tell you the limit of the series of the $a_n$ (≈27:45–28:31). "So the advantage with Cauchy sequence is that you don't have to figure out what the limit is" (≈28:31). He added that here "I should probably have done it using the monotone convergence theorem. But you can do that as an exercise" (≈28:31), and then sketched that proof anyway.

**Proof with the monotone convergence theorem** (≈29:17–30:48; board only). Each partial sum of the $a_n$ is at most the corresponding partial sum of the $b_n$, $s_n^{a} \leq s_n^{b}$ (≈30:03). The $s_n^{b}$ converge, so they are bounded by some real number $c$, for all $n$ (≈30:03–30:48). So the $s_n^{a}$ are a monotone increasing sequence bounded by $c$, and they converge (≈30:48). □ At this point the captions have Colding call it a sequence "that is not bounded from above"; the argument needs bounded from above (marked in the transcript). "So you can do it either of those two ways" (≈30:48).

**Example** (notes p. 2; ≈31:34–34:40). Is

$$\sum_{n=1}^{\infty} \frac{2^{-n}}{n}$$

convergent? "So this is typically how it works" (≈31:34): you have to find the comparison series yourself. Set

$$a_n = \frac{2^{-n}}{n} , \qquad b_n = 2^{-n} .$$

Then $0 \leq a_n \leq b_n$ (≈32:22), and the series of the $b_n$ is a convergent geometric series with $c = \frac{1}{2}$ (≈33:09). So "the sequence a n that was squeezed between that and 0 was also convergent" (≈33:55), by the comparison test. The notes give the same example with the same $a_n$ and $b_n$ (notes p. 2). On the board $a_n$ is first spoken as "2 to minus n over 2" (≈32:22), against $\frac{2^{-n}}{n}$ in the notes, and the ratio $\frac{1}{2}$ is captioned "1.5" (≈33:09); both are marked in the transcript.

## The comparison test, version 2 (≈34:40–40:30)

"Here is another more fancy version of comparing" (≈34:40).

**Comparison test, version 2** (notes p. 3). Suppose $a_n$ and $b_n$ are two sequences with $b_n \neq 0$ and

$$\lim_{n \to \infty} \frac{a_n}{b_n} = L \neq 0 .$$

Then $\sum_{n=1}^{\infty} a_n$ is convergent if and only if $\sum_{n=1}^{\infty} b_n$ is.

On the board (≈35:26–37:19), none of the $b_n$ is $0$, and the ratio $\frac{a_n}{b_n}$ converges to some $L$ that "is not 0 and is not infinity. I mean that it really is a limit" (≈36:17). Colding also takes the $a_n$ and $b_n$ to be non-negative numbers (≈36:17), which the notes do not say. Where the sum starts does not matter here: "what the sum is matters where you're starting, but whether or not it converges doesn't matter where you start" (≈35:26). The test is not proved, on the board or in the notes.

**Example** (notes p. 3; ≈37:19–40:30). The series

$$\sum_{n=2}^{\infty} \frac{1}{n^2 - 1}$$

starts at $2$ to make sure you are "not dividing by 0" (≈37:19). The first thing to observe is that its terms go to $0$. The second is that it is very close to $\sum \frac{1}{n^2}$, which converges (Lecture 7) (≈38:04). But the first comparison test does not apply directly, because $n^2 - 1$ is smaller than $n^2$: each term is "actually bigger than 1 over n squared" (≈38:04). "You could still use the first test", but it takes more work (≈38:53). Instead set

$$a_n = \frac{1}{n^2 - 1} , \qquad b_n = \frac{1}{n^2} .$$

Then, dividing numerator and denominator by $n^2$,

$$\frac{a_n}{b_n} = \frac{n^2}{n^2 - 1} = \frac{1}{1 - \frac{1}{n^2}} \to 1$$

by the algebraic rules for limits, since $\frac{1}{n^2} \to 0$ (≈38:53–39:42; see [algebraic properties of limits](algebraic-properties-of-limits.md)). The limit $1$ is "neither zero nor infinity" (≈39:42). So the series converges if and only if $\sum \frac{1}{n^2}$ does, and that one converges (≈40:30). The notes give the same example in one line: the series is convergent since $\frac{n^2}{n^2 - 1} \to 1$ and the series $\sum_{n=2}^{\infty} \frac{1}{n^2}$ is convergent (notes p. 3).

## The ratio test (≈40:30–56:33)

"I mean, the comparison tests are typically almost the easiest tests. But this one here is extremely useful" (≈40:30). Both the ratio test and the root test "are based on comparison with the geometric series. And so this is explaining why the geometric series is so crucial" (≈41:18). Unlike the comparison test, the ratio test needs no second series: "You don't have to look at any other series" (≈42:05).

**Ratio test** (board, ≈42:05–45:18). Take a series $\sum a_n$ with all $a_n \neq 0$ (≈48:26), and look at the ratio of two consecutive terms in absolute value. Suppose the limit

$$\lim_{n \to \infty} \left\vert \frac{a_{n+1}}{a_n} \right\vert = a$$

exists (≈42:05–42:55). Then:

1. If $a \lt 1$, the series is convergent.
2. If $a \gt 1$, the series is divergent.
3. If $a = 1$, the test is inconclusive.

(≈43:40–44:26.) It is important to remember that you get nothing out of the test "if you are in the unlucky case where this limit is 1" (≈44:26). "And I should also emphasize that it is crucial to have a limit" (≈44:26); what to do when there is none comes later (≈1:19:46).

**The notes' statement** (notes p. 3): "Let $a_n \geq 0$ and assume that" $\frac{a_{n+1}}{a_n} \to a$, with the same three cases. The notes give no proof. Their two examples show case 3. For $a_n = \frac{1}{n}$ and for $a_n = \frac{1}{n^2}$ the ratio tends to $1$, "so the test is inconclusive", although the first series is divergent and the second convergent (notes pp. 3–4; both decided in Lecture 7).

**Proof of case 1, sketched** (≈45:18–52:36). "And I'll just sketch the proof" (≈46:08). Choose a number between $a$ and $1$. Colding first calls it $a_0$, then renames it: "Let's call it alpha to make it just look much more distinct" (≈48:26). So $a \lt \alpha \lt 1$ (≈46:54). Since the ratio converges to $a$, which is strictly less than $\alpha$, there is an $N$ such that for $n \geq N$

$$\left\vert \frac{a_{n+1}}{a_n} \right\vert \lt \alpha , \qquad \text{that is} \qquad \vert a_{n+1} \vert \leq \alpha \vert a_n \vert$$

(≈47:40–48:26). Far enough out, "the next one is a fraction of the previous one" (≈49:17). Apply this at $n = N$ and at $n = N + 1$:

$$\vert a_{N+1} \vert \leq \alpha \vert a_N \vert , \qquad \vert a_{N+2} \vert \leq \alpha \vert a_{N+1} \vert \leq \alpha^2 \vert a_N \vert$$

(≈49:17–51:01). Continuing,

$$\vert a_{N+m} \vert \leq \alpha^m \vert a_N \vert$$

for all $m$ (≈51:01; the captions use the letters $n$ and $m$ for the same index here). The right side is a fixed constant $\vert a_N \vert$ times the terms of a convergent geometric series. "So the tail is bounded by a convergent geometric series" (≈51:49), and the first comparison test shows that the series converges (≈51:49). □ The comparison bounds the $\vert a_n \vert$, so what it shows directly is absolute convergence, which implies convergence; Colding says this in the root test's proof (≈1:03:20).

**Proof of case 2** (≈52:36–54:57). Now $a \gt 1$, and choose $\alpha$ with $1 \lt \alpha \lt a$ (≈53:22). Far enough out the ratio exceeds $\alpha$, so $\vert a_{n+1} \vert \gt \alpha \vert a_n \vert$ with $\alpha \gt 1$ (≈53:22–54:09). From some fixed stage on, the terms get larger and larger in absolute value, "So they don't converge to 0 as they were supposed to" (≈54:57), and the series diverges by the first check. □

**Case 3** has nothing to prove, "because it leaves open both possibilities" (≈54:57).

**A student's question: must the terms decrease?** (≈54:57–56:33.) A student asked whether case 1 assumes the sequence is monotonically decreasing. Colding: no, there is no such assumption, "But I could alternate signs and things like that" (≈55:45). What the test compares with is a convergent geometric series, where "the next element is some fixed fraction of the previous one" (≈55:45). "So you're right that in order for the ratio test to give you convergence", sufficiently far out the absolute values of the terms must be going down (≈55:45–56:33).

## The root test (≈56:33–1:08:23)

The root test is also based on comparison with the geometric series, but it does not compare consecutive terms (≈56:33). It allows a term to be larger than the one before. The terms cannot keep going up, but one can jump up, and then they go down for a while, and then maybe another jumps up a little (≈57:19). "And the root test is OK with that, whereas that test wasn't OK with that" (≈57:19).

**Root test** (board, ≈57:19–59:46). For a series $\sum a_n$, take the $n$-th root of the absolute value of the terms, $\vert a_n \vert^{\frac{1}{n}}$, and suppose it has a limit (≈58:05–58:50):

$$\lim_{n \to \infty} \vert a_n \vert^{\frac{1}{n}} = c .$$

Then, with "the same three parts" as the ratio test (≈58:50):

1. If $c \lt 1$, the series is convergent.
2. If $c \gt 1$, the series is divergent.
3. If $c = 1$, the test is inconclusive.

(≈58:50–59:46.)

**The notes' statement** (notes p. 4). "Let $a_n \geq 0$ be a sequence of non-negative numbers. Suppose $\lim_{n \to \infty} (a_n)^{\frac{1}{n}} = r$." If $r \lt 1$, then $\sum_{n=0}^{\infty} a_n$ is convergent; if $r \gt 1$, it is divergent; if $r = 1$, "then it is inconclusive". This is the one test the notes prove.

**Proof of case 1** (≈59:46–1:04:09; notes p. 4). Choose $c_0$ with $c \lt c_0 \lt 1$ (≈1:00:37). Because $\vert a_n \vert^{\frac{1}{n}}$ converges to $c$, which is strictly less than $c_0$, there is an $N$ such that for $n$ larger than $N$

$$\vert a_n \vert^{\frac{1}{n}} \leq c_0$$

(≈1:00:37–1:01:28). The captions give the reason only as $c_0$ being strictly bigger than $c$ (≈1:01:28). Taking the $n$-th power of both sides,

$$\vert a_n \vert \leq c_0^n$$

(≈1:01:28–1:02:22). "But that's already great" (≈1:02:22). From $N$ on, the $\vert a_n \vert$ are compared with the terms of the geometric series $\sum c_0^n$, which converges because $0 \lt c_0 \lt 1$. By the first comparison test the series converges (≈1:02:22–1:03:20). More precisely, the comparison was made with absolute values, so what is proved is that the original series is absolutely convergent, "But absolute convergence implies convergence. So you're actually proving absolute convergence" (≈1:03:20–1:04:09). □

The notes write the same proof with $r \lt r_0 \lt 1$: for $n \geq N$, $(a_n)^{\frac{1}{n}} \leq r_0$, "Therefore, $0 \leq a_n \leq r_0^n$", and "by the first version of the comparison test" the series converges (notes p. 4).

**Proof of case 2** (≈1:04:09–1:07:35; notes p. 4). Now $c \gt 1$; choose $c_0$ with $1 \lt c_0 \lt c$ (≈1:04:56–1:05:44). Far enough out the $n$-th root exceeds $c_0$, and taking $n$-th powers, $\vert a_n \vert \gt c_0^n$ (≈1:05:44–1:06:38). Since $c_0 \gt 1$, the right side goes to infinity, so the terms do not go to $0$ and the series diverges (≈1:06:38). Here the series "fails dramatically to be convergent" (≈1:04:09). □ The notes argue instead by comparison: for $n \geq N$, $a_n \geq r_0^n$, where $\sum r_0^n$ is a divergent geometric series, "Therefore, by the comparison test the original series is divergent" (notes p. 4).

**Case 3** again has nothing to prove (≈1:04:09). Neither the lecture nor the notes give an example of it for the root test.

**A question** (≈1:07:35–1:08:23). A student's question at ≈1:07:35 is inaudible in the captions. In his answer Colding recapitulates. In case 1 the proof shows the series is absolutely convergent, and in case 2 that it is divergent. In case 2 the terms do not merely fail to go to $0$, as a convergent series requires; in absolute value they go to infinity. "So it's very, very far from being convergent" (≈1:08:23).

## Power series (≈1:07:35–1:19:46)

**The first example** (≈1:07:35–1:09:12). The geometric series, with the number now called $x$ instead of $c$ (≈1:07:35):

$$\sum_{n=0}^{\infty} x^n = \frac{1}{1 - x}$$

(notes p. 4). It converges when $\vert x \vert \lt 1$, "And in that case, the sum here is just this familiar function" (≈1:09:12).

**Definition** (≈1:09:12–1:10:50; notes p. 5). Given a sequence $a_n$, the **power series** is

$$\sum_{n=0}^{\infty} a_n x^n ,$$

where $a_n$ is "the coefficient to the x to the power n" (≈1:10:04). "So if you will, this is like an infinite polynomial, a polynomial of infinite degree" (≈1:10:04). The notes call this the "Formel definition" (a printed slip for formal), with coefficients $c_n$: "Let $c_n$ be a sequence, then $\sum_{n=0}^{\infty} c_n x^n$ is a power series" (notes p. 5).

**Familiar functions** (≈1:10:50–1:11:38; notes pp. 4–5). "So a lot of the basic functions can be represented by power series" (≈1:10:50). Besides $\frac{1}{1-x}$:

$$\exp x = \sum_{n=0}^{\infty} \frac{x^n}{n!} ,$$

$$\cos x = \sum_{n=0}^{\infty} (-1)^n \frac{x^{2n}}{(2n)!} ,$$

$$\sin x = \sum_{n=0}^{\infty} (-1)^n \frac{x^{2n+1}}{(2n+1)!}$$

(notes pp. 4–5; ≈1:10:50–1:11:38). None of this is proved here. Of the exponential function Colding says "we'll come back and discuss this more" (≈1:10:50) and "we haven't proven that yet. But we'll talk about that next time" (≈1:14:58). The notes pose the question "Why does it give familiar functions?" (in blue) and answer: "We will answer the second question next time for the exponential function" (notes p. 5).

**Not every function has a power series** (≈1:11:38–1:12:23; board only). "And lots of functions have a power series representation. But it's not every function" (≈1:11:38). Colding draws a function "that starts off being dead zero and now it's becoming interesting" (≈1:12:23); the captions do not say what the curve is. It "does not have a power series. Even locally does not have a power series" (≈1:12:23). The reason: "a power series is an example of something that's called an analytic function. And this here is not an analytic function" (≈1:12:23). "But I'm not going to prove to you that it doesn't" (≈1:12:23).

**For which $x$ does a power series converge?** (≈1:13:11–1:13:57.) Given a sequence $a_n$ and its power series, "the first question that comes to mind is", for which $x$ does the series converge (≈1:13:11). "So this is like the most basic thing" (≈1:13:57). The notes ask the same question in red, "When does a power series converge?", and answer that it "comes from the root test or the ratio test" (notes p. 5). Earlier Colding had called the question one "which turned out to be quite subtle" (≈1:10:04).

**Example: $\sum x^n$** (≈1:13:57–1:14:58; notes p. 5). For each fixed $x$ this is a geometric series, so it converges when $\vert x \vert \lt 1$ and diverges otherwise (≈1:14:58). The notes: "This series is convergent for $\vert x \vert \lt 1$ and divergent otherwise" (notes p. 5).

**Example: $\sum \frac{x^n}{n!}$** (≈1:14:58–1:19:46; notes p. 5). For which $x$ does the series of the exponential function converge? Think of $x$ as fixed and apply one of the tests; "the natural one is either the root test or the ratio test" (≈1:15:48), and Colding uses the ratio test. At $x = 0$ the first term is $x^0 = 1$, "by definition", and every other term is $0$, so "it's definitely converging when x is equal to 0" (≈1:15:48–1:16:36). For $x \neq 0$, write the terms as

$$b_n = \frac{x^n}{n!}$$

(≈1:16:36; the board calls them $b_n$ here, the notes $a_n$). Colding takes the absolute value of the ratio of consecutive terms (≈1:16:36–1:17:23). Dividing by a fraction flips it upside down, so

$$\frac{b_{n+1}}{b_n} = \frac{x^{n+1}}{(n+1)!} \cdot \frac{n!}{x^n} = \frac{x}{n+1} ,$$

because $n$ of the $n + 1$ factors $x$ cancel against $x^n$, and $(n+1)! = (n+1) \thinspace n!$ (≈1:17:23–1:18:56). For each fixed $x$ this goes to $0$ as $n$ goes to infinity (≈1:18:56). The limit exists and is $0$, which is less than $1$, "So it's definitely fallen under 1. So it's convergent" (≈1:18:56). So the series converges for every $x$.

The notes' computation (notes p. 5): with $a_n = \frac{x^n}{n!}$,

$$\frac{a_{n+1}}{a_n} = \frac{n! \thinspace x^{n+1}}{(n+1)! \thinspace x^n} = \frac{x}{n+1} \to 0 .$$

"It follows that the power series is convergent for all $x$" (notes p. 5). The notes do not take absolute values, although their ratio test is stated for $a_n \geq 0$, and these terms are negative for some negative $x$.

**Question: for all $x$?** (≈1:20:33.) A student asked, "That means for all x, right, you're saying?" Colding: "This is for all x. But think about x as being fixed." You fix one $x$ and let $n$ go to infinity, and the conclusion holds for every $x$ (≈1:20:33). "Then you can ask, how does it vary in x? But that's a different story" (≈1:20:33).

See [power series](power-series.md).

## Where the lecture ends, and what is next (≈1:19:46)

"I posted already my lecture notes. There's a little bit more. And I'll probably talk about that next time" (≈1:19:46). The material left is $\limsup$ and $\liminf$. They answer a gap in the two tests just proved, which both assume that the ratio or the $n$-th root has a limit: "But what if it doesn't have a limit? And so it's dealing with that case" (≈1:19:46).

## From the notes only: $\limsup$ and the radius of convergence (notes pp. 6–7)

The lecture does not reach this part of the notes; Colding says he will start with it next time (≈1:19:46). None of it is proved in the notes.

"To talk about convergence of a general power series we need the notion of lim sup … of a sequence" (notes p. 6).

**$\limsup$** (notes p. 6). Let $a_n$ be a sequence. If it is not bounded from above, set $\limsup a_n = \infty$. Otherwise define

$$b_n = \sup \lbrace a_n, a_{n+1}, a_{n+2}, \cdots \rbrace .$$

Since the $a_n$ are bounded from above, the $b_n$ are real numbers, and the sequence $b_n$ is decreasing:

$$b_n = \sup \lbrace a_n, a_{n+1}, a_{n+2}, \cdots \rbrace \geq \sup \lbrace a_{n+1}, a_{n+2}, \cdots \rbrace = b_{n+1}$$

"(For $b_{n+1}$ supremum is taken over a smaller set.)" (notes p. 6). Since $b_n$ is decreasing, "it is converging with limit $b$ that possibly could be $-\infty$ if the sequence $b_n$ is not bounded from below" (notes p. 6). Then

$$\limsup_{n \to \infty} a_n = \lim_{n \to \infty} b_n = b .$$

The $b_n$ are the $\sup$ of the tails of the sequence. This is Lecture 5's board construction, which Colding then said "is how one defines limsup and liminf" (Lecture 5, ≈1:07:23–1:08:10; see [the monotone convergence theorem](monotone-convergence-theorem.md)). The notes do not define $\liminf$. See [limsup and liminf](limsup-and-liminf.md).

**Radius of convergence** (notes pp. 6–7). For a power series $\sum_{n=0}^{\infty} a_n x^n$ set

$$R = \frac{1}{\limsup_{n \to \infty} \vert a_n \vert^{\frac{1}{n}}} ,$$

the **radius of convergence**. By convention, if $\limsup_{n \to \infty} \vert a_n \vert^{\frac{1}{n}} = 0$ then $R = \infty$, and if it is $\infty$ then $R = 0$. "From the root test one can now show the following": the power series converges if $\vert x \vert \lt R$ and diverges if $\vert x \vert \gt R$ (notes p. 6; printed "in convergent"). The case $\vert x \vert = R$ "has to be examined on a case by case basis" (notes p. 7). The notes give no proof and no example. For the two examples above, $\sum x^n$ converges exactly for $\vert x \vert \lt 1$ and $\sum \frac{x^n}{n!}$ for all $x$. The notes do not compute $R$ for either.

## Board versus notes

Where they differ, this page follows the notes and gives the board's version with its timestamp. Collected here:

- **The first check on the terms.** Board only: from the Cauchy convergence theorem with $m = n - 1$ (≈2:27–5:46).
- **The geometric series.** Board: diverges for $c = 1$, $c = -1$ and $\vert c \vert \gt 1$ because the terms do not go to $0$ (≈8:13–8:59). Notes: "Convergent precisely when $\vert c \vert \lt 1$", with no argument, and the summand printed $c^{i}n$ (p. 1).
- **The family $\sum \frac{1}{n^{\alpha}}$, the alternating harmonic series and the alternating series test.** Board only (≈9:44–19:30).
- **Comparison test, version 1.** Board: two proofs, with Cauchy sequences and with the monotone convergence theorem, and its use for divergence (≈24:38–30:48). Notes: statement and example, no proof (p. 2).
- **Comparison test, version 2.** Board: $a_n$ and $b_n$ non-negative, $L$ "not 0 and is not infinity" (≈36:17); the example worked out, with why version 1 does not apply directly (≈38:04–40:30). Notes: $b_n \neq 0$ and $L \neq 0$, no non-negativity; the example in one line (p. 3).
- **Ratio test.** Board: absolute values $\vert \frac{a_{n+1}}{a_n} \vert$ with $a_n \neq 0$, and a sketched proof of cases 1 and 2 (≈42:05–54:57). Notes: $a_n \geq 0$, no proof, two examples of the inconclusive case (pp. 3–4).
- **Root test.** Board: $\vert a_n \vert^{\frac{1}{n}} \to c$, with $c_0$ in the proof; case 2 because the terms go to infinity (≈58:05–1:07:35). Notes: $a_n \geq 0$, $(a_n)^{\frac{1}{n}} \to r$, with $r_0$; case 2 by comparison with a divergent geometric series (p. 4).
- **Power series.** Board: coefficients $a_n$ (≈1:10:04), a function with no power series (≈1:12:23), the terms of the exponential series called $b_n$ with absolute values (≈1:16:36–1:17:23), and the case $x = 0$ (≈1:15:48). Notes: the "Formel definition" with $c_n$, the two coloured questions, $a_n = \frac{x^n}{n!}$ without absolute values (pp. 4–5).
- **$\limsup$ and the radius of convergence.** Notes only (pp. 6–7).

## Where the lecture stops

The tests now available are the first check on the terms, the comparison test in two versions, the ratio test and the root test. The first version of the comparison test and the ratio and root tests are proved; the second version of the comparison test is not. Several things are used without proof or left for later. These are: that a convergent sequence is Cauchy (for the check on the terms, ≈4:11–5:46, and the first proof of the comparison test, ≈29:17), still without a proof in this knowledge base; the convergence of $\sum \frac{1}{n^{\alpha}}$ for $\alpha \gt 1$ and the integral test (≈11:16); the precise alternating series test (≈15:28, ≈18:44); that the power series give $\exp$, $\cos$ and $\sin$ (≈1:14:58); the function with no power series (≈1:12:23); and, from the notes, the theorem on the radius of convergence. On the OCW lecture list, Lecture 9 is "Limsup and Liminf; Power Series; Continuous Functions; Exponential Function" (TBB Sections 2.13, 10.2, 5.4 and 5.5), which is not yet in this knowledge base.

## Related pages

- [Convergence tests for series](convergence-tests-for-series.md): all the tests so far, with this lecture's proofs.
- [Series](series.md): partial sums, the check on the terms, series of non-negative terms and absolute convergence.
- [The geometric series](geometric-series.md): the series every test here is compared with.
- [The harmonic series](harmonic-series.md): the family $\sum \frac{1}{n^{\alpha}}$ and the picture of the alternating harmonic series.
- [Power series](power-series.md): the definition, the familiar functions, and convergence by the ratio test.
- [Limsup and liminf](limsup-and-liminf.md): the notes' definition of $\limsup$ and Lecture 5's construction behind it.
- [Cauchy sequences](cauchy-sequences.md): the Cauchy convergence theorem behind the check on the terms and the first proof of the comparison test.
- [The monotone convergence theorem](monotone-convergence-theorem.md): series of non-negative terms and the second proof of the comparison test.
- [Algebraic properties of limits](algebraic-properties-of-limits.md): used in the example of the second comparison test.
- [Lecture 7 — Bolzano–Weierstrass Theorem; Cauchy Sequences; Series](07-bolzano-weierstrass-theorem-cauchy-sequences-series.md): the previous lecture, which started series.
