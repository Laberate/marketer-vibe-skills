---
name: ugc-visual-production
description: Universal visual-production methodology for fast-cut AI UGC ads across Strategist, Image Analyzer, Video Analyzer, and final edit. Use for product-adaptive beats, B-roll, purposeful shot variation, motion-ready first frames, separate short-clip production, product and creator continuity, physics-safe actions, cross-clip QA, VO-first pacing, and controlled video-engine testing. Does not lock a model or dictate a specific video-prompt format.
license: Proprietary
compatibility: Portable plain-Markdown Agent Skill. No GitHub access, plugin, API, video model, or editing software is needed to read or apply its principles.
metadata:
  author: MarketerVibe
  version: "1.3.0"
---

# MarketerVibe UGC Visual Production Skill V1.3.0 DEV

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

Do not confuse simplification with stripping every action down to "almost about to". When a physically credible, supported action is feasible, attempt that one meaningful action rather than padding the clip with readiness gestures. **Exception:** precise free-air liquid transfer from a tiny dropper to facial skin is not a default completion requirement; after repeated observed failures, prioritize a clean edit over physically implausible simulated liquid. Only attempt such dispensing as an explicit higher-risk user-approved experiment.

**Motion-simplification ladder:**
- L1: One realistic completed action.
- L2: Same action with a simpler, still purposeful trajectory; reduce range or speed only when physics requires it.
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

## 9. Frame-one coverage and reference-role routing

The **actual approved starting image controls frame one**. A product source can govern its true identity but does not give the video engine unseen pixels unless it is physically supplied in that generation task and the chosen mode can use it. Never demand that a model reconstruct a hidden side merely through increasingly long negative instructions.

Before choosing an engine, conduct a **future visibility audit**:
- What rigid product surfaces, printed information, hand regions, clothing or facial areas will become visible after frame one?
- Are they fully present in the start image? If not, are they identity-critical or safe to infer?
- Which additional approved source supplies that appearance, and does the actual selected mode support a **separate reference**, not merely another timeline keyframe?
- Will motion expose more of a hand or arm than its frame-one reference shows? If yes, expect anatomy/skin-generation risk and first consider changing the starting image to show a more complete real hand.

**Observed development finding (two product-slide experiments):** single-start-frame Kling 3.0 Standard invented product packaging as the hidden portion entered view. Kling 4.0 Omni with a separate full-product reference improved overall shape/identity but did **not** eliminate duplicated printed elements or an artificial-looking partially revealed hand. Treat the pattern as a routing signal, not a universal engine guarantee.

For hidden identity-critical geometry, recommend a **tested reference-capable path** before a blind first-frame-only path. In Kling Omni when the user's current interface supports it, explicitly distinguish the starting frame from the full product identity reference. The starting frame must keep its crop and hand position; the identity reference may only define the manufactured object as surfaces are revealed. Use reference identifiers such as `@Image1` and `@Image2` only when the interface accepts those tokens. A product packshot must not become the scene/camera authority.

For a **brisk partial-frame entrance**, keep enough original branding in frame one, a physical pushing hand contacting the container BODY, room/counter continuity, and movement space. Let the slide happen promptly and decelerate naturally. A fast slide does not justify floating, product rotation, side-panel invention or label duplication. Evaluate hand appearance and new visible packaging independently.

For a fully visible subject performing a simple human action, a first-frame-only video path can be the efficient default trial. This is a provisional *shot-type* recommendation, never a permanent model lock.

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

## 12. Realistic motion, natural sales energy and liquid physics

Prioritize gravity, inertia, contact, containment, creator anatomy, surface texture and identity. The default commercial energy is **engaged, purposeful and naturally brisk**, not bored and low-motion, nor hyperactive AI-influencer acting. Scale movement to the action.

