# MarketerVibe Skills

Portable plain-Markdown specialist skills for the MarketerVibe UGC workflow.

## Skills

- `skills/ugc-ad-strategy/SKILL.md` — **V1.4.0**: product/audience diagnosis, optional research, awareness, angles, hooks, natural UGC copy, claim grounding, and the compact creative-strategy handoff.
- `skills/ugc-visual-production/SKILL.md` — **V1.3.0**: fast-cut UGC visual production: purposeful short visual beats, simple believable actions, product-use progressions, controlled shot variety, B-roll, payoffs, edit-ready keyframes, and VO-friendly pacing.
- `skills/image-fidelity/SKILL.md` — **V1.1.0**: photorealism, product invariants, physical scale, material-light integration, human/contact realism, camera realism, environment integration, and a lean QA gate.

## Visual Production V1.3 highlights

- Conditional Kling 4.0 Omni reference routing: when identity-critical product geometry enters from off-frame, route to a reference-capable mode with a distinct full-product reference; a packshot never becomes scene/camera authority.
- First-frame-only Keyframes for simple actions: fully visible subjects with simple facial or hand movements use only the starting frame; no extra timeline keyframes.
- Brisk, natural sales motion: engaged, purposeful pacing—decisive entrances with credible acceleration and deceleration, never idle padding or hyperactive acting.
- Hand and packaging fidelity checks: evaluate hand appearance and newly revealed packaging independently; duplicated printed elements, label changes, and hand morphs are hard failures.
- Liquid-dispensing alternatives: precise dropper-to-skin transfer is not a default requirement after repeated observed failures—default to cut-over-liquid complexity (applicator detail, hard cut, pat-in) or approved experiments.
- Independent silent clips and external VO: one approved starting image produces one separately generated silent clip; failed clips are retaken locally and continuous VO is added in the edit.

## Image Fidelity V1.1 highlights

- Multi-beat environment continuity and product-state continuity across beats.
- Creator calibration for product-only opening beats without forcing creator appearance, plus consistent generic supporting props.
- Partial-frame product-entrance testing and action-ready keyframes for one simple movement.

## Strategy and production safeguards

- Options A/B/C must differ in their actual visual story—including hook, shot progression, emphasis, and payoff—not just buyer copy or voiceover. They should remain distinct when compared with the sound off.
- When a generic supporting prop is missing, use a consistent unbranded fallback with stable appearance and state across beats rather than blocking the strategy or introducing static filler.

## When each skill is used in the UGC workflow

1. **Strategy** — `ugc-ad-strategy` (strategy mode) runs before image planning to choose the buyer, positioning, angle, product interaction profile, and strategic visual beats.
2. **Image planning and video generation** — `ugc-visual-production` turns the strategy into concrete visuals: shot-by-shot beats, believable actions, cut-over-complexity pacing, B-roll, and edit-ready keyframes for image and video stages.
3. **Image realism** — `image-fidelity` supports the image-planning prompt with photorealism, product identity, and contact/anatomy realism checks.
4. **Script finalization** — `ugc-ad-strategy` (execution mode) runs again after visuals are approved to finalize one coherent voiceover script.

## Recommended remote-loading model

The end user should not need a GitHub account or GitHub connector. Production prompts can point to a public raw URL and include a tiny embedded fallback core.

For development, a mutable `main` URL is convenient. For a locked course release, use a tag or commit so the same prompt always loads the same skill version.

Example locked URL after publishing/tagging:

```text
https://raw.githubusercontent.com/<owner>/<repo>/v1.0.0/skills/ugc-ad-strategy/SKILL.md
```

Prompt behavior:

1. If external URL access is available, retrieve and apply the canonical skill.
2. If retrieval is unavailable, use the prompt's embedded fallback core and continue.
3. Never claim the remote skill was loaded unless it was actually retrieved.

## Portability

The skill folders follow the Agent Skills convention: each folder name matches the `name` field in its `SKILL.md`. The files are plain Markdown and do not require a specific AI vendor.
