# Production Brief: "The Midnight Platform"

Source concept: cinematic nighttime dead-drop scene, abandoned train station platform, Mr. Volkov & Sonia. Total runtime: 30 seconds.

---

## 1. Character List

| Name | Age | Physical Description | Wardrobe | Role |
|---|---|---|---|---|
| **Mr. Volkov** | Late 40s | Weary, weathered face, deep-set eyes, close-cropped greying hair, tall and lean with a slight stoop from years of watching his back | Dark wool overcoat with upturned collar, dark suit underneath, no tie, leather gloves, a plain fedora or bare-headed — pick one and lock it for consistency | The handler. Receives intelligence, reacts to the warning, exits with the evidence |
| **Sonia** | Mid-20s | Pale, striking, composed features that betray tension only in small tells (tight jaw, downcast eyes), dark hair pulled back or under a headscarf | Long dark trench coat, low heels or flat boots for quiet footsteps, a scarf or collar high enough to obscure the lower face | The courier. Delivers the warning and the photograph, then vanishes |

**Consistency note:** Lock a single reference description (face, coat color/texture, hair) for each character before generating any stills — every subsequent still and video clip should reference the *same* character sheet, not be re-described from scratch each time.

---

## 2. Location List

Only one distinct location appears in this concept:

1. **Abandoned train station platform** — outdoor/covered platform, empty tracks, a single flickering overhead lamp as the dominant light source, heavy ground fog, a luggage cart, and one unclaimed suitcase near the platform edge.

If you want coverage variety without adding a new "place," treat these as **sub-setups of the same location** rather than new locations: wide platform shot, lamp-lit mid shot, close luggage cart insert, platform exit into fog. Keeping it one location keeps continuity (fog density, lamp flicker rate, wet-ground reflections) consistent across every clip.

---

## 3. Scene Breakdown (30 seconds, 6 clips)

| # | Timing | What Happens | Characters | Location |
|---|---|---|---|---|
| 1 | 0:00–0:05 | Establishing shot: fog drifting over empty tracks, lamp flickering overhead. Mr. Volkov stands alone at the platform's edge, cigarette lit, collar up. | Mr. Volkov | Platform (wide) |
| 2 | 0:05–0:10 | Footsteps echo. Sonia enters and stops a few feet from him. Both face the tracks, not each other. | Mr. Volkov, Sonia | Platform (wide/mid) |
| 3 | 0:10–0:15 | Volkov exhales smoke, asks (without turning) whether the shipment left on schedule. Sonia hesitates. | Mr. Volkov, Sonia | Platform (mid, two-shot) |
| 4 | 0:15–0:20 | Sonia quietly explains the shipment was rerouted through the border checkpoint at dawn and he must warn the others. She slides a folded photograph onto the luggage cart, then turns and walks briskly off, vanishing into the fog. | Sonia (primary), Mr. Volkov | Platform (mid → wide as she exits) |
| 5 | 0:20–0:25 | Volkov palms the photograph, studies it under the flickering lamp, then slips it into his coat's breast pocket. | Mr. Volkov | Platform (close/insert) |
| 6 | 0:25–0:30 | Volkov drops his cigarette, crushes it underfoot, and walks off in the opposite direction down the platform, leaving the unclaimed suitcase behind. | Mr. Volkov | Platform (wide, final exit) |

---

## 4. Dialogue

Only two lines in the entire scene — sparse, whispered, no overlap.

1. **Mr. Volkov** (Clip 3, ~0:11): *"Did the shipment leave on schedule?"*
2. **Sonia** (Clip 4, ~0:16): *"It never left. They rerouted it through the border checkpoint — dawn. Warn the others before then."*

No other spoken lines. All other beats (the photograph slide, the walk-offs) are silent, non-verbal action.

---

## 5. Generation Order

Follow this sequence so every downstream asset inherits a locked, consistent reference rather than drifting frame to frame:

1. **Characters** — Generate a character reference sheet for Mr. Volkov and Sonia first (front/three-quarter turnaround, neutral lighting, in wardrobe). Lock these before anything else.
2. **Locations** — Generate the platform location plate(s) next: empty, no characters, so lighting/fog/props are locked independently (wide establishing plate, mid-shot plate, close luggage-cart plate).
3. **Still scenes** — Composite characters into the location per clip (1–6 above), one still per key beat/camera setup. These stills are your video-generation seed frames.
4. **Color grade** — Apply the B&W grade (Section 7) to *every* still uniformly, before video generation — never grade clips individually after the fact, or the fog/contrast will drift between shots.
5. **Video** — Generate video motion from each graded still, in clip order, using the same seed/reference character and location assets throughout to prevent identity drift across the 6 clips.

---

## 6. Aesthetic Direction

The film should feel like a half-remembered frame from a 1980s Cold War spy thriller — cold, damp, and paranoid, where every shadow could be surveillance: a single unstable overhead lamp casts hard, flickering pools of light against near-total darkness, low fog swallows the lower third of every frame and softens silhouettes into ghosts, and the empty platform's converging rail lines and geometric pillars create a sense of exposure and isolation even in the enclosed space; camera movement should be minimal and observational (slow push-ins, static wides) rather than kinetic, performances restrained and wary with almost no eye contact between characters, and the overall mood one of quiet dread and tradecraft discipline rather than action — tension carried entirely through silence, distance, and the small, deliberate gestures of the handoff.

---

## 7. Color Grading

Apply uniformly to all stills *before* video generation:

- **Full black & white conversion** — no color information at any stage; grade for tonal range, not hue.
- **High contrast, crushed blacks** — deep, near-pure black in shadow areas (tunnel mouths, fog edges, wardrobe) with limited midtone detail recovery.
- **Controlled highlight bloom** — let the overhead lamp blow out slightly with a soft halo/flicker glow, the only bright point in each frame.
- **Heavy film grain** — coarse, organic 35mm-era grain, not digital noise; grain should be consistent in size/density across every clip.
- **Fog/haze diffusion** — a soft, slightly hazy overall diffusion pass to sell the ground fog and cold, damp air.
- **Vignette** — moderate darkening at frame edges to concentrate focus on the lamp-lit center and reinforce the enclosed, watched feeling.
- **Slight gate weave / minor film artifacts** (optional) — subtle frame instability or a faint scratch/dust pass to sell the analog, period-accurate stock look.

Lock this grade as a single reusable preset/LUT and apply it identically to all 6 stills so lighting and contrast stay consistent once motion is generated.
