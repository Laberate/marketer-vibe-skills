---
name: ugc-ad-strategy
description: Persuasive UGC advertising strategy, research, positioning, hooks, and copy for real and concept products. Use before image planning to define the commercial direction and after final images exist to finalize the script. Designed for ChatGPT, Claude, Gemini, Kimi, Codex, and similar agents.
license: Proprietary
compatibility: Plain Markdown Agent Skill. Network access is optional; continue from supplied evidence when browsing is unavailable.
metadata:
  author: MarketerVibe
  version: "1.2.0"
---

# MarketerVibe UGC Ad Strategy Skill V1.2

# 1. Purpose

Create short-form UGC advertising that is:

- persuasive
- commercially useful
- natural
- specific
- visually executable
- reasonably grounded
- capable of actually selling

This skill has two modes:

## STRATEGY MODE

Used before image creation.

Decide:

- buyer motivation
- product positioning
- purchase driver
- commercial thesis
- angle
- hook direction
- story arc
- visual requirements
- CTA direction

## EXECUTION MODE

Used after final UGC images exist.

Finalize:

- spoken hook
- script
- persuasive sequence
- CTA
- audio distribution
- copy that fits the actual images

This skill does **not** generate images or video.

# 2. Core advertising doctrine

A strong ad needs three things:

RELEVANCE
+
REASON TO CARE
+
REASON TO ACT

Truthfulness matters.

But do NOT turn advertising into legal-review copy.

The objective is not:

"Only say things that can be proven in a laboratory."

The objective is:

"Do not invent concrete facts that are materially false."

Normal persuasive advertising may still use:

- emotion
- curiosity
- desire
- relatable frustrations
- subjective language
- creator opinion
- category context
- lifestyle framing
- aspirational language
- reasonable commercial positioning
- non-absolute benefit language
- conversational persuasion

Do not flatten good copy merely because every sentence is not independently verifiable.

# 3. Hard claims vs persuasive framing

Distinguish between:

## HARD FACTUAL CLAIM

Examples:

- "Reduces wrinkles by 43%."
- "Contains 10% vitamin C."
- "Dermatologist approved."
- "Clinically proven."
- "Used by 100,000 customers."
- "Works in 3 days."
- "50% off today."
- "Won Product of the Year."

These require real support.

## NORMAL COMMERCIAL FRAMING

Examples:

- "If dark spots are what bother you most..."
- "This is the kind of serum I'd look at for a simple routine."
- "If you're after brighter-looking skin..."
- "This feels like an easy product to work into a routine."
- "Worth a look if this is the problem you're trying to solve."
- "This is much more my kind of skincare setup."
- "The whole thing feels simple and straightforward."

These do NOT need clinical proof merely because they are persuasive.

## SUBJECTIVE / CREATOR LANGUAGE

Examples:

- "I like how simple this looks."
- "This packaging is really clean."
- "This is the kind of format I prefer."
- "I actually like how compact this is."

Subjective impressions are allowed when they refer to what the creator can reasonably observe in the current content.

Do not require documentary evidence for ordinary opinions.

# 4. Commercial latitude

Do not sterilize the ad.

The copy may confidently:

- frame a common problem
- intensify a relatable frustration
- appeal to a desired outcome
- describe who a product seems relevant for
- use emotional contrast
- create curiosity
- create product desire
- highlight appealing design or experience
- position the product within a routine
- use persuasive comparisons at a conceptual level
- encourage purchase consideration

Avoid unnecessary qualifiers such as:

- "may potentially"
- "could possibly"
- "according to the supplied reference"
- "if technically supported"
- "based on available evidence"

inside consumer-facing copy.

Those distinctions belong in internal reasoning.

The final UGC script should sound like advertising, not compliance documentation.

# 5. Do not fabricate material facts

Still do not invent concrete claims such as:

- fake statistics
- fake clinical studies
- fake ingredients
- fake certifications
- fake awards
- fake reviews
- fake testimonials
- fake discounts
- fake scarcity
- fake customer counts
- fake exact product results
- fake endorsements
- fake before-and-after outcomes

These are materially different from ordinary persuasive language.

# 6. Product reality status

Determine internally:

PRODUCT_REALITY_STATUS

Possible values:

REAL_PRODUCT

CONCEPT_PRODUCT

UNKNOWN

# 7. Real products

For a confidently identified real commercial product:

use real product information when available.

Useful sources:

1. official product page
2. brand website
3. packaging
4. supplied product material
5. real customer language
6. reviews
7. category research
8. competitor/category creative

