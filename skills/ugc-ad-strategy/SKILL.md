---
name: ugc-ad-strategy
description: Commercial strategy and VO-first persuasive storytelling for real, generic, and concept-product UGC ads. Use in STRATEGY MODE before image planning to choose the buyer, positioning, angle, product interaction profile and strategic visual beats; use in EXECUTION MODE after visuals are approved to finalize one coherent voiceover script. Designed for ChatGPT, Claude, Gemini, Kimi, Codex, and similar agents.
license: Proprietary
compatibility: Portable plain-Markdown Agent Skill. Network access is optional; do not require GitHub, paid tools, or live research to proceed.
metadata:
  author: MarketerVibe
  version: "1.3.0"
---

# MarketerVibe UGC Ad Strategy Skill V1.3

## 1. Purpose and architecture

Create persuasive, natural, commercially useful UGC ads that can be executed as a sequence of believable short visual moments. The default production style is **fast-cut, visual-first, external-voiceover-led**. Native on-camera dialogue is an optional variant, not the default.

The skill decides **what should persuade the buyer and why**. It supports the calling Strategist and downstream VO/script execution. It does not generate images, video, image prompts, video prompts, motion-engine settings, or an exact CapCut timeline.

The universal workflow is:

1. Strategist: diagnose product and buyer; choose one commercial argument; build a product interaction profile, strategic visual beat map, and VO story direction.
2. Image Analyzer: convert beats into visually faithful, edit-ready starting images with a shared session/environment anchor.
3. Video Analyzer: choose and test an appropriate generation path; create motion-ready clips or multi-beat footage; plan assembly.
4. VO execution: finalize one coherent spoken script against the approved visual sequence and feasible pacing.
5. CapCut or equivalent: edit footage, sync VO, tighten cuts, add captions/music as needed.

A **beat** is a storytelling moment. A **keyframe** is an image defining a visual state. A **clip** is generated footage. They are not interchangeable, and one beat need not equal one image or one clip.

Do not lock the creative strategy to a specific Kling model, Keyframes/Omni workflow, JSON-style video prompt, or clip count. Those are downstream test decisions.

## 2. Two modes

### STRATEGY MODE: before image generation

Own:
- product reality and authorized positioning
- buyer, awareness, desire, problem, objection, purchase driver
- optional product/category research
- commercial thesis, creative angles, hook and CTA direction
- product interaction profile and strategic selection of useful actions
- flexible visual beat map (usually 4–8; often 5–6)
- single continuous voiceover **narrative direction**, not the final transcript
- asset feasibility, evidence gaps, and concise structured handoff

### EXECUTION MODE: after approved visuals / video plan

Own:
- confirm the approved commercial thesis and actual surviving beats
- write the **final one-piece VO script** with natural spoken pacing
- select a buyer-relevant opening, persuasive progression and matching CTA
- coordinate spoken sections with the visual plan without narrating each obvious action
- adapt to realistic footage duration and edits; note gaps only when material

If the video plan or footage later changes materially, adapt timing and wording without restarting strategy by default. Keep the approved concept unless the change makes it commercially unworkable.

## 3. Core persuasion doctrine

A good ad needs:

**RELEVANCE + REASON TO CARE + REASON TO ACT**

The decisive internal question is: **“This viewer should consider this product because ______.”** If the answer is only “because the cap/dropper/scoop is shown,” the argument is weak.

One short ad should normally have **one dominant strategic idea**. Do not cram every feature, benefit, mechanism, offer, and objection into the same 20-second story.

Commercial strength matters as much as visual executability. Do not choose a bland ad merely because it is easy to animate.

## 4. Plug-and-play behavior

Infer first. Never open with a long questionnaire.

- If audience is not specified, infer a plausible buyer from product/category information, not from the creator's appearance.
- If platform is missing, default to `SHORT_FORM_SOCIAL`.
- If selling/promoting is the clear goal, default to `CONVERSION`.
- If offer is missing, do not fabricate one; choose appropriate product-discovery or routine-fit CTA direction.
- If positioning is `AUTO` for an authorized concept product, create a plausible concept spec.
- If duration is unknown, suggest a broad short-form range (often 15–30 seconds); do not lock exact beat/clip durations.
- Research only when available and genuinely useful; do not block if unavailable.
- Ask at most one concise question if an unknown truly changes the core creative decision and cannot reasonably be inferred. Offer AUTO where helpful.
- Use supplied scripts as inputs. Respect `USER_LOCKED` scripts; otherwise allow strategic suggestions without silently discarding user wording.

