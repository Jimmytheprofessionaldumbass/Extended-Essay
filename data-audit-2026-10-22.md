# EE data audit — what the numbers actually show (2026-10-22)

Read from the current `main.tex` (`Results and Discussion → Quantitative`). **No file was edited.**
This is the check to do *before* writing the conclusion, because two of these points change what the
conclusion can honestly claim.

---

## 1. The headline problem: there is no static coefficient anywhere in the data

The research question and the hypothesis are both about **the difference between static and kinetic
friction**:

> "This investigation aims to determine how material surface affects the difference between static and
> kinetic coefficient of friction." (`main.tex:338`)

But every results table computes only **μ_fr = F_fr / F_N** — one coefficient per row. There is **no μ_s
column, and no static-force measurement recorded as a separate quantity** in any of the tables. So the
quantity the essay says it set out to measure is not in the results.

**This matters for the conclusion.** Either:
- (a) the static coefficient was measured but not tabulated — then the tables need a μ_s column, or
- (b) it was not measured — then the conclusion must state that the data support a **kinetic-only**
  comparison, and the research question has to be answered as "the difference could not be quantified;
  what was measured is how much *kinetic* friction varies with surface."

Option (b) is honest and still answerable. Option (a) is better if the numbers exist.

---

## 2. Sharpie: the three trials are not measuring the same thing

| Trial | rows | mean μ_fr | range of μ_fr |
|---|---|---|---|
| 1 | 5 | **0.459** | single F_fr value (100) against 5 normal forces |
| 2 | 6 | **2.508** | 1.52 – 3.61 |
| 3 | 15 | **1.860** | 0.41 – 2.56 |

Trial 1 uses **one friction force (100) divided by five different normal forces** — that is not a
measurement of friction varying with load, it is the same friction force assumed constant. Trials 2 and 3
measure F_fr per row. So trial 1 is methodologically different from 2 and 3, and averaging all three would
be mixing two designs.

**Also: μ_fr > 1 in trials 2 and 3.** That is physically possible but unusual, and here F_fr (515–635) is
consistently *larger* than F_N (148–310) — a factor of 2–3. For a finger on a taped surface that is worth
double-checking against the raw sensor units before it goes in the conclusion.

**Trial 3's last row is almost certainly a data-entry error:** `402.5 / 165` → μ = 0.410, after a row of
`403.5 / 715` → μ = 1.772. A friction force dropping from 715 to 165 while normal force stays at ~403
is not a physical transition, it is a typo or a mis-read row.

---

## 3. The averaging method is stated nowhere

The means are **means of the ratio** (μ per row, then averaged), not **ratio of the means**. Verified:
trial 2 = 2.50818 both ways by coincidence of construction, trial 3 = 1.86003 as a mean of ratios but
**0.410** as ratio-of-means — so the choice genuinely changes the number by a factor of 4.5 in trial 3.

That is fine, but it must be **stated in the method**, and justified. Averaging ratios whose denominators
range from 148 to 403 weights small-normal-force rows much more heavily.

---

## 4. A wording bug that a reader will notice immediately

`main.tex:340`:

> "The independent variables are clear pc, cello rosin, and sharpie while the **independent** variable is
> the difference between static and coulomb coefficient of friction."

The second one is the **dependent** variable. This is the kind of thing an examiner circles.

---

## 5. What the conclusion can honestly say

Given the above, the defensible claims are:

1. **Kinetic friction varies substantially by surface treatment** — PC board μ ≈ 0.29, Sharpie μ ≈ 0.46–2.5,
   cello rosin μ ≈ 0.73–0.91 (per the table captions). That ordering is a real result.
2. **The static–kinetic *difference* was not quantified**, because only one coefficient was computed. Say
   so plainly; criterion D rewards an evaluated limitation over an overclaim.
3. **The hypothesis about rosin having the largest change cannot be tested by this data** — the change
   requires both coefficients. What the data show is that rosin gives high kinetic friction, which is a
   different (and weaker) claim.
4. **The sensor limitation is already documented** in `Limitations of the data` and should be cited, not
   repeated.

---

## 6. Fix order, cheapest first

1. Line 340: `independent` → `dependent` (one word).
2. Trial 3 last row: check `165` against the raw data (likely `765` or `615`).
3. Decide on trial 1: either re-express it as a single measurement (not a mean over varying F_N), or drop it
   from the Sharpie average and say so.
4. State the averaging convention in the method (mean of ratios, and why).
5. Add a μ_s column **if the static data exist**; if not, say in the results that only the kinetic
   coefficient was computed and why.
