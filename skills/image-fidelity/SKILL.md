---
name: image-fidelity
description: Universal image-fidelity specialist for photorealistic, multi-beat AI UGC. Protects product identity, state-specific physical scale, creator identity, hands/contact, lighting and camera realism, and continuity across changing shots. Adds stable environment and supporting-prop anchors without replacing the calling Image Analyzer.
license: Proprietary
compatibility: Portable plain-Markdown Agent Skill. No specific image API, GitHub connection, or external tool is required. Use as a specialist layer inside an Image Analyzer; continue with a lean fallback if remote access is unavailable.
metadata:
  author: MarketerVibe
  version: "1.1.0"
---

# MarketerVibe Image Fidelity Skill V1.1

## Purpose and usage

Improve the credibility and **cross-beat consistency** of AI UGC starting images, whether the shot shows a creator, hands, a product, a supporting prop, or an empty part of the established room. The new default workflow uses short visual beats, simple actions, external voiceover, and later editing. It does not require a speaking creator or one generated image per video clip.

**Use this skill in the UGC Image Analyzer** when mapping references, designing starting images, reviewing generations, and producing the image-to-video handoff. Apply its relevant rules only; don't print this skill or a giant checklist for every beat. The calling analyzer owns sequence state, approved strategy, asset mapping, reference selection, output JSON, and review decisions. The separate `ugc-visual-production` skill owns beat purpose, visual rhythm, cut-over-complexity, and editing principles. This skill does not choose the ad, change the hook, finalize VO, select Kling models, or write video prompts.

**Fundamental distinction:** a strategic beat is a useful story moment, a keyframe is an image of a particular state, and a clip is moving footage. They need not have one-to-one correspondence. The Image Analyzer determines which edit-ready images to generate and review.

## 1. Authority and reference roles

Assign each input an explicit, limited job. One source may have multiple *supported* roles, but do not let it silently control unrelated features:

- `MODEL_FACE_REFERENCE`: permanent facial identity root.
- `MODEL_BODY_REFERENCE`: body form, full hair, or explicitly assigned wardrobe, not facial identity or studio background.
- `ORIGINAL_UGC_REFERENCE`: existing recording style, room/environment and broad camera character, not replacement creator identity, product truth, or a compulsory pose.
- `PRODUCT_PRIMARY_REFERENCE`: manufactured product identity.
- `PRODUCT_STATE_REFERENCE`: exact supported open, closed, disassembled, use-ready, worn or other alternate configuration.
- `PRODUCT_MEASUREMENT_REFERENCE` and verified dimensions: physical-size authority.
- `PROP_REFERENCE`: exact appearance for a supplied supporting object, not an excuse to alter product identity.
- `SESSION_ENVIRONMENT_ANCHOR`: established one-room layout, decor, lighting and filming context.
- `SESSION_MASTER` / approved creator-visible image: successful session rendering and visual continuity, not a pose template or new identity authority.
- `CONFIGURATION_CALIBRATION_REFERENCE`: restricted aid for a *source-supported* recurring configuration, not source truth.
- `GENERIC_PROP_IDENTITY_ANCHOR`: consistent approved appearance of an explicitly authorized generic supporting prop; never a reference for the advertised product.

If evidence conflicts, resolve by *property*, not by averaging references. Strategy defines WHY and which visual function; original image and session anchors define WHERE/HOW; supplied product sources define WHAT; measurements define HOW BIG. A beautiful generated image never overrides verified manufactured facts.

## 2. Reference images carry identity better than redundant prose

With a good product or creator source image, let the image carry exact appearance. Use concise text to specify action, state, location, scale, and invariants that the generator might otherwise miss. Never assume attachments guarantee identity fidelity, but avoid copying long packshot descriptions that encourage redrawing. Keep the smallest sufficient set of references for each image; too many can cause identity averaging, background contamination, conflicting state or scale cues, and model overload.

## 3. Product identity lock

Preserve the supported manufactured truth: category, silhouette, component hierarchy, width-to-height proportions, cap/lid/pump/nozzle/dropper, label surface and logo location, intrinsic color, materials, finish, transparency, edges, seams and visible accessories. Do not add/remove/duplicate components, reshape the product to fill the crop, scale it to suit a convenient grip, or relocate branding independently of its physical surface. Product identity outranks aesthetic convenience.

