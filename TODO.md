# KB build — 18.100B

Open work only. Every run reads this file in full before doing anything and does
only unchecked work. Tick a box the moment its artifact is written, and commit
this file with it. When a run is committed and pushed, move its section verbatim
to [`BUILD_LOG.md`](BUILD_LOG.md): nothing ticked stays here.

## Run 8 — Lecture 8 (2026-10-22)

Scope: position 08 only. Same choices as Runs 1–7: PDFs link only, no images.

### Transcript
- [x] Position 08 — Lecture 8: Convergence Tests for Series; Power Series — video lEMeyFq4-zQ (the Future runs line, moved here)
- [x] 08 verbatim captions in `raw/transcripts/original/` (100 paragraphs)
- [x] 08 edited transcript (Sonnet), checked: timestamps, numbers, per-paragraph word ratio
  - 100/100 markers identical; number inventory identical except "true" restored as "2" (31:34, 50:08, 51:01, 54:57, 1:06:38) and digits inside removed false starts (46:54, 55:45, 1:17:23). Three ratios under 0.72 (2:27 at 0.58, 52:36 at 0.68, 1:04:56 at 0.51), all short paragraphs of stacked restarts, read and accepted; no ratio above 1.10 once Ed marks are stripped. A word-level diff reviewed every change. Parent reverted two silent corrections, "2 to minus n over 2" changed to "over n" (32:22) and "1.5" changed to "1 over 2" (33:09), both now as captioned with an Ed mark; restored "converges" for the captions' "converts" (39:42, 1:05:44), which the agent had left; restored the self-correction "m to be n plus 1-- sorry" (4:11), which "Doesn't matter" refers to; "your matrix" to "geometric" without an added "the" (7:26); "b, S m" back to "b S m" with an Ed mark (29:17); "And before I do this" kept at 1:04:56; an Ed mark added at 45:18 ("in conclusion", possibly the inconclusive case); dropped the agent's unneeded Ed mark at 1:18:56; moved the 30:48 Ed mark next to the words it concerns; lowercased the partial-sum names ("S n" to "s n", 41 places) to match the notes and the Lecture 7 transcript; dropped "Last time, we talked about--" as a false start (0:00).

