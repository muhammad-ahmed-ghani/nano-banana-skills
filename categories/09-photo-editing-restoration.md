# Category 9: Photo Editing & Restoration

Templates for smart outpainting, object/crowd removal, restoration, image repair, and surveillance-style simulations. These are image-to-image tasks — a reference photo is always required.

---

## 9.1 Smart Outpainting / Composition Rescue

**When to use:** User has a photo with the wrong aspect ratio or wants to extend the scene beyond its original borders.

```
Zoom out and expand this image to a [16:9 / 4:3 / 21:9 / 9:16] aspect ratio. Context Awareness: Seamlessly extend the scenery on [both left and right sides / the top and bottom / all sides]. Match the original lighting, weather, color temperature, and texture perfectly. Logical Completion: If there are cut-off objects at the borders — [a shoulder, a tree branch, a building edge, a person's body] — complete them naturally based on logical inference from the scene. Do not distort the original center image. The seam between original and extended areas must be invisible.
```

**Specific ratio variant:**
```
Expand this [portrait / landscape] photo into a [computer wallpaper / social media banner / cinema widescreen] format. Intelligently generate the missing [left-right / top-bottom] portions by extrapolating from the existing scene — [architecture, vegetation, sky, interior details, crowd]. The extension must feel like part of the original photo, not a generated addition. Maintain consistent [depth of field / lens distortion / color grading / film grain].
```

---

## 9.2 Smart Crowd & Object Removal

**When to use:** User wants to remove unwanted people, objects, or distractions from a photo.

```
Remove all the [tourists / people / cars / cables / logos / branded items / unwanted objects] in the [background / foreground / mid-ground] behind the main subject. Intelligent Fill: Replace them with realistic background elements that logically fit the scene — [extend the cobblestone pavement, add empty park benches, continue the wall texture, regenerate grass or foliage]. Consistency: Ensure no blurry artifacts, smudges, or obvious patching. The filled area must have the same grain, focus depth, lighting direction, and color temperature as the rest of the photo.
```

**Targeted removal:**
```
Remove only [the object/person description] from this image. Do not change anything else. Fill the removed area seamlessly with what would logically be behind it — [background wall, sky, floor, vegetation]. Match the texture, grain, and lighting of the surrounding area exactly. The final result should look like the object was never there.
```

---

## 9.3 CCTV / Surveillance Aesthetic Simulation

**When to use:** User wants a photo rendered in a security camera / surveillance style, optionally with face detection boxes.

```
Create a high-angle CCTV surveillance shot using the uploaded image as the source. Detect every visible person in the image and automatically draw a [white / green / red] rectangular bounding box around each face. For the most prominent person, add a large zoom-in inset: a sharp, enhanced close-up of their face displayed in a floating rectangular frame connected with a thin white line.

Keep the main image slightly noisy and security-camera-like: soft grain, slight lens distortion, muted desaturated colors, CRT scanline texture. The zoom-in face box should be [clearer, brighter, and more detailed — as if digitally enhanced]. No text, no timestamps, no overlays — except the bounding boxes and connecting line. Maintain the original scene layout, angle, and environment of the uploaded image.
```

---

## 9.4 Background Replacement / Environment Swap

**When to use:** User wants to keep the subject but completely change the setting or background.

```
Keep the [person / product / subject] from the uploaded image exactly as-is — same lighting on the subject, same pose, same everything. Replace only the background with: [NEW BACKGROUND DESCRIPTION — e.g., "a misty Japanese bamboo forest at sunrise", "a clean white studio backdrop with subtle vignette", "a crowded Times Square at night with neon reflections", "a luxury penthouse interior"].

Relight the subject subtly to match the new environment's lighting direction and color temperature. Add [ground shadow / contact shadow / ambient reflection on floor] to ground the subject in the new scene. Ensure the subject's edges are cleanly integrated — no halo, no edge artifacts.
```

---

## 9.5 Photo Restoration & Enhancement

**When to use:** User wants to restore, colorize, or enhance an old or damaged photo.

**Old photo restoration:**
```
Restore this old/damaged photograph. Tasks: [Remove scratches, tears, and dust spots] [Fix faded areas and restore contrast] [Sharpen blurry or degraded sections] [Correct color fading — restore warm skin tones and accurate background colors]. Preserve the original composition and all identifiable features of the subjects. Do not add modern elements or alter faces. The result should look like the original photo taken on a perfect day, not an AI-generated image. Output: 4K restoration quality.
```

**Black-and-white colorization:**
```
Colorize this black-and-white [photograph / film still / portrait] with historically accurate, realistic colors. Research what colors are appropriate for: [the era — e.g., 1940s / 1960s / 1980s], [the clothing styles visible], [the environment — indoor/outdoor, season, location]. Apply natural skin tones. Preserve all shadow detail and tonal contrast from the original. The colorization should feel like discovering the real colors of the original scene, not a tinted or filtered version.
```

---

## 9.6 Fisheye / Lens Distortion Simulation

**When to use:** User wants a specific camera lens effect applied to a photo.

```json
{
  "image_parameters": {
    "style": "[Canon IXUS / GoPro wide-angle / fisheye / tilt-shift miniature]",
    "type": "Point-and-shoot / action camera / artistic lens simulation",
    "quality": "Hyper-realistic",
    "tone": "Sharp, direct / dreamy soft / saturated vivid",
    "lighting_and_atmosphere": "[Realistic flash-style / natural daylight / golden hour]"
  },
  "lens_effects": {
    "distortion": "[strong barrel distortion / subtle pincushion / heavy vignette / tilt-shift focus plane]",
    "chromatic_aberration": "[subtle fringing on high-contrast edges / none]",
    "vignette": "[heavy dark corners / light natural / none]",
    "grain": "[authentic sensor noise / film grain / clean]"
  },
  "subject": {
    "constraints": {
      "facial_identity": "Match reference image exactly 100%",
      "face_edits": "None allowed"
    },
    "expression": "[natural / surprised / candid]"
  },
  "composition": {
    "angle": "[extreme low angle / eye-level / high angle bird's-eye]",
    "distance": "[very close-up filling frame / mid-distance / wide environmental]",
    "mood": "[fun and intimate / dramatic / documentary]"
  }
}
```
