# EE experiment — redesign options for the new force sensor (not yet run)

**Source:** his own `~/Extended-Essay/experimental_notes.txt` (8 observed problems) + `reflections`.
**Status:** planning only. Nothing here has been run, and nothing should be written into the essay as a
result.

---

## The eight problems recorded, and what each one forces

| # | His observation | What it actually is | Design consequence |
|---|---|---|---|
| 1 | "my current setup only looks for coulomb friction" | The rig only samples near-constant-speed motion, so it can only ever fit a Coulomb term | To fit LuGre you need the **Stribeck region**: many low-speed points, not one speed |
| 2 | "to get stribeck friction you need more velocities at lower speed" | Same point, already understood | **Sweep speed in small steps below ~5 mm/s**, log dwell at each |
| 3 | "the rope/string has some weight … straight, the force sensor measured about 6-8" | A **constant offset** from the string's own weight plus the load cell's zero | Measure the offset with the finger absent, subtract it; do not zero the sensor at a different pose |
| 4 | "this force sensor is horrible, it scales down by a factor of 0.385267" | Sensitivity is not 1:1 and may not be linear over range | **Calibrate against a known mass set** across the working range, fit the slope; report the fitted calibration, not the maker's figure |
| 5 | Middle finger of writing hand was most repeatable | The finger is a variable material — this is a *choice of standard*, not a nuisance | **State the finger as part of the apparatus**, keep it constant across all trials, and say so |
| 6 | "Ensure both hands are clean" | Cleaning is an uncontrolled treatment if not specified | Fix a **wash protocol** (same soap, time, drying) and record it as a controlled variable |
| 7 | "the motor oil hadn't been changed" | The surface is a consumable with drift | Either replace the surface per session, or **record order and re-test the first condition at the end** to detect drift |
| 8 | "fingernail is blocking accurate movement"; "the force holding my body still may be introduced" | The finger's contact geometry and the operator's bracing both leak into the measured tangential force | Cut the nail to a fixed length; **brace the forearm against a fixed stop** so the bracing force is transmitted to the frame, not through the contact |

---

## Option 1 — Constant-speed drag (the smallest change that can produce LuGre parameters)

**What it is:** clamp the sensor's cord to a motorised lead screw or a drop-weight pulley; drag the
finger across the surface **at one fixed speed per trial**, sweeping speeds in small steps.

- **Gives:** the friction–velocity curve f(v), which is exactly where the Stribeck dip lives — the region
  the current setup never sampled.
- **Fits:** Coulomb + static friction directly; LuGre's σ₀/σ₁/σ₂ and v_s by fitting the curve.
- **Reuses:** the existing linear-motion setup, the calibrated sensor, the same finger.
- **Cost:** needs a way to hold a speed constant — a lead screw (the "bearing screws" paper he already
  found) or a stepper-driven carriage. Drop-weight pulleys are cheap but the speed decays under load.
- **Fails at:** pre-sliding (the static-to-kinetic transition), which needs sub-millimetre displacement
  resolution the sensor cannot give.

## Option 2 — Acceleration-step / stick–slip cycle (measures the parameters he actually cares about)

**What it is:** pull at a slowly increasing force until the contact breaks free, then reduce the pull and
let it re-stick. Record the force trace through the transition, repeatedly.

- **Gives:** the **static peak**, the **breakaway drop**, and the **stick–slip period** — the features that
  make drag-clicking physically intelligible, and the ones a LuGre model predicts.
- **Fits:** σ₀ (stiffness of the contact bristles) and σ₁ (micro-damping) much better than a constant-speed
  sweep does.
- **Cost:** very low hardware cost — this needs *no* constant-speed rig, only a slow force ramp.
- **Weakness:** the speed is not controlled, so the friction–velocity curve cannot be produced from it.

## Option 3 — Both, in sequence (my recommendation if hardware time allows)

Run Option 2 first because it is nearly free, and it answers the question the essay is really about
(why a surface transitions between sticking and sliding). Then run Option 1 at 4–6 speeds for the curve.

---

## What to report, whichever option he picks

1. **Calibration line** — measured force against known mass, with the slope and residuals.
2. **The offset** — string weight + zero, measured with the finger absent.
3. **The finger** — which finger, which hand, nail length, wash protocol. Treated as apparatus.
4. **The surface** — material, age, cleaning, and the drift check if it was not replaced.
5. **Per trial, not per condition:** the raw force trace, so the transition is visible rather than
   reduced to a single average. An averaged force hides exactly the feature being studied.

## Things to keep out of the essay

- Do not present the failed first sensor's data as results — describe it as the method problem it exposed
  (this belongs in the RPPF, not the results section).
- Do not claim a LuGre parameter set from a sweep that only covers the Coulomb region — that is the mistake
  the current setup was already making.
- Do not report the 0.385267 factor as a calibrated instrument response; it is a symptom, and the calibration
  must be measured.

## Question for the supervisor (one line, worth asking before building anything)

> Given the sensor cannot resolve pre-sliding displacement, is a friction–velocity sweep (Stribeck region)
> an acceptable substitute for a full LuGre parameter identification, or should the scope be narrowed to
> static-vs-kinetic transition behaviour only?
