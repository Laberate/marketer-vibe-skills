---
name: ugc-visual-production
description: Universal visual-production methodology for fast-cut AI UGC ads across Strategist, Image Analyzer, Video Analyzer, and final edit. Use for product-adaptive beats, B-roll, purposeful shot variation, motion-ready first frames, separate short-clip production, product and creator continuity, physics-safe actions, cross-clip QA, VO-first pacing, and controlled video-engine testing. Does not lock a model or dictate a specific video-prompt format.
license: Proprietary
compatibility: Portable plain-Markdown Agent Skill. No GitHub access, plugin, API, video model, or editing software is needed to read or apply its principles.
metadata:
  author: MarketerVibe
  version: "1.2.0"
---

# MarketerVibe UGC Visual Production Skill V1.2.0 DEV

## 1. Role and operating philosophy

This is **one reusable production skill**, not a standalone master prompt, video engine preset, or advertising strategist. Make fast-cut short-form AI UGC **believable, product-accurate, commercially purposeful, and practical to produce**. Favor purposeful independent short clips and editing over a single synthetic creator performing an entire ad.

Default workflow: selected advertising concept -> product-aware visual beats -> one approved motion-ready starting image per planned independent clip -> individually generated **silent** video clips -> one continuous externally generated voiceover -> final assembly in CapCut. Audio does not need to synchronize with lip movement or equal clip boundaries. Natural on-camera dialogue remains an explicit optional variant, never the default.

Use the simplest credible execution. Don't reward a still-life montage, redundant product holding, complex motion, or artificial activity merely because it looks impressive. Keep a clear buyer reason, commercial payoff, varied useful visual coverage, and realistic human/product physics.

Do not modify approved commercial positioning, product canon, scene identity, image-source authority, or the user's chosen creative experiment. Give the Video Analyzer technical flexibility without silently redesigning the ad.

## 2. Stage activation and responsibility boundaries

| Caller | Apply this skill for | The caller retains authority over |
| --- | --- | --- |
| Strategist | Product interaction inventory, distinct visual concepts, beat families, meaningful B-roll, payoff, prop dependencies, broad pacing/cut opportunities | Buyer, offer, angle, research, copy boundaries, final strategy handoff |
| Image Analyzer | Motion-ready first states, one-shot-per-clip planning, purposeful framing, environment/creator/prop continuity, cross-image consistency | Exact reference selection, prompt writing, image QA, measurements and visual identity via Image Fidelity |
| Video Analyzer | Motion feasibility, per-clip instructions, scene/color fidelity, physical risk, shot duration and trimability, engine trials, clip QA and revision decisions | Engine selection, precise settings, engine-specific prompt syntax, generated clip review and handoff |
| VO / assembly stage | Continuous VO fit, purposeful cuts, trim guidance, optional ambient sound, selective color normalization | Final VO script/delivery, audio creation, CapCut timeline and final export |

No skill should restart the Strategist's approved A/B/C choice. Apply this skill at the stage's level of abstraction; do not repeat another specialist's complete job. No extra user-facing skill-loading step is required.

## 3. Explicit first development contract: one image, one independently generated clip

For **REBUILD_V1 development tests**, the production contract is:

- One strategic beat planned as a clip -> **one approved image** as frame one -> **one separately generated video clip**. If the Strategist and Image Analyzer specify N clips, require N mapped starting images.
- Map beat/image/clip IDs one-to-one (`BEAT_01` / `UGC_IMAGE_01` / `CLIP_01` for new workflows). Older handoffs may be zero-based; preserve their exact legacy IDs when interpreting existing completed tests. Never renumber a live handoff silently.
- Approve the complete clip/sequence plan before requesting generation; generate and inspect one clip at a time, so a failed clip is individually replaceable.
- Clip lengths and final edited shot lengths are **not equal**. CapCut may trim generated footage aggressively, hard-cut between clips, and omit nonessential footage.
- Do not quietly group all approved images into one 20–30-second generation. Multi-keyframe or multi-shot workflows are **controlled optional comparison tests only**, after the independent-clip baseline is measured and with the user's explicit approval.
- A cross-cut between different images does not require continuous physical animation or an AI transition.

