# KB build — 18.100B

Open work only. Every run reads this file in full before doing anything and does
only unchecked work. Tick a box the moment its artifact is written, and commit
this file with it. When a run is committed and pushed, move its section verbatim
to [`BUILD_LOG.md`](BUILD_LOG.md): nothing ticked stays here.

## Run 4 — Lecture 4 (2026-10-22)

Scope: position 04 only. Same choices as Runs 1–3: PDFs link only, no images.

### Transcript
- [x] Position 04 — Lecture 4: Sequences; Convergence — video PzeCGelnheE (the Future runs line, moved here)
- [x] 04 verbatim captions in `raw/transcripts/original/` (97 paragraphs)
- [x] 04 edited transcript (Sonnet), checked: timestamps, numbers, per-paragraph word ratio
  - 97/97 markers identical. Number diff explained: "1.4.1"/"1.4.1.4" to 1.41/1.414, "four 4" to "four times", "one"/"zero" written as digits. One ratio at 0.72 (38:08), false starts only. Parent reverted five agent changes: a notes example typed into 1:07:40, a formula carried into 1:00:36 from the next paragraph, a dropped sentence at 10:31, "S a plus 1" (25:43) and "the formula for the derivative" (54:10); turned a silent "denominator"→"numerator" fix (55:42) into an Ed mark; changed "capital N" insertions back to "N".

### Notes
- [x] raw/notes/04-sequences-convergence.md (Sonnet), every equation checked against the text layer
  - Every display matches the text layer. Span checks confirmed "max{Na, N_b}" (no subscript on the first), "If c = 0" (lower-case CMMI12), $a_n = 1$ (subscript present), no absolute value on the left of p. 4's $\frac{1}{b_n} - \frac{1}{b}$. The agent's file had mangled backslashes (form feed, vertical tab, tab, newline for \f \v \t \r); restored. "Formel definition:" set bold (CMBX12).

### Wiki
- [x] wiki/04-sequences-convergence.md
- [x] Topic pages: sequences-and-limits and others touched; grep wiki/ for "not yet" and "Lecture 4"
  - New: algebraic-properties-of-limits, subsequences. Rewrote sequences-and-limits. Updated writing-proofs (a section on ε–N proofs), archimedean-property, supremum-and-infimum, real-numbers, square-root-of-2, and the stale "Lecture 4 not yet" sentences on the Lecture 2 and Lecture 3 pages. Every quotation checked against the edited transcript.
- [x] INDEX.md table of contents, coverage sentence, readings sentence

### Publish
- [x] kb.json — coverage, notes.transcribed, caveats
- [x] LICENSE.md — Lecture 4 third-party check (none; no OCW exclusion notice)
- [x] BUILD_LOG.md — Lecture 4 record (below; moves with this section)
- [x] verify_kb.py clean, and its review section read
  - All hard checks OK; 2,994 formulas render in chat KaTeX and on github.com after fixing 18 `\,` in the notes, four `$\epsilon$–$N$` (GitHub does not open math after a dash) and two italic list leads with math inside. Review: partial coverage stated at top of INDEX.md; the one numeric claim ("the notes for Lectures 1 to 4 contain no figures") is true; open TODO boxes are this run's remaining publish steps and positions 05–25.
- [x] AGENTS.md — one lesson in general form: grep an agent's LaTeX for control characters
- [ ] Commit and push
- [ ] Move this run's finished sections to BUILD_LOG.md; TODO.md keeps only open work

### Lecture 4 record

- **Material.** OCW notes PDF `mit18_100b_s25_lec04.pdf`, 7 pages (6 of content plus the OCW
  back page), pdfTeX, no rasters. All vector objects are zero-height fraction bars. No figures,
  no third-party content, no OCW exclusion notice. $\mathbf{N}$, $\mathbf{Q}$, $\mathbf{R}$,
  $\mathbf{S}$ are CMBX12; "Formel definition:" is CMBX12 bold; "Limit:", "Sequences:",
  "Subsequence:" are roman.
