# KB build — 18.100B

Open work only. Every run reads this file in full before doing anything and does
only unchecked work. Tick a box the moment its artifact is written, and commit
this file with it. When a run is committed and pushed, move its section verbatim
to [`BUILD_LOG.md`](BUILD_LOG.md): nothing ticked stays here.

## Run 3 — Lecture 3 (2026-10-22)

Scope: position 03 only. Same choices as Runs 1–2: PDFs link only, no images.

### Transcript
- [x] Position 03 — Lecture 3: How to Write a Proof; Archimedean Property — video QJ96fO8Eef4 (the Future runs line, moved here)
- [x] 03 verbatim captions in `raw/transcripts/original/` (99 paragraphs, 7,965 words incl. header)
- [x] 03 edited transcript (Sonnet), checked: timestamps, numbers, per-paragraph word ratio
  - 99/99 markers identical. Number inventory identical once Ed marks are stripped (no number lost or added); body 7,920 to 7,480 words; every paragraph ratio within 0.79–1.03, so no outliers. Parent reworded the 6:39 Ed mark ("less than or equal to a is meant") to the factual "the notes have less than or equal to".

### Notes
- [x] raw/notes/03-how-to-write-a-proof-archimedean-property.md (Sonnet), every equation checked against the text layer

### Wiki
- [x] wiki/03-how-to-write-a-proof-archimedean-property.md
- [x] Topic pages: new supremum-and-infimum, sequences-and-limits; update writing-proofs, square-root-of-2, archimedean-property, least-upper-bound-property, real-numbers; stale "Lecture 3 not yet" sentences on the Lecture 2 page
  - Done as listed. Also fixed a Run 2 leftover on the Lecture 1 page that still said Lecture 2 was not covered. Every quotation on the touched pages checked against the transcripts and notes; four that opened with a formula (`"$`) rephrased.
- [x] INDEX.md table of contents, coverage sentence, readings sentence

### Publish
- [x] kb.json — coverage, notes.transcribed, caveats (new caveat: Lecture 3 notes run ahead of the video)
- [x] LICENSE.md — Lecture 3 third-party check (none; no OCW exclusion notice)
- [x] BUILD_LOG.md — Lecture 3 record (below; moves with this section)
- [x] verify_kb.py clean, and its review section read
  - All hard checks OK; 1,990 formulas render in chat KaTeX and on github.com after fixing five in three notes-slip lines that opened a quotation with a formula. Review: partial coverage stated at top of INDEX.md; the one numeric claim ("the notes for Lectures 1 to 3 contain no figures") is true; open TODO boxes are this run's remaining publish steps and positions 04–25.
- [x] AGENTS.md — two lessons in general form: grep `wiki/` for stale "not yet" sentences when a lecture lands; mark notes-only material
- [ ] Commit and push
- [ ] Move this run's finished sections to BUILD_LOG.md; TODO.md keeps only open work

### Lecture 3 record

- **Material.** OCW notes PDF `mit18_100b_s25_lec03.pdf`, 6 pages (5 of content plus the OCW
  back page), pdfTeX, no rasters. All vector objects are zero-height fraction bars. No figures,
  no third-party content, no OCW exclusion notice. Number sets and $\mathbf{S}$ are CMBX12; the
  one MSAM10 glyph is the end-of-proof box.
- **Notes transcription** (Sonnet, one pass, about 61k tokens). Every equation was compared in
  the parent against the text layer, placed from span bboxes:
  $h \leq \frac{1}{2 \alpha} \leq \frac{1}{2}$, both Part displays, $\frac{1}{n} \lt \epsilon$, $\alpha = \frac{1}{\epsilon}$,
  $(-1)^n$, and the strict $0 \lt 1 \lt \alpha$ on p. 2. The agent's $\alpha \gt 2$ slip (for
  $\alpha^2 \gt 2$, p. 2) is confirmed: no superscript span sits beside that $\alpha$. Printed
  slips: p. 1 "concentrate of"; p. 2 "that that", "this lead" (again p. 3), $\alpha \gt 2$;
  p. 3 "and show"; p. 4 "natural number", $M$ renamed $\alpha$ mid-proof, ", By"; p. 5
  "thought of a limit", "alternates". Parent changes to the "not a slip" list: dropped a remark
  that $A$ "may contain numbers with" square $2$ (commentary) and the trivial $n + 1 \leq \alpha$
  step; added the strict-versus-weak $1 \lt \alpha$ / $1 \leq \alpha$ and the unstated step
  from $\alpha_0^2 \gt 2$ to "upper bound". Three slip lines that opened a quotation with a
  formula were rephrased.
- **Transcript edit** (Sonnet, about 78k tokens). 99/99 markers identical; body 7,920 to 7,480
  words; paragraph ratios 0.79–1.03. The captions label the lecturer "TOBIAS COLDING:" and the
  students "AUDIENCE:" (14:08, 19:42, 26:51, 49:16, 50:50, 51:35, 1:06:09). Restorations: "I
  bounded"→"it is bounded" (8:12); "for all A in A, A here"→"a", "looking A"→"looking at A"
  (12:21); "H"→"h" (1:02:16). Ed marks: 6:39 (reworded by the parent to "the notes have less than
  or equal to"), 30:17 (unclear), 35:51 ("nominator"), 46:07 ("alpha 0" for alpha 1), 58:08
  (alpha 2 squared), 1:00:42 ("denominator" for numerator), 1:02:16 (garbled formula for h),
  1:10:49 ("sup of A" for the sup of the natural numbers), 1:15:06 (stray "1"), 1:18:20 (digits
  unclear).
- **Board versus notes**, recorded on the wiki page: the form of the bound and completeness
  definitions; the board asserting that bounded subsets of $\mathbf{R}$ have an infimum; the
  theorem's $\alpha \in \mathbf{R}$; the board's derivation of $\alpha \leq 2$; the names
  ($\alpha_1$, $\alpha_2$ on the board, $\alpha_0$, $\alpha_1$ in the notes; $M$ then $\alpha$
  in the notes' Archimedean proof); the board's $h \leq \frac{\alpha}{4}$ for positivity; the
  corrected reason for Part 1's last step ($\alpha^2 \geq 2$, ≈51:35); Part 2's bounds on $h$.
- **Notes ahead of the video.** The video ends (≈1:19:51) having defined a sequence. The notes'
  corollary $\frac{1}{n} \lt \epsilon$, Examples 2–3 and the definition of convergence are given
  on the wiki as notes-only.
- **Gaps noted on the wiki, not filled:** why $2$ is an upper bound for $A$; why $\alpha_0^2 \gt 2$
  makes $\alpha_0$ an upper bound; the existence of $\inf$ from completeness; the mostly inaudible
  student question on whether the half line is complete, and which other notion of completeness
  Colding meant; which contradiction symbol he wrote (≈49:16).
- **Topic pages.** New: `supremum-and-infimum`, `sequences-and-limits`. Updated: `writing-proofs`,
  `square-root-of-2`, `archimedean-property`, `least-upper-bound-property`, `real-numbers`, and
  stale sentences on the Lecture 2 page and (left from Run 2) the Lecture 1 page.

## Future runs — lectures not yet built

Catalog positions (the midterm review sits at position 12, so positions after it run one
ahead of the lecture numbers). Each needs: transcript, edit, notes, wiki page, topic-page and
INDEX updates.

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
