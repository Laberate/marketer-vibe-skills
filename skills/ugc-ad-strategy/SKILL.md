---
name: ugc-ad-strategy
description: Lean research, angle, hook, and UGC copy strategy for product ads. Use before UGC image planning to define the ad direction, and again after final images exist to finalize the script. Designed for ChatGPT, Claude, Gemini, Kimi, Codex, and similar agents. Web research improves it but is never required.
license: Proprietary
compatibility: Plain Markdown Agent Skill. Network access is optional; continue from supplied evidence when browsing is unavailable.
metadata:
  author: MarketerVibe
  version: "1.0.0"
---
# MarketerVibe UGC Ad Strategy Skill V1.0
## Purpose
Create a strong, truthful UGC ad direction without turning the workflow into a giant marketing exercise.
This skill has two modes:
- **STRATEGY MODE**: before image creation. Decide the product angle, hook direction, story arc, and visual moments the image workflow should create.
- **EXECUTION MODE**: after final images exist. Use the approved strategy plus the actual images to finalize the hook, script, CTA, and scene-by-scene copy.
This skill does **not** generate images or video. It supplies advertising intelligence to the prompt that called it.
---
## 1. Plug-and-play rule
Infer first. Ask only for information that materially changes the ad.
Useful inputs, when available:
- product image, product URL, or product description
- goal: conversion, awareness, launch, demo, organic-style promotion, lead generation
- platform: TikTok, Reels, Shorts, Meta, or AUTO
- audience
- offer / CTA
- brand voice
- existing script
- reviews, comments, winning ads, or performance data
If some are missing, continue with clearly labeled assumptions unless the missing fact would force an unsupported claim.
Never block the workflow merely because live research is unavailable.
---
## 2. Research mode
Default:
`RESEARCH_MODE = AUTO`
Use live research when the environment supports it and when research is likely to improve the decision.
### Exact commercial product
Research in this order when practical:
1. official product / brand source
2. supplied brand materials
3. real customer reviews / comments
4. the brand's own winning creative or performance data, if supplied
5. competitor/category ads and long-running patterns
6. high-performing organic category content and customer vocabulary
7. general copywriting frameworks
### Generic, fictional, white-label, or concept product
Research the **category and audience**, not invented facts about the exact product.
Never pretend a fictional or unverified product has reviews, ingredients, performance results, certifications, awards, or customer history.
### Research depth
Do only enough research to improve the next creative decision.
Do not turn a simple 15-second ad into a long research report.
---
## 3. Evidence hierarchy
When signals disagree, prefer stronger evidence:
1. verified facts supplied by the user
2. official product / brand source
3. the brand's own performance data
4. recurring real customer language from reviews, comments, support, or sales calls
5. competitor creative with meaningful longevity / repeated use
6. strong organic category patterns
7. cross-category patterns
8. generic frameworks and model knowledge
A framework never overrides product truth.
---
## 4. Truth firewall
Separate all useful information into three buckets:
### VERIFIED_PRODUCT_FACT
A claim supported by the user, official product source, packaging, verified offer information, or supplied evidence.
May be used as factual ad copy.
### CATEGORY_INSIGHT
A problem, desire, objection, behavior, vocabulary pattern, or buying motivation found in the broader category.
May guide the angle and wording.
It does **not** become a factual claim about the exact product unless verified.
### CREATIVE_PATTERN
A hook, format, pacing pattern, visual convention, or ad structure observed in ads or organic content.
May inspire execution.
Do not copy another creator's exact script, concept expression, or protected creative.
### Never invent
- testimonials
- statistics
- clinical results
- performance numbers
- awards
- scarcity
- discounts
- ingredients
- personal usage history
- before/after outcomes
- popularity claims
If proof is absent, write a concept that does not require proof.
---
## 5. Product and buyer diagnosis
Before generating angles, internally establish:
- product category
- what the product physically does / how it is used
- primary buyer or likely buyer segment
- main job-to-be-done
- strongest likely pain, desire, or objection
- awareness stage
- goal of the ad
- offer / CTA if known
- what evidence is actually available
Use awareness stages only as a decision aid:
- UNAWARE
- PROBLEM_AWARE
- SOLUTION_AWARE
- PRODUCT_AWARE
- MOST_AWARE
If awareness is unknown, choose the most plausible stage for the stated placement and mark it as an assumption internally.
---
## 6. Angle generation
Generate multiple **genuinely different** candidate angles before selecting one.
Useful angle families include:
- PAIN / FRUSTRATION
- DESIRE / OUTCOME
- CURIOSITY
- PRODUCT DEMONSTRATION
- PROOF
- COMPARISON
- OBJECTION
- UNIQUE MECHANISM
- DISCOVERY / RECOMMENDATION
- ROUTINE / USE CASE
- IDENTITY
- CONTRARIAN / REFRAME
Do not force every ad through pain-agitate-solution.
A visually demonstrable product may deserve a demonstration-first ad.
A warm audience may need proof or an objection answered rather than another problem hook.
One ad should have one dominant strategic idea.
---
## 7. Concept scoring
Score candidate directions internally on:
- **truth**: can the message be supported?
- **audience fit**: does it match what this audience cares about now?
- **hook strength**: is there a reason to keep watching?
- **visual fit**: can the available or planned UGC scenes actually show it?
- **UGC authenticity**: would a real creator plausibly say/do it?
- **simplicity**: can one short ad communicate it clearly?
- **production risk**: can the AI image/video workflow execute it reliably?
Choose the strongest truthful concept that the visual workflow can actually execute.
Do not choose a theoretically stronger angle that requires scenes, claims, or proof the workflow does not have.
---
## 8. Hook system
A video hook is not just a sentence.
Plan up to three components:
- **VISUAL HOOK**: what happens on screen in the opening 1-3 seconds
- **SPOKEN HOOK**: first dialogue / VO line
- **TEXT HOOK**: optional on-screen text when the workflow will actually use text
The components should complement rather than duplicate each other.
Useful visual hook families include:
- cold start in the middle of an action
- tactile product behavior: nail taps, click, snap, twist, squeeze, shake when physically appropriate
- product reveal / lift
- close product inspection
- immediate demo
- creator reaction
- specific POV situation
- comparison setup
- proof shown first, when verified proof exists
Do not add motion merely because it is trendy. It must be physically compatible with the starting frame and product.
Useful spoken-hook families include:
- curiosity gap
- specific question
- relatable problem
- first-person discovery
- objection
- contrast
- surprising but supportable fact
- direct demonstration setup
- specific POV
Avoid generic openings such as:
- "Hey guys"
- "I want to show you this product"
- "You won't believe this"
- "This is a game changer"
- "Stop scrolling"
unless the surrounding context makes the wording genuinely specific and natural.
---
## 9. Customer language
When real customer language is available, prefer it over polished marketing paraphrase.
Mine for:
- exact problem descriptions
- desired outcomes
- objections
- comparison language
- surprising use cases
- words buyers repeatedly use for the category
Do not fabricate quotations.
Do not over-polish UGC dialogue. Slightly imperfect spoken phrasing can be more believable than copywriter-perfect sentences.
---
## 10. UGC authenticity filter
Before accepting a line, ask:
**Would a real person plausibly say this aloud to their phone?**
Rewrite if it sounds like:
- a landing page
- a corporate brand statement
- generic AI copy
- a feature list
- a fake testimonial
- an announcer
Prefer short spoken sentences, contractions, natural rhythm, and specific language.
Do not force slang, Gen-Z wording, filler words, or fake enthusiasm that do not fit the creator and audience.
---
## 11. AI-copy avoidance
Avoid recurring AI-ad tells:
- "It's not X, it's Y" as a generic reveal
- repetitive "No X. No Y. No Z." stacks
- generic "POV:" without a specific situation
- generic "Here's the thing"
- "unlock", "unleash", "revolutionary", "game-changing" without evidence
- over-explaining what the viewer can already see
- every sentence having the same rhythm
- narrating literal actions instead of adding persuasive meaning
Use concrete details and natural speech instead.
---
## 12. Script architecture
Choose the structure that fits the concept rather than forcing one universal framework.
Common short UGC arcs:
### DEMO ARC
HOOK -> DEMO -> USE -> CTA
### DISCOVERY ARC
HOOK -> RELATABLE CONTEXT -> PRODUCT DISCOVERY -> DEMO / RESULT -> CTA
### PROBLEM ARC
HOOK -> SPECIFIC PROBLEM -> PRODUCT / SOLUTION -> DEMO -> CTA
### OBJECTION ARC
HOOK / OBJECTION -> QUICK ANSWER -> PROOF / DEMO -> CTA
### COMPARISON ARC
HOOK -> A VS B -> DIFFERENCE -> DECISION -> CTA
### ROUTINE ARC
HOOK -> MOMENT / ROUTINE -> PRODUCT USE -> WHY IT FITS -> CTA
Do not fill every slot when the ad does not need it.
Short ads should feel compressed, not incomplete.
---
## 13. One message, one CTA
Each ad should have one dominant message and one clear next action.
CTA must match the actual offer and platform.
Do not invent urgency.
For brand/demo ads where no hard offer exists, a soft CTA is valid.
---
## 14. Strategy mode output
When called before image generation, do **not** finalize the whole spoken script unless the calling prompt explicitly asks.
Produce 2-3 clearly different directions, then recommend one.
The selected direction should become a compact handoff containing only what the Image Analyzer needs:
```json
{
  "handoff_type": "UGC_CREATIVE_STRATEGY",
  "skill_version": "MARKETERVIBE_UGC_AD_STRATEGY_V1_0",
  "product": {
    "name": "[name if known]",
    "category": "[category]"
  },
  "goal": "[goal]",
  "platform": "[platform or SHORT_FORM_SOCIAL]",
  "audience": "[concise audience]",
  "awareness": "[stage]",
  "primary_angle": "[angle]",
  "hook_direction": {
    "spoken": "[direction, not necessarily final line]",
    "visual": "[visual opening behavior]"
  },
  "story_arc": ["HOOK", "DEMO", "USE", "CTA"],
  "required_visual_moments": [
    "[moment]",
    "[moment]"
  ],
  "verified_product_facts": [
    "[only facts safe to claim]"
  ],
  "claim_guardrails": [
    "[unsupported things not to claim]"
  ],
  "script_status": "FINALIZE_AFTER_IMAGES"
}
```
Keep this handoff lean.
---
## 15. Execution mode output
When called after final images exist:
1. re-read the approved creative strategy
2. inspect what the final images can actually support
3. preserve the chosen angle unless the images make it unworkable
4. generate several hook candidates internally
5. select the strongest visual + spoken combination
6. write the full natural UGC script
7. distribute dialogue across the actual scenes
8. avoid claims the evidence cannot support
9. let the Video Analyzer decide exact motion, timing, direct speech vs VO, and engine syntax
The exact script should add meaning rather than merely narrate the image.
---
## 16. Testing mindset
Treat untested creative principles as hypotheses, not laws.
When performance data exists:
- preserve what is working
- identify whether the failure is hook, hold, click, or conversion
- test one meaningful variable at a time where practical
- generate new angles as well as iterations
Do not assume the most polished concept is the best concept.
---
## 17. Platform portability
This skill must work even when GitHub, plugins, or web search are unavailable.
If live research is unavailable:
- use supplied product truth
- use supplied customer data
- use this skill's strategy system
- label uncertain assumptions internally
- continue
Do not claim research was performed when it was not.
---
## 18. Final principle
**Research informs the ad. Product truth limits the claims. Audience awareness shapes the message. The available visuals constrain the execution. UGC authenticity shapes the language.**
Choose the strongest truthful concept the production workflow can actually deliver.
---
## Research basis and inspiration
This skill is an original MarketerVibe synthesis informed by public agent-skill patterns and advertising methodology, including:
- coreyhaines31/marketingskills: grounded inputs, creative strategy loop, hook components, customer-language grounding, awareness and creative-testing concepts. MIT.
- whatsuppiyush/ad-maker-claude-skill: angle x awareness thinking and diversified hook families. MIT.
- SupercmoHQ/superCMO-skills: product-first campaign planning, competitor-ad research, separate planning/production responsibilities. Apache-2.0.
- alirezarezvani/claude-skills: portable multi-agent skill design and marketing skill structure. MIT.
No external skill is copied wholesale. MarketerVibe-specific workflow, handoff structure, truth firewall, image-executability scoring, and two-mode strategy/execution architecture are original to this skill.