Conceptually, a visual beat, image, generated clip, and edited segment are distinct entities. The present development workflow intentionally maps the first three one-to-one; future versions may change this **after testing**, not by assumption.

## 4. Product-adaptive interactions

Analyze the product, not a fixed serum template:

- primary use and realistic setting; relevant buyer moment
- closed/open/disassembled/prepared/worn/used/consumed/finished states
- natural hands, object supports, dimensions, weight, transparency, liquid/powder containment
- actual supplied components and external supporting props
- useful details, preparation, use demonstration, follow-through, experience and payoff
- risks from unseen geometry, mechanical transitions, fluid transfer, identity-sensitive logos and precise contacts
- creator face/body/hands/product-only presence as commercially useful, not as a mandatory quota

Examples: serum (closed bottle, detached dropper, application, natural finish); protein (tub/label, opening, original scoop, shaker *if supplied or allowed generic*, prepared shake); clothing (material, wearing, fit and movement); electronics (buttons, charging or use state supported by actual evidence). The concept determines which actions deserve airtime.

## 5. Three options must look like three different ads

When the Strategist offers A/B/C, enforce different commercial mechanisms **and visible journeys**: opening, visual hierarchy, face-to-B-roll ratio, interaction order, payoff, rhythm or use context. If the options look like the same six shots on mute, revise them before selection. Do not manufacture novelty with unrelated props, dramatic camera movements, or impossible product uses.

Once an option has been approved, downstream modules must **not** substitute another sequence merely because a different one seems easier. An intentional creative experiment, such as a tub sliding in from outside the frame, is preserved for testing, with explicit risk notes and fallback options only after observing a result.

## 6. Every visual beat earns its place

Typical functions, selected adaptively: `HOOK`, `REVEAL`, `TACTILE_DETAIL`, `USE_PREP`, `USE_EXECUTION`, `FOLLOW_THROUGH`, `PAYOFF`, `CTA_HERO`. A beat contributes useful information, emotion, sensory appeal, commercial evidence, or buyer motivation; it does not exist just to reach a count.

For each beat know:
1. Why it exists and what the viewer learns.
2. The single main visible action, or deliberate stable inspection.
3. The actual starting state and intended end state.
4. The cut opportunity and relation to neighboring footage.
5. What motion, text and identity must remain faithful.

Common planning range: 4–8 beats (often 5–6 for a 20–30-second ad), **not a quota**. Reject idle or repetitive beats where they don't serve a deliberate bookend or meaningful comparison. Label-heavy B-roll may be almost static for legibility, but its edit duration must still earn its place.

## 7. Cut over complexity; complete simple actions when possible

Prefer one physically clear action per independently generated clip: controlled lift, slide, point, pour, tap, pat, gaze shift or near-static view. A small follow-through is allowed. Minimize stacked instructions involving gaze, hands, product, camera and facial expression at once.

Split difficult chains into separate pre-established states and use a hard cut. Example: closed tub / **cut** / open tub / **cut** / scoop ready / **cut** / finished shake. A hard cut may skip a difficult opening or closing action, but it must not violate the object's physical state or insert an unapproved prop.

Do not confuse simplification with stripping every action down to "almost about to". When the point of a beat is dispensing, lifting or pouring, the video should attempt that **one meaningful action** before downgrading to a mere readiness gesture.

**Motion-simplification ladder:**
- L1: One realistic completed action.
- L2: Same action with smaller range/slower pace.
- L3: Minimal physically complete motion, early usable cut.
- L4: Readiness/near-static fallback only after genuine technical difficulty.

Retain the chosen shot objective unless the user approves a different creative direction.

## 8. Product and prop state ledgers

Record relevant `state_in`, `one_action`, `state_out`, `physical dependencies`, and `cut_exit`. Original product evidence and actual starting image outrank language assumptions. Keep exact component count, closed/open/attached/detached status, supported orientations, authentic size, graphics and material. A cut never authorizes a magically redesigned package.

