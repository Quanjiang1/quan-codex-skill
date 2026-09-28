# Character workflow

Use this workflow when the character is new, underspecified, or needs a stable production bible.

## 1. Normalize the brief

Extract only information the user supplied or that is clearly visible in reference images:

- narrative role and apparent age range;
- ancestry or regional cues only when supplied or visibly necessary;
- facial geometry and stable distinguishing marks;
- hair shape, length, texture, color, and hairline;
- height impression, build, shoulder/waist/limb proportions, and posture;
- signature wardrobe silhouette, layers, fabrics, colors, closures, wear, footwear, and fixed accessories;
- permanent props, scars, tattoos, prosthetics, or non-human anatomy;
- the world’s material language, period, and production style.

Do not infer sensitive identity attributes that are neither supplied nor needed.

## 2. Resolve design ambiguity

When the breef is broad, offer two or three materially different art-direction options. Make the differences concrete: silhouette, palette, materials, period cues, and social status. Once the user selects a direction—or when one direction clearly follows from the brief—freeze it into the identity bible.

## 3. Write the identity bible

Use this compact structure:

```markdown
## Identity lock
- Role / apparent age:
- Face geometry:
- Eyes / brows / nose / mouth:
- Skin and permanent marks:
- Hair:
- Body proportions and posture:
- Signature outfit:
- Footwear and fixed accessories:
- Permanent props or non-human traits:

## Scene-variable states
- Alternate costume:
- Temporary condition:
- Temporary prop:

## Never change
- ...
```

Keep the `Never change` list short and diagnostic. It should capture the traits that make a mismatch obvious.

## 4. Establish a visual source of truth

Generate or select one neutral hero portrait before generating complicated action shots. Favor:

- neutral expression;
- unobstructed face;
- restrained lens distortion;
- readable hairline and ears when relevant;
- accurate clothing neckline and signature accessories;
- plain lighting that does not hide identity features.

After approval, use that image as the main identity reference. Produce a four-view sheet from it, rather than independently generating four unrelated views from text alone.

## 5. Propagate into scenes

For each later shot, combine:

1. a short identity-lock block copied from the bible;
2. the specific scene, action, emotion, camera, and light;
3. a small negative-lock block targeting known drift risks;
4. the approved hero portrait or four-view sheet as the image reference.

Avoid copying the entire long bible into every shot when the model has limited prompt capacity. Preserve the most discriminating traits first.

## Platform settings

Recommend settings by function rather than inventing universal numbers:

- enable character/image reference conditioning;
- use the same approved reference across shots;
- keep reference strength high enough to preserve identity but not so high that pose and composition freeze;
- reuse seed or character-ID features when the platform supports them;
- change one major variable at a time while establishing the character;
- render the reference sheet at high resolution with a vertical 9:16 canvas when following the KSR workflow.
