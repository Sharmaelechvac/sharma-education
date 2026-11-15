# Grounding bridge — diagram fix for the TUG lesson

For: `~/workspace/sharma-education/docs/meter-main-combo/index.html`, main front-elevation diagram.
Note: the diagram in the file is `viewBox="0 0 600 400"` (not 460). All coordinates below are for that 600×400 diagram, whose existing layout is: combo x245–355, y52–220 (bottom edge y=220); GFI stub at x=318, GFI box x292–344, y238–280; GEC-in-PVC path `M258 220 V286 H180` (vertical run at x=258 from the combo bottom down to y=286, then horizontal left to the UFER stub at x=180).

## (a) The bridge as it actually is — from the real Sharma photos

Sources: `~/workspace/exj-root-tracker-app/seed-originals/17385-intersystem-bridge-gfci.jpg` and `~/workspace/exj-root-tracker-app/seed-originals/212-finished-bridge-gfci.jpg` (both show it clearly; 212 is the finished install with the GFI cover closed).

- **What it is:** a white, elongated rectangular plastic intersystem bonding bridge (Eaton, per the office record — brand name is embossed on the face; do not put the brand in the lesson drawing). Its long axis is **horizontal**, it sits flat against the block wall, and its face is smooth white with **one visible screw** near the middle. No exposed terminals or lugs on the face.
- **Where it mounts:** **in-line ON the vertical grounding (GEC) PVC pipe run** — the grey pipe that drops out of the **bottom-left of the combo** and runs straight down the wall to grade/the UFER. The pipe enters the **top of the bridge at its left end** and exits the **bottom of the bridge at the same left end**; the bridge body then extends **to the RIGHT** of the pipe (toward the GFI side). In the 212 photo you can even see the pipe interrupted at the bridge — in at the top, out at the bottom. The GEC inside is continuous; the bridge clamps/bonds at that point on the run. There is **no separate jumper wire** from the bridge to anything else.
- **How far down:** roughly **halfway down the wall run** — clearly **below the GFCI**, not up at the combo. In the 17385 photo the GFCI box bottom is at ~34% of the frame height and the bridge is at ~48%; in the 212 photo the GFCI cover bottom is at ~43% and the bridge at ~63%. Either way: bridge is on the left pipe, noticeably lower than the GFI.
- **Relative to the GFCI:** the GFCI is on its **own separate short stub** out of the bottom-right of the combo (x≈318 in the diagram). The bridge is **not** next to, under, or attached to the GFCI — it is left of it and below it, on the other pipe.
- **Straps:** the grounding pipe is strapped to the wall **above and below** the bridge (one strap between the combo and the bridge, one below the bridge) in both photos.
- **Proportions:** bridge body length ≈ 4–5× the pipe diameter; height ≈ the pipe diameter. Pipe passes through at roughly 15–20% of the body length from its left end.

## (b) What the current drawing gets wrong

Current bridge elements (diagram lines ~124–129): a white/green rect at `x196 y240 w62 h16`, three green dots on its face, a green vertical line from its underside down to the horizontal GEC run, and detached labels at x120.

1. **Wrong place — too high and floating beside the GFI.** The drawn bridge sits at y240–256, level with the GFI box (y238–280) and only ~20px below the combo. In the photos it is well down the grounding run, clearly below the GFCI.
2. **Wrong mounting — beside the run, not on it.** The drawn bar extends **left** from x258 and its right end merely touches the vertical GEC pipe; a separate green line then drops from its middle (x227, y256→286) to the horizontal GEC run, inventing a bonding jumper that does not exist. The real bridge is **in-line on the vertical pipe itself** — pipe in the top, pipe out the bottom — with no extra jumper.
3. **Wrong direction.** The real body extends **to the right** of the pipe it clamps (toward the GFI side). The drawing extends it to the left, into empty wall.
4. **Wrong face.** Three green dots make it read as a busbar/terminal strip. The real face is plain smooth white with a single center screw.
5. **Label placement follows the wrong position** — "GROUNDING BRIDGE / intersystem bonding" text floats at x120 y236/266, detached from the device it names.
6. (Text, optional but related) Step 4 still says the bridge mounts "at the base of the combo" — per the photos it mounts **on the grounding pipe run below the combo**. Worth a wording tweak when this fix is applied.

## (c) Exact replacement SVG

### DELETE these existing elements (the whole `<!-- grounding bridge -->` block)

```svg
        <!-- grounding bridge -->
        <rect x="196" y="240" width="62" height="16" rx="3" fill="#ffffff" stroke="#177245" stroke-width="2"/>
        <g fill="#177245"><circle cx="206" cy="248" r="3"/><circle cx="222" cy="248" r="3"/><circle cx="238" cy="248" r="3"/></g>
        <text x="120" y="236" fill="#177245" font-size="10">GROUNDING BRIDGE</text>
        <text x="120" y="266" fill="#5a6b7d" font-size="9">intersystem bonding</text>
        <line x1="227" y1="256" x2="227" y2="286" stroke="#177245" stroke-width="3"/>
```

### INSERT this block **immediately after** the two GEC `<path>` elements

(i.e. right after `<path d="M258 220 V286 H180" fill="none" stroke="#1d9e4b" stroke-width="2.5" stroke-dasharray="5 4"/>`, so the bridge body paints over the pipe — pipe visibly enters its top and exits its bottom at its left end, exactly as in the photos. The bridge is drawn at y261–278 on the vertical run: below the GFI box's midline, on the pipe, body extending right and stopping flush at the GFI box's left edge x292.)

```svg
        <!-- grounding bridge — white in-line device clamped ON the vertical GEC pipe run, below the GFI, body extending right from the pipe (per the real Sharma photos) -->
        <rect x="253" y="238" width="10" height="5" fill="#5a6b7d"/>
        <rect x="250" y="261" width="42" height="17" rx="4" fill="#ffffff" stroke="#177245" stroke-width="2"/>
        <circle cx="278" cy="269.5" r="2.4" fill="#177245"/>
        <text x="60" y="262" fill="#177245" font-size="10">GROUNDING BRIDGE</text>
        <text x="60" y="276" fill="#5a6b7d" font-size="9">in-line on the GEC pipe, below the GFI</text>
        <line x1="196" y1="266" x2="248" y2="269" stroke="#177245" stroke-width="1"/>
```

Notes on the replacement:

- The small grey rect at `x253 y238` is the pipe strap above the bridge (both photos show a strap above and below it; one reads clearly at diagram scale — add a second at `x253 y288` only if it doesn't crowd the horizontal turn at y286 — it does, so leave it out).
- Bridge body: `x250–292, y261–278`. The GEC pipe (center x258, stroke width 7 → x254.5–261.5) passes behind its left end, 8px from the body's left edge — matching the photo, where the pipe goes through near the left end and the body stretches right.
- Single green circle = the one face screw. No terminal dots.
- No jumper line — deleted, not replaced. The green dashed GEC inside the pipe already runs continuously through the bridge point, which is the truth of the install.
- The leader line runs from the label (ends x≈196 at y266) to the bridge's left edge (x248, y269).
- Colors/style match the existing diagram: white fill `#ffffff`, grounding green `#177245`, grey label `#5a6b7d`, strap grey `#5a6b7d`, font sizes 10/9 like the other callouts.
- Sanity checks after pasting: bridge must not overlap the GFI box (x292–344, y238–280) — it ends exactly at x292, flush, no overlap; must not cover the "GROUNDING WIRE IN PVC PIPE" labels (x52–…, y180–208) — labels are at y262/276, clear; footing top is y300 — clear.