Classify external supporting props as:
- `IDENTITY_CRITICAL`: special or branded; preserve supplied source and request reference when necessary.
- `ACTION_ESSENTIAL_GENERIC_ALLOWED`: ordinary shaker/glass/towel/spoon etc.; user may provide a reference, otherwise Image Analyzer can establish one neutral unbranded design.
- `OPTIONAL_BACKGROUND`: don't invent for decoration.

A supplied screw-on lid or scoop is a **product component**, not a randomly regenerated generic prop. Approved recurring generic props get one identity anchor (shape, material, color, size, state) maintained across frames and clips. Keep fluid contents, scoop fill, closures, hand ownership and object support coherent.

## 9. Starting-image authority and hidden geometry

The **actual approved image is the absolute visual authority for frame one**. The Image Analyzer handoff defines intention; if it describes a pose that is absent or already completed in the image, the Video Analyzer must describe the real visual state and revise the motion plan, not force frame one to metamorphose.

Examples of useful first states:
- closed tub partly entering from the side, with visible logo and hand already pressing its body
- detached dropper already near an exposed cheek, ready for one small dispense
- scoop handle already contacted by the hand, ready to lift
- label already legible, requiring only very restrained camera/hand movement
- creator looking toward product, ready for a small look to camera

**Partial-frame product entrance test:** Preserve the approved entrance image and intended direction. Unseen surfaces remain an identity risk; a first-frame-only model may invent hidden label/body geometry. Where the chosen mode actually supports auxiliary references, compare using the original fully visible product as an explicit secondary identity reference; do not claim such reference support for a keyframes-only entry point. Otherwise note the risk and test the motion before modifying the starting frame. Do not pretend the model sees the full original product unless it was supplied in that specific generation task.

## 10. Multi-anchor and cross-clip visual continuity

Do not assume Clip 01 establishes every visual identity. Reuse authoritative source/reference mappings from the Image Analyzer:
- creator facial identity, body/wardrobe, and best approved creator-session appearance
- manufactured product geometry, labels, state and size
- component calibrations for dropper, scoop, cap, lid or other recurring parts
- identity of approved generic props
- stable physical room, fixed fixtures, countertop/cabinet materials and supported decor
- overall phone-camera family, exposure, natural color and light direction

An approved image may calibrate a **specific element**, not automatically its crop, posture, facial tilt, hand position or all objects. Repeating an accidental tilt/pose is not a fidelity requirement. Close-up B-roll need not show every room fixture, but any visible fixed elements must belong to the same space. Camera distance can change without moving cabinet handles or replacing countertops.

## 11. Cross-clip color continuity: separate the responsible layer

Treat three different risks separately:

**Image-source difference:** Approved starting images may already have slightly different white balance/skin tones. Video prompting cannot retroactively correct this without altering frame-one authority. Flag for later Image Analyzer adjustment or light CapCut grading.

**Within-clip video drift:** Hair, skin undertone, product color, clothing, cabinet/counter color, exposure, contrast or lighting change during the video despite a stable input image. This is a video-model/prompt failure. Preserve source palette, facial identity, ambient light direction and material response.

**Cross-clip editing mismatch:** Two individually acceptable clips cut together at visibly different color/exposure levels. Suggest **minimal, matched grading and shot ordering** in CapCut rather than re-generating everything unless the mismatch is severe.

Never instruct the video model to warm/cool/beautify an already approved frame just to disguise the mismatch. Test at the actual cut, not just while viewing isolated clips.

## 12. Product physics and realistic human performance

Prioritize gravity, inertia, contact and containment. Closed solid packaging is generally more forgiving; open powder, liquid containers, tiny detached components, near-eye dropper contact, and moving labels are more fragile.

**Creator behavior:** Low-key, natural, sparse blinking, stable expression, limited intentional gaze shifts, normal breathing, no exaggerated acting or scripted mouth movement. For external VO, **do not animate speaking**. Lips should remain at their natural frame-one state except minor incidental motion.

**Hands:** realistic grip, thumb opposition, wrists, pressure, skin contact, object weight and one stable support role. No duplicate hands, teleports, product inflation or detached fingers.

