# EE conclusion — scaffold with the real numbers filled in

**Why this file exists:** the essay has no conclusion at all (verified 2026-10-21), and it is the last
item blocking submission. This is a **structure with the actual figures inserted**, so writing it becomes
filling in prose rather than hunting for numbers. Nothing here is in the essay yet.

**Research question:** *How can slip stick friction be maximized between finger and computer mice?*

---

## Paragraph 1 — answer the question directly (≈70 words)

The answer the data support, stated plainly:

> Kinetic friction between finger and mouse surface varies by a factor of about **2.3** across the three
> treatments tested — mean μ ≈ **0.43** for cello rosin, **0.65** for the clear PC board, and **1.61** for
> Sharpie — so surface treatment is a first-order lever on slip–stick behaviour, not a second-order one.
> The mechanism is the compliance of the contact: a viscoelastic surface (tape) and a particulate layer
> (rosin dust) both store elastic energy before slip, while a rigid, oil-free plastic surface does not.

Numbers to cite (recomputed from the tables, not copied): rosin 0.428 ± 0.159, PC 0.646 ± 0.321,
Sharpie 1.609 ± 1.047.

## Paragraph 2 — say what the data do NOT support (≈80 words)

This is the paragraph that earns criterion D, and it must not be softened:

1. **The stated hypothesis was not supported.** Rosin was predicted to give the largest change and PC the
   smallest; the measured means are the **reverse** for those two surfaces (rosin 0.43 < PC 0.65).
2. **The spread within a surface is as large as the difference between surfaces** (PC trials range
   0.29–0.91, a 3.1× spread). With three trials per surface and no error bars, the ordering is suggestive
   rather than established.
3. **The static–kinetic *difference* was never computed.** Every table reports a single coefficient
   (μ = F_fr / F_N). The quantity in the research question's hypothesis requires both coefficients.

## Paragraph 3 — evaluate the method against its own limitations (≈70 words)

Do not repeat `Limitations of the data`; **use** it. One sentence of synthesis:

> The dominant uncertainty is instrumental rather than physical: the load cell was a mass scale that
> latched when the force stopped changing, so the friction trace — the one signal that would separate
> static from kinetic behaviour — was truncated exactly at the transition of interest. Two Sharpie trials
> returned μ > 1, which is not physically credible for this contact and is most likely an artefact of the
> normal-force channel under-reading (the finger's own weight and the bracing arm are both unaccounted).

## Paragraph 4 — what would settle it (≈60 words)

> A moving-surface design — surface translated under a stationary finger — would remove the operator's
> bracing force from the measurement and make the velocity genuinely controlled, which is the condition
> the LuGre parameterisation assumes. Pairing it with a load cell that samples continuously would allow
> σ₀ and σ₁ to be fitted rather than assumed.

## Closing sentence — the transfer (≈25 words)

> What this study establishes is narrower than the original hypothesis but firmer: surface compliance and
> surface chemistry each move kinetic friction substantially, and they do so independently of load.

---

## Checks before this goes into `main.tex`

- [ ] Word budget: ~329 words of draft prose above; current essay is **3,272 of 4,000**, so there is
      room (see `tools/ee-wordcount.py`). Adding 329 → ~3,600, still under.
- [ ] Resolve the **μ > 1** question first — if the 0.385267 sensor factor applies to one channel, the
      Sharpie mean changes and paragraph 1's numbers change with it.
- [ ] Check trial 3's last row (`F_fr` 715 → 165 with `F_N` unchanged) before quoting the Sharpie mean.
- [ ] Decide the μ_s question: either add the static readings, or keep paragraph 2's honesty about it.
- [ ] Then move the supervisor's `% Conclusion?` comment at line 759 out of the file.
- [ ] **There are four trial videos per surface in `EE Data/` but only three trials in the tables** —
      `Rosin first/second/third/fourth trial.mp4` and `Sharpie first/second/third/fourth trial.mp4`, plus
      three PP videos. Either the fourth trials were discarded (say why, in the method) or one set of
      numbers is missing from the results. Worth checking before quoting a mean over "three trials".

## Do not

- Do not claim the hypothesis was supported.
- Do not quote a Sharpie μ above 1 as a result until the units question is settled.
- Do not add a fifth surface or a new experiment to the conclusion — there is no data for it.