For authorized **fictional concept products**, user-defined/project-approved canon and supplied references are the product truth for this production. The fidelity system should not turn routine image generation into a clinical-claims audit. Avoid inventing *visual* technical features, certifications, ingredients, testimonials, results or labels that aren't in the approved sources/canon. Keep any deliberate user-approved creative changes explicit rather than silently redesigning products.

## 4. Product-state lock and component inventory

Track object state and visible parts at every beat: `CLOSED`, `OPEN`, `DETACHED_COMPONENT`, `DISPENSING_READY`, `CONTENTS_VISIBLE`, `WORN`, `ASSEMBLED`, etc., using category-adaptive states. For each state, count the relevant product body and attachments, their physical relationships and which parts are in or out of frame.

Use state-specific sources for hidden mechanisms, internal geometry, threading, hinges, inner containers, scoops, applicators and contents. Avoid independently inventing a new product configuration. If a transition is too complex for one shot, show supported stable states on either side of an edit cut. A missing state reference may justify simplifying *the action* without abandoning the commercial beat.

## 5. Physical size authority

Apply the proven hierarchy:

1. verified real dimensions;
2. measurement card/reference dimensions;
3. known-object or hand-scale reference;
4. reliable human and scene anchors;
5. original product footprint or slot;
6. conservative estimation.

Higher authority overrides lower authority. Never average contradictions. When exact size is unknown, prefer a smaller physically plausible reading over inflated hero-size packaging. Optionally use one or two human comparisons (adult hand length approximately 17–20 cm, palm width 7–9 cm, face height 20–24 cm) only as aids, never superior measurements.

## 6. Measurement and Session Master firewalls

Dimensions apply to the measured **object and state**, not every piece of a disassembled product. Distinguish assembled total height, open body height, detached complete applicator length, and subcomponent lengths. Example: 7.8 cm for a *complete detached dropper* is not automatically the length of only the clear glass pipette.

When verified dimensions exist, original UGC product size, face/hand coverage, screen prominence, Session Master apparent size and generated scene footprints have **no authority to change physical product dimensions**. A camera crop, product proximity to lens, or calibrated generated appearance can affect pixel size, not real-world size.

## 7. Hands adapt to product

Reason in this order: establish physical object size → place it → assign necessary hand roles → adapt grip. Respect finger reach, thumb opposition, wrist angle, weight, gravity, occlusion and points of contact. One creator normally has two arms and two hands. If an image needs more hand roles, preserve action-critical objects and use a natural support surface or let secondary packaging leave the frame. Never invent a third hand, duplicated wrist, floating finger or impossible grip.

## 8. Contact geometry and tangible physics

Product, supporting props and people must share the same physical space. Check finger wrap, skin pressure, contact shadow, crossing/occlusion order, surface contact, realistic liquid or powder position, and no object interpenetration. Near-skin applicators need a credible gap unless contact is intended. A jar resting on a counter needs physical counter contact and appropriate shadow, not a pasted-on product. Simplify risky actions instead of writing contradictory micro-rules.

## 9. Material-light integration

Creator, product, and props must respond to the same room light. Glass reflects/refracts that room; glossy plastic has coherent specular response; matte plastic has broad highlights; metal reflects the environment; liquids have plausible transparency and flow cues; skin has natural localized sheen; fabric has believable folds, thickness and shadow. Avoid a pristine studio packshot pasted into casual UGC. Product sources control intrinsic appearance; scene light controls reflections and shading.

## 10. Scene-native shadows and realism

Maintain consistent light direction, softness, contact shadows and white balance. Avoid random dramatic rim lights or contradictory highlights in an ordinary phone-recorded room. UGC realism is photographic: believable exposure, perspective, texture, slight natural imperfection and caught-moment timing, not adding fake blemishes or changing someone's facial identity.

## 11. Creator identity and expression

Protect assigned facial structure, eye and brow relationships, nose, lips, jaw, skin tone and hairstyle across visible beats. Face source remains authoritative even if an approved Session Master has a minor identity rendering deviation. Do not invent scars, moles, asymmetry, age or identity changes to make a face "more real". Prefer credible skin texture, natural hair strands, realistic lip/eye appearance, fabric response and context-appropriate gaze.