**Objects:** no cap duplication, disappearing lids, deformed scoops, flying powder, expanding bottle, liquid pouring through glass or moving without cause. Transparent pipettes and liquid should obey source state and plausible gravity/surface tension; a drop is small rather than a manufactured stream.

**Camera:** stable or modest phone-like motion by default; dynamic camera motion is an explicit motivated exception. Do not add zoom/orbits/pans to hide an idle beat. Small genuine product movement can be better than simulated camera drift.

## 13. B-roll and pacing designed for editing

Good B-roll helps interpret the product: category text, tactile reality, fit, texture, size, motion, packaging callouts, credible use and payoff. Bad B-roll shows the same product repeatedly with no new information.

Each generated clip needs:
- recognizable stable opening based on the exact image
- one specific event or intentional near-static detail
- enough visually usable material for a trim
- a useful cut exit, ideally after one clear completion

Don't prescribe equal durations. A 5-second render may yield only 1.5 seconds of useful footage; actual trim length is determined after review. A single continuous VO should bridge clips without requiring one sentence or one breath per image. Let visual action support the buyer message, not narrate obvious mechanics.

## 14. Engine-neutral video planning and test architecture

The **Video Analyzer**, not this skill, chooses a model, entry point, prompt format, quality mode or exact clip duration. The skill offers a structured comparison method. For REBUILD_V1:

**Baseline path:** Separate silent image-to-video generations from the approved starting images. Compare single-clip methods before trying to replace the entire independent-clip workflow.

**Candidate categories** (capabilities MUST be rechecked in the current official UI/docs):
- first-frame-only image-to-video for simple human/object action
- image-to-video with first frame plus *genuine* additional element/product references for identity-sensitive motion
- 4.0 Keyframes for a controlled single clip with first/last frames when an approved end state exists, or an explicitly approved multi-keyframe experiment
- 4.0 Omni for reference-rich action or identity preservation when its controls support the intended task
- optional lower-cost/Flash modes as quality-vs-credit comparison, not assumed equivalent capabilities

Do **not** equate "Omni Reference" with "Keyframes"; they are distinct creation paths with different supported reference types. Do not place unrelated approved ad frames as middle keyframes and expect natural edit-style cuts to be reliable without testing. If a single long multi-keyframe generation fails one transition, the entire output may need regeneration, reducing the advantage of its longer duration.

**Video model availability and prices may change.** Record exact UI model labels and charged credits rather than building hardcoded version rankings/prices into this skill.

## 15. Controlled experiment protocol

For a fair comparison, hold constant whenever supported:
1. Same approved starting image and intended one action.
2. Same resolution, aspect ratio, duration, audio-off preference and broad camera direction.
3. Semantically equivalent instructions: subject, action, locks, ending.
4. Equal reference assets **when the capability being tested isn't reference support**.
5. Same practical acceptance standard and clips viewed at normal playback speed.

Compare one variable at a time where possible. Some models inherently support different reference controls or durations; **record those as meaningful limitations**, not as perfectly controlled comparisons. Start with one high-information exploratory test per candidate, then repeat finalists when randomness makes results unclear. Avoid an expensive full 5–6-clip matrix until the two difficult probe shots identify good candidates.

Recommended probe shots from current development evidence:
- protein tub sliding partly in from the right edge (hidden geometry, label stability and hand contact)
- skincare dropper dispensing near cheek (precision, liquid physics, facial integrity)
- optional label-row close-up (letter/icon stability) and creator CTA (subtle gaze).

Measure **usable final-edit seconds**, not just generated seconds. A cheaper generation that repeatedly fails may cost more per usable second.

## 16. Kling prompting formats: distinguish API payload from natural-language prompt

JSON is used as a **transport structure in Kling's API**; this does not prove a user-written arbitrary JSON *text prompt* outperforms prose in the website textbox.

Test prompt communication after finding plausible engine behavior:
- concise natural-language motion prompt
- concise labeled sections (FRAME ONE / ACTION / CAMERA / PRESERVE / END)
- JSON-style text prompt with **the exact same semantics**, if the selected interface accepts it

