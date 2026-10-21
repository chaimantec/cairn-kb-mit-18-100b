# Build log — 18.100B knowledge base

The record of how this knowledge base was built and checked, one section per
finished run, in order: each deck's licence notices and lecture pointers, each
transcript's edit and checks, what each figure audit found, each deck's printed
slips, and which slides were rendered as images and why the others were not.
A run's section is its `TODO.md` checklist, moved here verbatim once the run
was committed and pushed. It holds no unchecked box: open work lives only in
`TODO.md`.

It is a build record, **not needed to answer questions**: every fact a learner
needs is on the wiki page, slide file or transcript it concerns. The rules
every build follows, and each lesson in general form, are in
[`AGENTS.md`](AGENTS.md).

## Index

| Lecture | Runs |
| --- | --- |
| 01 Introduction to Real Numbers | Run 1 |
| 02 Introduction to Real Numbers (cont.) | Run 2 |
| 03 How to Write a Proof; Archimedean Property | Run 3 |
| 04 Sequences; Convergence | Run 4 |

## Runs

_Each finished run's section is appended below._

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
- [x] Topic pages: real-numbers, rational-numbers, fields-and-ordered-fields, intermediate-value-theorem, writing-proofs
- [x] INDEX.md table of contents

### Publish
- [x] kb.json — coverage, materials.method, provenance caveats
- [x] LICENSE.md — CC BY-NC-SA 4.0 (OCW)
- [x] verify_kb.py clean, and its review section read
  - All hard checks OK; 425 formulas render in chat KaTeX and on github.com (3 quote-before-$ fixes). Review: partial coverage stated at top of INDEX.md; the one numeric claim ("Lecture 1 notes contain no figures") is true; open TODO boxes are this run's remaining publish steps and lectures 2–25.
- [x] Commit and push — https://github.com/chaimantec/cairn-kb-mit-18-100b (new public repo, commits 5a2f38c, 92ea5ca)
- [x] PATCH kbUrl onto the catalog entry — re-fetched, kbUrl set; raw INDEX.md returns 200
- [x] Move this run's finished sections to BUILD_LOG.md; TODO.md keeps only open work

### Lecture 1 record

- **Material.** OCW notes PDF `mit18_100b_s25_lec01.pdf`, 5 pages (4 of content plus the OCW
  back page), pdfTeX, no rasters. The vector objects on pages 1 and 3 are square-root bars;
  page 2's are fraction bars. No figures, no third-party content, no OCW exclusion notice.
  Number sets and $\mathbf{F}$, $\mathbf{S}$ are CMBX12 (bold), not MSBM.
- **Notes transcription** (Sonnet, one pass, about 50k tokens). Every equation was compared
  in the parent against the text-layer dump; all agreed. The agent listed a page 2
  "slip" (the proof chain stops before its conclusion). That is an incomplete step, not a
  typo, so it was moved to a note under the slips list. "is also Field" (missing "a") was
  added. Printed slips: p1 "continuous functions", "how to we", stray "."; p3 "This
  illustrate", "satisfies", "axion", empty bullet before the distributive law; p4 "For an x,
  y", "also Field".
- **Transcript edit** (Sonnet, about 62k tokens). 82/82 markers identical. Words went from
  6,155 to 6,007. Restorations: "2 set"→"Z set", "integral"→"interval", "irrational"→
  "rational" (13:39), "n2 times N2 … N2 times n1"→"m1 times n2 … m2 times n1" (17:47),
  "p1 comma q1"→"p1/q1", "m2 times q2"→"n2 times q2", "reputation"→"representation",
  "O1/O2"→"0₁/0₂", "serial elements"→"zero element", "c"→"z" (55:01, 59:09). Ed marks:
  19:21, 21:37, 27:26, 28:59, 50:37, 51:29, 1:02:19 (four added by the parent). The
  agent's *[Student question, inaudible]* at 1:05:20 was removed, because nothing in the
  captions supports it.
- **Board versus notes**, recorded on the wiki page: the distributive law is $x(y+z)$ on the
  board and $(x+y)z$ in the notes; the zero-uniqueness proof uses commutativity explicitly on
  the board and silently in the notes; transitivity of an ordered set is only in the notes.
- **Crawl.** 42 pages, 36 PDFs (13MB, gitignored) and 2 external TBB links.
  `inventory_to_sources.py` files everything under "other", which is acceptable for now.

## Run 2 — Lecture 2 (2026-10-21)

Scope: position 02 only. Same choices as Run 1: PDFs link only, no images.

### Transcript
- [x] Position 02 — Lecture 2: Introduction to Real Numbers (cont.) — video 6i6sV8WIzLc (the Future runs line, ticked and moved here)
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
- [x] Commit and push — commit e62770e to https://github.com/chaimantec/cairn-kb-mit-18-100b (kbUrl already set; no PATCH needed)
- [x] Move this run's finished sections to BUILD_LOG.md; TODO.md keeps only open work

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
- [x] Commit and push — commit b720e8e to https://github.com/chaimantec/cairn-kb-mit-18-100b (kbUrl already set and re-confirmed; raw INDEX.md and the Lecture 3 page return 200)
- [x] Move this run's finished sections to BUILD_LOG.md; TODO.md keeps only open work

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
- [x] Commit and push — commit 333131a to https://github.com/chaimantec/cairn-kb-mit-18-100b (kbUrl already set and re-confirmed; raw INDEX.md and the Lecture 4 page return 200)
- [x] Move this run's finished sections to BUILD_LOG.md; TODO.md keeps only open work

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
