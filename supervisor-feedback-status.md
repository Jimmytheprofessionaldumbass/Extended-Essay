# Supervisor feedback — status of every comment (verified in `main.tex`, 2026-10-21)

The supervisor's comments are still sitting at the bottom of `main.tex` (lines 755–767) as `%` comments.
Each one is checked below against the **current** file, not against the version he read.

| # | Supervisor's comment | Status | Evidence |
|---|---|---|---|
| 1 | "Methodology is well written, but of course data is still not in" | **Partly addressed** | `Results and Discussion → Quantitative` now holds measured tables (e.g. PC Board: 17 normal-force readings, F_fr = 70, μ_fr = 0.290). So data *is* in — but it is the **old sensor's** data, and the essay itself says that sensor "would stop updating when no change is detected". |
| 2 | "Lugre model differential equation is not there" | **Addressed** | `main.tex:162–168` now carries both equations: `\dot{z} = v − h(v)z` and `F = σ₀z + σ₁\dot{z} + f(v)`, with a paragraph explaining them. |
| 3 | "Some punctuation errors are present throughout the document, periods, etc" | **Open** | Not systematically checked. Needs a read-through; a script cannot judge whether a period belongs. |
| 4 | "Conclusion?" | **NOT DONE — the biggest gap** | There is **no conclusion section at all**. The only occurrence of the word is inside his own comment at line 759. The essay ends at `Limitations of the data` and goes straight to the bibliography. |
| 5 | "You mention a state space system with 'Vector' matrices … but no matrices are seen" | **Addressed (by removal)** | Zero occurrences of `matrix`/`bmatrix` in the file — the phrase is gone, so there is nothing to explain. |
| 6 | "Coloring of that stress-strain diagram doesn't fit … black and white would look better" | **Open** | Cosmetic; the figure is `images/sscurve.png`. Would need the source `sscurve.xcf` (16 MB, in the EE folder) re-exported in greyscale. |
| 7 | "Background Figure 1 could be clearer by making the curve another color" | **Open** | Cosmetic; it is a TikZ drawing, so a colour change is a one-line edit. |
| 8 | "sections 2.1.1 and 2.1.2 are a bit short but maybe it makes sense" | **No action** | He hedged it himself; they are sub-sub-sections. |
| 9 | "Formatting: Maybe bold the equations / relationships" | **Open** | Cosmetic, and arguably against convention — display equations are already visually separated. Low value. |
| 10 | "placement of the stress strain diagram doesn't fit in so well in the middle of a derivation" | **Open** | Real readability point: move the figure to after the derivation. |
| 11 | "The visualization figure could be placed before or after the methodology, currently it is in the middle and a bit randomly placed" | **Open** | Same class as #10 — float placement. |
| 12 | "more in-text citations and references to the literature" | **Partly** | 24 citation commands now. Whether that is "more" depends on what he had before; the bibliography file holds 18 entries (16 cited). |

## What actually blocks submission

**Only two things:** the **missing conclusion** (#4) and the **data question** (#1 — whether the old-sensor
tables stay as the results or the new experiment replaces them). Everything else is polish.

## The conclusion — what criterion A/D asks for

The guide requires "a conclusion that considers your answer to the research question in the light of your
close readings" (criterion A), and criterion D wants a balanced evaluation of the essay's own strengths and
limitations. So the conclusion needs to do four things, in this order:

1. **Answer the research question directly** — *"How can slip stick friction be maximized between finger and
   computer mice"* — with the mechanism he actually established (surface choice, normal-force consistency,
   the stick–slip transition), not a restatement of the topic.
2. **State what the data support and what they do not.** The μ_fr values are single-force-point Coulomb
   estimates from a sensor that froze; they cannot support a LuGre parameter set. Saying that plainly is
   worth more than over-claiming.
3. **Evaluate the method against its own limitations section** — he already wrote that section; the
   conclusion must use it rather than repeat it.
4. **One sentence of forward transfer** — what a better instrument or a moving-surface design would settle.

Suggested length: **200–300 words**, which fits inside the current headroom (3,272 of 4,000 used).

## Where I stop

I have not written the conclusion or edited the figures — both are his content and his aesthetic call.
This file is the checklist; the drafting is his.