Do NOT invent hard product facts merely because information is missing.

But do not become unnecessarily timid either.

You may still use:

- category pain points
- audience desires
- reasonable buyer framing
- emotional hooks
- non-technical product positioning
- observable product experience
- normal subjective creator language

# 8. Unknown products

If it is unclear whether the product is real or fictional:

do not silently create detailed technical claims.

Use:

- visible product facts
- category context
- broad commercial framing

and clarify only when the distinction materially matters.

# 9. Concept Product Mode

Some products are intentionally fictional.

Examples:

- MarketerVibe course products
- prototype brands
- creative mockups
- unreleased concepts
- portfolio products
- fictional ecommerce brands

These products may have no:

- real website
- reviews
- ingredients
- official benefits
- positioning
- customer history

Do not treat this as a failure.

# 10. Concept positioning authorization

Concept-product positioning may be created when the user explicitly or implicitly authorizes it.

Examples:

- Product status: CONCEPT_PRODUCT
- Positioning: AUTO
- This product is fictional
- Create the positioning
- This is for a course/demo
- Invent a plausible product proposition

Then:

CONCEPT_PRODUCT_MODE = AUTHORIZED

# 11. Concept Product Spec

When concept positioning is authorized:

create a:

CONCEPT_PRODUCT_SPEC

This becomes the product's project canon.

It may define:

- product category
- primary buyer
- primary problem
- primary desired outcome
- primary benefit
- secondary benefit
- product experience
- meaningful feature
- positioning
- differentiator
- routine fit
- broad mechanism
- price/value positioning if useful
- tone
- claim boundaries

Keep it commercially plausible and simple.

Do not overload a fictional product with ten benefits.

# 12. Concept product truth

A CONCEPT_PRODUCT_SPEC is:

PROJECT-DEFINED PRODUCT TRUTH

It is not:

- researched product fact
- manufacturer evidence
- clinical evidence
- customer evidence

Once defined, however, it may legitimately be used by:

Strategist
→ Image Analyzer
→ Video Analyzer

because it defines what the fictional product is intended to be.

# 13. Concept-product examples

A fictional serum could be defined as:

Product:
Vibe.

Positioning:
Lightweight everyday hydration serum.

Buyer:
People whose skin often feels dehydrated or tight.

Primary benefit:
Supports hydrated, fresher-looking skin.

Experience:
Lightweight everyday serum for a simple routine.

Commercial angle:
Simple hydration without making skincare feel complicated.

That becomes valid project positioning.

Do not repeatedly apologize that the product is fictional.

# 14. Category research for concept products

When:

CONCEPT_PRODUCT
+
Positioning = AUTO

use category research to help design commercially useful positioning.

Process:

CATEGORY DEMAND

→

BUYER PAINS / DESIRES

→

POSITIONING OPPORTUNITIES

→

SELECT ONE PRODUCT ROLE

→

CREATE CONCEPT_PRODUCT_SPEC

Category research informs the fictional positioning.

It does not become fake third-party evidence for the fictional product.

# 15. Concept-positioning selection

When Positioning = AUTO:

internally consider several plausible positioning foundations.

Evaluate:

- buyer relevance
- category demand
- sales potential
- hook potential
- visual compatibility
- differentiation opportunity
- simplicity
- suitability for available product images

Then choose ONE recommended positioning.

Do not create another questionnaire unless user preference genuinely matters.

# 16. Evidence classes

Use four useful information types:

## VERIFIED_PRODUCT_FACT

Real supported product information.

## CONCEPT_PRODUCT_SPEC

User-authorized fictional product positioning.

## CATEGORY_INSIGHT

Broader market/customer information.

## CREATIVE_PATTERN

Advertising execution pattern.

These serve different purposes.

# 17. Commercial inference

You may also use:

COMMERCIAL_INFERENCE

This is reasonable non-factual interpretation based on:

- product category
- design
- use context
- buyer behavior
- visible product experience

Examples:

"This feels positioned as a simple everyday serum."

"The compact format makes it easy to present as routine-friendly."

"This product visually lends itself to a minimalist skincare angle."

Commercial inference may guide creative strategy.

Do not convert it into a hard technical product claim.

# 18. Buyer diagnosis

Before selecting an angle determine:

- primary buyer
- awareness stage
- main desire
- main frustration
- main objection
- job-to-be-done
- emotional driver
- product relevance
- likely purchase driver
- available reasons to believe
- visual opportunities

Awareness:

UNAWARE

PROBLEM_AWARE

SOLUTION_AWARE

PRODUCT_AWARE

MOST_AWARE

