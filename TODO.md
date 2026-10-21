# KB build — 18.100B

Open work only. Every run reads this file in full before doing anything and does
only unchecked work. Tick a box the moment its artifact is written, and commit
this file with it. When a run is committed and pushed, move its section verbatim
to [`BUILD_LOG.md`](BUILD_LOG.md): nothing ticked stays here.

## Future runs — lectures not yet built

Catalog positions (the midterm review sits at position 12, so positions after it run one
ahead of the lecture numbers). Each needs: transcript, edit, notes, wiki page, topic-page and
INDEX updates.

- [ ] Position 02 — Lecture 2: Introduction to Real Numbers (cont.) — video 6i6sV8WIzLc — in progress under Run 2 below
- [ ] Position 03 — Lecture 3: How to Write a Proof; Archimedean Property — video QJ96fO8Eef4
- [ ] Position 04 — Lecture 4: Sequences; Convergence — video PzeCGelnheE
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

## Run 2 — Lecture 2 (2026-10-21)

Scope: position 02 only. Same choices as Run 1: PDFs link only, no images.

### Transcript
- [x] 02 Lecture 2: Introduction to Real Numbers (cont.) — video 6i6sV8WIzLc — verbatim captions in `raw/transcripts/original/` (93 paragraphs, 6,229 words)
- [x] 02 edited transcript (Sonnet), checked: timestamps, numbers, per-paragraph word ratio
  - 93/93 markers identical. Number diff explained: "11" dropped with the false start "And then there's an 11 property" (3:16), "1.4.1"→"1.41" (17:40); every other new number sits inside an Ed mark. Ratio outliers with Ed marks stripped: 16:47 (0.70), 48:24 (0.71), 41:23 (0.55) are false-start removals, read and kept; 57:17 (1.27) had text added outside its Ed mark, moved inside by the parent. Parent rewrote three Ed marks that used notation (14:13, 21:35, 1:05:52) into speech.

### Notes
- [x] raw/notes/02-introduction-to-real-numbers-cont.md (Sonnet), every equation checked against the text layer
  - All 30-odd formulas match the text layer (radical and superscript positions read from span bboxes). Agent slips confirmed in the parent: p1 "2 m_1 = n" (squares missing; spans show subscript 1, no superscript), p3 "x^2 + 2 - x^2 < 2" (should be =). Dropped two of its "not a slip" notes that rested on outside knowledge (the rounding of 1.4142136, non-emptiness in the definition).

### Wiki
- [x] wiki/02-introduction-to-real-numbers-cont.md
- [x] Topic pages: update real-numbers, rational-numbers, fields-and-ordered-fields, writing-proofs, intermediate-value-theorem as needed; new pages for completeness / least upper bound and the Archimedean property
  - New: least-upper-bound-property, square-root-of-2, archimedean-property. Updated all five existing pages.
- [x] INDEX.md table of contents and coverage sentence

### Publish
- [x] kb.json — coverage, notes.transcribed, caveats
- [x] LICENSE.md — Lecture 2 third-party check (none; no OCW exclusion notice)
- [x] BUILD_LOG.md — Lecture 2 record: notes slips, transcript edits, board versus notes (below; moves with this section)
- [x] verify_kb.py clean, and its review section read
  - All hard checks OK; 1,202 formulas render in chat KaTeX and on github.com after 13 fixes, all a quotation opening with a formula (`"$`) plus one `$$` block inside a list item. Review: partial coverage stated at top of INDEX.md; the one numeric claim ("the notes for Lectures 1 and 2 contain no figures") is true; open TODO boxes are lectures 3–25 and this run's remaining publish steps.
- [ ] Commit and push
- [ ] Move this run's finished sections to BUILD_LOG.md; TODO.md keeps only open work

### Lecture 2 record

- **Material.** OCW notes PDF `mit18_100b_s25_lec02.pdf`, 5 pages (4 of content plus the OCW
  back page), pdfTeX, no rasters. All vector objects are zero-height lines: fraction bars and
  radical overbars. No figures, no third-party content, no OCW exclusion notice. Number sets
  and $\mathbf{S}$ are CMBX12. Page 4's MinionPro spans are blank spaces.
- **Notes transcription** (Sonnet, one pass, about 60k tokens). Every equation was compared in
  the parent against the text layer, with radicals and superscripts placed from span bboxes.
  This confirmed that p. 2 prints $A = (0, \sqrt{2}) \cap \mathbf{Q}$: the radical glyph sits
  directly before "2)". The agent's two mathematical slips were confirmed: p. 1 $2 m_1 = n$
  (subscript 1 present, no superscripts) and p. 3 $x^2 + 2 - x^2 \lt 2$ (should be $=$).
  Printed slips: p. 1 "does not exists", "does not have", "This show", "The real numbers R
  is"; p. 3 "This contradict", "and show". Of the agent's "not a slip" notes, the parent dropped
  two that rested on outside knowledge (that 1.4142136 is rounded; that the completeness
  definition omits non-emptiness) and one vague one (the Archimedean last step). It added the
  note that $A$ is written using $\sqrt{2}$ itself.
- **Transcript edit** (Sonnet, about 68k tokens, applied as scripted replacements). 93/93
  markers identical; body 6,095 to 5,959 words. The captions label the lecturer "PROFESSOR:"
  (Lecture 1: "TOBIAS COLDING:") and label four student questions "STUDENT:" from 1:09:46.
  Restorations: "c"→"z" (4:57), "the squared"→"x squared" (11:49), "1.4.1"→"1.41" (17:40),
  "s that"→"So that" (24:44), "And is a subset"→"A is a subset" (25:35), "for a"→"for A"
  (26:36), "at least upper bound"→"a least upper bound" (35:07), "The squared"→"h squared"
  (39:53), "minus a x squared"→"minus x squared" (51:35), "set a"→"set A" (52:20),
  "Archimedean problem"→"Archimedean property" (1:01:41). Ed marks: 1:38, 6:33, 14:13, 21:35,
  41:23, 52:20 (two), 57:17, 58:09, 59:57, 1:02:34, 1:05:52 (four), 1:07:26
  ("denominator" for numerator), 1:08:14 (two). Parent fixes: text added outside the 57:17 Ed
  mark moved inside it; three Ed marks written in notation (14:13, 21:35, 1:05:52) respelled
  as speech.
- **Board versus notes**, recorded on the wiki page: $A$ is a set of reals on the board and of
  rationals in the notes; the board's existence theorem says "a smallest" complete ordered
  field; the board defines a complete ordered field, the notes a complete ordered set; the
  $\lbrace 1, 2, 3 \rbrace$ example sits in $\mathbf{N}$ on the board and in $\mathbf{Z}$ in the
  notes; step 1's expansion uses $\geq$ on the board and $\gt$ in the notes; the least upper
  bound of $\mathbf{N}$ is $y$ on the board and $\alpha$ in the notes; $\beta$ is $y - x$ on the
  board and $\frac{1}{y - x}$ in the notes.
- **Gaps noted on the wiki, not filled:** why $(x - h)^2 \gt 2$ makes $x - h$ an upper bound;
  in the notes, whether $x + h$ is rational; why a largest integer $m - 1 \leq x n$ exists;
  Colding's "complement" answer on lower bounds, kept as a pointer to Lecture 3.
- **Topic pages.** New: `least-upper-bound-property`, `square-root-of-2`,
  `archimedean-property`. Updated: `real-numbers`, `rational-numbers`,
  `fields-and-ordered-fields`, `intermediate-value-theorem`, `writing-proofs`.
