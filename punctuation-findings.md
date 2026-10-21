# EE punctuation pass — mechanical findings (2026-10-21)

Produced by `~/.openclaw/workspace/tools/ee-punct-scan.py` against `main.tex`. **Report only — nothing
was edited.** Re-run after fixing:

```
python3 ~/.openclaw/workspace/tools/ee-punct-scan.py ~/Extended-Essay/main.tex
```

## Real fixes — do these

| Line | Issue | Fix |
|---|---|---|
| **79** | **Missing closing parenthesis**: `…interlocking with one another (Figure \ref{fig:asperities illustration}.` | add `)` before the period |
| **89** | Sentence starts lowercase after a full stop: `…dependent on normal force. this is because…` | capitalise → `This is because` |
| **237** | `…similar to Hooke's law. rearranging, we get:` | `Rearranging` |
| **742** | `…it slips. the addition of the elastic…` | `The addition` |
| **742** | **Repeated word**: `the fact that that the $\alpha$` | delete one `that` |
| **198** | **Repeated word**: `as they are are history-dependent models` | delete one `are` |
| **136** | Double space — but it is **trailing whitespace at end of line** (`…next cycle.  `) | harmless in LaTeX; strip if you care |
| **89** | Comma splice, not just punctuation: `This, for instance explains` | `This, for instance, explains` |

## Worth a decision (not mechanical)

- **Line 89** ends `…such as:` with a colon and then continues into a list — fine if a list follows, but the
  following paragraph does not read as one. Check the structure.
- **Line 198** contains an actual aside to the reader: *"wait, aren't we talking about presliding
  displacements to be the thing that is supposed to be derived, why are we particularly putting friction
  back, we rearrange"*. That is a draft note, not prose. **Remove or rewrite it** — this is the single most
  visible drafting artefact in the document.
- **Line 322** `There exists several known methods` → `There exist several known methods`.
- **Line 134** `because some guys did a research` — informal; `because previous research has` reads better
  in an academic register.

## Ignore these

- **Apostrophes**: `'` in the source renders as `’` in pdflatex, so `Dahl's`, `subject's`, `coulomb's` are
  already typographically correct in the PDF. The scan labels them informational.
- **Line 14** `\addbibresource{works cited.bib}` — a bibliography command, not prose.

## Paragraphs that do not end in terminal punctuation

Four blocks flagged. Three are followed by a display equation or a list, which is legitimate; check the
first one (`This, for instance explains … apparent surface area`) because it also has the comma-splice
problem above.

## What this cannot do

Mechanical rules only. Whether a period *belongs* at a particular place is a judgement call — the scan
finds shapes, not meaning. The supervisor's "punctuation errors throughout" almost certainly refers to a
mix of the items above plus sentence-boundary judgement across the whole document, so a read-through is
still needed after the mechanical fixes.