The new default is **external VO**. Do not design every creator-visible still as a talking-head frame or require an open mouth for speech. For precision actions, action-aware gaze is usually more credible than direct eye contact. Facial expression can vary naturally; avoid exaggerated influencer posing.

## 12. Smartphone UGC camera and focus

Use the original reference or approved session to establish believable phone perspective, general camera side/height, modest handheld character, depth of field, exposure and white balance. Do not spontaneously switch to studio macro rendering, exaggerated shallow-focus cinema lenses, extreme camera orbit or HDR hyper-sharpness. Keep useful subjects readable with plausible background detail falloff. A closer crop is allowed without changing the physical recording location.

## 13. Environment anchor across visual beats [V1.1 NEW]

For a single-session ad, establish a **Session Environment Anchor** before generating the sequence. Record only visible, reasonably supportable facts:

- room identity and spatial relationships (walls, cabinets, counter, doors, appliance zone);
- material/finish families of fixed surfaces (counter, backsplash, cabinet fronts);
- persistent decor and props, with approximate fixed locations;
- light direction, daylight/room-light character, color temperature and time-of-day family;
- broad phone-camera height, side, and plausible nearby viewpoints;
- creator's likely working position relative to fixed room elements.

Preserve these relationships through wide, medium, detail, and B-roll frames. **A close-up is a tighter view of the same room, not permission to build a new room.** Objects may leave frame due to crop; fixed features should not spontaneously move or change. Do not introduce a plant, window, cabinet style, wall fixture, decorative item or appliance solely to decorate an unseen background. If a surface area is not visible in any authority, continue it conservatively, not with confident invented detail.

The anchor may start from `ORIGINAL_UGC_REFERENCE` and be refined by approved images. Do not promote a random hallucination in one generation into a required piece of the location. The calling Analyzer decides which features are protected, which uncertain, and which viewpoint variations are plausible.

## 14. Session Master does not require a talking-head first beat [V1.1 NEW]

The **first strategic beat may be product-only, hands-only, a partial-frame entrance, or a creator shot**. Do not rewrite it into a talking-head portrait just to establish a Session Master.

Separate continuity responsibilities when necessary:

- `SESSION_ENVIRONMENT_ANCHOR`: initial room truth from environment/original reference, refined by approved shots;
- `CREATOR_IDENTITY_ROOT`: permanent model face source;
- `CREATOR_SESSION_CALIBRATION`: first *approved creator-visible* image when useful for hair/wardrobe/in-session rendering;
- `PRODUCT_IDENTITY_ROOT`: original product/state/measurement sources.

When Beat 00 is not creator-visible, it may establish product-in-room/camera continuity without claiming to calibrate facial identity or wardrobe. The first later creator-visible image can calibrate that appearance. This need not add a new image or disturb the selected opening sequence. The calling Image Analyzer owns the exact names, approval gate, and set tracker.

## 15. Shot variation inside one physical session [V1.1 NEW]

Change what the shot *shows*, not the identity of its source environment. Valid variations: tighter/wider crop, reasonable distance change, front to slight nearby angle, creator+product to hands-only, shelf/counter level, visible face to action focus. Vary to reveal a new commercial or physical detail, not merely to satisfy a numeric shot-diversity rule.

For every proposed variation ask whether the camera could plausibly occupy that location in the same real room. If not, prefer a crop or another local view. A new decor item or unexplained room side is not visual variety. Preserve the selected strategist beat and its visual function; optimize only flexible framing and feasible placement.

## 16. Supporting-prop authority [V1.1 NEW]

Classify supporting objects separately from the advertised product:

- `SUPPLIED_PRODUCT_COMPONENT`: lid, scoop, dropper, cable, cap etc. visible in product sources. Preserve **exact** supported identity, geometry and count.
- `IDENTITY_CRITICAL_PROP`: branded/custom or mechanically unique external object. Its reference is necessary when precise appearance or mechanics matters.
- `GENERIC_ALLOWED_PROP`: ordinary, nonbranded shaker, drinking glass, bowl, towel etc. explicitly permitted in the strategy when no reference is supplied.
- `OPTIONAL_BACKGROUND_OBJECT`: present only if actually supported or naturally necessary; do not invent clutter.

