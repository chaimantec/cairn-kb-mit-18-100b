# Power series

**Series of the form $\sum a_n x^n$, as introduced in Lecture 8. The page gives the definition and the series for $\frac{1}{1-x}$, $\exp x$, $\cos x$ and $\sin x$, which are stated but not yet proved. It gives Colding's remark that not every function has a power series, and the question of which $x$ a power series converges for. It works two examples: $\sum x^n$, which converges exactly when $\vert x \vert \lt 1$, and $\sum \frac{x^n}{n!}$, which converges for every $x$ by the ratio test. From the Lecture 8 notes only, it gives the radius of convergence.**

Notation: $x$ is a real number, $a_n$ a sequence of real numbers, $\vert x \vert$ the absolute value of $x$, and $n!$ is $n$ factorial, $1 \cdot 2 \cdots n$, with $x^0 = 1$. What a series is, and what it means for one to converge, is on [series](series.md).

## Definition

**Power series** (Lecture 8, ≈1:09:12–1:10:50; Lecture 8 notes p. 5). Given a sequence $a_n$, the series

$$\sum_{n=0}^{\infty} a_n x^n$$

is a power series, where $a_n$ is "the coefficient to the x to the power n" (Lecture 8, ≈1:10:04). "So if you will, this is like an infinite polynomial, a polynomial of infinite degree" (≈1:10:04). The notes call the coefficients $c_n$: "Let $c_n$ be a sequence, then $\sum_{n=0}^{\infty} c_n x^n$ is a power series" (Lecture 8 notes p. 5, under the printed heading "Formel definition"). Their section on the radius of convergence calls the coefficients $a_n$ again (notes p. 6).

For each fixed $x$ a power series is an ordinary series of numbers, and that is how its convergence is decided. Asked at the end of the lecture whether the result about $\sum \frac{x^n}{n!}$ holds for all $x$, Colding said "This is for all x. But think about x as being fixed": fix $x$, let $n$ go to infinity, and the conclusion then holds for every $x$ (≈1:20:33). "Then you can ask, how does it vary in x? But that's a different story" (≈1:20:33).

## Familiar functions

"So a lot of the basic functions can be represented by power series" (Lecture 8, ≈1:10:50). The lecture and the notes give four (Lecture 8 notes pp. 4–5; ≈1:07:35–1:11:38):

$$\sum_{n=0}^{\infty} x^n = \frac{1}{1 - x} ,$$

$$\sum_{n=0}^{\infty} \frac{x^n}{n!} = \exp x ,$$

$$\sum_{n=0}^{\infty} (-1)^n \frac{x^{2n}}{(2n)!} = \cos x ,$$

$$\sum_{n=0}^{\infty} (-1)^n \frac{x^{2n+1}}{(2n+1)!} = \sin x .$$

The first is the [geometric series](geometric-series.md) with the number called $x$ instead of $c$ (≈1:07:35); it holds for $\vert x \vert \lt 1$, where "the sum here is just this familiar function" (≈1:09:12). The other three are stated, not proved. The notes give no range of $x$ for any of the four. For the exponential function, Colding says "we'll come back and discuss this more" (≈1:10:50) and "we haven't proven that yet. But we'll talk about that next time" (≈1:14:58). The notes ask "Why does it give familiar functions?" and answer: "We will answer the second question next time for the exponential function" (Lecture 8 notes p. 5).

**Not every function has one** (Lecture 8, ≈1:11:38–1:12:23; board only). "And lots of functions have a power series representation. But it's not every function" (≈1:11:38). Colding draws a function "that starts off being dead zero and now it's becoming interesting"; the captions do not say what the curve is. It "does not have a power series. Even locally does not have a power series", because "a power series is an example of something that's called an analytic function. And this here is not an analytic function" (≈1:12:23). "But I'm not going to prove to you that it doesn't" (≈1:12:23).

## For which $x$ does it converge?

Given a power series, "the first question that comes to mind is", for which $x$ does the series converge (Lecture 8, ≈1:13:11). "So this is like the most basic thing" (≈1:13:57), and it is a question "which turned out to be quite subtle" (≈1:10:04). The notes ask "When does a power series converge?" and answer that it "comes from the root test or the ratio test" (Lecture 8 notes p. 5). See [convergence tests for series](convergence-tests-for-series.md).

**$\sum x^n$** (Lecture 8 notes p. 5; ≈1:13:57–1:14:58). For each fixed $x$ this is the geometric series, so it converges for $\vert x \vert \lt 1$ and diverges otherwise.

**$\sum \frac{x^n}{n!}$** (Lecture 8 notes p. 5; ≈1:14:58–1:19:46). Fix $x$. At $x = 0$ only the first term, $x^0 = 1$, is non-zero, so "it's definitely converging when x is equal to 0" (≈1:16:36). For $x \neq 0$ apply the ratio test to the terms, which the board calls $b_n = \frac{x^n}{n!}$ and the notes $a_n$. Colding takes the absolute value of the ratio of consecutive terms (≈1:17:23). Since $(n+1)! = (n+1) \thinspace n!$,

$$\frac{b_{n+1}}{b_n} = \frac{x^{n+1}}{(n+1)!} \cdot \frac{n!}{x^n} = \frac{x}{n+1} ,$$

which for each fixed $x$ goes to $0$ (≈1:17:23–1:18:56). The limit is $0$, less than $1$, "So it's definitely fallen under 1. So it's convergent" (≈1:18:56). So the series of the exponential function converges for every $x$. The notes write the same computation as $\frac{a_{n+1}}{a_n} = \frac{n! \thinspace x^{n+1}}{(n+1)! \thinspace x^n} = \frac{x}{n+1} \to 0$, without absolute values, and conclude "the power series is convergent for all $x$" (Lecture 8 notes p. 5).

## From the notes only: the radius of convergence

(Lecture 8 notes pp. 6–7; not in the lecture, which ends by saying this part comes next time, ≈1:19:46.) The ratio and root tests need a limit, and "what if it doesn't have a limit?" (≈1:19:46). "To talk about convergence of a general power series we need the notion of lim sup … of a sequence" (notes p. 6); see [limsup and liminf](limsup-and-liminf.md). For a power series $\sum_{n=0}^{\infty} a_n x^n$ set

$$R = \frac{1}{\limsup_{n \to \infty} \vert a_n \vert^{\frac{1}{n}}} ,$$

the **radius of convergence**, with the convention that $R = \infty$ when that $\limsup$ is $0$ and $R = 0$ when it is $\infty$ (notes p. 6). "From the root test one can now show the following": the power series converges if $\vert x \vert \lt R$ and diverges if $\vert x \vert \gt R$ (notes p. 6). The case $\vert x \vert = R$ "has to be examined on a case by case basis" (notes p. 7). The notes give no proof and compute $R$ for no example.

## Not yet in this knowledge base

That the series above give $\exp$, $\cos$ and $\sin$; the proof of the theorem on the radius of convergence. On the OCW lecture list, Lecture 9 is "Limsup and Liminf; Power Series; Continuous Functions; Exponential Function" (TBB Sections 2.13, 10.2, 5.4 and 5.5), Lecture 10 is "Continuous Functions; Exponential Function (cont.)", and Lecture 22 is "Differentiating and Integrating Power Series; Ordinary Differential Equations (ODEs)". None of them is in this knowledge base yet.

## Lectures

- [Lecture 8 — Convergence Tests for Series; Power Series](08-convergence-tests-for-series-power-series.md): everything on this page.