**Motion energy by action family:**
- `HOOK / ENTRANCE`: immediate decisive action, e.g. a brisk horizontal product slide with credible acceleration and deceleration; minimize idle setup.
- `PRODUCT REVEAL`: a short confident lift/reposition at ordinary natural speed; label settles readable.
- `TACTILE / RIGID`: crisp simple manipulation, one hand role, product remains physically supported.
- `LABEL DETAIL`: minimal camera/object motion for typography stability; trim short in edit.
- `SKIN / FACE CONTACT`: soft normal-speed pat/withdrawal, subtle engaged eyes, not an extended frozen pose.
- `CTA`: gentle but confident human expression and product memory; no forced speaking mouth.

The chosen generated render length is **not the chosen edit length**. Complete attention hooks near the beginning of the render where feasible, and cut out the remaining dead hold. If timing matters, express it as an approximate early-action target (e.g. slide completed near first second), never a guarantee or license for physically impossible speed.

**Creator:** lively but credible eye and facial behavior; preserve original expressive intent. Avoid sleepy slow acting, excessive blinking, dramatic surprise, forced smile, prolonged sideways staring, lip-sync and random swaying. In external-VO mode the person need not talk.

**Hands:** require actual contact, skin texture, normal fingernails and credible pressure, wrist/forearm continuity, stable thumb opposition and believable mass. If part of a hand must emerge from offscreen, prefer improving **frame-one hand coverage** over another long prose prompt. A real creator-hand reference may be trialed in a compatible reference mode, but it must not substitute another person's identity or transform the frame-one pose. Flag plastic/waxy fingers as a meaningful human-fidelity defect.

**Liquid physics:** a single forced tiny drop is not inherently how a squeeze dropper dispenses liquid; quantity depends on bulb compression, fill and viscosity. Two observed serum dropper-to-cheek generations (Kling 3.0 Standard and 4.0 Omni) showed unconvincing appearing-on-skin liquid and/or disconnected trajectories. **Default to cut-over-liquid complexity**: detached applicator detail / hard cut / creator already patting serum into skin. Other practical alternatives: a product-ready pose without visible discharge, or natural finger/back-of-hand application when source and user support it. Do NOT generate fake liquid to imply a completed interaction. Direct visible liquid transfer is optional and explicitly high-risk, not globally banned if the user wants to experiment.

**Objects:** preserve exact component count, rigid product shape, label geometry, powder/serum state, countertop contact, no extra props, disappearing lids or warped pipettes. Camera stays stable smartphone-native unless motion clearly serves the shot.

## 13. Edit-driven rhythm and usable action window

Useful B-roll adds distinct information: label/category, physical scale, component state, preparation, tactile feel, finished use or relevant buying cue. Do not produce several long near-identical product holds to fill a target duration.

Plan three windows for each clip: **action begins**, **useful moment/clear completion**, **safe cut/trim exit**. Avoid long delays before action and overly generous static tail. Recommend a usable edit range only after reviewing actual footage. An illustrative 4-second render might supply a good 0.8-1.5-second product hook or a 1-2-second facial pat; these are not fixed prescribed timings.

When a reference-led product slide succeeds mechanically but has a duplicated printed label or artificial hand, classify those defects independently. Shortening the edit does not make inaccurate packaging acceptable if the defect remains visible in the kept section.

Cross-clip lighting/exposure mismatch may need limited CapCut matching. Do not invent a different light source or force the video to recolor an approved starting frame to disguise a cross-image mismatch.

The continuous external VO carries persuasion across cuts. Clips do not need their own dialogue or identical run times. Short useful motion beats + sensible trim + confident conversational VO produce energy more reliably than asking a silent model to overact.

## 14. Conditional engine routing and independent video architecture

The **Video Analyzer**, not this skill, owns engine choice, UI-specific upload instructions, exact settings, prompt syntax and clip-by-clip approvals. Do not permanently lock one Kling model from a few samples.

**Current provisional shot-type routing, derived from tests:**

| Shot need | First trial to consider | Evidence and caveat |
| --- | --- | --- |
| Identity-critical product moves from cropped/offscreen into view | A reference-capable Kling 4.0 Omni mode using start image + distinct full product image, if current UI permits | Better product completion than tested 3.0 Standard, but duplicate text and hand problems persisted |
| Subject fully visible, simple facial/hand movement | Kling 4.0 Keyframes interface with **only the starting frame** (or comparable first-frame I2V) | Serum pat-in yielded a usable natural short clip; no extra keyframe required |
| Fully visible label/product detail | Available first-frame-only path with very restrained motion | Unverified for every model; prioritize stable printed text |
| Hard multi-stage physical actions or precise liquids | Separate edited clips; simplify or omit the fragile transfer | Both tested serum dropper-dispense paths failed; do not force Omni to fix physics |

