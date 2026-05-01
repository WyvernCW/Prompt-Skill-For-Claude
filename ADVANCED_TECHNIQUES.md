# Advanced Techniques

## Technique 1: Prompt Inversion
Instead of describing what TO do, describe what NOT to do first. Then invert.
Example: "Must not use any animation. Must not exceed 2 colors. Must not have navigation." → Then describe the single-page, monochrome, static result.

## Technique 2: Constraint Stacking
Layer constraints to force creative solutions:
- Must load in <100ms.
- Must work offline.
- Must fit in 14KB.
- Must support 50 languages.
The intersection of impossible constraints produces breakthrough design.

## Technique 3: Temporal Layering
Describe the experience across time:
- T+0ms: First impression.
- T+500ms: Initial interaction.
- T+2s: Engagement peak.
- T+10s: Task completion.
- T+1min: Memory formation.
Each moment has distinct emotional target.

## Technique 4: Sensory Substitution
When visual description insufficient, substitute with other senses:
- "Sounds like a mechanical keyboard with o-rings."
- "Feels like brushed aluminum at room temperature."
- "Smells like fresh printer paper and ozone."
- "Moves like a suspension bridge in wind."

## Technique 5: Reference Anchoring
Anchor to known quantities:
- "If Stripe and Notion had a baby."
- "Apple circa 2007 but with dark mode."
- "Wikipedia if designed by Supreme."
Then diverge sharply from anchor.

## Technique 6: Negative Personas
Define who this is NOT for:
- "Not for enterprise procurement teams."
- "Not for users who want customization."
- "Not for accessibility-first contexts."
Clarifies target by exclusion.

## Technique 7: Failure Mode Design
Describe what graceful degradation looks like:
- "If JS fails, show raw data table."
- "If API down, cache last known state with timestamp."
- "If image missing, show dominant color block with alt text."

## Technique 8: Scale Spectrum
Describe behavior at extremes:
- 1 user vs 1M users.
- 1 item vs 1M items.
- 1KB data vs 1TB data.
- Mobile portrait vs ultrawide monitor.
Design must survive all scales.

## Technique 9: Frontend Slap Test
Describe the frontend so vividly that slapping the screen would feel like the described texture:
- "Rough concrete with embedded glass fragments."
- "Smooth lacquered wood with visible grain."
- "Cold brushed steel with oil-slick rainbow patina."
Forces material thinking over flat design.

## Technique 10: Anti-Pattern Inoculation
Explicitly name and forbid common AI slop patterns:
- "Must not use card-based layout."
- "Must not center all content."
- "Must not use default browser focus rings."
- "Must not have generic loading spinner."
Each prohibition forces creative alternative.
