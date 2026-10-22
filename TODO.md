# KB build — 18.100B

Open work only. Every run reads this file in full before doing anything and does
only unchecked work. Tick a box the moment its artifact is written, and commit
this file with it. When a run is committed and pushed, move its section verbatim
to [`BUILD_LOG.md`](BUILD_LOG.md): nothing ticked stays here.

## Run 5 — Lecture 5 (2026-10-22)

Scope: position 05 only. Same choices as Runs 1–4: PDFs link only, no images.

### Transcript
- [x] Position 05 — Lecture 5: Monotone Convergence Theorem — video EjXtpzysDL4 (the Future runs line, moved here)
- [x] 05 verbatim captions in `raw/transcripts/original/` (97 paragraphs)
- [x] 05 edited transcript (Sonnet), checked: timestamps, numbers, per-paragraph word ratio
  - 97/97 markers identical; number inventory identical in every paragraph; four ratios 1.11–1.15 (12:10, 44:28, 45:14, 56:56) are the "an"→"a n" splitting, 1.00–1.03 with names merged. A word-level diff found only the listed restorations and false starts. Parent reverted three agent changes: "theorem" for his "monotone convergence sequence" (21:03, now an Ed mark), an inserted "capital" at 39:32 (now "a n" with an Ed mark), and "lim sup"/"lim inf" for the captions' correct "limsup"/"liminf"; reworded three Ed marks that guessed (18:29, 51:50, 1:03:28).

### Notes
- [x] raw/notes/05-monotone-convergence-theorem.md (Sonnet), every equation checked against the text layer
  - Every display matches the text layer; span checks: $(b_n + 1)^2$ on p. 4 (the "+1" is CMR8, not a subscript), the order of $\frac{1}{n}$ and $\frac{1}{n^2}$ on p. 2, "defined by $a_n$" on p. 2. Parent moved the agent's p. 3 exponent note ($(2 \cdot 10^{2n-2})^2$ in the reason for $b_n \leq 2 \cdot 10^{n-1}$) into the slips, on the evidence of the same line and the board (≈54:12–54:57); added the unstated step from $a_n^2 \leq 2$ to $a^2 \leq 2$; dropped a missing-period note; "Subsequence:" set bold (CMBX12); fixed the figures line (drawings on pp. 1–4 and 8).

### Wiki
- [x] wiki/05-monotone-convergence-theorem.md
  - Every quotation checked against the edited transcript and the notes (105 quotes; only OCW lecture titles unmatched, as expected).
- [x] Topic pages: sequences-and-limits and others touched; grep wiki/ for "not yet" and "Lecture 5"
  - New: monotone-convergence-theorem, cauchy-sequences, contracting-mapping-theorem. Updated: sequences-and-limits, square-root-of-2, supremum-and-infimum, least-upper-bound-property, real-numbers, algebraic-properties-of-limits, subsequences, writing-proofs, archimedean-property, and the stale "Lecture 5 not yet" sentences on the Lecture 3 and Lecture 4 pages. Every quotation on the touched pages checked against the transcripts and notes.
- [x] INDEX.md table of contents, coverage sentence, readings sentence (TBB Sec. 2.8, 2.9, 2.11)

### Publish
- [x] kb.json — coverage, notes.transcribed, caveats (new caveats: facts Lecture 5 uses without proof; the board-only tails construction; the quoted Wikipedia passage)
- [x] LICENSE.md — Lecture 5 third-party check (no OCW exclusion notice; the p. 6 Wikipedia biography of Cauchy attributed, CC BY-SA)
- [x] BUILD_LOG.md — Lecture 5 record (below; moves with this section)
- [x] verify_kb.py clean, and its review section read
  - All hard checks OK; 3,806 formulas render in chat KaTeX and on github.com after fixing three: two notes lines that opened a quotation with a formula, and an INDEX formula GitHub did not take as math ($g(k)$ followed by ")"), reworded. Review: partial coverage stated at top of INDEX.md; the one numeric claim ("the notes for Lectures 1 to 5 contain no figures") is true; open TODO boxes are this run's remaining publish steps and positions 06–25.
