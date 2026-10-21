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