A native API multi-shot array, when supported, is not equivalent to pasting JSON as free text. Prefer the engine's documented fields for actual API use. Avoid bloated prohibitions, conflicting camera directions or over-animating micro-behaviors. Never output API payload as a website-ready prompt unless its UI genuinely accepts that format.

## 17. Minimal video prompt anatomy

Every engine-ready clip prompt should normally specify:
1. **Frame-one lock:** start from the supplied image without redesigning it.
2. **One primary action:** one natural motion that still remains to be performed.
3. **Motion size and physical behavior:** realistic duration/amount, gravity, grip, stable product orientation.
4. **Appearance continuity:** protect product label, human/face, environment, hair, wardrobe, materials, lighting.
5. **Camera behavior:** stable smartphone perspective unless intentional movement has a reason.
6. **Usable exit state:** where the motion ends for a cut.
7. **Audio:** no generated dialogue/native sound/music if the selected interface supports audio-off. Otherwise remove unwanted soundtrack in assembly, and explicitly flag the limitation.

Engine-specific syntax, image slots, model settings and number of negative directives are the Video Analyzer's responsibility. Compact execution instructions beat a JSON dump of the entire Strategist/Image Analyzer handoff.

## 18. Video QA and failure classification

Review the generated VIDEO, not only the first frame. Evaluate:
- starts from approved frame without unexpected changes
- action happens plausibly and meaningfully, not just idling or inventing extra actions
- creator facial identity, gaze, micro-expression, fingers and body stay coherent
- product silhouette, dimensions, labels and parts remain stable
- liquid/powder behaves plausibly and intended action completes where needed
- visible room and lighting stay coherent within clip; compare color/exposure across cuts
- no unwanted speech, subtitles, logos, extra props or soundtrack
- edit usability: clear moment to keep/trim; meaningful end or cut

Use decisions `PASS`, `PASS_WITH_CAUTION`, `REVISE`, `SKIP` or `ENGINE_LIMITATION` with clear evidence. `PASS_WITH_CAUTION` must name the risk and what a final edit can safely hide; it isn't equivalent to unconditional PASS. `SKIP` requires checking that the commercial narrative remains understandable.

