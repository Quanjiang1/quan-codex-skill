# Prompt templates

Replace bracketed fields with facts from the approved identity bible. Do not leave placeholder text in a final deliverable.

## Hero portrait

```text
Create a neutral production reference portrait of [CHARACTER].

IDENTITY: [compact face, hair, age, build, permanent marks, signature neckline and accessories].

COMPOSITION: head-and-shoulders or three-quarter portrait, face unobstructed, looking toward camera, neutral expression, natural posture, restrained perspective distortion.

STUDIO: seamless [BACKGROUND] backdrop, one neutral key light about 45 degrees camera-left, soft controlled shadow, no colored spill, no dramatic rim light, no props.

QUALITY: photographic character reference for film production, faithful skin texture, accurate fabric construction, even exposure, restrained grade, high detail.

DO NOT CHANGE: [short negative-lock list]. No beauty-filter skin, facial reshaping, enlarged eyes, costume redesign, new accessories, watermark, or decorative text.
```

## Four-view reference sheet

```text
Create a clean four-panel photographic character reference sheet for film production, using the attached approved character image as the only identity source.

IDENTITY LOCK: The same [CHARACTER] appears in every panel. Preserve identical facial structure, apparent age, skin tone and texture, hairstyle, hairline, body proportions, outfit construction, fabric, footwear, permanent marks, and fixed accessories. Do not beautify, reinterpret, or redesign the character.

LAYOUT: One vertical 9:16 canvas divided into four orderly panels with narrow, even gutters. Keep scale and exposure consistent.

PANEL 1 — FRONT PORTRAIT: head-and-shoulders close-up, facing camera directly, neutral expression, eyes forward, all identity-defining facial details visible.

PANEL 2 — SIDE PROFILE: head-and-shoulders strict 90-degree profile, neutral expression, same hairstyle, makeup state, clothing neckline, proportions, and identity as Panel 1.

PANEL 3 — FULL-BODY FRONT: neutral full-length front view, arms naturally relaxed, feet completely visible, no dramatic gesture; show the full outfit and true body proportions.

PANEL 4 — FULL-BODY BACK: full-length rear view matching Panel 3 in stance, scale, outfit, and framing; clearly show rear hairstyle, garment construction, accessories, and footwear.

STUDIO: The same seamless [BACKGROUND COLOR] studio backdrop in all panels. One firm neutral key light about 45 degrees camera-left. No fill-light look, colored ambient spill, dramatic rim light, props, scenery, or set dressing. Natural contact shadows only.

QUALITY: production-use photographic character sheet, even exposure, accurate fabric weave and seams, natural matte skin with real texture, clean restrained color, high detail.

NEGATIVE LOCK: no identity drift, facial reshaping, beauty-filter skin, glossy plastic complexion, idol makeup, face slimming, enlarged eyes, skin smoothing, pose drift, clothing redesign, extra accessories, height or body-ratio changes, lighting changes, color-temperature jumps, duplicate people, cropped feet, watermark, or decorative text. Tiny functional panel labels are optional.
```

## Shot prompt adapter

```text
IDENTITY LOCK: [five to eight most discriminating stable traits]. Match the approved character reference exactly.

SHOT: [location, action, emotion, framing, lens behavior, camera movement, lighting, time, weather].

STATE CHANGE: [only the temporary changes required by this scene]. Everything else remains unchanged.

CONTINUITY: preserve [face geometry, hair, body ratios, signature garments/props]. Do not introduce [known failure modes].
```

## Recommended KSR-style sequence

1. Generate several hero-portrait candidates from the same identity bible.
2. Select one authoritative image; do not average conflicting candidates.
3. Submit the selected image plus the four-view prompt.
4. Use a 9:16 high-resolution canvas; the original workflow showed 4K and high detail, but adapt to the platform’s actual controls.
5. Reject sheets where panels show different faces, hair, garments, body ratios, or lighting.
6. Use the accepted sheet in later image and image-to-video generations.
