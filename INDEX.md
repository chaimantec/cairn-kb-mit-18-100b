# 18.100B — Real Analysis (MIT, Spring 2025)

MIT's introduction to analysis, taught by **Tobias Holck Colding** and published on [MIT OpenCourseWare](https://ocw.mit.edu/courses/18-100b-real-analysis-spring-2025/). The course has two goals: learning to write mathematical proofs, and proving the theorems of calculus rigorously. According to the syllabus it covers real numbers, limits, convergence, series and continuity, then metric spaces, differentiation and Riemann integrals, and ends with ordinary differential equations (existence and uniqueness via Picard–Lindelöf). The main textbook is Thomson, Bruckner and Bruckner, *Elementary Real Analysis*, 2nd ed. (TBB), which is free online; Rudin's *Principles of Mathematical Analysis* is the second text. Colding lectures at the blackboard and types lecture notes for every lecture. There are no slides.

**Coverage: Lecture 1 only**, the first of 25 videos (23 lectures and two exam reviews). For any other lecture this knowledge base has nothing yet. Say so rather than answering from general knowledge, because a learner will take an answer here as what this course teaches. The [lecture list](#all-lectures) below gives each video's status.

## How to read this knowledge base

- Start from the **wiki** pages below. They cite the transcript as (≈M:SS) and the lecture notes as "notes p. N".
- **Transcripts:** read the edited ones in [`raw/transcripts/`](raw/transcripts/). They are a light copy-edit of OCW's professional captions, with every uncertain spot marked *[Ed: …]*. The verbatim captions are in [`raw/transcripts/original/`](raw/transcripts/original/).
- **Lecture notes:** Colding's typed notes for each lecture, transcribed page by page with the mathematics in LaTeX, are in [`raw/notes/`](raw/notes/). Each notes file lists its printed typos under "Printed slips".
- **Notation:** the notes set the number systems in bold, $\mathbf{N}$, $\mathbf{Z}$, $\mathbf{Q}$, $\mathbf{R}$, and a field as $\mathbf{F}$, and this knowledge base follows them. In this course $\mathbf{N} = \lbrace 1, 2, 3, \cdots \rbrace$ does not contain $0$.
- **Where the board and the notes differ** (the form of a law, how much detail a proof shows), the wiki follows the notes and gives the board's version with its timestamp.
- **Images:** this knowledge base has none, and the Lecture 1 notes contain no figures. Never construct an image path.

## Contents

### Lecture pages

- [Lecture 1 — Introduction to Real Numbers](wiki/01-introduction-to-real-numbers.md). Course logistics and grading; the intermediate value theorem as motivation; Q1–Q3 about $\sqrt{2}$ and the answer that $\mathbf{R}$ is a complete ordered field containing $\mathbf{Q}$; $\mathbf{N}$, $\mathbf{Z}$, $\mathbf{Q}$; equality, addition, multiplication and order on $\mathbf{Q}$; the proof that multiplication is well defined; the eleven field axioms; why $\mathbf{N}$ and $\mathbf{Z}$ are not fields; ordered sets and ordered fields; proofs that the zero is unique and that $x \lt y$, $z \gt 0$ imply $x z \lt y z$. Completeness is deferred.

### Topic pages

- [The real numbers](wiki/real-numbers.md). The course's one-sentence characterization of $\mathbf{R}$, why it starts there, and which parts are explained so far. Completeness is not yet covered.
- [The rational numbers](wiki/rational-numbers.md). $\mathbf{Q}$ as quotients $\frac{m}{n}$ with $m \in \mathbf{Z}$, $n \in \mathbf{N}$; when two quotients are equal; the operations and the order; why well-definedness must be checked; $\mathbf{Q}$ as an ordered field.
- [Fields and ordered fields](wiki/fields-and-ordered-fields.md). The eleven field axioms in a table, ordered sets, the two ordered-field axioms, the theorems proved from them, and the examples and non-examples ($\mathbf{Q}$; $\mathbf{N}$, $\mathbf{Z}$).
- [The intermediate value theorem](wiki/intermediate-value-theorem.md). The statement as given in Lecture 1, the chalk-on-the-board intuition for continuity, and why the picture is not a proof. The course proves it in Lecture 11, which is not yet covered.
- [Writing proofs](wiki/writing-proofs.md). Colding's case for rigor, the level of detail he expects, Lecture 1's three model proofs, and how the board and the notes differ.

## All lectures

The file prefix `NN` is the video's position in the course playlist. The midterm review is video 12, so from there on the prefix runs one ahead of the lecture number, and the OCW notes PDF for Lecture *k* is `mit18_100b_s25_lec{k}.pdf`.

| # | Title | In this KB |
| --- | --- | --- |
| 01 | Lecture 1: Introduction to Real Numbers | [wiki](wiki/01-introduction-to-real-numbers.md) · [transcript](raw/transcripts/01-introduction-to-real-numbers.md) · [notes](raw/notes/01-introduction-to-real-numbers.md) |
| 02 | Lecture 2: Introduction to Real Numbers (cont.) | not yet |
| 03 | Lecture 3: How to Write a Proof; Archimedean Property | not yet |
| 04 | Lecture 4: Sequences; Convergence | not yet |
| 05 | Lecture 5: Monotone Convergence Theorem | not yet |
| 06 | Lecture 6: Cauchy Convergence Theorem | not yet |
| 07 | Lecture 7: Bolzano–Weierstrass Theorem; Cauchy Sequences; Series | not yet |
| 08 | Lecture 8: Convergence Tests for Series; Power Series | not yet |
| 09 | Lecture 9: Limsup and Liminf; Power Series; Continuous Functions; Exponential Function | not yet |
| 10 | Lecture 10: Continuous Functions; Exponential Function (cont.) | not yet |
| 11 | Lecture 11: Extreme and Intermediate Value Theorem; Metric Spaces | not yet |
| 12 | Review for the Midterm | not yet |
| 13 | Lecture 12: Convergence in Metric Spaces; Operations on Sets | not yet |
| 14 | Lecture 13: Open and Closed Sets; Coverings; Compactness | not yet |
| 15 | Lecture 14: Sequential Compactness; Bolzano–Weierstrass Theorem in a Metric Space | not yet |
| 16 | Lecture 15: Derivatives; Laws for Differentiation | not yet |
| 17 | Lecture 16: Rolle's Theorem; Mean Theorem; L'Hôpital's Rule; Taylor Expansion | not yet |
| 18 | Lecture 17: Taylor Polynomials; Remainder Term; Riemann Integrals | not yet |
| 19 | Lecture 18: Integrable Functions | not yet |
| 20 | Lecture 19: Fundamental Theorem of Calculus | not yet |
| 21 | Lecture 20: Pointwise Convergence; Uniform Convergence | not yet |
| 22 | Lecture 21: Integrals and Derivatives under Uniform Convergence | not yet |
| 23 | Lecture 22: Differentiating and Integrating Power Series; Ordinary Differential Equations (ODEs) | not yet |
| 24 | Lecture 23: Existence and Uniqueness for ODEs: Picard–Lindelöf Theorem | not yet |
| 25 | Review for the Final Exam | not yet |

## Raw materials

- [`raw/transcripts/`](raw/transcripts/) holds the lecture transcripts with `[M:SS]` paragraph marks: edited at the top level, verbatim in `original/`.
- [`raw/notes/`](raw/notes/) holds the full text of Colding's typed lecture notes, page by page, with the mathematics in LaTeX.
- [`sources.md`](sources.md) lists every document on the course site with its canonical OCW URL: the lecture notes for all 23 lectures and both reviews, the ten problem sets, and the free TBB textbook.

The PDFs are **not** committed to this repo; [`sources.md`](sources.md) gives the canonical URL of each. The course site's readings page assigns TBB Sections 1.1–1.4 to Lecture 1. Licence and attribution are in [`LICENSE.md`](LICENSE.md).