A missing reference for a generic allowed prop **does not block** generation. Choose a plausible, neutral, unbranded design and keep its design, proportions, material, color, lid/handle details, and component count stable. Do not substitute an arbitrary branded shaker or modify the supplied product component. If the chosen concept does not require a prop, do not add it.

## 17. Generic Prop Identity Anchor and state [V1.1 NEW]

At the **first generated appearance** of an approved generic prop, establish a concise `GENERIC_PROP_IDENTITY_ANCHOR` (e.g. "plain clear unbranded shaker, gray screw lid, no printed text"). Once approved, preserve the same object across later relevant frames. Maintain a prop state ledger such as `EMPTY → POWDER_ADDED → CLOSED_FOR_SHAKING → MIXED_DRINK`, with cuts permitted between stages.

Approved generated images may act as restricted continuity references for this invented generic object's *established appearance*. They do not create real product facts or override a later user-supplied exact prop source. Don't invent new logos, markings, logos on the advertised product, accessories, or brand endorsements.

When repeated image generation causes generic prop drift, correct it with the prop anchor and suitable source/approved calibration before adding prompt volume. Limit anchors to props genuinely recurring across the ad.

## 18. Partial-frame entrances and reveal experiments [V1.1 NEW]

Do **not** automatically ban a product sliding or entering from the edge of a frame. Such a hook can be a valuable creative and technical test. A starting image may show the product partially visible when that is the planned beat; preserve physically possible contact, visible geometry and the intended motion runway.

The *full product reference remains available* to define appearance, even if the target photo shows only a part of it. However, an image-to-video system receiving only the cropped starting image might still invent the hidden portion. Mark that as a downstream generation risk, **not** an automatic reason to replace the creative idea. Do not guarantee the eventual video model can preserve unseen details; test the resulting video. Where practical, keep enough visual identity in the opening frame to improve model grounding, without silently turning an intentional entrance into a static full-product hero.

The Image Analyzer should review whether the starting state actually permits a slide and whether the frame is physically believable. The Video Analyzer will later test engine/reference-input options. Never make a Kling-model decision in this skill.

## 19. State ledger across beats [V1.1 NEW]

Track for each important product and prop:

- `state_in`: configuration before the beat;
- `intended_action`: one principal visual change;
- `state_out`: required state after the action;
- `next_beat_dependency`: what must be the same, can be hidden, or is skipped by an edit cut.

Cross-cut progression may omit an opening, closing, transfer, or cleanup action. It must not imply contradictory visible components within a single frame. No two product units or two scoops should materialize accidentally. The goal is coherent edit-ready states, not one continuous impossible mechanical performance.

## 20. Edit-ready starting frame [V1.1 EXPANDED]

An image should represent **frame one of useful motion**, not a complete action frozen after the fact. Define what is true **NOW**, what is **NOT YET** done, and what **NEXT MOTION** could plausibly happen. Examples: finger touching a real button before pressing; supported scoop already loaded near a shaker before one small pour; serum applicator near skin, ready for a single controlled action; closed product at the side of a counter with natural hand contact ready for a short slide.

Avoid requiring the video model to reach far, rotate a complex object, unscrew, retrieve, pour, react and speak within one shot. The Image Analyzer decides exact pose and camera; the Video Analyzer tests motion. Repeated static information beats can sometimes share an image or be handled as edit crops rather than forcing a new generated keyframe. Preserve the chosen commercial function.

## 21. Configuration calibration: restricted use

An approved generated image may become `PRODUCT_CONFIGURATION_CALIBRATION_REFERENCE` only when it shows a **source-supported recurring** state correctly: open bottle and complete applicator, exposed jar contents, supplied scoop, worn accessory etc. Define target and scope, for example verified relative component scale/material integration under the session lighting.

It may **not** replace the original product source, change real size, invent new internal geometry, or impose its creator pose, gaze, hand assignment, crop, room geometry or image composition on the next beat. Later scenes should normally use the session/environment root + current original product/state sources + measurements; add *restricted* configuration calibration only when it genuinely helps. Avoid a progressive Scene 00 → Scene 01 → Scene 02 chain that compounds visual errors.