# 19. Persuasion inventory

Possible purchase-driver families:

BENEFIT / OUTCOME

PROBLEM SOLUTION

MEANINGFUL FEATURE

UNIQUE MECHANISM

DIFFERENTIATOR

PROOF

CONVENIENCE

EXPERIENCE / SENSORY

DESIGN / AESTHETIC DESIRE

IDENTITY / LIFESTYLE FIT

ROUTINE FIT

VALUE

OFFER

OBJECTION REMOVAL

Not every ad needs proof-heavy persuasion.

Different categories sell for different reasons.

# 20. Conversion argument

When GOAL = CONVERSION:

the ad needs a meaningful reason to care.

Ask internally:

1. What does the buyer want?
2. What bothers them?
3. Why is this product relevant?
4. What makes the product worth considering?
5. What should make the viewer more likely to act?

Do not approve a concept merely because it is easy to generate visually.

# 21. Conversion status

Use internally:

PERSUASION_STATUS

Possible values:

READY

LIMITED

INSUFFICIENT

## READY

A useful commercial argument exists.

## LIMITED

The argument is somewhat generic but still usable.

Do NOT automatically stop.

Instead create the strongest commercially sensible version available.

## INSUFFICIENT

No meaningful purchase argument exists and one cannot reasonably be established.

For REAL_PRODUCT:

research further or ask for the minimum missing information.

For CONCEPT_PRODUCT + AUTHORIZED:

create or strengthen the CONCEPT_PRODUCT_SPEC.

Only stop when there is genuinely no reasonable route forward.

# 22. Do not over-trigger insufficiency

This is important.

Do NOT mark:

INSUFFICIENT

merely because the product lacks:

- clinical proof
- reviews
- statistics
- unusual ingredients
- a patented mechanism

Many products sell through:

- desire
- design
- convenience
- identity
- routine fit
- emotion
- aesthetics
- simplicity
- experience
- positioning

Use the strongest legitimate commercial argument available.

# 23. Feature-to-buyer-consequence test

Whenever a feature becomes part of the sales argument ask:

SO WHAT?

Use:

FEATURE

→

BUYER CONSEQUENCE

→

WHY IT MATTERS

If no useful buyer consequence exists:

do not make that feature the central ad argument.

# 24. Ordinary component rule

Ordinary components may appear visually.

They should not automatically become the reason to buy.

Examples:

- regular cap
- ordinary dropper
- standard zipper
- common pump
- normal lid
- ordinary scoop

They become commercially important only when their use creates meaningful value.

# 25. Visual support vs selling argument

A visual element may be useful even when it is not persuasive by itself.

Example:

Dropper demonstration

may provide:

- product tangibility
- motion
- authenticity
- visual variety

while the AUDIO sells:

- hydration
- dark-spot positioning
- convenience
- routine fit
- desired outcome

Do not require the visuals to carry the entire sales argument.

# 26. Buyer-care test

Every major ad beat should pass:

WHY WOULD THE BUYER CARE?

Good answers include:

- relevant problem
- desired outcome
- emotional tension
- useful information
- product relevance
- objection removal
- meaningful differentiation
- aspiration
- identity
- convenience

Weak answer:

"Because this part of the product exists."

# 27. Curiosity quality

Curiosity should ideally connect to something meaningful.

Strong curiosity:

- unresolved problem
- desired result
- surprising product relevance
- objection
- mechanism
- useful difference
- experience
- buyer tension

Weak curiosity:

ordinary product trivia.

Do not confuse information gaps with purchase motivation.

# 28. Commercial thesis

Reduce the ad internally to:

"This viewer should consider this product because ______."

If the sentence is compelling enough:

strategy is probably viable.

If the blank contains:

"because the dropper is visible"

strategy is probably weak.

# 29. Reason to believe

A reason to believe strengthens the ad.

Possible forms:

- verified product claim
- visible demonstration
- product experience
- meaningful design
- ingredient/mechanism
- customer proof
- offer
- comparison
- concept-product positioning
- routine fit

Not every ad requires clinical evidence.

Do not turn "reason to believe" into a requirement for scientific proof.

# 30. Angle generation

Generate several genuinely different angles.

Possible families:

PAIN / FRUSTRATION

DESIRE / OUTCOME

CURIOSITY

PRODUCT DEMONSTRATION

DISCOVERY

ROUTINE / USE CASE

OBJECTION

PROOF

COMPARISON

UNIQUE MECHANISM

IDENTITY

CONTRARIAN

CONVENIENCE

EXPERIENCE

AESTHETIC

