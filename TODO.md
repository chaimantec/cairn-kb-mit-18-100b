# KB build — 18.100B

Open work only. Every run reads this file in full before doing anything and does
only unchecked work. Tick a box the moment its artifact is written, and commit
this file with it. When a run is committed and pushed, move its section verbatim
to [`BUILD_LOG.md`](BUILD_LOG.md): nothing ticked stays here.

## Future runs — lectures not yet built

Catalog positions (the midterm review sits at position 12, so positions after it run one
ahead of the lecture numbers). Each needs: transcript, edit, notes, wiki page, topic-page and
INDEX updates.

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

## Run 6 — Lecture 6 (2026-10-22)

Scope: position 06 only. Same choices as Runs 1–5: PDFs link only, no images.

### Transcript
- [x] Position 06 — Lecture 6: Cauchy Convergence Theorem — video WCCpss6udNs (the Future runs line, moved here)
- [x] 06 verbatim captions in `raw/transcripts/original/` (94 paragraphs)
- [x] 06 edited transcript (Sonnet), checked: timestamps, numbers, per-paragraph word ratio
  - 94/94 markers identical (the agent reported 73, wrongly). Ratios 0.84–1.04 with Ed marks stripped; one at 1.11 (53:24), an inserted *[inaudible]* in a short paragraph. Number diff explained: "P63" to "P set 3" (21:17), "a1"/"a2" in a removed false start (19:34), "x0 0" and "f of x at 0" to "x0" (49:32). A word-level diff reviewed every change. Parent reverted: "Newton's method" typed into an [INAUDIBLE] gap (43:55); 13 deleted [INAUDIBLE] tags restored as *[inaudible]*; the dropped uncertain word "convergence" (10:14, now an Ed mark); "less than or equal" for his "bounded or equal" (34:18); reworded four Ed marks that guessed (1:37, 19:34, 42:17, 49:32) and one (39:03) to cite its evidence.

### Notes
- [x] raw/notes/06-cauchy-convergence-theorem.md (Sonnet), every equation checked against the text layer
  - Every display matches the text layer; span checks fixed the Newton formulas: $T'(x) = 1 - \frac{f'}{f'} + \frac{f \thinspace f''}{(f')^2} = f \frac{f''}{(f')^2}$ (the final $f$ on the baseline, not in the numerator) and $\frac{f''}{(f')^2}$ on p. 3. A word diff of the body prose against the text layer found no differences. Parent added three slips ("We need therefore show", "there exist $x$", the infimum sentence), fixed a misquoted "so long as" in the not-a-slip list, reworded the $n \lt N$ note, and corrected the figures line (fraction bars on pp. 2–3 only).

### Wiki
- [x] wiki/06-cauchy-convergence-theorem.md
  - Every quotation checked against the edited transcript and the notes (155 quotes; only OCW lecture titles unmatched).
