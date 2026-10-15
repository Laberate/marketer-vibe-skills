---
name: image-fidelity
description: Lean image-fidelity specialist for photorealistic UGC and product-in-hand generation. Improves product identity, physical scale, materials, human realism, lighting integration, anatomy, contact geometry, and reference discipline without replacing the calling Image Analyzer's workflow.
license: Proprietary
compatibility: Plain Markdown Agent Skill. No image API, GitHub access, or external tool is required; it augments the calling image-planning prompt.
metadata:
  author: MarketerVibe
  version: "1.0.0"
---
# MarketerVibe Image Fidelity Skill V1.0
## Purpose
Improve the physical and photographic credibility of AI UGC images while keeping the main Image Analyzer lean.
This skill is a **specialist layer**, not a standalone workflow.
It does not choose the advertising angle, scene sequence, or video script.
It strengthens:
- creator realism
- product fidelity
- physical product scale
- material behavior
- hand / object interaction
- camera realism
- scene-native lighting
- environment integration
- final quality control
---
## 1. Do not replace the calling prompt
The calling Image Analyzer owns:
- workflow state
- scene IDs
- source authority
- Session Master logic
- scene diversity
- creative strategy handoff
- response format
This skill only improves image fidelity decisions.
If a rule conflicts with the calling analyzer's explicit authority system, the calling analyzer wins unless this skill is protecting physical impossibility or product truth.
---
## 2. Reference-role discipline
Every supplied image should have one clear role.
Examples:
- creator identity
- body reference
- Session Master / environment
- product identity
- product state
- physical measurements
- prop identity
Do not let a reference silently control unrelated properties.
Do not average conflicting references.
When multiple references are used, label their roles explicitly.
A product packshot should not import its studio lighting into a UGC room.
A model reference should not import its studio background or wardrobe unless assigned that authority.
---
## 3. Reference images carry identity better than prose
When a strong product reference is attached:
- let the image carry exact product appearance
- use text primarily for state, placement, action, orientation, scale, and what must remain invariant
- do not redundantly rewrite every visual detail when that increases the chance the model redraws the product instead of preserving it
Text should fill gaps the reference cannot communicate reliably.
Do not assume merely attaching a reference guarantees fidelity. State the important invariants explicitly.
---
## 4. Product identity lock
Preserve supported manufactured truth:
- silhouette
- proportions
- width-to-height relationship
- component hierarchy
- closure / cap / pump / dropper / nozzle
- label surface placement
- logo location
- color blocking
- intrinsic colors
- materials
- transparency / translucency
- finish
- seams / edges / molded geometry
- visible accessories
Do not:
- add components
- remove components
- duplicate components
- reshape the product to suit the composition
- detach parts unsupported by a state reference
- rotate labels independently of the physical surface
- enlarge branding by physically distorting the package
Product identity outranks aesthetic convenience.
---
## 5. Product-state lock
Treat each supported product state as a real physical configuration.
Examples:
- CLOSED
- OPEN
- OPEN_WITH_DETACHED_COMPONENT
- APPLICATION_READY
- CONTENTS_TRANSFERRED
Use state references for hidden or alternate geometry whenever practical.
Do not invent internal mechanics, underside geometry, threading, seals, hinges, applicators, scoops, or contents merely because a scene would benefit from them.
When state evidence is weak, simplify the scene or bridge states with an edit cut.
---
## 6. Physical size authority
Use this hierarchy:
1. verified real dimensions
2. measurement-card / measurement-reference dimensions
3. known-object or hand-scale reference
4. reliable human / scene anchors
5. original slot / previous visual footprint
6. conservative estimate
Higher authority overrides lower authority.
Never average contradictory scale evidence.
---
## 7. Measurement firewall
When reliable real measurements exist:
lower-authority images have **zero physical-size authority**.
This includes:
- original UGC product footprint
- Session Master product footprint
- earlier generated scenes
- hand span in a reference pose
- face coverage
- screen prominence
Those sources may still control interaction intent and placement.
They may not resize the product against verified dimensions.
---
## 8. State-specific measurement scope
Measurements belong only to the exact object/state they describe.
Example:
- assembled bottle total height
- open bottle-body height
- detached complete dropper assembly length
Do not apply assembled dimensions to a separated component.
Clarify scope when ambiguity could cause stretching.
Example:
"7.8 cm is the complete dropper assembly from bulb top to pipette tip, not the glass pipette alone."
---
## 9. Use only a few scale cues
If exact measurements are available, optionally derive one or two simple visual anchors from the current scene.
Examples:
- clearly shorter than the visible hand
- roughly half the visible face height
- noticeably narrower than the palm
These are rendering aids, not new authorities.
Do not flood the prompt with many conflicting size analogies.
When uncertain, choose the smaller physically plausible interpretation rather than hero-scale inflation.
---
## 10. Hand adapts to product
Always reason in this order:
1. establish physical product size
2. place the product
3. adapt hand and finger geometry to it
Never preserve a convenient hand pose by resizing the product.
Grip should respect:
- object diameter / thickness
- finger reach
- thumb opposition
- gravity
- contact points
- wrist angle
---
## 11. Human feasibility
One visible creator normally has:
- two arms
- two hands
Assign hand roles before generation when interaction matters.
If a concept needs more hand roles than anatomy allows:
- preserve the action-critical object
- preserve the action target
- remove secondary packaging from frame
- use an already-established support surface only when natural
Never solve the scene by inventing a third hand, duplicated wrist, floating fingers, or impossible multi-role grip.
---
## 12. Contact geometry
Objects should look physically held, worn, touched, or placed rather than pasted into the frame.
Check:
- finger wrap and pressure
- contact shadow
- occlusion order
- product edge crossing the hand correctly
- no floating gap where contact should exist
- no product sinking through fingers or skin
- no impossible penetration
For application tools near skin, preserve a believable small gap unless contact is intentionally required.
---
## 13. Material-light integration
The product and creator exist under the same scene lighting.
Do not describe material and lighting as unrelated facts.
Ask how the established scene light affects each important material:
- glass: reflections, edge highlights, transparency, refraction
- glossy plastic: controlled specular highlights
- matte plastic: broader soft reflections
- metal: scene-colored highlights and darker reflected environment
- liquid: plausible transparency / viscosity cues
- skin: regional texture and nonuniform highlights
- fabric: folds, fiber response, shadow in creases
A product should not look like a separately lit packshot pasted into a UGC frame.
Scene light controls reflected appearance. Product identity controls intrinsic material/color.
---
## 14. Scene-native shadows
Use physically coherent shadows:
- correct direction relative to the light source
- plausible softness for source size / distance
- contact shadows where objects meet hands or surfaces
- no floating product
- no multiple contradictory key-light directions
Do not add dramatic rim light or studio highlights if the Session Master does not support them.
---
## 15. Creator photorealism
Realism should come from photography and physical texture, not by changing the person's identity.
Preserve the creator reference.
Do not deliberately invent:
- facial asymmetry
- moles
- blemishes
- scars
- age changes
- ethnic-feature changes
unless actually supported by the reference.
Instead create realism through:
- natural skin texture
- regional variation in pores / sheen
- believable sclera and eye moisture
- natural lips
- hair strands and flyaways where appropriate
- fabric texture and pose-driven creases
- physically motivated light falloff
- caught-moment expression
Avoid waxy, porcelain, airbrushed, beauty-filter skin unless the reference clearly has that aesthetic.
---
## 16. Caught-moment expression
For UGC, prefer a frame that feels captured during real behavior rather than a posed beauty portrait.
Examples:
- just beginning to speak
- glancing from product back to camera
- concentrating on an applicator
- soft smile beginning
- small eyebrow reaction
Eyes, brows, mouth, and head position should agree emotionally.
Do not add random facial imperfections to force realism.
---
## 17. Smartphone UGC camera realism
The Session Master or original reference controls camera character.
For ordinary UGC:
- preserve believable phone-camera perspective
- preserve camera side and broad height
- allow modest perspective distortion expected from a phone held at conversational distance
- avoid unexplained DSLR beauty compression
- avoid cinematic depth-of-field or dramatic lens language unless established
- keep exposure and white balance plausible for the room
The goal is a believable phone capture, not a studio campaign photograph disguised as UGC.
---
## 18. Focus and detail falloff
Real images do not have every surface equally sharp.
Preserve plausible focus hierarchy:
- key face/product detail can be sharp
- nearby secondary detail slightly softer
- background progressively less detailed when the reference supports it
Avoid uniform hyper-sharpness and artificial HDR microcontrast.
Do not force shallow bokeh when the Session Master looks like a typical smartphone frame with broad depth of field.
---
## 19. Environment integration
The room is a rigid physical place.
Preserve known:
- cabinet lines
- wall boundaries
- counters / tables
- door geometry
- background object locations
- perspective direction
For unseen areas, continue existing architecture conservatively.
Do not invent decor merely to balance composition.
The creator adapts to the room. The room does not redesign itself around the creator.
---
## 20. Fabric and wardrobe realism
Preserve wardrobe identity from the proper authority.
Fabric should show believable:
- gravity
- drape
- compression
- folds at elbows / waist / shoulder
- thickness
- seam tension
Avoid perfectly smooth clothing that looks digitally painted onto the body.
Do not change garment cut, neckline, straps, color, or material merely to improve aesthetics.
---
## 21. Anti-CGI rule
Avoid the common "AI commercial render" look when the target is casual UGC.
Watch for:
- plastic skin
- perfect bilateral symmetry
- uniform highlights
- unrealistically clean hands
- sterile product reflections
- oversaturated color grade
- fake rim lighting
- excessive background blur
- repeated texture
- over-sharpening
- product floating or visually pasted into hand
Fix through better physical description, not piles of generic quality words such as "8K", "ultra-detailed", or "masterpiece".
---
## 22. Prompt economy
Do not turn every image prompt into a photography textbook.
Include only fidelity instructions that solve a real risk in the current scene.
References carry visual facts.
Measurements carry scale.
The Session Master carries the session.
The current JSON carries the current pose/action/composition.
This skill adds only the missing physical realism.
Priority hierarchy beats keyword volume.
---
## 23. Fidelity QA gate
Before the calling Image Analyzer outputs a generation JSON, internally check only these questions:
### CREATOR
- Does the identity still come from the correct reference?
- Does the face read as a real captured person rather than a beauty-render template?
### PRODUCT
- Is manufactured geometry preserved?
- Is the product in the correct physical state?
- Are component count and label placement stable?
### SCALE
- Is the highest available size authority being used?
- Is any lower-authority image accidentally overriding it?
### HANDS / CONTACT
- Can the action be performed with the visible anatomy?
- Does the grip/contact geometry make physical sense?
### LIGHT / MATERIAL
- Does the product respond to the same room light as the creator?
- Are reflections, transparency, shadows, and finish plausible?
### CAMERA / ROOM
- Does perspective match the UGC session?
- Does architecture remain rigid and coherent?
### PROMPT ECONOMY
- Is every included instruction necessary?
- Is anything being redescribed that the reference already carries better?
If all are acceptable, proceed.
Do not output this entire checklist to the user unless diagnosing a failure.
---
## 24. Failure diagnosis
When a result fails, identify the layer before adding rules:
- **SOURCE FAILURE**: reference or state evidence is insufficient
- **AUTHORITY FAILURE**: two sources were allowed to compete
- **PHYSICAL FAILURE**: scale, anatomy, state, or contact plan is impossible / unclear
- **RENDER FAILURE**: the plan was valid but the model produced a stochastic defect
- **REALISM FAILURE**: materials, lighting, camera, or skin feel synthetic
Change the smallest responsible layer.
Do not expand the entire skill because of one random render failure.
---
## 25. Platform portability
This skill works as plain text.
It must not require:
- GitHub access
- an MCP server
- a specific image API
- a specific generator
- a paid external tool
If external skill retrieval is unavailable, the calling prompt's fallback core plus its own authority system should continue the workflow.
---
## 26. Final principle
**Photorealism is not more adjectives. It is correct authority, correct physics, correct scale, correct contact, and scene-native photography.**
Preserve the creator. Preserve the product. Respect measurements. Make the interaction physically possible. Let the reference do the work it is best at.
---
## Research basis and inspiration
This skill is an original MarketerVibe synthesis informed by public image-generation methodologies, including:
- OpenAI `imagegen` skill: explicit reference roles, prompt structure, edit/generation discipline, and reference-aware prompting.
- SupercmoHQ `generating-product-photos`: product-first analysis, invariant product identity, minimal re-description when a reference image is supplied, and scene-specific photographic craft.
- hlyboki-sensy `photosession`: material-light coupling and self-check thinking. MIT.
- cheney-yan `photorealistic-skill`: caught-moment realism, natural skin/light/focus cues, with identity-altering imperfection rules intentionally excluded. Public repository; principles synthesized, not copied.
- beatra-ai ecommerce/product-image skills: confirmed SKU facts, scale/fit facts, and fidelity-first product workflows.
MarketerVibe's measurement firewall, state-specific size authority, hand-adapts-to-product doctrine, human-feasibility rules, Session Master scale firewall, and UGC-specific authority architecture are original MarketerVibe methodology.
