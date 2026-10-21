# KB build — 18.100B

Open work only. Every run reads this file in full before doing anything and does
only unchecked work. Tick a box the moment its artifact is written, and commit
this file with it. When a run is committed and pushed, move its section verbatim
to [`BUILD_LOG.md`](BUILD_LOG.md): nothing ticked stays here.

## Run 1 — Lecture 1 (2026-10-21)

Scope: position 01 only. Material per lecture is a typed LaTeX notes PDF (no slides);
notes are transcribed to `raw/notes/`. PDFs link only; no images (user's choice).

### Transcript
- [x] 01 Lecture 1: Introduction to Real Numbers — video BWvjy0a1Ffg — verbatim captions in `raw/transcripts/original/`
- [x] 01 edited transcript (Sonnet), checked: timestamps, numbers, per-paragraph word ratio
  - 82/82 markers identical. Number diff fully explained by restorations ("2 set"→"Z set", "N2"→"m1"/"m2", "O1/O2"→"0₁/0₂"). Ratio outliers 27:26 (1.24), 47:33 (1.12), 50:37 (1.12): Ed-mark insertions and the zero subscripts, wording unchanged.
  - Parent: removed the agent's inferred *[Student question, inaudible]* at 1:05:20 (no evidence in captions); added Ed marks at 19:21, 21:37, 51:29, 1:02:19.

### Crawl
- [x] Fetch course site index: https://ocw.mit.edu/courses/18-100b-real-analysis-spring-2025/
- [x] Download linked PDFs (gitignored)
- [x] Write sources.md

### Notes
- [x] raw/notes/01-introduction-to-real-numbers.md (Sonnet), every equation checked against the text layer

### Wiki
- [x] wiki/01-introduction-to-real-numbers.md
- [ ] Topic pages (cross-lecture concepts)
- [ ] INDEX.md table of contents

### Publish
- [ ] kb.json — coverage, materials.method, provenance caveats
- [ ] LICENSE.md — CC BY-NC-SA 4.0 (OCW)
- [ ] verify_kb.py clean, and its review section read
- [ ] Commit and push
- [ ] PATCH kbUrl onto the catalog entry
- [ ] Move this run's finished sections to BUILD_LOG.md; TODO.md keeps only open work

## Future runs — lectures not yet built

Catalog positions (the midterm review sits at position 12, so positions after it run one
ahead of the lecture numbers). Each needs: transcript, edit, notes, wiki page, topic-page and
INDEX updates.

- [ ] Position 02 — Lecture 2: Introduction to Real Numbers (cont.) — video 6i6sV8WIzLc
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
