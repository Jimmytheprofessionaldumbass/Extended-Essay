# EE title page — compliance check against the official guide (2026-10-22)

**Source:** `~/Extended-Essay/Sources/extended-essay-first-assessment-2027-guide-sbs.pdf`, **Figure 15,
guide p.89** (rendered and read directly, not paraphrased). The guide says: *"Your title page must clearly
show the information indicated in figure 15."*

## What Figure 15 requires

| # | Required item | Verbatim from Figure 15 |
|---|---|---|
| 1 | **Student code** | "Your student code" |
| 2 | **Research question** | "Your research question" |
| 3 | **DP subject** (subject-focused essay) | "State the DP subject the essay relates to." |
| 4 | **Word count** | "The word count" — with the note that if footnotes are used for anything other than referencing, the count must include them and say so explicitly |

## What the current title page actually has

`main.tex:22–24`:

```latex
\title{How can slip stick friction be maximized between finger and computer mice}
\author{Jimmy Zeng}
\date{\today}
```

Rendered title page: **title, "Jimmy Zeng", and today's date.**

| Required | Present? | Note |
|---|---|---|
| Student code | **NO** | A personal name is not a student code, and the guide asks for the code. |
| Research question | **partly** | The text is phrased as a question, but it is presented as a *title*, not labelled as the research question. Worth making explicit. |
| DP subject | **NO** | Physics (subject-focused pathway). |
| Word count | **NO** | Currently **3,272** assessable words (measured with `tools/ee-wordcount.py`). |

Also: `\date{\today}` prints the build date, so the title page changes every time he compiles. The IB does
not ask for a date; a fixed date (or none) is safer than a date that drifts.

## Suggested replacement block

Placeholder in `<>` — **only he knows his student code**, and it must be the code the IB/school issued,
not a guess.

```latex
\title{How can slip stick friction be maximized between finger and computer mice?}
\author{Student code: <YOUR STUDENT CODE>}
\date{}

\begin{document}
\maketitle

\vspace{1em}
\noindent\textbf{Research question:} How can slip stick friction be maximized between finger and computer mice?

\noindent\textbf{Subject:} Physics

\noindent\textbf{Word count:} 3,272
```

Three deliberate choices in that block:

1. **`\date{}`** — removes the drifting date rather than printing a build timestamp.
2. **The question mark** — the research question is a question; the current title has no terminal `?`.
3. **Word count stated on the title page**, per Figure 15, using the measured 3,272. **Re-measure after the
   conclusion is added** — 329 words of conclusion brings it to about 3,600.

## The name question

The current page prints "Jimmy Zeng". Two separate rules touch this:

- Figure 15 asks for a **student code**, not a name — so the name does not satisfy requirement 1.
- The guide's note on acknowledgements/dedications says those pages "must not contain any 'identifiers':
  for example, the names of people that would make you or your school identifiable." That rule is scoped to
  acknowledgements, not the title page, so a name on the title page is not forbidden by that sentence.

**Recommendation:** put the student code on the title page (as required) and drop the name — it costs
nothing and keeps the submission anonymous-consistent with how the IB marks. If his school's own template
requires a name, follow the school.

## What I did not do

I did not edit `main.tex`. The student code is unknown, the subject/pathway wording is his call, and the
word count will change once the conclusion exists — so a placeholder block is safer than a guess that looks
finished.

## Checklist

- [ ] Insert the student code.
- [ ] Add the research-question line, with the question mark.
- [ ] Add "Subject: Physics".
- [ ] Add the word count — re-measure **after** the conclusion goes in.
- [ ] Replace `\date{\today}` with `\date{}`.
- [ ] Decide name vs code.