A product image, identifiable product URL, or sufficiently clear product description is enough to begin. Other assets are optional.

## 5. Reference roles and available production resources

Identify, when provided:

- `ORIGINAL_UGC_REFERENCE`
- `MODEL_FACE_REFERENCE`, `MODEL_BODY_REFERENCE`, `MODEL_GENERAL_REFERENCE`
- `PRODUCT_PRIMARY_REFERENCE`, `PRODUCT_STATE_REFERENCE`
- `PRODUCT_MEASUREMENT_REFERENCE`
- `ENVIRONMENT_REFERENCE`, `PROP_REFERENCE`, `OTHER_REFERENCE`

One image may have multiple supported roles. Do not force a role that is unclear. Show a concise reference map initially, and repeat it only if assets change.

Use references for **production feasibility**: whether a creator exists; what states are shown; what kind of recording setting is possible; which props and physical interactions are available; whether a one-session ad is practical.

Do not turn this skill into a renderer. The Image Analyzer owns exact pose, crop, face authority, geometry, scale, hand calibration, environment anchor details, and image prompting. An original UGC image may inform the recording style without locking the exact pose. **Creator appearance is casting context, not buyer targeting.**

If a needed product state is not shown or safely inferable, mark `NEEDS_REFERENCE` or propose a simpler alternative. Do not invent unseen mechanical details.

## 6. Product reality and creative latitude

Classify internally:

- `REAL_IDENTIFIED`: confidently identifiable real product
- `REAL_UNVERIFIED`: real or apparently real product without reliable exact identification
- `CONCEPT_PRODUCT`: fictional, portfolio, prototype, or explicitly creative product
- `GENERIC_WHITE_LABEL`: generic or private-label product with limited product-specific evidence
- `UNKNOWN`: insufficient context to confidently classify

Use normal persuasive advertising confidently. Allowed commercial language includes:

- emotional or aspirational framing
- audience frustrations and desired outcomes
- curiosity, subjective impressions, opinion and lifestyle fit
- design, simplicity, experience, convenience and routine positioning
- reasonable category-informed, non-absolute benefit framing
- strong hooks and calls to action

Do **not** require formal scientific evidence for ordinary opinion, taste, or positioning. Avoid copy that sounds like compliance paperwork: “may potentially,” “possibly perhaps,” or repeated evidence disclaimers.

Separate **commercial flexibility** from **asserted evidence**. Do not independently fabricate purportedly real clinical trials, specific percentages, reviews, awards, certifications, third-party endorsements, personal histories, medical outcomes, discount terms, popularity numbers, or scarcity. When the user supplies a claim, treat it as `USER_PROVIDED_CLAIM`, preserve the requested strategic intent where possible, and do not silently relabel it `VERIFIED_PRODUCT_FACT`. Ask for substantiation only when essential to a specific hard-fact creative; otherwise choose strong truthful or subjective framing. Do not let a routine uncertainty derail the whole workflow.

## 7. Concept Product Mode and canon

Concept positioning is authorized by instructions such as `CONCEPT_PRODUCT`, `Positioning: AUTO`, “fictional,” “portfolio/demo product,” “invent positioning,” or an equivalent user request.

Create one compact `CONCEPT_PRODUCT_SPEC` defining only useful elements:

- name/category and intended buyer
- primary problem, desired outcome, product role
- primary and (if relevant) secondary benefit
- user experience, routine fit, meaningful feature or mechanism
- differentiator and positioning
- tone, claim scope, optional price/value position

This becomes **project-defined creative canon**, not actual independent manufacturer, customer, or clinical evidence. Once selected, use it consistently across strategy, image planning, video planning, and VO. Do not keep apologizing that a fictional product is fictional.

If the user has already established canon, preserve it. If they delegate with AUTO, choose a commercially plausible spec using category knowledge/research; do not generate ten contradictory versions. Distinguish approved canon from optional unselected suggestions. Do not invent purported real third-party proof for the concept product.

## 8. Research doctrine

Default `RESEARCH_MODE = AUTO`. Research only deeply enough to inform the specific creative choice. If unavailable, proceed from supplied information and established domain knowledge. Never claim web research was performed if it was not.

For a confidently identified real product, prioritize official product/brand material, packaging, supplied claims, authentic reviews/customer language, supplied performance data, competitor/category advertising, organic category patterns, and platform-native conventions. Do not confuse an existing popular ad with proven conversion performance.

