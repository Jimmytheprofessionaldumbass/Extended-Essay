# RPF assembly sheet — mechanical order, 2026-10-25

For the **EE Reflective Statement, due Wed 28 Oct**. Companion to
`RPF-worksheet-2026-10-24.md` (why) and `RPF-draft-skeleton.md` (what criterion E asks).

**This file contains no prose to copy.** Every line below is either *your own sentence number*
from `reflections`, or an instruction to write one sentence yourself. The point is that the
ordering is mechanical, so you spend your time on the four evaluative sentences — the only part
that needs thinking.

Sentence numbers are stable: they come from `python3 ~/.openclaw/workspace/tools/rpf-check.py
--sentences ~/Extended-Essay/reflections`.

---

## Build it top to bottom

| # | Put this in | Words | Running | What it is |
|---|---|---|---|---|
| 1 | **your sentence 4** — keep nearly whole, it is the best sentence in the draft | 35 | 35 | the rejected broad question |
| 2 | **your sentences 5 + 6 merged into one sentence** — they are one action split across two, and 6 is a fragment starting "And" | 42 | 77 | reading Dahl/LuGre/Coulomb to find a factor |
| 3 | **NEW (yours):** what rejecting the broad question taught you about what a research question has to be | ~35 | 112 | ← evaluative. The material is already in sentence 4 |
| 4 | **NEW (yours):** name whose decision the design flaw was, then **your sentence 9's own admission** ("I should have looked a bit more into the experiment and adapted my experiment into it") | ~45 | 157 | ← evaluative. Currently buried inside the bearing-screw sentence |
| 5 | **your sentence 16** — the sensor locking and nullifying the data; trim the technical restatement | 48 | 205 | the failure, stated plainly |
| 6 | **your sentence 17** — the qualitative observation that survived | 31 | 236 | what outlived the broken rig |
| 7 | **your sentence 18** — the new sensor, not yet used *(optional: the checker counts this as plan, not reflection — keep it only because it explains why the experiment was not run; dropping it buys 17 words)* | 17 | 253 | must stay past/present; **do not imply results** |
| 8 | **NEW (yours):** how discovering the finger is a variable changed how you design an experiment | ~40 | 293 | ← evaluative |
| 9 | **your sentences 11 + 13, compressed** — finger is not a constant material; the ethanol result did not reproduce | ~75 | 368 | the two specific examples |
| 10 | **NEW (yours):** one thing you will do differently in the next piece of research, and why this project is the reason | ~90 | 458 | ← the transfer statement. Criterion E names it explicitly |

**Projected 458 / 500.** Twenty-two words of slack for the joins.

## Cut, and do not mourn them

Sentences **7, 8, 9 (as a whole), 10, 12, 14, 19, 20, 21** — 293 words. Read the list once:
· 7 is the old experiment's subject matter, superseded by 16–17
· 8 is "six-axis sensors too expensive", folds into 16 as a clause if you want it
· 9 is the bearing-screw digression — **rescue only the admission**, that is row 4 above
· 10 restates the experimental question the essay already states
· 12 is the literature claim that alcohol removes oil — background, and 11/13 already carry it
· 14 is a note to yourself
· **19, 20, 21 are a to-do list** — what you will ask your supervisor, what further experiment you might
  run. Criterion E does not ask for a plan. This is the largest single cut and the one that feels most
  like losing something real; it is not, because a plan is not reflection.

## The one test for rows 3, 4, 8, 10

> Does the sentence say something about **you as a learner**, or about **what happened**?

If it is the second, it belongs in rows 1–2, 5–7 or 9, not there. Each of the four new sentences
must contain a judgement, a change, or a lesson — not an event.

## Then check it

```
python3 ~/.openclaw/workspace/tools/rpf-check.py <your new file>
```

It reports the word count against 500, how many of your sentences evaluate, how many are a plan
rather than a reflection, how many specific examples you have, and whether a transfer statement
exists. It exits non-zero if any of those fail.
Current draft: 649 words, 1 of 21 evaluative, 6 plan sentences, no transfer — every one of those
numbers has to move.

## Still only you can supply

1. **Dates of reflection sessions 1 and 2** — the form records attendance at all three; only the
   third (viva voce, Mon 19 Oct) is known.
2. **What the supervisor actually said at the viva** — the guide calls it "an important source of
   ideas for your reflective statement", and row 3's judgement should reflect it.
