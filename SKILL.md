---
name: quan
description: Build production-ready character identity bibles, hero portraits, four-view reference sheets, and continuity checks for AI film, comic-drama, storyboard, and image-to-video workflows. Use when the user wants to design or lock a recurring character, generate 人物四宫格/角色设定图, reduce face or costume drift, or turn a character concept or reference image into reusable prompts. Do not use for a one-off portrait when cross-shot identity consistency is irrelevant.
---

# Quan Character Continuity

Turn a character concept or selected reference image into a compact continuity package that downstream image and video models can reuse.

## Route the request

- For a new character or an incomplete idea, read [references/character-workflow.md](references/character-workflow.md) and build the identity bible before writing generation prompts.
- For a four-view sheet, hero portrait, or model-ready prompt, also read [references/prompt-templates.md](references/prompt-templates.md).
- For reviewing existing images, comparing generations, or diagnosing drift, read [references/continuity-qa.md](references/continuity-qa.md).

Use only the references relevant to the request.

## Required invariants

1. Separate identity facts from shot-specific direction. Face, age, body proportions, hair, permanent marks, signature wardrobe, and fixed props belong in the identity bible; pose, action, camera, weather, and mood belong in the shot prompt.
2. Treat an approved hero portrait or four-view sheet as the visual source of truth. Do not silently redesign it in later prompts.
3. Make changeable elements explicit. Mark alternate costumes, injuries, aging, wet hair, or temporary props as scene states rather than permanent identity traits.
4. Prefer observable descriptions over abstract labels. Describe silhouette, proportions, fabric, construction, placement, and color rather than relying on words such as “handsome” or “cinematic.”
5. Preserve the user’s chosen model and platform. Give model-agnostic prompts by default; add platform-specific syntax only when the platform is known.
6. Do not claim that a generated sheet guarantees perfect consistency. Explain that reference strength, seed support, image conditioning, and model behavior still affect the result.

## Default deliverable

Unless the user asks for only one component, provide:

- a concise identity bible;
- a negative-lock list describing what must not drift;
- a hero-portrait prompt;
- a 9:16 four-view character-sheet prompt;
- recommended reference and rendering settings without inventing unsupported numeric parameters;
- a continuity checklist for later shots.

Write prompts in the user’s language. When an English generation prompt is likely to perform better for the selected model, provide both a concise Chinese brief and an English production prompt.

## Reference-image handling

If the user supplies images, inspect them before extracting identity facts. Distinguish directly visible facts from inference, and flag ambiguous details instead of locking guesses into the bible. If multiple images conflict, ask which one is authoritative only when that choice would materially change the character; otherwise use the clearest common traits and note the conflict.

## Completion standard

The package is complete when another agent can generate new shots without reinterpreting the character’s identity, and a reviewer can identify drift using explicit checks rather than subjective resemblance alone.