Treat Kling 3.0 Standard, 3.0 Omni, Kling 4.0 Omni, 4.0 Keyframes and other accessible modes as **experiments**; current UI features, duration and credits must be confirmed rather than presumed. Distinguish Omni's auxiliary image reference from the *additional timeline keyframes* in Keyframes mode. A Keyframes task with only its first frame does not magically see a separately uploaded product source.

Baseline remains **one approved starting image -> one separately generated silent clip**, replace failed clips locally, assemble VO/cuts later. Multi-keyframe full-ad generation is an optional side experiment with explicit user approval and retake-cost evaluation. Never silently switch to a single long render.

If a user has **explicitly selected** a mode, respect it and report risks; suggest a reference-capable alternative only when the observed failure warrants it. Preserve chosen user creative experiments, including the partial-frame tub slide.

## 15. Credit-aware controlled tests

Hold the same starting image, intent, approximate render length, aspect ratio, quality/audio settings, and meaningful hard locks across comparable trials where supported. Record when reference capability itself changes, as that is **a different workflow condition**, not a perfectly controlled model-only comparison.

Recommended development probes in sequence:
1. Cropped product entrance: first-frame-only vs separate-full-reference path; inspect **label text and hand anatomy**, not just overall shape.
2. Same reference-capable product entrance: normal vs **brisk front-loaded slide prompt**; compare arrival time, hand position, kept segment and product fidelity.
3. Simple human follow-through: one-frame Keyframes serum pat-and-release or equivalent; inspect face/skin/hand, gaze and usable duration.
4. Other shot families, only after these probes: label B-roll, scoop lift, creator CTA.
5. Direct dropper-to-face liquid dispensing is **not** a mandatory default probe after repeated failure. Retest only with a materially changed physical setup or explicit user request.

Repeat finalists only when results are ambiguous or random variation matters. Measure spend, useful seconds and retakes. One passing video never proves an engine globally superior. After the full serum, protein and third-category advertisements are edited, compare clip quality, continuity and commercial effectiveness before locking the stack.

## 16. Kling prompting formats: distinguish API payload from natural-language prompt

JSON is used as a **transport structure in Kling's API**; this does not prove a user-written arbitrary JSON *text prompt* outperforms prose in the website textbox.

Test prompt communication after finding plausible engine behavior:
- concise natural-language motion prompt
- concise labeled sections (FRAME ONE / ACTION / CAMERA / PRESERVE / END)
- JSON-style text prompt with **the exact same semantics**, if the selected interface accepts it

A native API multi-shot array, when supported, is not equivalent to pasting JSON as free text. Prefer the engine's documented fields for actual API use. Avoid bloated prohibitions, conflicting camera directions or over-animating micro-behaviors. Never output API payload as a website-ready prompt unless its UI genuinely accepts that format.

## 17. Minimal engine prompt anatomy and reference instructions

For any per-clip engine-ready prompt, supply only the inputs the model can truly receive:
1. **Frame-one authority:** exact starting image and existing pose/state.
2. **Reference roles if supported:** e.g. `@Image1` starting environment/hand/composition, `@Image2` full identity of cropped product. Explicitly instruct that the packshot is **not** a new scene or end keyframe.
3. **Single action + energy:** direct, understandable movement; brisk for a product entrance, gentle for skin contact; avoid contradictory pacing words.
4. **Hard visual locks:** shape, source label, component count, creator, contact, stable camera/environment/lighting.
5. **Completion and edit exit:** what should become fully visible or physically settle; trim dead tail.
6. **Only likely-failure prohibitions:** no duplicate text, hand morph, label changes, impossible liquid, extra product, etc.
7. **Audio OFF in controls** whenever possible. A text-only 'silent video' command is not a reliable native-audio disable; mute in final assembly if UI cannot disable it.

