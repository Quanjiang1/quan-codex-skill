# Continuity QA

Use this reference when reviewing candidate images, four-view sheets, storyboards, or video keyframes.

## Compare in this order

1. **Identity geometry:** head shape, jaw, cheekbones, eye spacing and shape, brow shape, nose bridge and tip, mouth width, ears, permanent marks.
2. **Hair:** hairline, parting, fringe, length, volume, texture, tied sections, color, and rear silhouette.
3. **Body:** apparent height, shoulder width, torso-to-leg ratio, build, hands, and posture.
4. **Wardrobe construction:** silhouette, layers, collar, closures, seams, hem, sleeves, fabric behavior, damage, footwear, and accessories.
5. **State:** dirt, blood, wetness, injury, aging, temporary props, and whether the story justifies them.
6. **Presentation:** exposure, color temperature, camera distortion, and whether lighting merely changes appearance or the underlying design actually drifted.

## Severity labels

- **Critical:** unmistakably different identity, missing permanent feature, redesigned signature outfit, incompatible anatomy.
- **Major:** changed hair construction, body proportions, garment structure, fixed prop, or unexplained scene state.
- **Minor:** small color, texture, seam, makeup, or accessory-placement discrepancy that does not change identity.

## Review output

```markdown
## Continuity verdict
- Result: pass / revise / reject
- Highest severity:

## Drift found
| Area | Expected | Observed | Severity | Correction |
|---|---|---|---|---|

## Corrective prompt
[Only the minimum changes needed; preserve everything already correct.]
```

## Correction strategy

- Correct critical identity failures by returning to the approved source image, not by layering more adjectives onto a bad derivative.
- Correct garment or prop drift with observable construction details and explicit placement.
- When one panel is wrong, regenerate that panel or the sheet with stronger identity/reference conditioning; do not accept a visually attractive but inconsistent composite.
- If all candidates fail in different ways, simplify pose, background, and light before increasing prompt complexity.
- Distinguish generation error from intentional story change. Do not “fix” an approved temporary state back to the default design.
