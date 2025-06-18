from pathlib import Path

# Define output path
output_dir = Path("/mnt/data/Cutscene_Addon_RustBucket")
output_dir.mkdir(parents=True, exist_ok=True)

# Markdown content for the lab cutscene
cutscene_markdown = """# 🎬 CUTSCENE_PLAN_Cleatus_Lab.md

## Title: Optics Upgrade – “Through New Eyes”

### Setting
- Interior: Cleatus’ Lab
- Lighting: Dim, amber-tinted worklights with flickering shadows
- Audio: Welding arcs, steam hisses, faint analog jazz or tinkerer’s hum

---

### Sequence

1. **RB lies inert** on the repair table, still showing visible rust, missing pieces.
2. **Cleatus enters**, shaking dust off a box labeled "OPTICAL MODULE v0.9-B."
   - Dialogue:  
     > "Ah, this oughta do the trick. Little scratchy on the edges, but it’s got *character*..."
3. **Insert animation**: sparks fly, RB twitches.
4. **Vision POV shifts to RB** — CRT border flickers.
   - Audio cue: high-pitched charge-up whine
   - Visual: scanlines stretch and bend
5. **Frame glitches, then melts away.**
   - UI transitions to hi-res overlay
   - New HUD elements fade in: compass, faint outline highlighting salvage zones
6. **RB sits upright**, blinking synthetic eye now glowing.
   - Cleatus:
     > "There ya go. Welcome to the *real* world, Rustbucket."

---

### Technical Implementation Notes

- Use `CanvasGroup` alpha transition to crossfade CRT UI with Hi-Res HUD.
- Trigger Post-Processing volume at 50% blend (Bloom, Vignette, Sharpness)
- Swap background sprite layers to more detailed pass (or parallax override).

---

### Player Outcome

- Gains temporary control with updated perception
- Use this phase to highlight interactables: glowing salvage heap, exposed console
- Scene ends with Cleatus gesturing to the scrapyard gate:
  > "Now, let's see what else we can bolt onto that bucket of yours."
"""