For time-directed attention hooks, favor e.g. 'the tub slides in immediately and comes to rest near the first second' over 'slow smooth controlled movement'. Do not ask for unrealistic acceleration or camera tricks to manufacture energy.

Do not dump the whole Image Analyzer JSON into Kling, claim support for invented reference tokens, or use JSON free text as a presumed special structured format. Website prompt text, API JSON envelope, and native multi-shot schemas are different concepts; test each fairly.

## 18. Video QA: separated quality dimensions and vetoes

Review actual video through multiple points in time and at normal playback speed. Rate separately: **motion/commercial pace; manufactured product/label accuracy; creator/hand realism; physics; environment/color stability; edit usability; unwanted audio**. A fast slide may pass motion and still FAIL product fidelity.

**Hard-failure examples:** duplicated `NET WT.`/weight text, fabricated side-panel design, changed orange logo or category, deformed tub, waxy/plastic fingers covering label, pipette liquid appearing on skin without believable transfer, new face/hand/object, extreme room changes. An error that remains visible in the proposed final cut is not excused because the rest of the clip looks attractive.

Decisions: `PASS`, `PASS_WITH_CAUTION` (only if defect demonstrably avoidable by trimming/matching), `REVISE`, `SKIP` (with narrative continuity check), `ENGINE_LIMITATION` (repeated valid failure).

Distinguish root causes: `HIDDEN_PRODUCT_INFORMATION`, `REFERENCE_MODE_MISMATCH`, `START_FRAME_HAND_COVERAGE`, `PRODUCT_LABEL_DUPLICATION`, `HAND_PLASTICITY`, `ACTION_TEMPO_TOO_SLOW`, `PRECISION_LIQUID_TRANSFER`, `SOURCE_COLOR_MISMATCH`, `WITHIN_CLIP_COLOR_DRIFT`, `EDIT_MATCHING`, `PHYSICS_COMPLEXITY`, `PROMPT_AMBIGUITY`, `MODEL_CAPABILITY`, `COMMERCIAL_BEAT_WEAKNESS`, `UNWANTED_AUDIO`.

If an error is concentrated in the last 2 seconds while the first 1 second is clean, an edit may pass. If the logo/label is already wrong during the intended usable entrance, REVISE. Do not use a superficial total score to conceal a fatal product-truth error. If only screenshots are available, do not claim action timing, duration, audio, or movement fidelity.

## 19. Revision and escalation order

1. **Trim first** if an actually clean useful motion segment exists and the defects are outside it.
2. **Retarget tempo/action** if product/hand fidelity is good but a hook is sluggish. Change only motion timing and a few critical instructions.
3. **Add supported full-product references** if the engine must reconstruct a hidden identity-critical surface; do not rely on extra negative text.
4. **Improve hand coverage** by using an approved starting frame that already shows the relevant fingers/palm; a compatible same-creator hand reference is an optional test, not a guarantee.
5. **Simplify physical action / cut around it** if precise liquid/face/powder physics fail. Do not reroll the same one-drop-to-cheek prompt repeatedly.
6. **Change engine/mode** if valid inputs repeatedly fail and an alternate mode can address the actual missing capability.
7. **Escalate to Image Analyzer** only if the starting frame itself is unsuitable. Preserve the selected Strategist concept unless the user approves a redesign.

Regenerate **only the failed clip**. Every REVISE returns a complete copy-ready prompt with the changed assumptions clearly named. Record credit spend, failure origin, editable seconds and the hypothesis for next attempt. Avoid endless prompt edits without meaningful input/mode changes.

## 20. Test log and evidence discipline

Record: `test_id`, `product/clip`, `starting_image_id`, `engine_actual_mode`, `reference_roles_and_count`, `extra_visible_identity_coverage`, `render_duration`, `audio_enabled_in_UI`, `prompt_format`, `action_target`, `action_completion_time_observed`, `charged_credits`, `usable_edit_range`, `motion_grade`, `product_label_grade`, `hand_realism_grade`, `physics_grade`, `color_grade`, `edit_grade`, `decision`, `failure_code`, `rerender_reason`.

