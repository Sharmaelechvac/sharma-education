# QA Audit — TUG Lesson vs Sanjay's 2026-11-14 Specs

File audited: `docs/meter-main-combo/index.html` ("How to Set Up a Meter Main Combo — the Sharma TUG")
Audit type: read-only. No lesson files were edited.

## Verdicts

### 1. TUG GFI cover — extra-duty while-in-use (bubble), NOT a flip cover, 406.9(B)
**PRESENT — strong, in 6 places.**
- Step 2: "fitted with a **listed extra-duty while-in-use cover** — the deep bubble cover that closes over a plugged-in cord and stays weatherproof while it's in use (NEC 406.9(B)). **Not a regular flip cover:** a flip lid only protects the outlet when nothing is plugged in…" + cite chip "NEC 406.9(B) — extra-duty in-use cover".
- Gear list: "a **listed extra-duty while-in-use (bubble) cover** — … **not a regular flip cover**".
- Quick Numbers (TUG outlet row): "weatherproof box + **listed extra-duty while-in-use (bubble) cover — not a regular flip cover**, marked".
- Diagram label: "extra-duty in-use (bubble) cover — not a flip cover".
- Checklist item 2: "extra-duty in-use (bubble) cover on".
- Common fails: "**Regular flip cover on the TUG GFI.** Wrong cover … per 406.9(B)."

### 2. Male adapter + locknut + bushing at every conduit entry — VERY important
**PRESENT — strong, in 6 places.**
- Step 1: "Every pipe that enters the can lands on a **male adapter**, with the **locknut run up tight** inside and a **bushing** over the threads where the conductors pass — **very important**, and it's its own line on the Sharma TUG checklist."
- Gold callout box: "**Very important — male adapter · locknut · bushing.** No pipe stubbed into the can raw…"
- Gear list: "**PVC male adapters, locknuts, and bushings** for every pipe entry".
- Quick Numbers (Pipe entries row): "**Male adapter + locknut + bushing** at every conduit entry — very important."
- Checklist item 4 and Common fails ("pipe stubbed in with no male adapter") also carry it.

### 3. Exception: small ground hole / back ½-inch knockout best practice
**PRESENT — complete, all elements, in 4 places.**
- Step 1: "One exception: the **small ground hole** in the bottom of the can, where the grounding conductor leaves — that one typically doesn't need a bushing. **Great practice when the can allows it:** if the combo has a **½-inch knockout toward the very back** of the can, out of the way of the underground pipe, bring the ground out there **with a bushing**. But that's **not typical at all**…"
- Same nuance repeated in the gold callout, in Step 3's parenthetical, and in the Quick Numbers Pipe entries row ("Best practice if the can has a ½-in knockout toward the very back, clear of the underground pipe: ground out there, with a bushing — not typical").

### 4. Underground downpipe — 2-in Sch 40 PVC, 3 ft under, 90° sweep toward street, 2 straps min, Duke/SECO
**PRESENT — every element, in 5 places.**
- Step 1: "**The underground downpipe:** **2-inch Schedule 40 PVC**, down from the bottom of the can to **3 feet under** grade, a **90° sweep attached** at the bottom with the sweep **pointed toward the street**. Strap the downpipe to the wall — **2 straps minimum**. This is a **power company requirement (Duke Energy and SECO)**, not a Sharma preference…"
- Quick Numbers (Underground downpipe row): "**2-in Schedule 40 PVC**, **3 ft under** grade, **90° sweep** attached at the bottom, pointed **toward the street**; **2 straps minimum** — power company requirement (Duke Energy / SECO)".
- Checklist item 1, gear list (sweep + 2-in Sch 40 + "pipe straps — 2 minimum"), and Common fails all carry the full spec.
- Minor weakness only: the downpipe is not drawn or labeled in the main TUG diagram (the diagram shows combo, GFI, bridge, GEC-in-PVC and UFER). Text coverage is complete.

### 5. Sharma standard gear — Siemens (MM0202B1200); no Eaton
**PRESENT.**
- Gear list: "Sharma usually runs **Siemens** — meter main combo (example: Siemens MM0202B1200, 200A main)."
- Quick Numbers (Meter combo row): "Siemens meter main — e.g. MM0202B1200, 200A main".
- Full-text check: "Eaton" = 0 hits; "MBT48 / Type BR / CSR" = 0 hits. No competing brand appears anywhere in the lesson.

### 6. UFER-first grounding (250.52(A)(3); GEC cap #4 Cu per 250.66(B)); run in PVC
**PRESENT — strong.**
- Top banner: "**Grounding at Sharma — UFER first:** typically we ground the TUG to the **UFER** … with the grounding conductor run in **PVC pipe**."
- UFER section chips: "NEC 250.52(A)(3)" and "NEC 250.66(B)"; body: "at least **20 ft** of either **½-inch rebar** … or **bare copper conductor, #4 AWG or larger**, encased in at least 2 inches of concrete".
- "**#4 copper is the largest GEC the code requires to a UFER** (250.66(B)) — bigger is allowed, never required."
- PVC run stated in the UFER bullets ("Run it in PVC"), Step 3 ("run it **down the wall in PVC pipe**"), the diagram ("GROUNDING WIRE IN PVC PIPE"), and Quick Numbers.

### 7. Sanjay's 6-item TUG checklist, in order
**PRESENT — exact order, exact six items.**
1. "Meter base mounted — plumb, solid, right location and height; downpipe 2-in Sch 40 PVC, 3 ft under, 90° sweep toward the street, 2 straps minimum"
2. "TUG Service GFCI Outlet — 20A breaker in, GFI in, extra-duty in-use (bubble) cover on, and marked"
3. "Intersystem grounding bridge installed and bonded"
4. "Locknut & bushing check — male adapters seated, locknuts tight, bushings on the conduit entries (small ground hole doesn't need one)"
5. "Grounding — GEC to the UFER, run in PVC pipe, clamped"
6. "TUG complete — wide shot photo taken (plus bridge + GFI close-up)"
Progress reads "0 of 6 done"; step sections cross-reference the same item numbers (Step 3 → Item 5, Step 4 → Item 3, etc.).

### 8. TUG scope only — no leftover full-service content
**PRESENT (clean).**
- Intro fences the scope: "It's not the whole house service — the panel, feeders, and branch work come at rough and trim. **The TUG is these five things, done right:** meter on the wall · breaker and GFI in, and marked · grounding to the UFER in PVC pipe · grounding bridge on · covers, labels, and photos."
- The five steps are exactly: meter on wall (+ downpipe) / breaker + GFI marked / UFER grounding in PVC / grounding bridge / close up, label, photograph.
- Full-text checks: "SPD" = 0, "surge" = 0, "back-to-back" = 0, "310.12" = 0. The single "feeder" hit is the intro's scope exclusion above, not a work step. No panel-feed step, no SPD step, no service-conductor sizing step remains. (The UFER section's "#4 AWG or larger" is the electrode definition under 250.52(A)(3), not service-conductor sizing.)

## Overall gap list

**No blocking gaps. All 8 specs are present in the lesson text.**

Minor / optional polish only:
1. **Spec 4 (visual):** the underground downpipe (2-in Sch 40, 3 ft under, 90° sweep toward the street, 2 straps) is fully specified in Step 1, Quick Numbers, checklist item 1, the gear list, and Common Fails, but it is not drawn or labeled in the main TUG diagram.
2. **Spec 1 (wording):** checklist item 2 and Step 5 say "extra-duty in-use cover" without the word "listed" — the full "listed extra-duty while-in-use (bubble) cover" wording is carried in Step 2, the gear list, and Quick Numbers, so nothing is actually missing.
