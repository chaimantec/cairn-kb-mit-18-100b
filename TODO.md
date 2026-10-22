# KB build — 18.100B

Open work only. Every run reads this file in full before doing anything and does
only unchecked work. Tick a box the moment its artifact is written, and commit
this file with it. When a run is committed and pushed, move its section verbatim
to [`BUILD_LOG.md`](BUILD_LOG.md): nothing ticked stays here.

## Run 7 — Lecture 7 (2026-10-22)

Scope: position 07 only. Same choices as Runs 1–6: PDFs link only, no images.

### Transcript
- [x] Position 07 — Lecture 7: Bolzano–Weierstrass Theorem; Cauchy Sequences; Series — video qeDewaJ4n24 (the Future runs line, moved here)
- [x] 07 verbatim captions in `raw/transcripts/original/` (104 paragraphs)
- [x] 07 edited transcript (Sonnet), checked: timestamps, numbers, per-paragraph word ratio
  - 104/104 markers identical; body 8,622 to 8,585 words; ratios all within 0.72–1.10 after the parent's changes; number inventory identical. Started before the notes file existed, with the notes' text layer (clean pdfTeX prose) as the terminology authority. A word-level diff reviewed every change. Parent reverted the agent's respelling of the captions' "2n", "s2n" and "cn plus 1" as "2 to the n" and "c to the n plus 1" (50:30–1:15:50, 39:21): kept as captioned, since at 52:05 the captions give both forms; restored "so for a series, always check" (54:24), which the agent had removed as a false start; reworded the Ed marks at 37:35 and 1:18:21, which guessed, to cite their evidence; restored "a n k" at 5:35; put the blank lines between paragraphs back (the agent's file ran all 104 paragraphs together). 8 [INAUDIBLE] tags, all kept.

### Notes
- [x] raw/notes/07-bolzano-weierstrass-theorem-cauchy-sequences-series.md (Sonnet), every equation checked against the text layer
  - Every display checked against text-layer spans; a word diff of the body prose against the text layer found no differences. Parent fixes: the bold label is printed "Bolzano-Weirstrass" too (four misspellings on p. 1, not two); added the slip $s_{n+1} = s_n + a_n$ (should be $a_{n+1}$, p. 4); confirmed the harmonic series printed as $\sum_{i=1}^{\infty} \frac{1}{2}$ (p. 3) and the red bold s (CMBX12) for the partial sums of $\vert a_i \vert$ (p. 4); removed "the later" as a slip; replaced 29 `\,` before punctuation; joined the stray ". If" on p. 6; reworded the not-a-slip items on the Cauchy remark in the Bolzano–Weierstrass proof and on the absolute-convergence proof (it uses convergent implies Cauchy).

### Wiki
- [x] wiki/07-bolzano-weierstrass-theorem-cauchy-sequences-series.md
  - Every quotation checked mechanically against the edited transcripts and the notes (quotes crossing a paragraph or page break split with an ellipsis; only OCW lecture titles unmatched).
- [x] Topic pages: bolzano-weierstrass-theorem, cauchy-sequences, new series pages; grep wiki/ for "not yet" and "Lecture 7"
  - New: series, geometric-series, harmonic-series, convergence-tests-for-series. Rewritten: bolzano-weierstrass-theorem (with the proof). Updated: cauchy-sequences, subsequences, sequences-and-limits (new Series section), monotone-convergence-theorem (Uses in Lecture 7), algebraic-properties-of-limits, real-numbers, extreme-value-theorem, writing-proofs (proof by induction), and the stale "Lecture 7 not yet" sentences on the Lecture 6 page. Every quotation on the touched pages checked (929 quotes across wiki/; the unmatched are OCW titles and pre-existing quotes on pages this run did not touch).
- [x] INDEX.md table of contents, coverage sentence, readings sentence (TBB Sec. 2.11–2.12, 3.4, confirmed on the OCW readings page)

### Publish
- [x] kb.json — coverage, notes.transcribed, caveats (new: what Lecture 7 uses without proof, deferred and notes-only; the Lecture 6 caveat no longer says Bolzano–Weierstrass is unproved; the Wikipedia caveat names Weierstrass)
- [x] LICENSE.md — Lecture 7 third-party check (the notes quote Wikipedia on Weierstrass, p. 2; attributed, CC BY-SA; no OCW exclusion notice)
- [x] BUILD_LOG.md — Lecture 7 record (below; moves with this section) and the index row
- [x] verify_kb.py clean, and its review section read
  - All hard checks OK once the new files were staged; every formula renders in chat KaTeX and on github.com after two fixes: a space after the underscore in $\bar{s}_ n$ and $\mathbf{s}_ n$ (25 places; a `_` straight after `}` opens italics on github.com), and two notes slips reworded so no quotation opens with a formula. Review: partial coverage stated at top of INDEX.md; the one numeric claim ("the notes for Lectures 1 to 7 contain no figures") is true (the Lecture 7 vector objects are fraction bars); open TODO boxes are this run's remaining publish steps and positions 08–25.
- [x] AGENTS.md — lessons in general form: an Ed mark cites its evidence or says unclear; a caption's compressed notation stays as captioned; "AUDIENCE:" is one of the caption labels
- [ ] Commit and push
- [ ] Move this run's finished sections to BUILD_LOG.md; TODO.md keeps only open work

### Lecture 7 record

- **Material.** OCW notes PDF `mit18_100b_s25_lec07.pdf`, 8 pages (7 of content plus the OCW back page), pdfTeX, no rasters; the vector objects on pp. 1–7 are fraction bars, p. 8's belong to the back page. No figures and no OCW exclusion notice. Third-party: a three-sentence Wikipedia biography of Weierstrass on p. 2 (attributed in LICENSE.md, CC BY-SA). Fonts checked in the text layer: "Lecture 7", "Last time:", the label "Bolzano-Weirstrass theorem", "Harmonic series" (red), "Ratio test" and "Example" are bold (CMBX12); "Proof." italic (CMTI12); the partial sums of $\vert a_i \vert$ on p. 4 are a red bold s (CMBX12), written $\mathbf{s}_ n$. Readings: TBB Sec. 2.11–2.12 and 3.4 (OCW readings page; Lecture 8 is Sec. 3.5–3.6).
- **Notes transcription** (Sonnet, one pass, about 72k tokens). Every display compared in the parent against text-layer spans; the prose word-diffed against the text layer with no differences. Printed slips: p. 1 "Weirstrass" (four times, including the bold label, which the agent had reported as correct), "the Bolzano-Weirstrass implies" (missing "theorem"), "infinite many" (twice), "lies" for "lie" (twice), "all the element"; pp. 1–2 "converges" for "converge" (twice); p. 2 "if it do"; p. 3 the harmonic series printed as $\sum_{i=1}^{\infty} \frac{1}{2}$; p. 4 "is Cauchy sequence", $s_{n+1} = s_n + a_n$ for $a_{n+1}$ (found by the parent), "there exist $M$"; p. 5 "This show". Not-a-slip list: the recap states only "Every Cauchy sequence is convergent"; the Bolzano–Weierstrass proof treats $[0, 1]$ only and remarks the subsequence is Cauchy without using it; the switching start index; the geometric divergence cases not argued; the first $\geq$ in the harmonic estimate is an equality; $\sum \frac{(-1)^n}{n}$ deferred; the absolute-convergence proof uses convergent implies Cauchy; the unstated estimate in the $\frac{1}{n^2}$ induction step; the root test named, not stated; the ratio test does not require $a_n \gt 0$.
- **Transcript edit** (Sonnet, about 87k tokens). Started before the notes file existed, with the notes' text layer as the terminology authority (the notes are clean pdfTeX, so the prose the notes file would carry was already available). 104/104 markers identical; body 8,622 to 8,585 words. Captions label "TOBIAS COLDING:" and "AUDIENCE:" (7:54, 8:40, 1:20:42); no "STUDENT:". 8 [INAUDIBLE] tags, all kept as *[inaudible]*. Parent reversals: the respelling of "2n", "s2n" and "cn plus 1" as "2 to the n" and "c to the n plus 1" (50:30–1:15:50, 39:21), kept as captioned because the captions give both forms at 52:05; "so for a series, always check" restored at 54:24; Ed marks at 37:35 and 1:18:21 reworded to cite their evidence instead of saying what he meant; "a n k" restored at 5:35; blank lines between the 104 paragraphs restored (the agent's file ran them together, so they would have rendered as one paragraph).
- **Board versus notes**, recorded on the wiki page: the order of the Bolzano–Weierstrass construction ($b_k$, $c_k$ built with the subsequence and the recursion $c_{k+1} - b_{k+1} = \frac{1}{2} (c_k - b_k)$ on the board; subsequence first, the Cauchy remark, then the endpoints in the notes); why the endpoints are bounded (first $c$, first $b$ on the board; "(as it is also bounded)" in the notes); the students' questions (board only); the notation and starting-point remarks, Achilles and the turtle (board only); the geometric series' divergence for all $\vert c \vert \geq 1$ by consecutive differences (board) against $\vert c \vert \gt 1$, $c = -1$ and "separately" $c = 1$ (notes); the harmonic estimate through $\frac{1}{2^{n+1}}$ (board) or directly to $\frac{1}{2}$ (notes); the term check (board only); non-negative series as an observation (board) or an if-and-only-if theorem (notes); $\bar{s}_ n$ with $m \gt n$ (board) against a bold red $\mathbf{s}_ n$ with $m \lt n$ (notes); $\sum \frac{1}{n^2}$ first written from $0$ and the explicit bound $2$ (board); the tests named on the board (five) and in the notes (three), with the second comparison test and the ratio test in the notes only; Weierstrass's biography (notes only).
- **Gaps noted on the wiki, not filled:** the squeeze step (a sequence between two with the same limit); the reduction of a general bounded sequence to $[0, 1]$; $\vert c \vert^{n} \to 0$ for $\vert c \vert \lt 1$; convergent implies Cauchy, used at ≈43:16, ≈55:11 and ≈1:04:44, still without a proof in the KB; why a bounded subsequence bounds an increasing sequence (≈1:10:18); the convergence of the alternating harmonic series (promised); proofs of all the tests; the garbled spots (what the difference equals at ≈8:40, the recursion at ≈19:47, the claim at ≈1:09:29, the range at ≈1:03:11, the comparison inequality at ≈1:18:21); the second student question at ≈8:40 and the question at ≈1:20:42 (partly inaudible).
- **Topic pages.** New: `series`, `geometric-series`, `harmonic-series`, `convergence-tests-for-series`. Rewritten: `bolzano-weierstrass-theorem`. Updated: `cauchy-sequences`, `subsequences`, `sequences-and-limits`, `monotone-convergence-theorem`, `algebraic-properties-of-limits`, `real-numbers`, `extreme-value-theorem`, `writing-proofs`, and the Lecture 6 page.
- **Parent slip caught before publishing.** A replacement string written as an ordinary (not raw) Python string turned four `\v` of `\vert` into vertical-tab characters on `cauchy-sequences.md`; the control-character grep found them. Parent edits that carry LaTeX need the same grep as an agent's.

## Future runs — lectures not yet built

Catalog positions (the midterm review sits at position 12, so positions after it run one
ahead of the lecture numbers). Each needs: transcript, edit, notes, wiki page, topic-page and
INDEX updates.

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