VALUE

EDUCATION

One ad should have one dominant commercial idea.

# 31. Concept scoring

Evaluate internally:

TRUTH / PLAUSIBILITY

BUYER CARE

PURCHASE DRIVER

COMMERCIAL STRENGTH

HOOK STRENGTH

AUDIENCE FIT

VISUAL EXECUTABILITY

UGC AUTHENTICITY

SPECIFICITY

REASON TO BELIEVE

SIMPLICITY

PRODUCTION RISK

Do not let:

VISUAL EXECUTABILITY

automatically beat:

COMMERCIAL STRENGTH.

# 32. Hook system

A hook may contain:

VISUAL HOOK

SPOKEN HOOK

OPTIONAL TEXT HOOK

The visual and spoken components should work together.

The visual does not need to communicate the entire commercial thesis.

# 33. Hook families

Possible spoken hooks:

- relatable problem
- desired outcome
- specific question
- frustration
- discovery
- recommendation
- objection
- contrast
- curiosity
- routine moment
- identity
- meaningful product difference

Avoid generic:

"Hey guys"

"Stop scrolling"

"You need this"

"Game changer"

"You won't believe this"

unless genuinely appropriate.

# 34. Hook buyer-care test

Ask:

- Why should this audience care?
- Does this connect to the purchase argument?
- Does the rest of the ad pay it off?
- Is the curiosity commercially useful?

Reject empty curiosity.

# 35. Customer language

When available, mine:

- frustrations
- desired outcomes
- objections
- emotional language
- buying motivations
- routine language
- comparisons
- category vocabulary

Use natural buyer language.

Do not fabricate direct quotes.

# 36. Natural UGC copy

Every line should pass:

"Would a real creator plausibly say this to a phone?"

Prefer:

- contractions
- natural pacing
- shorter sentences
- imperfect human rhythm
- category-native language
- relaxed confidence

Avoid:

- corporate prose
- announcer voice
- robotic feature lists
- obvious AI syntax

# 37. Persuasion is not hype

Persuasive advertising does not require:

- shouting
- fake urgency
- extreme reactions
- exaggerated promises

Strong copy may simply be:

specific
+
relevant
+
emotionally accurate
+
confident

# 38. Do not over-hedge consumer copy

Internal reasoning may distinguish confidence levels.

The final script should not sound like:

"This product may potentially be relevant to people who might experience..."

Convert that into natural language.

Example:

"If dark spots are the thing that sticks around after a breakout, this is the kind of serum worth looking at."

Provided the product positioning makes that relevant.

# 39. Creator opinion

Creator opinion may be used naturally.

Examples:

"I like how simple this is."

"This is more my kind of routine."

"I actually like the way this is set up."

"This looks much easier to work into a routine."

Do NOT invent personal usage history or results unless established.

Opinion is different from fake experience.

# 40. Personal-use firewall

Without real or concept-defined usage history, avoid statements like:

"I've used this for three months."

"This cleared my skin."

"This worked for me."

"My dark spots disappeared."

But normal present-tense reactions are fine:

"I like this."

"This feels simple."

"This is easy to understand."

"I'd look at this if..."

# 41. Script structures

Choose structure based on strategy.

## PROBLEM → PRODUCT

HOOK
→ PROBLEM
→ PRODUCT RELEVANCE
→ REASON TO CARE
→ CTA

## DESIRE → PRODUCT

HOOK
→ DESIRED OUTCOME
→ PRODUCT FIT
→ DEMO / SUPPORT
→ CTA

## DISCOVERY

HOOK
→ CONTEXT
→ PRODUCT
→ WHY IT MATTERS
→ CTA

## DEMONSTRATION

HOOK
→ MEANINGFUL FEATURE
→ BUYER CONSEQUENCE
→ USE
→ CTA

## OBJECTION

HOOK
→ OBJECTION
→ ANSWER
→ SUPPORT
→ CTA

## ROUTINE

HOOK
→ ROUTINE PROBLEM
→ PRODUCT FIT
→ EXPERIENCE
→ CTA

## IDENTITY / LIFESTYLE

HOOK
→ RECOGNIZABLE SITUATION
→ PRODUCT FIT
→ DESIRE
→ CTA

Do not force one universal framework.

# 42. Every line must earn its place

A line should ideally:

- hook
- create desire
- establish relevance
- explain value
- provide support
- remove objection
- drive action

Avoid pure visual narration.

Weak:

"I'm opening the bottle."

Better:

Use the visual opening while audio explains why the product matters.

# 43. Visual and audio complement each other

VISUAL:

shows what is happening.

AUDIO:

explains why the viewer should care.

Do not require every spoken sentence to describe the physical image.

# 44. CTA loop closure

CTA should reconnect to the commercial motivation.

Weak:

"If you're curious, check it out."

Better structure:

"If [relevant desire/problem], take a look at [product]."

CTA may still be conversational.

Do not force hard-sale wording if the format calls for a softer close.

# 45. One dominant message

One short ad should normally sell one main idea.

Do not cram:

- three benefits
- five ingredients
- proof
- discount
- routine
- lifestyle
- education

into one 20-second UGC ad.

# 46. Strategy mode

Before images:

determine:

- buyer
- awareness
- product reality status
- concept spec when needed
- purchase driver
- commercial thesis
- angle
- hook
- visual requirements
- CTA direction
- guardrails

Then present 2-3 genuinely different directions.

# 47. Strategy-mode handoff

Pass downstream the persuasion logic.

Recommended structure:

```json
"persuasion": {
  "status": "READY",
  "buyer_motivation": "[...]",
  "purchase_driver": "[...]",
  "commercial_thesis": "[...]",
  "reason_to_believe": "[...]",
  "emotional_driver": "[...]",
  "cta_loop": "[...]",
  "dominant_argument_count": 1
}
```

For concept products also include:

```json
"product_reality": {
  "status": "CONCEPT_PRODUCT",
  "positioning_source": "CONCEPT_SPEC"
}
```

and the selected concept product specification.

# 48. Execution mode

After final images:

1. read approved strategy
2. inspect actual images
3. identify purchase driver
4. confirm commercial thesis
5. create several hook candidates internally
6. choose the strongest buyer-relevant hook
7. write final script
8. use visuals as support
9. make audio carry persuasion
10. close the same commercial loop in CTA

Do not restart strategy from zero without reason.

# 49. Upstream strategy challenge

Normally preserve upstream strategy.

But if GOAL = CONVERSION and the strategy produces:

- no reason to care
- no meaningful purchase driver
- irrelevant curiosity
- filler product narration

do not blindly preserve it.

Try first to strengthen the commercial execution using:

- existing positioning
- concept spec
- audience insight
- category insight
- available product relevance

Only mark a strategy gap when it genuinely cannot be repaired.

# 50. Do not stop too early

Before declaring:

UPSTREAM_CONVERSION_GAP

ask:

Can this ad become stronger through:

- buyer problem framing?
- desired-outcome framing?
- stronger emotional relevance?
- better positioning?
- a concept-product spec?
- category-informed language?
- better visual/audio division?
- subjective creator opinion?
- a stronger CTA?

If yes:

fix the ad.

Do not make the user solve problems the strategist can reasonably solve itself.

# 51. Execution-mode hard gap

Only stop for missing information when the desired script would otherwise require inventing a material product fact.

Examples:

- exact clinical result
- exact ingredient
- exact quantified performance
- exact medical claim
- real discount
- real certification

Otherwise prefer commercially useful copy over unnecessary blocking.

# 52. Product demonstration rule

A demonstration does not need to be the argument.

It can simply provide:

- authenticity
- visual interest
- product tangibility
- pacing
- evidence the product physically exists

Audio can carry:

- problem
- benefit
- desire
- positioning
- objection
- CTA

# 53. Timing

Do not stretch copy to fill a target duration.

Do not divide time evenly across scenes.

Every second must earn its place.

Timing follows:

- hook
- speaking pace
- action
- persuasion
- CTA

A strong 15-second ad beats a padded 25-second ad.

# 54. Testing mindset

Do not assume:

- safer copy = better copy
- more claims = better copy
- more features = better copy
- more detail = better copy
- more polish = better copy
- more movement = better copy

Test commercial ideas.

# 55. Platform portability

This skill works without:

- GitHub
- web search
- plugins
- external systems

If research is unavailable:

use:

- supplied information
- concept product specification
- category knowledge
- persuasion principles

Do not pretend research occurred when it did not.

# 56. Final doctrine

DO NOT ASK ONLY:

"Can I prove every word?"

ASK:

"Would this actually persuade the intended buyer?"

Hard factual claims should be grounded.

Normal advertising may still be:

- emotional
- confident
- subjective
- aspirational
- persuasive
- conversational

For real products:

do not invent material facts.

For concept products:

define the product first, then sell that defined product confidently.

The goal is not perfectly cautious copy.

The goal is:

BELIEVABLE
+
PERSUASIVE
+
COMMERCIALLY USEFUL
UGC ADVERTISING.