Do not promote random generated fill level, texture, liquid viscosity, color or component construction into original product truth. The separate *generic prop* anchor applies only to a strategy-authorized non-product prop whose visual design is necessarily being defined during generation.

## 22. Cross-beat review gate [V1.1 EXPANDED]

Evaluate each generated still both on its own and relative to approved frames:

**Creator:** Does the face match the source identity? Is wardrobe/hair consistent when the creator reappears? Does a face-less initial beat avoid falsely claiming identity validation?

**Product:** Same manufactured product, label text/location, proportions, dimensions and state-specific component inventory? Physically plausible perspective, grip and light?

**Environment:** Same architecture, counter/backsplash, fixed objects, decor inventory, camera character and lighting family? Are apparent differences explainable by crop/viewpoint?

**Props:** Are supplied components unchanged? Do authorized generic props match their established anchor and state sequence? Any unplanned branded or extra objects?

**Motion readiness:** Does frame one leave a feasible next action? Does partial-frame entry preserve the intended reveal? Is the action simple enough or in need of a cut?

**Commercial function:** Does this frame visibly accomplish the strategic beat without being redundant? Is it usable in a fast-cut, VO-first edit?

**Economy:** Are the current sources, instructions, and generated frames sufficient without unnecessary duplicates?

Do not print this checklist in full by default; report concrete PASS/REVISE findings and only material blockers.

## 23. Failures and smallest responsible fix

Classify before rewriting:

- `SOURCE_FAILURE`: critical source, state, or unique prop evidence missing;
- `AUTHORITY_FAILURE`: conflicting references or lower-quality image overriding source truth;
- `PHYSICAL_FAILURE`: size, contact, geometry, hand roles or motion state impossible;
- `CONTINUITY_FAILURE`: changing room, creator, product state or generic prop identity across beats;
- `RENDER_FAILURE`: sensible plan but random generator defect;
- `REALISM_FAILURE`: material/lighting/camera/skin feels synthetic;
- `BEAT_TRANSLATION_FAILURE`: image misses strategist beat, prevents motion or provides no useful information.

Fix the smallest relevant layer. Reduce reference conflict, reestablish source/state/size or environment anchor, correct generic prop registry, or simplify an overcomplex action. Keep proven rules. Do not expand every prompt with generic negative instructions because one result failed.

## 24. Wardrobe and fabric realism

Body reference need not dictate wardrobe unless the strategy or user assigns it that role. When wardrobe is locked, preserve cut, straps/neckline, color and garment type. Render believable folds, weight, seam tension and compression. Do not import studio wardrobe or backdrop from an unrelated body photo by accident. Keep creator styling consistent across one session.

## 25. Screenshot and social UI firewall

Original UGC sources may be screenshots of social video with a play icon, username, caption, progress bar or other interface overlay. Reconstruct **the underlying photographic scene only**. Do not import UI chrome, captions, creator identity, or the source product unless explicitly assigned as authority. A screenshot may guide recording character and visible room layout without becoming the literal final composition.

## 26. Anti-CGI and prompt economy

Watch for waxy/plastic skin, artificial symmetry, sterile reflections, excessive background blur, unrealistically clean hands, invented perfect rim lighting, floating products, uniform hyper-sharpness and obvious compositing. Solve these with coherent photographic physics and priority, not "8K, ultra-realistic, masterpiece" keyword volume.

Only include fidelity details relevant to the current risk. The product source carries product identity, measurements carry size, face reference carries identity, environment anchor carries room, and approved strategy carries commercial function. Priority hierarchy beats prompt length.

## 27. Portability and final principle

This plain Markdown skill works with ChatGPT, Claude, Gemini, Kimi, Codex, and similar agents. It requires no GitHub access, plugin, particular image generator, paid external service or video model. When unavailable remotely, the calling Image Analyzer should use a compact embedded fallback and continue; never pretend a skill was retrieved when it wasn't.

**Final doctrine:** Preserve source truth, real dimensions, realistic contact, one coherent session, stable approved props, and action-ready first frames. A different crop is not a new kitchen. A product-only hook is not a reason to abandon identity continuity. A bold partial-frame product reveal is a testable shot, not something to prohibit prematurely. Keep the ad visually believable and practically producible without forcing extra tools or needless generations.