- [x] AGENTS.md — one lesson in general form: quote the edited transcript and check every quotation mechanically
- [ ] Commit and push
- [ ] Move this run's finished sections to BUILD_LOG.md; TODO.md keeps only open work

### Lecture 5 record

- **Material.** OCW notes PDF `mit18_100b_s25_lec05.pdf`, 8 pages (7 of content, the references running onto p. 7, plus the OCW back page), pdfTeX, no rasters. The vector objects on pp. 1–4 are flat fraction bars and radical rules; p. 8's belong to the back page. No figures, no OCW exclusion notice. Third-party: p. 6 quotes a four-sentence biography of Cauchy "From Wikipedia", attributed in `LICENSE.md` (CC BY-SA). Bold (CMBX12): "Theorem", "Subsequence:", "Example", "Monotone convergence theorem", "Proof of the monotone convergence theorem", "Cauchy sequence:", "Definition", "Contracting mapping theorem:"; "Limit:" and "Application:" are roman.
- **Notes transcription** (Sonnet, one pass, about 67k tokens). Every display compared in the parent against the text layer; span checks for $(b_n + 1)^2$ on p. 4 (the "+1" is CMR8 beside a CMMI8 $b$ and CMMI6 subscript, so not $b_{n+1}$), the order of $\frac{1}{n}$ and $\frac{1}{n^2}$ on p. 2, "defined by $a_n$" on p. 2, and the printed $(2 \cdot 10^{2n-2})^2$ on p. 3. Printed slips: p. 1 "convergenet" (three times), "covergent"; p. 3 the exponent $2n-2$ inside the parenthesis of the reason for $b_n \leq 2 \cdot 10^{n-1}$ (the agent listed it as "not a slip"; the parent moved it, on the evidence of the claim on the same line and the board, ≈54:12–54:57); p. 4 "This show"; p. 6 "(Tail of the sequence bunch together.)", "for a maps". Parent changes to the "not a slip" list: added the unstated step from $a_n^2 \leq 2$ to $a^2 \leq 2$; dropped a missing-period note; rephrased two lines that opened a quotation with a formula. "Subsequence:" set bold; the figures line corrected (the agent had drawings on pp. 2–5).
- **Transcript edit** (Sonnet, about 77k tokens). 97/97 markers identical; number inventory identical in every paragraph; body 7,747 words to 7,956 because sequence names are spelled out ("a n"), paragraph ratios 1.00–1.03 with names merged back. Captions label "TOBIAS COLDING:" and "AUDIENCE:" (25:48, 26:33, 1:06:36). Restorations as listed in the transcript header. Parent reversals: "theorem" for his "monotone convergence sequence" (21:03, now an Ed mark); an inserted "capital" at 39:32 (now "a n" with an Ed mark); "lim sup"/"lim inf" back to the captions' "limsup"/"liminf". Ed marks reworded where the agent had guessed: 18:29 ("the caption breaks off" was inaccurate), 51:50 (now gives the notes' form), 1:03:28 (now "unclear; he seems to mean squaring it"). 15 Ed marks in all.
- **Board versus notes**, recorded on the wiki page: the order of the first two algebraic rules; the fourth rule as $\frac{1}{a_n}$ (board) and $\frac{1}{b_n}$ (notes), both reciprocals now; the quotient example spelled out rule by rule on the board; the bound spoken "a" (notes $A$) and the versions called "part 1" and "Part B"; the sup and inf of the tails, board only; "less than" for $\leq$ at 37:00; "largest natural number" against "largest integer"; the scrap-paper reduction to $10 \thinspace b_n \leq b_{n+1}$; the bound computed with $2 \cdot 10^{n-1}$ (the notes' slip); $\frac{1}{10^{n-1}}$, once spoken "1 over 10 to the n", against $10^{1-n}$; "bigger than $N$" against $m, n \geq N$ for Cauchy; $c$ positive on the board, only $c \lt 1$ in the notes; Cauchy's biography notes-only.
- **Gaps noted on the wiki, not filled:** that $\frac{1}{n^2}$ and $10^{1-n}$ tend to $0$; that a limit keeps an inequality satisfied by every term, and the related $c \leq b$ ("we'll prove this later", ≈32:54); why an integer whose square is too large exceeds $b_n$; the values $a_2$ to $a_4$, never checked against the definition; the existence of the sup in the proof (completeness, not named in the lecture); how the board compared $c$ and $b$ terms at different indices (captions muddled, ≈30:31); the shorthand for "decreasing" (≈27:19); his remark that $c$ is positive (≈1:14:35).
- **Topic pages.** New: `monotone-convergence-theorem`, `cauchy-sequences`, `contracting-mapping-theorem`. Updated: `sequences-and-limits`, `square-root-of-2`, `supremum-and-infimum`, `least-upper-bound-property`, `real-numbers`, `algebraic-properties-of-limits`, `subsequences`, `writing-proofs`, `archimedean-property`, and the stale sentences on the Lecture 3 and Lecture 4 pages.
- **Quotation check.** A script matched every quotation on the new and touched pages against the edited transcripts and the notes. On the Lecture 5 page it caught eight quotations drafted from the verbatim captions ("bn") that no longer matched the edited text ("b n"), and one notes quotation that ran into a display.

## Future runs — lectures not yet built

Catalog positions (the midterm review sits at position 12, so positions after it run one
ahead of the lecture numbers). Each needs: transcript, edit, notes, wiki page, topic-page and
INDEX updates.

- [ ] Position 06 — Lecture 6: Cauchy Convergence Theorem — video WCCpss6udNs
- [ ] Position 07 — Lecture 7: Bolzano–Weierstrass Theorem; Cauchy Sequences; Series — video qeDewaJ4n24
- [ ] Position 08 — Lecture 8: Convergence Tests for Series; Power Series — video lEMeyFq4-zQ
- [ ] Position 09 — Lecture 9: Limsup and Liminf; Power Series; Continuous Functions; Exponential Function — video MjRb8R33Ucc
- [ ] Position 10 — Lecture 10: Continuous Functions; Exponential Function (cont.) — video 1qHVpGA_qfs
- [ ] Position 11 — Lecture 11: Extreme and Intermediate Value Theorem; Metric Spaces — video bhBQbi9sWFA
- [ ] Position 12 — Review for 18.100B Real Analysis Midterm — video r_AGxxITsbQ
- [ ] Position 13 — Lecture 12: Convergence in Metric Spaces; Operations on Sets — video VZnB3dGdHP4
- [ ] Position 14 — Lecture 13: Open and Closed Sets; Coverings; Compactness — video og-zyMIa5Dc
- [ ] Position 15 — Lecture 14: Sequential Compactness; Bolzano–Weierstrass Theorem in a Metric Space — video eGKpOd_0oSY
- [ ] Position 16 — Lecture 15: Derivatives; Laws for Differentiation — video UP--RL-YKhE
- [ ] Position 17 — Lecture 16: Rolle’s Theorem; Mean Theorem; L’Hôpital’s Rule; Taylor Expansion — video v9lcA7lwLlo
- [ ] Position 18 — Lecture 17: Taylor Polynomials; Remainder Term; Riemann Integrals — video yG4bJnFT5-o
- [ ] Position 19 — Lecture 18: Integrable Functions — video 9rG-bs0TFQ8
- [ ] Position 20 — Lecture 19: Fundamental Theorem of Calculus — video _tZ102Wi0hE
- [ ] Position 21 — Lecture 20: Pointwise Convergence; Uniform Convergence — video ISVOH18BIHM
- [ ] Position 22 — Lecture 21: Integrals and Derivatives under Uniform Convergence — video _4m8hYQ3cR0
- [ ] Position 23 — Lecture 22: Differentiating and Integrating Power Series; Ordinary Differential Equations (ODEs) — video EDUMN4s44YU
- [ ] Position 24 — Lecture 23: Existence & Uniqueness for ODEs: Picard–Lindelöf Theorem — video fsbVJxOhRcU
- [ ] Position 25 — Review for the 18.100B Real Analysis Final Exam — video 75PZmUc0TK0
