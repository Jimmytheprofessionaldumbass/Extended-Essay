# EE Conclusion — what to add, and the exact figures to use

**Section:** `main.tex:771`, `\subsection{Conclusion}` — currently **143 words**.
**Essay total:** 3,561 / 4,000, so **439 words of headroom**.

`tools/conclusion-check.py` reports three of four required features missing:

| | |
|---|---|
| ANSWER | **missing** — says "there was influence between differing surfaces", not what the effect on the static–kinetic difference is |
| RESULT | **missing** — no number anywhere in the section |
| EXPECTATION | **missing** — never says the data reverse the hypothesis |
| LIMIT | present |

All three are fixable in about **100 words** and every figure below is already computed from the
report's own tables (`tools/ee-surface-summary.py`, `reports/ee-surface-summary-2026-10-24.md`).

---

## The three sentences that are missing

### 1. The answer (~35 words)

The aim at line 346 is *how material surface affects the difference between static and kinetic
coefficient of friction*. The current conclusion never says. It needs to name the mechanism it
established — surface compliance and surface chemistry each move the kinetic coefficient — rather
than reporting that "influence" existed.

### 2. The result (~35 words)

Cite the numbers. Measured mean coefficients across three trials each:

| surface | mean μ | SD | range |
|---|---|---|---|
| Sharpie | **1.609** | 1.047 | 0.459 – 2.508 |
| PC Board | **0.646** | 0.321 | 0.290 – 0.914 |
| Cello Rosin | **0.428** | 0.159 | 0.276 – 0.594 |

Highest surface is **3.8×** the lowest. That single ratio is the result.

### 3. The expectation (~30 words)

The hypothesis at line 347 predicts **Cello Rosin largest, PC Board smallest**. The data give
**Sharpie largest, Cello Rosin smallest** — the prediction is reversed for exactly the two surfaces
it named.

Material to explain it already exists at line 754: rosin jumps straight to Coulomb friction because
its `α` in the LuGre model is large, which predicts a *smaller* static–kinetic difference, not a
larger one. So the reversal is consistent with the model the essay built — it is not a failure to
explain, it is a result the essay's own mechanism anticipated.

---

## The caveat that has to sit beside the numbers

Within-surface spread is comparable to the gaps between surfaces: PC Board's range is 0.624 wide
against a mean of 0.646. With three trials per surface and no error bars, the ordering is suggestive,
not established. One sentence saying so costs nothing and protects the ranking from being read as
stronger than it is.

## A method caveat worth 30 words

The force channel was never calibrated against a known mass, so μ is a ratio of two channels'
readings. A single multiplicative correction **cannot reorder the surfaces** — proven in
`reports/ee-calibration-2026-10-24.md` — so the ranking stands, but the absolute values are not
comparable to literature values. Saying this converts a hidden defect into a stated limitation,
which is what criterion D rewards.

---

## What I have not done

Written any of it. These are the figures and the sequence; the prose is his, and this is assessed
work. The structure above maps one-to-one onto the four features the checker looks for, so
`conclusion-check.py` is the pass/fail test once he has written it.