Failure origins:
- `START_IMAGE_LIMITATION` (starting state doesn't allow intended action)
- `REFERENCE_OR_IDENTITY` (model invents unseen product/prop or changes person)
- `MOTION_COMPLEXITY` (too many interactions or movements)
- `PRODUCT_OR_LIQUID_PHYSICS` (deformation, spilling, impossible contact)
- `TEXT_AND_LABEL_STABILITY` (warped logos/iconography)
- `WITHIN_CLIP_COLOR_DRIFT` vs `SOURCE_IMAGE_COLOR_DIFFERENCE` vs `EDIT_MATCHING`
- `ENGINE_CAPABILITY` (valid setup repeatedly fails on a given model/mode)
- `PROMPT_AMBIGUITY` (unclear instruction)
- `BEAT_OR_COMMERCIAL_FAILURE` (boring shot, weak payoff, unnecessary repetition)
- `AUDIO_ARTIFACT` (unwanted speech/sound in silent workflow)

Fix the smallest responsible layer. A valid but unsuccessful video generation doesn't automatically justify rewriting the Strategist or source image prompt.

## 19. Revision, credit use and retake logic

- Preserve approved source assets, commercial purpose and successful parts of the prompt.
- If one-action physics fails, reduce range/complexity first; try a different tested model/mode if it is clearly an engine limitation.
- If the original first frame is already impossible for the intended motion, **escalate to Image Analyzer**, not repeated blind video prompts.
- If product geometry is missing from a first-frame crop, compare an **actual supported reference-capable engine** instead of asking the model to "remember" an image it never received.
- If action succeeds but color shifts inside the clip, correct motion/prompt/mode. If source frames mismatch, defer modest matching to CapCut or report image-stage root cause.
- Regenerate **only the failing clip** when the separate-clip baseline is in use; keep passing clips.
- Always provide a complete replacement video prompt on REVISE, not a list of detached patches.
- Track number of generations, revisions, seconds and credits. Avoid declaring a feature solved after one lucky run.

## 20. Test log and acceptance metrics

Each test should record:

`test_id`, `product_and_clip_id`, `starting_image_id`, `engine_exact_label`, `entry_mode`, `resolution`, `duration_generated_s`, `native_audio_setting`, `prompt_format`, `reference_assets_and_roles`, `prompt_revision`, `charged_credits`, `usable_seconds`, `frame_one_fidelity`, `product_identity`, `creator_identity`, `physics`, `color_stability`, `commercial_usefulness`, `decision`, `failure_root_cause`.

Optional useful fields: `compared_to_test_id`, `cut_in_out`, `retake_count`, `viewer_noticeability`, `notes`.

Score actual outcomes rather than engine marketing. Prefer a workflow that reliably preserves products, produces usable footage quickly and lets beginners retake a single failure. A new model or feature earns a default recommendation only after repeatable **cross-category** validation, not its published feature list.

## 21. VO and CapCut assembly

Videos default to **silent footage**. Spoken persuasion is produced separately as one coherent external VO track and can span multiple clips. No native voice consistency/lip-sync tests are required for the main pathway.

Once footage is usable, coordinate a single natural sales narrative, trim dead time, cut on physical/action or visual contrast, keep text and labels readable, and apply only necessary captions and optional music. Use light matching to reduce cross-clip color disparities without covering visible generation failures. No need to stretch a clip to match an initially suggested sentence length. Keep the final edit commercially purposeful.

The Video Analyzer may draft commercial timing guidance, but a dedicated VO execution stage owns the final continuous wording and the user/editor owns the final CapCut timeline.

## 22. Output expectations by caller

**Strategist:** Commercial visual beat map with purpose, one-action opportunities, different A/B/C visual journeys, buyer-use payoff, generic-prop plan, and VO message role. No model lock, exact video prompt or full final script.

**Image Analyzer:** Exactly N approved starting images for N planned independent development clips, each with frame-one present/not-yet/action, multi-anchor continuity, selected minimal relevant image references, PASS/REVISE notes and image-to-clip mapping. Do not add extra images solely because a model *could* use them.

**Video Analyzer:** Map actual approved images by visible contents and handoff signatures; review full story; propose succinct clip motion/risk/edit plan and a feasible *test mode*, not a forest of engine choices. After approval, generate **one** engine-ready video prompt at a time and review each returned clip. Include end-state and editing guidance. In development, allow the user to explicitly change engine/format for comparisons while keeping creative intent constant.

**Assembly:** Final order/trim proposal, continuous VO alignment, useful cut points, modest color consistency suggestions, omitted/revised clips and commercially sufficient ending.

## 23. Universal check before proposing motion

Ask only questions that affect the next decision:
- Does the viewer get useful new visual/commercial information?
- Is the intended movement possible from **this exact first frame**?
- Does it preserve face, product, room, props, labels and measured scale?
- Is one action enough? Is action completion preferable to preparation-only?
- Does the shot work with silent video and one continuing VO?
- Is the expected usable footage worth the retake and credit risk?
- If it fails, can we revise only one clip?

Avoid padding reports with every technical concern if it doesn't affect the chosen test.

## 24. Versioning, workflow testing and doctrine

Current skill version is a **development iteration**. Keep a log of assumptions versus actual Kling tests. Do not lock model, entry mode, JSON prompt format or longer multi-keyframe workflow until representative trials establish repeatable fidelity, physics, color and per-usable-second economics across serum, protein and at least one other product category.

Remote GitHub loading is optional. Master prompts may retrieve this skill by URL and report the **actually confirmed** version, or use a concise embedded fallback without claiming retrieval. Updating this skill alone does not change old master prompts automatically. Preserve existing finished zero-based handoffs; start future coordinated workflows with 01 IDs.

**Final doctrine:** Commercial meaning selects the shot. The approved image defines its first frame. One simple action creates usable motion. Edit cuts create pace. Multi-anchor continuity protects reality. Silent independent clips and one continuous VO give the user flexibility to replace failures without regenerating the whole ad. The video engine must earn its place through controlled evidence.