For concept, generic, or unidentified products, research **CATEGORY + AUDIENCE + CREATIVE PATTERNS**, not imaginary exact-product results. If identification confidence is low, uploaded product information controls what is known about that product.

Distinguish:

- `VERIFIED_PRODUCT_FACT`: supported product-specific information
- `USER_PROVIDED_CLAIM`: claim provided by user but not independently verified
- `CONCEPT_PRODUCT_SPEC`: authorized fictional project canon
- `CATEGORY_INSIGHT`: broader buyers, objections, language, behavior
- `CREATIVE_PATTERN`: plausible advertising/production pattern
- `COMMERCIAL_INFERENCE`: reasonable interpretation, not an established product fact

Do not convert category insights or creative patterns into actual product evidence. Keep reported research signals short and relevant.

## 9. Buyer and awareness diagnosis

Before proposing angles, infer:

- primary buyer and job-to-be-done
- awareness: `UNAWARE`, `PROBLEM_AWARE`, `SOLUTION_AWARE`, `PRODUCT_AWARE`, `MOST_AWARE`
- core desire, problem, frustration and emotional driver
- main objection, purchase driver, product relevance
- reason to believe (if applicable), available proof, offer
- realistic visual demonstration possibilities

Potential purchase drivers: outcome/benefit, problem solution, meaningful feature, mechanism, differentiator, proof, convenience, tactile experience, design, identity/lifestyle, routine fit, value, offer, objection removal.

A product need not have testimonials, clinical proof, patented technology, or a dramatic transformation to produce a viable ad.

Use internal `PERSUASION_STATUS`:
- `READY`: useful commercial argument exists
- `LIMITED`: argument is generic but viable; strengthen it rather than stopping
- `INSUFFICIENT`: no reasonable argument and essential context truly cannot be inferred

Do not over-trigger `INSUFFICIENT`. For authorized concept products, improve the concept spec first.

## 10. Feature-to-buyer-consequence test

For each promoted feature ask:

`FEATURE → BUYER CONSEQUENCE → WHY IT MATTERS`

Ordinary caps, droppers, zippers, scoops and pumps may create excellent visuals without being a meaningful purchase driver. **Visual interest is not automatically commercial persuasion.**

Each major beat should answer at least one of these: create attention, establish relevance, demonstrate useful information, build desire, support credibility, remove objection, or advance CTA. A tactile beat can earn its place visually even when the VO carries the selling argument.

## 11. Angles and concept selection

Generate several truly distinct strategic options internally. Typical families: problem/frustration, desired outcome, curiosity, discovery, demonstration, objection, comparison, routine, mechanism, convenience, sensory experience, aesthetic/design, lifestyle/identity, value, education, credible proof.

Score for:

- buyer care, purchase driver, commercial thesis, hook strength
- audience/awareness fit, specificity, reason to believe
- truth/plausibility and concept canon consistency
- available reference assets and supported product states
- believable visual variety, UGC authenticity, possible payoff
- motion simplicity, cut-over-complexity, editability, production risk
- simplicity and generation-credit efficiency

Visual convenience alone must not defeat the stronger sales idea, but avoid concepts dependent on impossible anatomy, fabricated proof, many unsupported product states, elaborate transformations, or unnecessary actors.

When the master prompt calls for three directions, present exactly three genuinely different options, a recommendation and `A / B / C / AUTO`. Do not finalize the downstream handoff until a direction is chosen, unless the user explicitly delegates selection.

## 12. Hook system

Plan complementary components:

- `visual_hook`: immediate, believable visual reason to look
- `vo_hook_direction`: buyer-relevant spoken opening; **external voiceover by default**
- `text_hook`: optional editorial reinforcement, not a mandatory duplicate

A useful hook promises a commercial payoff, not just a random movement. A product lift, texture reveal, cap click, immediate demonstration, comparison, unexpected context, or already-in-progress action can work when physical logic supports it.

Avoid empty formulaic hooks (“Hey guys,” “Stop scrolling,” “Game changer”) unless unusually well justified. The rest of the ad should pay off the curiosity and reconnect to the CTA.

## 13. Product Interaction Profile (new shared strategy output)

Create a compact profile based on the actual product, not a fixed niche template. Suggested fields:

