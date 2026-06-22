---
name: ai-photo-shoot-director
description: Turn AI portrait, photo-shoot, realistic photography, ChatGPT image-2, gpt-image-2, studio, CCD, film, phone snapshot, gufeng, hanfu, Chinese period-style portrait, modern gufeng photography, ancient-life snapshot, and image prompt requests into stable photography-directed prompts. Use when drafting, optimizing, diagnosing, or generating AI portrait prompts that need concrete scene layers, imaging method, makeup anchors, pose skeletons, lighting logic, skin texture controls, route decisions, and negative constraints instead of vague beauty words.
---

# AI Photo Shoot Director

Build AI portrait prompts as a photographed moment. Treat the model like a photography team, not a wish pool: specify the place, imaging method, styling, action, camera, light, and guardrails that make the photo believable.

## Required Method

For any non-trivial portrait or photo-shoot prompt, read [references/photo-shoot-method.md](references/photo-shoot-method.md) before composing the final prompt.

Use this fixed workflow:

1. Identify why the image stands up: scene, light, makeup, camera angle, pose, or prop relationship.
2. Convert the idea into a shoot brief:
   - aspect ratio and realistic photography intent
   - specific imaging method, such as film, Fuji-style outdoor color, Nikon realism, phone snapshot, direct-flash CCD, or high-key soft-mist studio
   - texture lock: lens flaws, foreground pressure, exposure behavior, color grade, grain, haze, bloom, and anti-AI-polish constraints
   - clearly adult fictional subject, face temperament, hairstyle, and one makeup anchor
   - route decision when relevant: modern styled shoot, period-life snapshot, studio portrait, or editorial reconstruction
   - clothing, colors, materials, and wearable realism
   - foreground, subject plane, background, and optional props
   - camera distance, lens feeling, angle, crop, and depth of field
   - one pose skeleton with natural head-shoulder logic
   - light direction, where it lands, and what visual effect it creates
   - negative constraints
3. If the target is article-example texture, prioritize imperfect photography over clean beauty: near-lens blur, flare, overexposed edges, film grain, soft haze, lifted shadows, and visible light physics.
4. Make all visible elements know each other. Tie props, makeup, clothing, light, and action to one coherent theme.
5. Leave controlled variation when helpful: allow distance, gaze, expression, foreground occlusion, and prop selection to vary inside the chosen scene.

## Output Modes

- **完整导演稿**: Default. Return a short director analysis, then a copy-ready prompt and negative prompt.
- **只要最终提示词**: Return only two fenced `text` blocks: final prompt and negative prompt.
- **直接生成图片**: Only invoke image generation when the user explicitly asks to generate an image, directly produce an image, or uses equivalent wording. Otherwise, produce text prompts only.

## Prompt Rules

- Start from why the photograph works, not from "beautiful woman".
- Prefer concrete spaces over broad labels. Write "old wooden desk, birdcage, hand-copied paper, scrolls, bamboo curtain, lattice window" instead of only "ancient room".
- Write imaging behavior, not only style words. Explain hard flash, soft mist, high-key exposure, film grain, lens distance, or phone-capture immediacy.
- Add a **质感锁 / texture lock** when the user wants sample-like texture. Name what makes the photo imperfect: near foreground occupying 20-40% of the frame, optical blur, flare, blooming highlights, visible dust or mist, film grain, halation, lifted blacks, or mild motion softness.
- Avoid over-cleaning. Do not stack "8K", "ultra sharp", "perfect skin", "commercial retouch", "HDR", or "crystal clear" when the desired look is film-like, nostalgic, misty, or candid.
- Use makeup as a minimal recognizable anchor, not a full makeup tutorial.
- For gufeng or hanfu portraits, decide whether the target is modern gufeng photography or ancient-life snapshot before writing face, light, makeup, clothing, and expression details.
- Use a pose skeleton, not a high-risk body puzzle. Avoid large twisted necks, back-facing bodies with full head turns, and overly complex limbs unless explicitly required.
- Treat props as an atmosphere library. Use phrases like "not all props need to appear; select according to composition" when the prompt contains many props.
- Keep subjects fictional and clearly adult by default. Avoid minor-coded framing, exposed genitals, exposed nipples, explicit sexual acts, or identity imitation without authorization.

## Response Shape

For default output:

1. **成立点**: One or two sentences naming the photograph's support: scene, light, camera, action, or relationship between elements.
2. **导演检查**: Compact bullets for scene layers, imaging method, texture lock, makeup anchor, pose skeleton, light logic, and risk controls.
3. **最终提示词**: One fenced `text` block.
4. **负面约束**: One fenced `text` block.

For direct image generation, prepare the prompt internally and pass the final prompt to the available image generation tool. Do not show long hidden reasoning.
