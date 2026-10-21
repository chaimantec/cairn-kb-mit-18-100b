# Lecture 3 — How to Write a Proof; Archimedean Property

**18.100B Real Analysis, Spring 2025 · Tobias Holck Colding · [video](https://www.youtube.com/watch?v=QJ96fO8Eef4) (80 min)**

Sources for this page: the [edited transcript](../raw/transcripts/03-how-to-write-a-proof-archimedean-property.md) (timestamps below are written ≈M:SS and point into it), the course's typed [lecture notes](../raw/notes/03-how-to-write-a-proof-archimedean-property.md) for this lecture (cited "notes p. N"; [PDF on OCW](https://ocw.mit.edu/courses/18-100b-real-analysis-spring-2025/mit18_100b_s25_lec03.pdf)), and the OCW readings list, which assigns Section 1.7 of Thomson, Bruckner and Bruckner, *Elementary Real Analysis* (TBB) to this lecture. Colding teaches from the blackboard; there are no slides.

## What this lecture establishes

Lecture 2 proved that $\sqrt{2}$ is a real number and proved the Archimedean property, but, Colding says, it did so the way you work a problem out on scrap paper. This lecture is about **how to write a proof** that you would hand in or show to somebody. It first completes the vocabulary of bounds. **Lower bounds** join upper bounds, the least upper bound of a set $A$ gets its name, $\sup A$, and the greatest lower bound is $\inf A$ (notes p. 1). Colding stresses that a bound lives in the surrounding ordered set, not necessarily in $A$, and that changing the surrounding set can change whether $A$ is bounded at all. The lecture then rewrites two results from Lecture 2 as formal proofs: that **there is an $\alpha \gt 0$ with $\alpha^2 = 2$**, with the auxiliary number $h$ defined up front (notes pp. 2–3), and the **Archimedean property**, stated as the theorem that $\mathbf{N}$ is not bounded from above (notes p. 4). It ends by defining a **sequence** of real numbers as a function from $\mathbf{N}$ to $\mathbf{R}$ (notes p. 5).

The notes go further than the video. They also prove that for every $\epsilon \gt 0$ there is a natural number $n$ with $\frac{1}{n} \lt \epsilon$, give two more examples of sequences, and define what it means for a sequence to converge (notes pp. 4–5). The lecture leaves limits for next time.

Notation: as in Lectures 1 and 2, the notes set the number systems in bold, $\mathbf{N}$, $\mathbf{Q}$, $\mathbf{R}$, and an ordered set as $\mathbf{S}$; this page follows them. In this course $\mathbf{N} = \lbrace 1, 2, 3, \cdots \rbrace$ starts at $1$.

## Notes, course information and textbooks (≈0:00–4:48)

Colding opens with how to use the course materials. He writes the lecture notes a couple of days in advance and goes over them on the day to catch typos. His advice: "if I were you, I would first read the lecture notes that I post after the lectures" (≈1:35). The last page of the course information lists each lecture's date with some key words from it. He posts it in advance and revises it afterwards, so it is "only a sort of approximation" of what a lecture will cover (≈1:35–4:48).

The references on that page will be to the main textbook, TBB, only. Colding calls Rudin's *Principles of Mathematical Analysis* "a great book", "a classic in the subject", "a book that was created here a long time ago", and more formal than TBB, which is more accessible "and so it might actually be better the first time you learn it". He deleted his references to Rudin but encourages students to look at it, and at the chapters the course skips (≈2:22–4:48). Later in the lecture he adds the difference in approach. TBB, like his lectures, motivates things from $\mathbf{R}$ and abstracts afterwards, whereas Rudin "starts with the abstraction, and then it specializes to R" (≈14:56–15:42).

## Upper and lower bounds (≈3:55–15:42)

The lecture starts from the theorem of Lecture 2, taken for granted in the course, that $\mathbf{R}$ is a complete ordered field (≈3:55–4:48). The notes open with the full theorem, that $\mathbf{R}$ "is a complete ordered Field that contains $\mathbf{Q}$" (notes p. 1).

**Definitions** (≈4:48–6:39; notes p. 1). Let $A$ be a subset of $\mathbf{R}$.

- $A$ is **bounded from above** if there is an $M$ in $\mathbf{R}$ such that $a \leq M$ for all $a \in A$. Such an $M$ is an **upper bound** for $A$.
- $A$ is **bounded from below** if there is an $m$ in $\mathbf{R}$ such that $m \leq a$ for all $a \in A$. Such an $m$ is a **lower bound** for $A$.
- Said without qualification, **bounded** means bounded from above and from below (≈8:12).

The notes state the definitions for a non-empty subset $A$ of an ordered set $\mathbf{S}$, which "is said to have an upper bound" or "to have a lower bound". On the board the lower-bound inequality is said aloud as "less than" when it is first defined (≈6:39) and as "less or equal" when the greatest lower bound is defined (≈18:56); the notes print $m \leq a$.

At the end of Lecture 2 a student asked why only upper bounds had been defined. This lecture defines lower bounds directly, and Colding calls the two notions "a symmetric property" (≈19:42). He does not come back to the remark about complements that he made in answer to the question.

### Where a bound lives (≈6:39–9:48)

Several students had asked on Piazza in which set $M$, or $m$, has to be. The answer is that **an upper bound does not need to be in $A$** (≈7:26). The example is the open interval $(0, 1)$, which contains everything between $0$ and $1$ but contains neither $0$ nor $1$. As a subset of $\mathbf{R}$ it is bounded. Every $x$ in it satisfies $x \leq 1$, in fact $x \lt 1$, so $1$ is an upper bound, but no element of the interval is an upper bound for it. "The upper bound is outside the set. But it is in all of R. And that's fine." An upper bound will typically be in the larger set, and the same goes for lower bounds (≈8:12–9:48).

### The surrounding set matters (≈9:48–15:42)

Apart from the theorem about $\mathbf{R}$, none of this needs $\mathbf{R}$: the definitions make sense in any ordered set (≈9:01–11:32). If $\mathbf{S}$ is an ordered set and $A$ a subset of $\mathbf{S}$, then $A$ is bounded from above if there is an $M$ in $\mathbf{S}$ with $a \leq M$ for all $a \in A$. Again $M$ need not be in $A$, only in the larger set.

The example, which Colding warns may seem counterintuitive (≈11:32–14:08): let $\mathbf{S}$ be the half line of real numbers between $0$ and infinity, not including $0$, and let $A$ be the interval from $0$ to $1$ inside it. You know the ordering from $\mathbf{R}$, "but forget about it": only the ordered set $\mathbf{S}$ counts. Then $A$ is bounded from above, since every $a \in A$ is less than $1$ and $1$ is in $\mathbf{S}$. But **as a subset of $\mathbf{S}$, $A$ is not bounded from below**, because a lower bound would have to be in $\mathbf{S}$, and "0 is not in this set, and no negative numbers in this set" (≈13:10). As a subset of the real line, of course, $A$ is bounded from below.

Two clarifications followed (≈14:08–15:42). Infinity and minus infinity are not real numbers. And a student asked whether the sets in a homework question should be taken as subsets of $\mathbf{R}$. If the problem does not say what the larger set is, assume it is $\mathbf{R}$, "because we're going to concentrate mostly on R". The notes say the same: "From now on we will concentrate of the case of $\mathbf{R}$" (notes p. 1, with a printed slip, "of" for "on").

## Completeness, $\sup$ and $\inf$ (≈15:42–22:52)

**Completeness** (≈15:42–17:24). An ordered set $\mathbf{S}$ is complete if every subset of $\mathbf{S}$ that is bounded from above has a least upper bound. The notes put it as "Completeness is the property that every bounded non-empty subset has a least upper bound" (notes p. 1).

**Supremum** (≈17:24–18:11; notes p. 1). The least upper bound of $A$ is written $\sup A$. If $M = \sup A$, then

1. $a \leq M$ for all $a \in A$, and
2. if $M_1$ is another upper bound for $A$, then $M \leq M_1$.

**Infimum** (≈18:11–19:42; notes p. 1). Similarly, the **greatest lower bound** of a set $A$ that is bounded from below is written $\inf A$. If $m = \inf A$, then

1. $m \leq a$ for all $a \in A$, and
2. if $m_1$ is another lower bound for $A$, then $m_1 \leq m$.

The notes define it as "a lower bound that is greater or equal to all other lower bounds". On the board Colding concludes that since $\mathbf{R}$ is complete, every bounded subset of $\mathbf{R}$ has both a least upper bound and a greatest lower bound (≈19:42). Neither the board nor the notes derive the existence of the greatest lower bound from the least upper bound property; the board presents it as the symmetric counterpart. Finally, $\sup A$ and $\inf A$ are in general not elements of $A$: "they could be. But in general, they wouldn't be" (≈19:42). See [supremum and infimum](supremum-and-infimum.md).

### Is the half line complete? (≈19:42–22:52)

A student asked about the earlier example, the half line $\mathbf{S}$ without $0$, and whether it is complete. The question is mostly inaudible in the captions. Colding's answer: if a subset $A$ of $\mathbf{S}$ is bounded from below in $\mathbf{S}$, then $A$ cannot have numbers approaching $0$, and then it would have a greatest lower bound (≈21:16). He says he is not going to prove that anything is or is not complete, but "it's pretty convincing that it is actually complete, in this sense". There is another sense in which it is not complete, and the course will later talk about "maybe some other notion of completeness" (≈21:16–22:07). The lecture does not say which notion.

## Why write a formal proof (≈22:07–25:18)

How to write a mathematical proof is "a super important thing to learn in this class". It may seem like a formal thing, "Why bother with that? But it's really, really useful. And the more complicated things become, the more useful it is" (≈22:07–22:52). Colding illustrates it by writing out formally two results already proved in Lecture 2, so that the class can focus on how to write the proof rather than on why the statement is true (≈22:52, ≈1:08:27–1:09:15).

What Lecture 2 did for $\sqrt{2}$ was the idea: what you would be writing on a piece of scrap paper. If you were handing the proof in, or showing it to somebody, you would write it the way this lecture does (≈23:41–24:27). He warns that "a formal proof doesn't necessarily make for a great lecture, because it's kind of formal" (≈24:27). The example is very simple, but it should give an idea of what to do, and it is a skill "you're bound to use in many other classes later on" (≈24:27). See [writing proofs](writing-proofs.md).

## A formal proof that $\sqrt{2}$ is real (≈25:18–1:08:27)

### The statement and the set (≈25:18–26:51)

$\sqrt{2}$ was the number that is positive and squares to $2$ (≈25:18). So the theorem that $\sqrt{2}$ is a real number, written more formally, is the following.

**Theorem** (notes p. 2; ≈26:03). There exists $\alpha \gt 0$ such that $\alpha^2 = 2$.

On the board the statement is that there exists $\alpha \in \mathbf{R}$ with $\alpha \gt 0$ and $\alpha^2 = 2$. The proof uses the set (notes p. 2; ≈26:03–26:51)

$$A = \lbrace x \in \mathbf{R} \vert x \gt 0 \text{ and } x^2 \leq 2 \rbrace .$$

Two things differ from Lecture 2. The condition is now $x^2 \leq 2$ rather than $x^2 \lt 2$, and $A$ is explicitly a set of real numbers (in Lecture 2's notes it was a set of rationals). A student asked where $x$ lives. Colding had left it out because "now I will specialize to the real numbers", but agreed that writing $x \in \mathbf{R}$ "certainly can't hurt" (≈26:51).

The notes then announce the plan: "We will show that $A$ is a non-empty bounded subset and that $\alpha = \sup A$ has the property that $\alpha \gt 0$ and $\alpha^2 = 2$" (notes p. 2).

### Setting up (≈26:51–32:36)

- **$A$ is non-empty**, because $1 \in A$: $1$ is positive and $1^2 = 1 \leq 2$ (≈26:51–27:43; notes p. 2).
- **$A$ is bounded from above**, since $2$ is an upper bound for $A$ (≈27:43–28:28; notes p. 2). Neither the board nor the notes say why. Colding remarks at this point that in a proof you only try to establish the properties you need; establishing others "just makes it confusing" (≈27:43–28:28).
- **Set $\alpha = \sup A$** (≈28:28), which exists by completeness.
- **$1 \leq \alpha \leq 2$.** Since $1 \in A$ and $\alpha$ is an upper bound for $A$, $1 \leq \alpha$; since $\alpha$ is the least upper bound and $2$ is an upper bound, $\alpha \leq 2$ (≈30:17–31:49). The notes write the first half as $0 \lt 1 \lt \alpha$, with a strict inequality, and use $1 \leq \alpha \leq 2$ later without saying where $\alpha \leq 2$ comes from.

So $\alpha \gt 0$, and all that is left is $\alpha^2 = 2$. As in Lecture 2, it is proved as two inequalities, each by contradiction (≈31:49–32:36).

### Part 1: $\alpha^2 \leq 2$ (≈32:36–52:21)

The notes' version (pp. 2–3). Suppose not, so $\alpha^2 \gt 2$. The plan is stated before anything is computed: there is then an $\alpha_0$ with $0 \lt \alpha_0 \lt \alpha$ and $\alpha_0^2 \gt 2$, so $\alpha_0$ is an upper bound smaller than $\alpha$, contradicting that $\alpha$ is the least upper bound. To show this, set

$$h = \frac{\alpha^2 - 2}{4 \alpha} \quad\text{and}\quad \alpha_0 = \alpha - h .$$

Since $\alpha^2 \gt 2$, $h \gt 0$, and therefore $\alpha_0 \lt \alpha$. (The notes print this assumption as $\alpha \gt 2$, a [printed slip](../raw/notes/03-how-to-write-a-proof-archimedean-property.md#printed-slips) for $\alpha^2 \gt 2$.) Since $1 \leq \alpha \leq 2$,

$$h \leq \frac{1}{2 \alpha} \leq \frac{1}{2} ,$$

and in particular $\alpha_0 \gt 0$. Next,

$$\alpha_0^2 = \alpha^2 + h^2 - 2 h \alpha \gt \alpha^2 - \frac{\alpha^2 - 2}{2} = \frac{\alpha^2}{2} + 1 \geq 2 .$$

On the board, the first inequality comes from ignoring $h^2$, "because that's positive" (≈46:54), and the middle step from filling in what $h$ was, which turns $2 h \alpha$ into $\frac{\alpha^2 - 2}{2}$ (≈47:41). The last inequality uses $\alpha^2 \geq 2$ (≈51:35). So $\alpha_0^2 \gt 2$, which is the desired contradiction. As in Lecture 2, the step from $\alpha_0^2 \gt 2$ to the conclusion that $\alpha_0$ is an upper bound for $A$ is asserted, on the board (≈50:02) and in the notes (p. 2), but not argued.

**On the board** the argument took a detour, and Colding used it as a lesson. He called the smaller number $\alpha_1$, and once $\alpha_0$ (≈36:37, ≈46:07). He checked that it is positive differently from the notes: $h$ is at most $\frac{\alpha^2}{4 \alpha} = \frac{\alpha}{4}$, so $\alpha_1$ is at least $\frac{3}{4}$ of $\alpha$ (≈37:25–38:14). He then began bounding $\alpha_1^2$ from above (≈39:04–44:36), stopped, and asked "what am I trying to prove here?" (≈45:21). Restating the goal, that the number just to the left of $\alpha$ should still have square bigger than $2$, showed that he needed a lower bound for $\alpha_0^2$: what he had been writing "is really for the second part" (≈46:07–46:54). He then gave the argument above (≈46:54–48:28). At first he justified the last inequality "using that alpha is bigger or equal to 1". After questions from the audience he corrected himself: "I'm using that alpha squared is bigger or equal to 2" (≈48:28–51:35). The notes print the $\geq 2$ without a reason.

His comment on the detour: "I fell into the trap. I was doing it so formally that I lost track of what I was doing." But "the formal proof is much easier to read afterwards" (≈50:02). And later: "if I really had written that before, then I wouldn't have been in trouble, because I was trying to prove something else" (≈58:08). Writing down what you want to show is the remedy.

Two more remarks from this part. One often writes a standard symbol to mark a contradiction (≈49:16); the captions do not say which symbol, and the notes use words ("This is the desired contradiction"). And the difference from Lecture 2 is where $h$ appears. There, a little calculation came first and the right $h$ came out at the end; in a formal proof that calculation has already been done, and "you would, up front, say what $h$ was supposed to be" (≈50:02–50:50). "Obviously, if this was the first time you would do it, you wouldn't just come up with this sort of thing", Colding says of $h$: "This is coming from the scrap paper that you had" (≈35:02).

### Part 2: $\alpha^2 \geq 2$ (≈52:21–1:04:36)

The notes' version (p. 3). Suppose not, so $\alpha^2 \lt 2$. The plan: there is then an $\alpha_1 \gt \alpha$ with $\alpha_1^2 \lt 2$, contradicting that $\alpha$ is an upper bound for $A$. This time set

$$h = \frac{2 - \alpha^2}{4 \alpha} \quad\text{and}\quad \alpha_1 = \alpha + h .$$

Then $1 \gt h \gt 0$, where the first inequality follows from $1 \leq \alpha$, and

$$\alpha_1^2 = \alpha^2 + h^2 + 2 h \alpha \lt \alpha^2 + h + \frac{2 - \alpha^2}{2} \leq \alpha^2 + 2 \frac{2 - \alpha^2}{2} = 2 .$$

The board fills in the steps (≈59:55–1:03:50). Since $\alpha \geq 1$ and the numerator of $h$ is at most $2$, $h$ is positive and at most $\frac{1}{2}$ (≈1:00:42; the captions say "denominator" there). Because $h$ is positive and less than $1$, $h^2$ is less than $h$, which makes the first inequality strict (≈1:00:42, ≈1:03:03). Multiplying $h$ by $2 \alpha$ cancels the $\alpha$ and one factor of $2$, giving $2 h \alpha = \frac{2 - \alpha^2}{2}$ (≈1:01:27). And since $\alpha \geq 1$, $h$ itself is at most $\frac{2 - \alpha^2}{2}$, which gives the second inequality (≈1:02:16). So $\alpha_1^2 \lt 2$. Then $\alpha_1$ is in $A$ and larger than $\alpha$: "this is the desired contradiction" (≈1:03:50).

On the board the larger number is called $\alpha_2$ (≈54:56–58:08). This time Colding said in advance where the contradiction would come from: there is some $\alpha_2 \gt \alpha$ whose square is still less than $2$, contradicting that $\alpha$ is an upper bound for the set $A$ (≈54:06–55:49). "I think it's a good idea to write what you want to show" (≈58:08).

The notes close with the last line Colding recommends: "Together parts 1 and 2 show that $\alpha^2 = 2$; completing the proof" (notes p. 3; ≈1:04:36). □

### The shape of a formal proof (≈1:03:50–1:06:09)

Colding sums up the structure (≈1:04:36–1:06:09). Divide the proof into its steps, here two, and write each step separately. Both steps were proved by contradiction, so say so up front, and then assume the negation of what you want to prove. If you can, and it does not feel like too much, write how you are going to get the contradiction. Then, and this is the big difference from working out the proof, you just define the objects you need, here $h$ and $\alpha_2$. "That seems to come out of nowhere." Finally, establish the property that leads to the contradiction, and end with a line saying that the parts together complete the proof. See [writing proofs](writing-proofs.md).

### Which properties of $\mathbf{R}$ does the proof use? (≈1:06:09–1:08:27)

A student asked, partly inaudibly, which properties of the real numbers the proof relies on. Colding listed several (≈1:06:55). It uses the ordering, and that $\mathbf{R}$ is an ordered field: multiplication, "to at all define square root", and the fact that $1$ is bigger than $0$. And it uses completeness, to define the least upper bound. Very soon, he added, everything will be in the real numbers. General fields are not part of this course, though when you can define something like a square root of $2$ in a field is an interesting question (≈1:07:41–1:08:27).

## The Archimedean property, written formally (≈1:08:27–1:14:20)

**Theorem** (notes p. 4; ≈1:09:15). The set of natural numbers is not bounded from above.

That is one way of formulating the Archimedean property. The other, from Lecture 2, says that for every real number there is a larger natural number, "but that's the same" (≈1:09:15–1:10:01). Unless something else is said, sets are subsets of $\mathbf{R}$ (≈1:10:01).

**Proof, by contradiction** (≈1:10:01–1:14:20; notes p. 4). Suppose $\mathbf{N}$ is bounded from above, and let $\alpha$ be its least upper bound. On the board, Colding takes any upper bound $\alpha$ and then replaces it by the supremum (≈1:10:49); the notes start "let $M$ be the least upper bound" and call it $\alpha$ from the next line on, a [printed slip](../raw/notes/03-how-to-write-a-proof-archimedean-property.md#printed-slips). So $n \leq \alpha$ for all $n \in \mathbf{N}$. Next comes the announcement of where the contradiction will come from: we will show that $\alpha - 1$ is also an upper bound, contradicting that $\alpha$ was the least upper bound (≈1:11:43–1:12:33). Now take any $n \in \mathbf{N}$. Since $n + 1$ is also a natural number and $\alpha$ is an upper bound for all natural numbers,

$$n + 1 \leq \alpha ,$$

and subtracting $1$ from both sides,

$$n \leq \alpha - 1 .$$

This holds for every natural number $n$, so $\alpha - 1$ is an upper bound for $\mathbf{N}$, which is the desired contradiction (≈1:13:32–1:14:20). □

The argument is the one from Lecture 2. What has changed is the writing: the proof states what it will show before showing it. See [the Archimedean property](archimedean-property.md).

### A corollary in the notes

The notes add a corollary that the lecture does not reach (notes p. 4).

**Corollary.** For any $\epsilon \gt 0$, there exists an $n \in \mathbf{N}$ such that $\frac{1}{n} \lt \epsilon$.

**Proof.** Set $\alpha = \frac{1}{\epsilon}$. By the Archimedean property there exists an $n \in \mathbf{N}$ with $n \gt \alpha$. It follows that $\frac{1}{n} \lt \epsilon$. □

The notes leave the last step to the reader.

## Sequences (≈1:14:20–1:19:51)

The lecture ends by starting sequences, which "will be a big topic" (≈1:14:20).

Lecture 2 already suggested placing $\sqrt{2}$ on the real line as the limit of its decimals, the increasing sequence

$$1 \lt 1.4 \lt 1.41 \lt 1.414 \cdots$$

(≈1:15:06–1:16:02; notes p. 5). Plug $\sqrt{2}$ into a calculator and it prints many digits, of which these are the first. To make this precise, the course needs to say what a sequence is and what its limit is (≈1:16:02).

**Sequence** (≈1:16:48; notes p. 5). A sequence of real numbers is a function $f : \mathbf{N} \to \mathbf{R}$: for each natural number you get a real number. It is common to write the argument as a subscript, $a_n = f(n)$, rather than in brackets (≈1:17:35).

**Example** (≈1:17:35–1:19:05; notes p. 5, Example 1). $a_1 = 1$, $a_2 = 1.4$, $a_3 = 1.41$, $a_4 = 1.414$, and so on: $a_n$ keeps the first $n$ digits of $\sqrt{2}$. This sequence is increasing, $a_n \lt a_{n+1}$, and $\sqrt{2}$ will be its limit, written $\lim_{n \to \infty} a_n$. What a limit means is for next time (≈1:19:05).

### In the notes but not in the lecture

The notes continue (notes p. 5):

- **Example 2.** $a_n = (-1)^n$. "This sequence has NO limit." The terms alternate between $-1$ and $1$.
- **Example 3.** The sequence $a_n = \frac{1}{n}$ has zero as its limit.
- **Limit.** Let $a_n$ be a sequence and $a$ a real number. Then $a_n$ **converges** to $a$ if for all $\epsilon \gt 0$ there exists an $N \in \mathbf{N}$ such that if $n \geq N$, then

$$\vert a_n - a \vert \lt \epsilon .$$

The notes also ask "When does a limit exist?" without answering it on the page. [Lecture 4](04-sequences-convergence.md), "Sequences; Convergence" (TBB Sections 2.1–2.2 and 2.4–2.7), gives Examples 2 and 3 and the definition on the board. See [sequences and limits](sequences-and-limits.md).

## Board versus notes

Where they differ, this page follows the notes and gives the board's version with its timestamp. Collected here:

- **The definitions of bounds.** Board: "bounded from above" and "bounded from below", for subsets of $\mathbf{R}$ first and then of any ordered set (≈4:48–11:32). Notes: a non-empty subset of an ordered set $\mathbf{S}$ "is said to have an upper bound" or "a lower bound" (p. 1).
- **Completeness.** Board: every subset bounded from above has a least upper bound (≈16:28); and every bounded subset of $\mathbf{R}$ has a greatest lower bound as well (≈19:42). Notes: "every bounded non-empty subset has a least upper bound", and $\inf A$ is only defined (p. 1).
- **The theorem.** Board: $\alpha \in \mathbf{R}$ with $\alpha \gt 0$ and $\alpha^2 = 2$ (≈26:03). Notes: $\alpha \gt 0$ with $\alpha^2 = 2$ (p. 2).
- **Bounds on $\alpha$.** Board: $1 \leq \alpha$, and $\alpha \leq 2$ because $\alpha$ is the least upper bound and $2$ an upper bound (≈30:17–31:49). Notes: $0 \lt 1 \lt \alpha$, then $1 \leq \alpha \leq 2$ without a reason for $\alpha \leq 2$ (p. 2).
- **Names.** The smaller number in Part 1 is $\alpha_1$ on the board (once $\alpha_0$, ≈46:07) and $\alpha_0$ in the notes; the larger number in Part 2 is $\alpha_2$ on the board and $\alpha_1$ in the notes. In the Archimedean proof the least upper bound is $\alpha$ on the board and first $M$, then $\alpha$, in the notes.
- **Why $\alpha_0$ is positive.** Board: $h \leq \frac{\alpha}{4}$, so $\alpha_1$ is at least $\frac{3}{4}$ of $\alpha$ (≈37:25–38:14). Notes: $h \leq \frac{1}{2 \alpha} \leq \frac{1}{2}$ (pp. 2–3).
- **The last step of Part 1.** Board: uses $\alpha^2 \geq 2$, after a correction (≈51:35). Notes: no reason given (p. 3).
- **Part 2's bounds on $h$.** Board: $h \leq \frac{1}{2}$ and $h \leq \frac{2 - \alpha^2}{2}$, both from $\alpha \geq 1$ (≈1:00:42–1:02:16). Notes: $1 \gt h \gt 0$, with the second bound left implicit in the display (p. 3).
- **Only in the notes:** the corollary that some $\frac{1}{n}$ is less than any given $\epsilon \gt 0$ (p. 4), Examples 2 and 3, and the definition of convergence (p. 5).

## Where the lecture stops

The proof that $\sqrt{2}$ is real and the proof of the Archimedean property are now written out as formal proofs, and the course has its notation for least upper and greatest lower bounds, $\sup$ and $\inf$. The lecture stops having defined a sequence, with the meaning of a limit promised for next time (≈1:19:05). The notes already give the definition of convergence. [Lecture 4](04-sequences-convergence.md), "Sequences; Convergence" (TBB Sections 2.1–2.2 and 2.4–2.7), takes it from there. On the OCW lecture list, Lecture 5 is "Monotone Convergence Theorem", which is not in this knowledge base yet.

## Related pages

- [Writing proofs](writing-proofs.md): this lecture's advice on writing a formal proof, together with the model proofs of Lectures 1 and 2.
- [Supremum and infimum](supremum-and-infimum.md): upper and lower bounds, $\sup A$ and $\inf A$, and why the surrounding set matters.
- [Completeness and the least upper bound property](least-upper-bound-property.md): completeness and what it proves.
- [The square root of 2](square-root-of-2.md): the informal proof of Lecture 2 and the formal one above.
- [The Archimedean property](archimedean-property.md): both formulations, both proofs, and the corollaries.
- [Sequences and limits](sequences-and-limits.md): the definition of a sequence and the notes' definition of convergence.
- [Lecture 2 — Introduction to Real Numbers (cont.)](02-introduction-to-real-numbers-cont.md): the previous lecture, where both results were first proved.
- [Lecture 4 — Sequences; Convergence](04-sequences-convergence.md): the next lecture, on convergence.