Observed current evidence, not locked policy:
- Kling 3.0 Standard, protein partial-frame slide: missing product area was invented; result rejected.
- Kling 4.0 Omni with separate full-product source, protein slide: substantially improved geometry, but label duplication and artificial hand persisted; changing prompt yielded faster entrance.
- Kling 3.0 Standard and 4.0 Omni, dropper-to-cheek liquid: both visibly implausible.
- Kling 4.0 Keyframes with first frame only, serum cheek pat: usable natural motion after trimming.

Do **not** claim success for other product types, other engine settings, or the full assembled ad until tested. Use credit cost per accepted edit second and consistency at actual cuts when comparing workflows.

## 21. VO and CapCut assembly

Videos default to **silent footage**. Spoken persuasion is produced separately as one coherent external VO track and can span multiple clips. No native voice consistency/lip-sync tests are required for the main pathway.

Once footage is usable, coordinate a single natural sales narrative, trim dead time, cut on physical/action or visual contrast, keep text and labels readable, and apply only necessary captions and optional music. Use light matching to reduce cross-clip color disparities without covering visible generation failures. No need to stretch a clip to match an initially suggested sentence length. Keep the final edit commercially purposeful.

The Video Analyzer may draft commercial timing guidance, but a dedicated VO execution stage owns the final continuous wording and the user/editor owns the final CapCut timeline.

## 22. Outputs by calling stage

**Strategist:** Product-aware creative beats, distinct A/B/C options, reasonable interaction risks, meaningful visual progression, payoff, generic prop policy, VO message direction. Not an engine picker.

**Image Analyzer:** N approved starting frames for N individual development clips, multi-anchor identity, edit-ready motion runway, source-complete product/state, economical references. For a shot revealing hidden product/hands, flag the **future visibility dependency** without automatically cancelling the idea.

**Video Analyzer:** Visually map actual starting images; preflight expected motion and unseen geometry; choose conditional engine and reference coverage; publish a concise full-clip plan; after approval generate one clip prompt at a time; review actual clip and make a cause-specific PASS/REVISE with usable cut range. Record observed timing and label/hand/physics defects separately. Default silent videos + external VO.

**Assembly:** Trim dead tails, match modest color differences, lay one natural energetic VO over cuts, preserve product readability, omit failed segments only with buyer-story/CTA coverage.

## 23. Preflight check before any generation

- Is the approved starting image actually suitable for the intended one action?
- Will the movement reveal **unseen logo, text, bottle/tub surfaces, fingers or forearm**? If yes, is the additional identity information available through the chosen mode?
- Is a branded product visually correct already? Are any text/label changes unacceptable in the final cut?
- Is the action's tempo appropriate to selling rather than sleeping, without breaking physics?
- Are liquid or tiny near-face tasks better communicated by an edit than direct simulation?
- Does the clip contribute new information? Can it be cut at a clean useful moment?
- Have native audio settings been disabled, rather than relying only on written words?
- Can a failed clip be rerendered independently at acceptable credit cost?

Don't bury users in a form or a giant test matrix. Make a recommendation and ask for only essential missing inputs.

## 24. Versioning, workflow testing and final doctrine

**V1.3.0 DEV** is a test-informed update, not a LOCKED engine recommendation. Continue testing multiple clip families and full edited ads. Validate against serum, protein and at least one third product category before locking any Kling model, default prompting format or multi-keyframe approach.

Loading a remote skill is optional. If actually fetched, report its true version. If unavailable, use a lean embedded fallback without inventing a skill-load result. Keep legacy zero-based handoffs unchanged; use one-based IDs for new compatible productions, and synchronize numbering across all modules later.

**Doctrine:** The video model provides a short convincing motion moment, not the entire ad. Brand accuracy and real human physics matter as much as pace. Give missing product information to a capable reference mode instead of hoping a prompt invents it correctly. Cut past hard liquid physics when that creates a more believable video. Generate separate silent clips, retake locally, build energy with decisive action + edits + a single confident external voiceover.

