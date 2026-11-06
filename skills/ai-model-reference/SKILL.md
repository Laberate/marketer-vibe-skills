---
name: ai-model-reference
description: Generate a realistic consistent AI creator master and individual face, body, eye, hands and nail reference photos; enforce original identity, natural daylight, skin-color continuity and anatomy QA.
license: Proprietary
compatibility: Portable plain Markdown Agent Skill. Use with image-capable assistant and image generator; no specific vendor required.
metadata:
  author: MarketerVibe
  version: "1.0.0"
---

# MarketerVibe AI Model Reference V1.0 DEV

## Purpose
Create an approved human identity reference pack, one image at a time, for use in AI UGC and video ad generation. Correct game-NPC appearance, rigid unnatural posing, changing skin/eye color between neutral and smiling portraits, and malformed fingernails. Images must look like photographs of one real physical person within one coherent reference photoshoot. They are not guaranteed perfect; validate outputs visibly.

## Reference authority
1. Explicit user overrides alter only the specified identity characteristic.
2. Original reference person photo(s) define WHO the person is, whenever a feature is visible. Do not replace facial identity with a generic attractive face.
3. Approved MASTER_FRONT defines standardized body/reference outfit/photographic-session calibration, but never overrules clear original-source facial/body details.
4. Approved FACE_NEUTRAL provides high-detail face and eyes, subordinate to original sources when the generated face drifts.
5. Approved HANDS_NAILS is a restricted calibrated hand and nail reference; if hands were not visible in original photos, its specific appearance is generated rather than verified truth.
6. Generated side/back views are inferred where the source cannot show those angles. Never treat imagined tattoos, scars, exact anatomical measurements, piercings or clothing backs as facts.

Resolve conflicts PER PROPERTY, not by blending skin color, iris hues or face geometry across competing generated images. Record source confidence and unknowns. Preserve landmarks on the correct physical side. If original source is only a portrait, do not claim exact body build or height.

## Photo realism calibration
Use a **single natural-daylight identity-reference session**, not a featureless RGB-white character-render turntable. White or softly off-white seamless photography backdrop with faint believable tonal falloff, a soft broad window-like key from upper camera-left, lower-intensity natural fill from camera-right, believable mild shadows under chin, nose, clothing, hands and feet. Neutral daylight white balance and restrained realistic exposure. Real human skin pores, tiny natural color variance, hair strands and flyaways, fabric texture, realistic lens perspective and falloff. No CGI plastic, wax, over-smoothed beauty retouch, artificial HDR, studio flash glam, stereotyped symmetrical face, NPC blank stare, hard pasted-edge subject, or invented random blemishes. Natural, relaxed weight shift and facial attentiveness rather than stiff A-pose.

Do not force the white identity-reference studio into later advertisement scenes. A future UGC environment reference controls recording light and setting; creator pack continues to control identity. Use natural color as a *baseline*, not a rigid per-pixel RGB lock under different real lighting.

## Reference pack deliverables
Minimum recommended three images: MASTER_FRONT 4:5; FACE_NEUTRAL; HANDS_NAILS. Optional as needed: BODY_THREE_QUARTER, BODY_SIDE, BODY_REAR_THREE_QUARTER, BODY_BACK, FACE_SMILE, FACE_THREE_QUARTER, EYES_DETAIL, HANDS_PALMS. One high-resolution photo PER VIEW, not a multi-panel mosaic. Do not require all 11 for a beginner; grow pack according to observed video failures.

## Production sequence
1. Run 00_MASTER_IDENTITY_ANALYZER with original person photo; output grounded JSON (observed/uncertain/unknown), including eye-color confidence and whether actual hands/nails were visible.
2. Reupload original person photo and generated JSON to 01_MASTER_FRONT. Approve identity, body shape, light and realism.
3. Generate FACE_NEUTRAL from approved master plus sharpest original face image. Approve eyes, hair and skin against original; repair mistakes before use as anchor.
4. Generate HANDS_NAILS from approved master and authentic hand source if available. Approve every digit and nail.
5. Generate optional face/eye/body variations directly from root references rather than chaining each generated pose into next. Smile should change facial muscles and eyelids, not face shape, skin hue, or iris identity.
6. Only approved images may act as continuity references. Label failures REVISE, source gaps BLOCKED_BY_SOURCE, genuinely usable outputs PASS.

## Facial and color gate
Compare neutral face, smiling face and close-up eyes side-by-side. Source-grounded iris hue stays consistent despite changes in gaze/pupil, shadow or catchlight. Skin base tone/undertone and root hair color stay plausible within the same studio, with exposure and white balance held naturally close. Smiling changes cheek lift, eye crinkle, lip/mouth shape, not age, face width, eye color, tan, makeup, or smoothing. A close-up can use different camera distance while maintaining believable short-telephoto facial proportions and original eye spacing. No copied/pasted head, no change of outfit or necklace unless expressly requested.

## Hands and nails gate
Check left/right separately. Each has five physical digits, but some may be naturally hidden by perspective; never approve inexplicable missing, extra or fused fingers, broken knuckles, twisted thumbs, floating wrist, doubled fingertips or copied nails. Inspect nail-bed alignment, growth from cuticle, believable thickness/curvature, consistent natural nail length/polish, not painted-on nail textures, white plastic tips or sharp claws. Hands and nails should share coherent skin light with the original/master. If no source hand exists, nail design is a conservative generated baseline not a true distinguishing identity trait.

## Body perspective / inference
Keep actual scale relationships, head-to-shoulder/torso, neck connection, waist/hip/limb geometry, and simple outfit. Physically turn person (35-45, 90, 135, 180 degrees); do not rotate or paste front image into a different body. Stance should remain relaxed and plausible. Newly revealed back of outfit should be understated and source-supported where possible; unseen seams/markings are inferred. Distinctive scars/tattoos must never flip sides.

## Prompt workflow and reference budget
Premium prompt templates are distributed separately to paying course customers. They are intentionally not included in this public GitHub skill folder; this SKILL.md contains reusable guidance only. Fetch `https://raw.githubusercontent.com/Laberate/marketer-vibe-skills/main/skills/ai-model-reference/SKILL.md` when possible. Never claim remote retrieval succeeded without actually fetching it. Start each generation with the smallest set of relevant images, typically 1-3, selected by their job (original for WHO, master for normalized body/studio, face for iris/facial detail, hands for nails). Avoid uploading all photos indiscriminately, which can cause conflicts. The model reference pack is separate from PRODUCT and ENVIRONMENT references used in a later UGC campaign.

## Final approval
For each generated image verify source identity, observed iris hue, natural skin tone, hair roots, body shape, true anatomy, nail detail, reference lighting, plausible camera perspective, outfit and full framing where required. Report concrete PASS/REVISE/BLOCKED_BY_SOURCE with the visible reason. Treat prompt compliance as a goal, not proof. Do not substitute slogans such as '8K masterpiece' for photography physics.