- **Notes transcription** (Sonnet, one pass, about 66k tokens). Every display compared in the
  parent against the text layer; span checks for the doubtful glyphs: $\max\lbrace Na, N_b \rbrace$
  (first entry 12pt, no subscript), "If $c = 0$" (lower-case CMMI12), $a_n = 1$ (subscript
  present), no bars on the left of $\frac{1}{b_n} - \frac{1}{b}$ on p. 4. The agent wrote its
  LaTeX through escape-interpreting strings, so the `\f`, `\v`, `\t` and `\r` of `\frac`, `\vert`,
  `\to` and `\rbrace` became form feed, vertical tab, tab and a line break in four lines; restored. Printed slips: p. 1 "sup A the greatest lower
  bound of A" (should be smallest upper bound), "thought of a limit"; p. 2 "alternates",
  "convergenet", "covergent"; p. 3 "convergenet" (twice); p. 4 "If c = 0", "This show", "that
  show", "Na", "There are the details", the missing absolute value on the left of the
  reciprocal identity; p. 5 "NOT s subsequence", "Formel definition", "also denoted by"
  (missing "is"), "show that is all", "so large so that". The parent added to the "not a slip"
  list that the page never says $n_k$ stands for $g(k)$, and rephrased one slip line that
  opened a quotation with a formula; 18 `\,` in the body became `\thinspace` for github.com.
- **Transcript edit** (Sonnet, about 81k tokens). 97/97 markers identical; body 7,894 to about
  7,250 words; one ratio at 0.72 (38:08), false starts only. Captions label "TOBIAS COLDING:"
  and "AUDIENCE:" (23:15, 25:43, 40:34, 41:21, 1:17:28, 1:18:13). Restorations as listed in the
  transcript header. Parent reversals: the notes' "1, 1, 2, 2" typed into the board example at
  1:07:40 (back to the captions with an Ed mark); "c n minus 1 over a" carried into 1:00:36 from
  the next paragraph; a dropped sentence at 10:31; "S a plus 1" (25:43) now an Ed mark rather than
  a guess; "the formula for the derivative" (54:10) back to his words; the silent
  "denominator"→"numerator" at 55:42 now an Ed mark; "capital N" insertions (7:11, 12:54,
  20:43–26:28) back to "N"; "capital S" at 32:50 kept with his own correction.
- **Board versus notes**, recorded on the wiki page: $n \gt N$ on the board, $n \geq N$ in the
  notes; "less than" then equality for $1 - a_n$; the $\sup$ form of the boundedness bound; the
  fourth property as $\frac{1}{a_n}$ (board) or $\frac{a_n}{b_n}$ (notes); full board proofs of
  the third property and most of the fourth against the notes' outlines; the $\frac{\vert a \vert}{2}$
  lower bound; different subsequence examples; $b_k$ versus $b_n$.
- **Gaps noted on the wiki, not filled:** $10^{-n} \lt \frac{1}{n}$; why a finite set is bounded;
  $n_k \geq k$; how the quotient case follows from the reciprocal and the product; the claims
  about the limits of $(-1)^n$, $\frac{1}{n}$ and the decimals of $\sqrt{2}$; the strict-versus-weak
  last step of the board's product proof (stated as "bounded by"); the student's question about
  oscillating convergence (≈41:21), which the captions show answered only in general terms.
- **Topic pages.** New: `algebraic-properties-of-limits`, `subsequences`. Rewritten:
  `sequences-and-limits`. Updated: `writing-proofs`, `archimedean-property`,
  `supremum-and-infimum`, `real-numbers`, `square-root-of-2`, and stale sentences on the
  Lecture 2 and Lecture 3 pages.

## Future runs — lectures not yet built

Catalog positions (the midterm review sits at position 12, so positions after it run one
ahead of the lecture numbers). Each needs: transcript, edit, notes, wiki page, topic-page and
INDEX updates.

- [ ] Position 05 — Lecture 5: Monotone Convergence Theorem — video EjXtpzysDL4
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