```yaml
product_interaction_profile:
  archetype: "container / wearable / device / apparel / cleaning / food / other"
  natural_use_context: "..."
  primary_interaction: "..."
  secondary_interactions: ["..."]
  supported_states: ["..."]
  state_progression: ["..."]
  tactile_opportunities: ["..."]
  demo_opportunities: ["..."]
  credible_payoff: "..."
  result_visibility: "DIRECT / IMPLIED / NONE"
  creator_visibility_needed: "..."
  useful_shot_families: ["..."]
  physics_or_geometry_risks: ["..."]
  transitions_to_cut_over: ["..."]
  reference_gaps: ["..."]
```

The profile is an **inventory**, not a requirement to film every possible interaction. Choose actions that reinforce the commercial argument. Use the shared `ugc-visual-production` skill for beat/shot/rhythm principles when available; otherwise apply the short principles in this skill and continue.

## 14. Visual beat map (new strategic plan)

Default to 4–8 visual beats, usually 5–6 for a 20–30 second ad, but allow fewer, more, shorter or longer when clearly better. Do not divide duration evenly or introduce filler to reach a count.

Choose beat families flexibly: attention/hook; product reveal; tactile detail; use preparation; use execution; follow-through; credible payoff; recommendation/CTA. Not all products need every family. Add B-roll only when it shows meaningful product information, not as arbitrary filler.

For each chosen beat, pass concise **strategic** fields (the calling master prompt controls exact JSON shape):

- `beat_id` (stable across stages)
- `commercial_role` and `visual_purpose`
- `simple_action` / `interaction_type`
- `product_state_in` and `product_state_out` when relevant
- `creator_visibility` and broad `shot_family` / framing direction
- `voiceover_message_role` (not necessarily a single spoken line)
- `starting_state_intent`, `motion_opportunity`, `cut_logic`
- `reference_needs`, `hard_requirements`, `flexible_suggestions`
- `complexity_or_continuity_risk`, `avoid`

Use **one simple primary movement per shot** when possible. Treat complex transitions (open → scoop → pour → shake) as candidate edit cuts rather than forcing one model to perform everything. The Strategist identifies the logical cut opportunities, not exact editing timestamps.

## 15. Visual continuity and product-state progression

A one-session story should preserve the same creator, wardrobe, product identity, room family, lighting family and physically logical state progression. Do not propose unexplained time/room changes as a solution to shot variety.

Strategist states the **session continuity intention** and any scene changes that are deliberately part of the narrative. The Image Analyzer owns the precise environment anchor, architecture, view angles, scale, hand positions, and cross-beat verification. The Video Analyzer owns temporal/motion realization.

A visual beat can show a product already opened when the edit communicates an intentional cut. Do not plan transitions that require an object to morph or duplicate. If a state requires missing references, flag them and simplify when practical.

## 16. VO-first commercial story

Design **one connected spoken argument** spanning the full advertisement. The VO sells the reason to care; visuals show meaningful product behavior. Do not write six disconnected mini-scripts merely because the visual map contains six beats.

Narrative direction should specify:

1. verbal hook and unresolved buyer tension/desire
2. product relevance / introduction
3. persuasive payoff: meaningful benefit, experience or difference
4. support or objection handling where appropriate
5. CTA closing the same commercial loop

Map phrases or narrative portions loosely to beats, allowing VO to run across hard cuts. Visual and audio may contrast or complement; they do not need to describe the same thing literally.

Voice tone: natural creator language, contractions, short understandable ideas, category-native phrasing, confidence without forced hype. External VO is the default, so the creator in the images is **not required to mouth the words**.

In STRATEGY MODE, pass a narrative direction, hook example if useful, VO purpose per beat, and CTA direction. Do not normally finalize the whole spoken script until image/video constraints are clearer.

## 17. Story structures and CTA loop

Choose the structure that fits the argument, not a universal framework:

- Problem → product relevance → reason to care → CTA
- Desire → product fit → visual demonstration → CTA
- Discovery → context → product → buyer consequence → CTA
- Objection → answer → support → CTA
- Routine → friction → product fit → payoff → CTA
- Identity/lifestyle → recognizable moment → desire → CTA

A CTA should relate back to the original motivation, even when soft and conversational. Do not fabricate an offer to make the ending stronger.

## 18. Natural copy, creator opinion and experience

Every line should pass: **“Would a real creator plausibly say this?”** Prefer conversational confidence, natural rhythm and customer vocabulary; avoid robotic feature lists and landing-page phrasing.

A present-tense subjective impression of something visible is not automatically a fake testimonial. But do not invent a real person's months of use or measured personal outcome when none has been established. For fictional concepts, distinguish fictional creative canon from independently existing user/customer experiences.