### Notes
- [x] raw/notes/08-convergence-tests-for-series-power-series.md (Sonnet), every equation checked against the text layer
  - Every display checked against text-layer spans (the printed $c^{i}n$ in the geometric series, the index mismatch $\sum_{i=1}^{\infty} \frac{1}{n}$, $r_0^n$ with the 0 as subscript and the n as exponent); a word diff of the body prose against the text layer found no differences. Parent removed three punctuation items from the agent's slips (the red label "Absolutely convergent;", the comma after $L \neq 0$ and the stray full stop, "where,"), removed the agent's own inference that $-\infty$ cannot occur for $\vert a_n \vert^{\frac{1}{n}}$, reworded "decreasing" (the course's sense, not a slip), the coefficient-letter note and the contrapositive note.

### Wiki
- [x] wiki/08-convergence-tests-for-series-power-series.md
  - Every quotation checked mechanically against the edited transcripts and the notes, and each transcript quotation against the paragraph at its cited timestamp (123 quotes; only the OCW lecture title unmatched).
- [x] Topic pages: convergence-tests-for-series, series, new power-series and limsup pages; grep wiki/ for "not yet" and "Lecture 8"
  - New: power-series, limsup-and-liminf. Rewritten: convergence-tests-for-series (Lecture 8's proofs of the first comparison test, the ratio and root tests). Updated: series, geometric-series, harmonic-series (the family $\sum \frac{1}{n^{\alpha}}$, the alternating harmonic series in words), cauchy-sequences, monotone-convergence-theorem, sequences-and-limits, supremum-and-infimum, real-numbers, algebraic-properties-of-limits, writing-proofs (a number strictly between), and the stale "Lecture 8 not yet" sentences on the Lecture 7 page and on six topic pages. Every quotation on the touched pages checked (1,095 quotes across wiki/; unmatched only OCW titles and pre-existing quotes on pages this run did not touch, plus one pre-existing span on the Lecture 7 page); every Lecture 8 quotation checked against the paragraph at its cited timestamp.
- [x] INDEX.md table of contents, coverage sentence, readings sentence (TBB Sec. 3.5–3.6, confirmed on the OCW readings page; Lecture 9 is Sec. 2.13, 10.2, 5.4, 5.5)

### Publish
- [x] kb.json — coverage, notes.transcribed, caveats (new: what Lecture 8 uses without proof, states without proof and has in the notes only; the Lecture 7 caveat now says which tests Lecture 8 proves; first caveat and the figure-audit note say eight lectures)
- [x] LICENSE.md — Lecture 8 third-party check (none; no OCW exclusion notice; the only outside reference is TBB, linked). Also fixed the stale "Lectures 1 to 6 contain no figures" (now 1 to 8).
- [x] BUILD_LOG.md — Lecture 8 record (below; moves with this section) and the index row
- [x] verify_kb.py clean, and its review section read
  - All hard checks OK once the new files were staged; 6,526 formulas render in chat KaTeX and on github.com after one fix: the notes agent had written the four power series on notes pp. 4–5 as list items holding `$$` displays, which github.com shows as raw text, now plain displays with a note. Review: partial coverage stated at top of INDEX.md; the one numeric claim ("the notes for Lectures 1 to 8 contain no figures") is true (the Lecture 8 vector objects are fraction bars); open TODO boxes are this run's remaining publish steps and positions 09–25.
- [x] AGENTS.md — lessons in general form: a `$$` display inside a list item does not render on github.com; a spoken number that disagrees with the notes stays as captioned with an Ed mark
- [ ] Commit and push
- [ ] Move this run's finished sections to BUILD_LOG.md; TODO.md keeps only open work

### Lecture 8 record

- **Material.** OCW notes PDF `mit18_100b_s25_lec08.pdf`, 8 pages (7 of content plus the OCW back page), pdfTeX, no rasters; the vector objects on pp. 1–7 are fraction bars, p. 8's belong to the back page. No figures, no OCW exclusion notice, no third-party content (TBB is the only reference). Bold (CMBX12): "Lecture 8", "Series", "Geometric series:", "Harmonic series", "Absolutely convergent;" (all red), "Theorem", "Comparison test; version 1" and "version 2", "Example", "Example 1", "Example 2", "Ratio test", "Root test", "Power series" (blue), "Formel definition", "Definition"; "Proof." italic (CMTI12). Coloured roman text: "When does a power series converge?" (red), "Why does it give familiar functions?" (blue), "lim sup" (red, p. 6), "(of lim sup)" and "radius of convergence" (blue), "Convention" (green). Readings: TBB Sec. 3.5–3.6 (OCW readings page; Lecture 9 is Sec. 2.13, 10.2, 5.4, 5.5).
- **Notes transcription** (Sonnet, one pass over pages 1–8, about 81k tokens). Every display compared in the parent against text-layer spans; the prose word-diffed against the text layer with no differences. Printed slips: p. 1 "if it do"; the geometric series printed $\sum_{i=0}^{\infty} c^{i}n$ (a baseline $n$ after $c^i$, from the span positions); the harmonic series printed $\sum_{i=1}^{\infty} \frac{1}{n}$; p. 5 "Formel definition"; p. 6 "The power series in convergent"; p. 7 "The case of where". The agent's three punctuation items (the semicolon label, the comma after $L \neq 0$ and the stray full stop, "where,") were dropped. Not-a-slip list: only the root test is proved; index letters and starting points vary, and the coefficients are $c_n$ and $a_n$; version 2 of the comparison test does not require non-negative terms; the ratio test is stated for $a_n \geq 0$ and applied to $\frac{x^n}{n!}$ without absolute values; the root test from $n = 0$; the unstated steps of the root-test proof (the definition of the limit, the first $N$ terms, the contrapositive of the comparison test); the four power series with no range of $x$; the limsup definition's cases and its limit possibly $-\infty$; the convention for $R$ after the sentence naming it; no example for $\vert x \vert = R$. The four power-series bullets were rewritten as plain displays so that they render on github.com.
- **Transcript edit** (Sonnet, about 99k tokens; built by asserted string replacements on the original rather than retyping). 100/100 markers identical; body 8,271 to 7,851 words; 10 Ed marks. Captions label "TOBIAS COLDING:" and "AUDIENCE:" (27:45, 28:31, 54:57, 1:07:35, 1:20:33); no "STUDENT:". One [INAUDIBLE], audience speech at 1:07:35, kept. Parent reversals: "over n" back to the captioned "over 2" (32:22) and "1 over 2" back to "1.5" (33:09), each now with an Ed mark citing the notes or the preceding words; "converges" for the captions' "converts" (39:42, 1:05:44), a mishearing the agent had left; the self-correction "m to be n plus 1-- sorry" restored (4:11); "your matrix" to "geometric" with no added article (7:26); "b, S m" to "b S m" with an Ed mark (29:17); Ed mark added at 45:18; Ed mark dropped at 1:18:56; the partial sums lowercased ("S n" to "s n", 41 places) to match the notes and the Lecture 7 transcript.
- **Board versus notes**, recorded on the wiki page: the check on the terms, the geometric divergence from the terms, the family $\sum \frac{1}{n^{\alpha}}$, the alternating harmonic picture (board only); comparison test version 1 proved twice (board) against no proof (notes); version 2 with non-negative terms and $L$ "not infinity" (board) against $b_n \neq 0$, $L \neq 0$ (notes); the ratio test with absolute values, $a_n \neq 0$ and a sketched proof (board) against $a_n \geq 0$ and no proof (notes); the root test with $c$, $c_0$ and divergence from the terms going to infinity (board) against $r$, $r_0$ and comparison with a divergent geometric series (notes); power-series coefficients $a_n$ (board) against $c_n$ (notes); the function with no power series and the case $x = 0$ (board only); $b_n$ with absolute values (board) against $a_n$ without (notes) in the exponential example; limsup and the radius of convergence (notes only).
- **Gaps noted on the wiki, not filled:** convergent implies Cauchy, used for the check on the terms (≈4:11–5:46) and the first proof of the comparison test (≈29:17), still without a proof in the KB; which series is which in the divergence use of the comparison test (≈24:38); the second comparison test (unproved); the convergence of $\sum \frac{1}{n^{\alpha}}$ for $\alpha \gt 1$ and the integral test; the precise alternating series test; that the series give $\exp$, $\cos$, $\sin$; what the function with no power series is (≈1:12:23); the theorem on the radius of convergence (notes only, unproved); what a limit of $-\infty$ means; the garbled spots at ≈29:17, ≈30:48, ≈45:18, ≈51:01 and ≈55:45; the student question at ≈1:07:35 (inaudible).
- **Topic pages.** New: `power-series`, `limsup-and-liminf`. Rewritten: `convergence-tests-for-series`. Updated: `series`, `geometric-series`, `harmonic-series`, `cauchy-sequences`, `monotone-convergence-theorem`, `sequences-and-limits`, `supremum-and-infimum`, `real-numbers`, `algebraic-properties-of-limits`, `writing-proofs`, and the Lecture 7 page.
- **Inference removed before publishing.** The notes agent's not-a-slip list said the value $-\infty$ cannot occur for $\vert a_n \vert^{\frac{1}{n}}$; true, but the notes do not say it, so it was dropped. A draft sentence on the limsup page said the course had defined convergence only to real numbers; the Lecture 7 notes already write $\frac{n}{2} \to \infty$, so it was cut back to what the notes do not say.

## Future runs — lectures not yet built

Catalog positions (the midterm review sits at position 12, so positions after it run one
ahead of the lecture numbers). Each needs: transcript, edit, notes, wiki page, topic-page and
INDEX updates.

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