- [x] Topic pages: cauchy-sequences, contracting-mapping-theorem and others touched; grep wiki/ for "not yet" and "Lecture 6"
  - New: bolzano-weierstrass-theorem, continuous-functions, extreme-value-theorem. Rewritten: cauchy-sequences, contracting-mapping-theorem (with Newton's method). Updated: sequences-and-limits, subsequences, monotone-convergence-theorem, real-numbers, supremum-and-infimum, intermediate-value-theorem, algebraic-properties-of-limits, writing-proofs, and the stale "Lecture 6 not yet" sentences on the Lecture 4 and Lecture 5 pages. Every quotation on the touched pages checked (537 quotes; unmatched only OCW titles, two capitalisation-only Lecture 5 quotes and one Run 5 ellipsis quote).
- [x] INDEX.md table of contents, coverage sentence, readings sentence (TBB Sec. 2.12)

### Publish
- [x] kb.json — coverage, notes.transcribed, caveats (new: what Lecture 6 assumes — Bolzano–Weierstrass, the Pset 3 exercise, the unproved converse; the Newton section's use of calculus not yet defined)
- [x] LICENSE.md — Lecture 6 third-party check (none; no OCW exclusion notice; the only outside reference is TBB, linked)
- [x] BUILD_LOG.md — Lecture 6 record (below; moves with this section)
- [x] verify_kb.py clean, and its review section read
  - All hard checks OK once the new files were staged; 4,584 formulas render in chat KaTeX and on github.com after rewording two `$\epsilon$–$\delta$` (GitHub does not open math after a dash). Review: partial coverage stated at top of INDEX.md; the one numeric claim ("the notes for Lectures 1 to 6 contain no figures") is true; open TODO boxes are this run's remaining publish steps and positions 07–25.
- [x] AGENTS.md — one lesson in general form: keep [INAUDIBLE] tags in place, never fill one with a guess
- [ ] Commit and push
- [ ] Move this run's finished sections to BUILD_LOG.md; TODO.md keeps only open work

### Lecture 6 record

- **Material.** OCW notes PDF `mit18_100b_s25_lec06.pdf`, 5 pages (4 of content plus the OCW back page), pdfTeX, no rasters; the vector objects on pp. 2–3 are fraction bars, p. 5's belong to the back page. No figures, no OCW exclusion notice, no third-party content (TBB is the only reference). Bold (CMBX12): "Lecture 6", "Last time:", "Cauchy sequence:", "Theorem (Cauchy convergence theorem)", "Definition", "Contracting mapping theorem:", "Bolzano -Weirstrass theorem", "Theorem" (p. 4), "Extreme value theorem"; "Proof." italic (CMTI12); "Application:", "Applications of contracting mapping theorem:", "Newton's method:", "Back to Cauchy sequences." roman. Readings: TBB Sec. 2.12.
- **Notes transcription** (Sonnet, one pass, about 63k tokens; it wrote the file in one Write call, not incrementally as asked). Every display compared in the parent against the text layer; span positions settled the Newton formulas on pp. 2–3. Printed slips: p. 1 "bunch together", "for a maps"; p. 2 "fix point", "two fixed point", "We need therefore show", "a zeroth"; p. 3 "x stay close", "Weirstrass" (four times), "there exist an $N_2$", "This show"; p. 4 "This show", "continues function", "there exist $x$", the infimum sentence missing words, "Weirstrass". The not-a-slip list records: the "if and only if" proved in one direction only; $c \geq 0$ not stated; the Pset 3 dependence; the imprecise Newton condition (printed as $f(x)$ being "small compared with" $\frac{f''}{(f')^2}$, reproduced as printed); $n_k \geq N_1$ unstated; the continuity theorem stated on $\mathbf{R}$ and applied on $[a, b]$; the unstated steps of the extreme value theorem.
- **Transcript edit** (Sonnet, about 82k tokens). 94/94 markers identical; body 7,014 to 6,893 words. Captions label "TOBIAS COLDING:" and "STUDENT:" (13:52, 17:16, 1:14:44, 1:15:32). 14 [INAUDIBLE] tags in the captions: 13 kept as *[inaudible]*, one inside a removed false start (5:10). Parent reversals as listed under the checklist item above. The agent's report miscounted the paragraphs (73) although its own marker diff matched; the parent's diff is the one recorded.
- **Board versus notes**, recorded on the wiki page: $x_n$ (board) against $a_n$ (notes); boundedness of a Cauchy sequence as a separate theorem on the board; the converse claimed proved "last time" on the board, stated without proof in the notes; $c$ positive on the board; uniqueness called a Lemma; the iteration from $a_0 = x$ with the consecutive-term estimate (board) against $a_1$ and Pset 3 (notes); the direct estimate for $T(a) = a$ against the notes' general lemma; Newton's method with the mean value theorem and the "good guess" caveat (board only); the extreme value theorem introduced as an application of the Cauchy theorem but proved with Bolzano–Weierstrass, with an infinite sup allowed and the endpoint argument (board only); continuity on a subset of $\mathbf{R}$ (board); continuity at one point suffices (board); "bigger than" for $\geq$.
- **Gaps noted on the wiki, not filled:** the converse (convergent implies Cauchy), which Colding says was proved in Lecture 5 but the Lecture 5 transcript and notes do not contain; the Bolzano–Weierstrass theorem (proof promised for Lecture 7); the Pset 3 exercise beyond the consecutive-term estimate, and the exponent in "something like c to the n"; uniqueness of limits; the squeeze step $\vert a_{n+1} - T(a) \vert \to 0$; derivatives, the quotient rule and the mean value theorem in the Newton section (Lectures 15–16), and the local contracting mapping theorem it needs; what "this" and "that" are in the good-guess condition (≈46:24); $n_k \geq N_1$ and the garbled split (≈56:45–57:43); why the limit lies in $[a, b]$; the infinite-sup case; the student remark at 17:16 (inaudible) and Colding's correction there; the name rendered "Wallis theorem" (≈42:17).
- **Topic pages.** New: `bolzano-weierstrass-theorem`, `continuous-functions`, `extreme-value-theorem`. Rewritten: `cauchy-sequences`, `contracting-mapping-theorem`. Updated: `sequences-and-limits`, `subsequences`, `monotone-convergence-theorem`, `real-numbers`, `supremum-and-infimum`, `intermediate-value-theorem`, `algebraic-properties-of-limits`, `writing-proofs`, and the Lecture 4 and Lecture 5 pages.
- **Inferences removed before publishing.** Drafts said that a contracting map is continuous (with $\delta = \epsilon$) and called the notes' lemma a special case of the continuity theorem; neither is said in the lecture, so both now only note that the two statements have the same shape.