Every line should earn attention, relevance, desire, support, objection removal, or action. Do not narrate visually obvious steps (“Now I'm opening the bottle”) unless the instruction itself is useful to the buyer.

## 19. STRATEGY MODE output requirements

The calling master prompt may choose its response format. The useful two-step pattern is:

**First response**: concise reference map, product/audience snapshot, salient category/research signals, exactly three differentiated creative directions, recommendation and `A/B/C/AUTO` choice. Each direction previews hook, purchase driver, visual beat shape, VO narrative direction, important assets, and one clear limitation.

**After selection**: one compact machine-readable handoff for the Image Analyzer, with at least:

- `project`, `product_reality`, verified/user-provided/concept facts, evidence limitations
- `audience`, `persuasion` (buyer motivation, purchase driver, commercial thesis, reason to believe, CTA loop)
- `production_context` and references by **role**, not file upload number
- selected `creative_direction` and hook
- `product_interaction_profile`
- `visual_beat_map` with stable IDs, states, simple actions, image starting-state intent, VO roles, and complexity markers
- `voiceover_strategy` (one coherent story; final script pending)
- claim boundaries and `image_analyzer_instructions` with hard vs flexible requirements

Pass only what is useful downstream; avoid duplicated fields that can contradict one another. The Image Analyzer is free to solve exact poses, angles and motion-ready states while preserving the commercial necessities.

## 20. EXECUTION MODE after visuals are approved

Use the existing approved strategy and final visual/beat order. Do not recreate research or the concept from zero merely because some footage changed.

1. Identify the surviving beats and footage constraints; distinguish planned from actually feasible actions.
2. Reconfirm the dominant purchase driver, buyer-care angle and intended outcome.
3. Generate several hook possibilities internally; choose the strongest relevant one.
4. Write **one complete VO script** with a clear opening, middle, and CTA loop.
5. Use visual actions as support rather than literal narration.
6. Adjust for conversational pacing; do not pad narration to fill time or divide words evenly across beats.
7. Provide concise section-to-beat alignment or assembly cues if requested.
8. Retain product reality status, selected canon and claim boundaries.

If the approved strategy lacks buyer motivation, try to strengthen it using allowed positioning, category insight, subjective framing, or a better CTA. Only escalate an upstream gap if a compelling commercial argument genuinely cannot be made without essential missing facts.

## 21. Boundaries with Visual Production, Image and Video

- **Strategist + this skill**: buyer, reason to care, product interaction possibilities, commercial visual beats, high-level pacing and VO narrative.
- **Visual Production skill**: reusable shot families, beat density, simple motion doctrine, cut-over-complexity, edit readiness, cross-beat rhythm.
- **Image Analyzer + Image Fidelity skill**: exact visual reference authority, scale, anatomy, room anchor, camera/framing, photorealism and approved image outputs.
- **Video Analyzer**: engine-specific model choice, prompts (natural/structured/JSON-format experiments), beat/clip allocation, motion, durations and feasible cut points.
- **VO execution**: final continuous spoken copy and read timing.
- **CapCut**: actual assembly, trims, sync, captions and music.

Do not choose Kling 3.0 vs 4.0, Keyframes vs Omni, or JSON text prompting here. Test these later. A failure of video physics does not automatically invalidate a good sales concept.

## 22. Testing and quality checks

Before approving a strategy, ask internally:

- Does the buyer have a meaningful reason to care and act?
- Is the hook connected to a payoff the ad delivers?
- Is there one clear commercial thesis?
- Does each visual beat contribute something useful rather than filler?
- Are physical actions and states plausible with the supplied references?
- Does the external VO form one continuous narrative across the cuts?
- Is there a credible payoff or product experience where appropriate?
- Does the plan support a realistic one-session look when intended?
- Is it simple and economical enough for a beginner to execute?

The first production versions are **experimental**. Log what failed, trace the failure to the responsible layer, and revise the system before locking final versions and engine choices. Do not add five pages of defensive micro-rules to the Strategist because of one random generation artifact.

## 23. Portability and fallback

This skill is plain Markdown and works without web access, GitHub, plugins, or a specific AI/video platform. If a master prompt can load this skill remotely, use it; otherwise use its embedded fallback commercial core. Never claim a remote skill was retrieved unless it actually was. Skill availability must not prevent a basic useful strategy.

**Final doctrine:** Strong UGC advertising is not a sequence of unrelated attractive product clips. It is **one persuasive buyer story, supported by believable visual moments, with a natural voice and a clear reason to act**.
