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
