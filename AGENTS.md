# How this knowledge base is organized

This repo is the knowledge base for **18.100B — Real Analysis, Spring 2025**. It is read
by Cairn's in-extension AI chat, which starts at `INDEX.md`, fetches files over
raw.githubusercontent.com and follows relative markdown links.

The chat never reads this file. It is for whoever builds the KB, and Claude Code
loads it into every step of every build agent, so keep it to the rules every
lecture's build follows. The per-lecture record (licence notices, audit findings,
printed slips, which slides were rendered and why) goes in
[`BUILD_LOG.md`](BUILD_LOG.md); anything the chat needs goes in `INDEX.md`.

## Layout

| Path                | Contents                                                      |
| ------------------- | ------------------------------------------------------------- |
| `INDEX.md`          | Entry point. Course summary + annotated table of contents.    |
| `wiki/`             | Durable pages: one per lecture, plus cross-lecture topics.    |
| `raw/notes/`        | Full text of the typed lecture notes, headed `## Page N`.     |
| `raw/transcripts/`  | Lecture transcripts with `[MM:SS]` paragraph marks.           |
| `raw/pdfs/`         | Notes and problem-set PDFs from OCW. Gitignored, never linked. |
| `sources.md`        | Crawl inventory: source URL → local file, fetch date.         |
| `LICENSE.md`        | CC BY-NC-SA 4.0 (OCW) and attribution.                        |
| `kb.json`           | Machine-readable coverage and provenance. Update with coverage. |
| `TODO.md`           | Open work only. Finished runs move to `BUILD_LOG.md`.       |
| `BUILD_LOG.md`      | Finished runs, one section each. Not needed to answer questions. |

## Conventions

- **INDEX.md is the front door.** The chat reads it first on every conversation.
  Every wiki page must appear there with a one-line description of what it holds.
  An unindexed page is effectively invisible.
- **Relative links only** (`[gradient descent](gradient-descent.md)`,
  `[notes](../raw/notes/03-…md)`). Absolute GitHub URLs break when the
  repo is renamed or forked. PDFs are gitignored, so link them only at their
  canonical OCW URL (from `sources.md`), never as `../raw/pdfs/…`.
- **Cite everything.** Claims trace back to a transcript timestamp `(≈M:SS)` or the
  notes ("notes p. N").
- **Never invent course content.** If the transcript is unclear at some point,
  say so on the page. Do not fill the gap from outside knowledge — the chat
  presents these pages as authoritative material from this course.
- **Prose over fragments.** The chat quotes these pages to learners; bullet
  fragments quote badly.
- **Math in LaTeX**: `$...$` inline, `$$...$$` displayed. Renders both in
  Cairn's chat and on github.com. Never inside a code fence — that shows the
  source instead of the formula. Define each symbol on first use, and follow the
  course's own notation rather than a tidier one, since the learner is comparing
  the page against the lecturer's board. Never open a quotation with a formula
  (`"$…`): github.com then shows it as raw text. Rephrase so the quote starts with a word.
- **Transcripts stay verbatim.** Captions spell notation out as speech ("theta
  sub j"); reconstructing it as $\theta_j$ belongs in `wiki/`, not in
  `raw/transcripts/`.

## Course materials

- **Source.** MIT OCW, CC BY-NC-SA 4.0. The site's `pages/lecture-notes/` lists one
  notes PDF per lecture (`mit18_100b_s25_lecNN.pdf`) plus `review_midterm`, `review_final`
  and an all-in-one `lec_full`. `pages/readings/` gives the TBB sections per lecture: cite
  them on the lecture page. `pages/problem-sets/` has ten psets, linked from `sources.md`
  only. The crawl needs `--max-pages 80 --exclude video_galleries --exclude /download`.
- **File numbering.** `NN` is the catalog/playlist position, not the lecture number. The
  midterm review is position 12, so positions 13–24 are Lectures 12–23 and position 25 is
  the final review. Each page states its lecture number.
- **No slides.** Colding lectures at the blackboard; the typed notes are the written record.
  Transcribe each lecture's notes to `raw/notes/NN-<slug>.md`: front matter (pages,
  `source_pdf`, `resource_page`, numbering, figures), a contents table (section, pages), a
  "Printed slips" list, then `## Page N`. The notes print no equation numbers; keep the
  notes' own list numbering. The last PDF page is OCW's back page, summarized in one line.
  Delegate the reading to Sonnet (pages as one contiguous range). The prose may be copied
  from the text layer, which is clean pdfTeX; equations never (fractions flatten). Check
  every equation against the text layer in the parent. A slip the agent reports is a claim:
  an incomplete step is not a typo.
- **Notation.** The notes set number systems and named sets in bold (`CMBX12`), not
  blackboard bold: $\mathbf{N}$, $\mathbf{Z}$, $\mathbf{Q}$, $\mathbf{R}$, $\mathbf{F}$,
  $\mathbf{S}$. Read the font from the text layer when a new symbol's style matters. In this
  course $\mathbf{N}$ starts at 1.
- **Board versus notes.** Where they differ (the form of a law, a step the notes leave
  implicit), the wiki follows the notes and gives the board's version with its timestamp.
- **Transcripts.** OCW captions are professional: punctuated, speaker-labelled
  ("TOBIAS COLDING:" or "PROFESSOR:"), with sound tags. The edit is light (tags, filler, false starts;
  caption mishearings such as "O1" for 0₁ or "c" for z). Some lectures' captions
  label students ("STUDENT:") and some carry no audience labels: keep the labels the
  captions give, and never infer a student question without evidence in the text. Where
  Colding misspeaks (e.g. "denominator" for "numerator"), keep his words and add an
  *[Ed: …]* mark rather than correcting silently. Ed marks are spelled out like the
  speech around them, never notation.
- **Not yet covered.** Topic pages state what later lectures will add only by their OCW
  titles and readings, never by supplying the content; say "not yet in this KB". When a
  lecture is added, grep all of `wiki/` for "not yet" and for its title, and rewrite every
  sentence that still says it is missing, on lecture pages as well as topic pages.
- **Notes can run ahead of the video.** The notes may print material the lecture never
  reaches (a corollary, examples, the next definition). Give it on the lecture page under
  its own heading, marked as notes-only, and cite it by page with no timestamp.

## Rebuilding

Built and updated by the `cairn-kb` skill. To add newly released lectures,
append entries to `TODO.md` and re-run the skill — it only does unchecked work.
When a run is committed and pushed, move its `TODO.md` section verbatim to
`BUILD_LOG.md`, so `TODO.md` keeps only open work. Add here only a lesson
that applies to every lecture, stated in general form.
