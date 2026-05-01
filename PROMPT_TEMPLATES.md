# Prompt Templates (Descriptive Patterns)

## Template: Code Generation
Role: [Expert] with [X] years in [Tech Stack].
Task: Build [System/Feature] using [Framework].
Input: [Data sources, user types, constraints].
Process: [Step 1] → [Step 2] → [Step 3].
Build-Test-Validate: All files complete. Test after every change. Validate integration.
Constraints: [Performance, security, accessibility, compatibility].
Output: [File structure, component list, API surface].
Tone: [Aesthetic direction].
Level: [L1/L2/L3/L4].
Domain: [fintech|medical|legal|gaming|ecommerce|security|edu|creative] (optional, auto-detected if omitted).
Model: [claude|gpt4o|gemini|llama3|mistral] (default: claude).

## Template: UI/UX Design (Frontend)
Role: [Design lead] specializing in [Domain].
Task: Design [Interface type] for [User segment].
Purpose: [Problem solved]. [User goal].
Tone: [One extreme aesthetic]. Commit.
Constraints: [Device targets, performance budget, accessibility level].
Differentiation: [One unforgettable element].
Emotion: [Feel at each touchpoint].
Motion: [Transitions, micro-interactions].
Frontend Design:
- Typography: [Distinctive display font] + [Refined body font]. NO Inter/Roboto/Arial.
- Color: [Dominant] + [Accent]. NO purple gradients on white.
- Motion: [High-impact animation strategy].
- Spatial: [Unexpected layout approach].
- Background: [Atmospheric effect]. NO solid colors.
- NO AI slop: [Specific prohibitions].
Output: [Design system description, component behavior, interaction flow].
Level: [L1/L2/L3/L4].
Domain: [fintech|medical|legal|gaming|ecommerce|security|edu|creative] (optional).
Model: [claude|gpt4o|gemini|llama3|mistral] (default: claude).

## Template: API/Backend
Role: [Staff engineer] in [Domain].
Task: Design [Service/API] for [Use case].
Input: [Data models, request patterns].
Process: [Endpoint definition] → [Validation rules] → [Error handling] → [Performance optimization].
Build-Test-Validate: Schema complete. Test query complexity. Validate backward compatibility.
Constraints: [Rate limits, auth, compliance].
Output: [Schema, resolver signatures, error catalog].
Tone: Industrial/utilitarian.
Level: [L1/L2/L3/L4].
Domain: [fintech|medical|legal|gaming|ecommerce|security|edu|creative] (optional).
Model: [claude|gpt4o|gemini|llama3|mistral] (default: claude).

## Template: Content/Copy
Role: [Voice specialist] for [Brand type].
Task: Write [Content type] for [Audience].
Tone: [Voice characteristics].
Constraints: [Length, keywords, brand guidelines].
Differentiation: [One memorable phrase or angle].
Output: [Structure, sections, call-to-action].
Level: [L1/L2/L3/L4].
Domain: [fintech|medical|legal|gaming|ecommerce|security|edu|creative] (optional).
Model: [claude|gpt4o|gemini|llama3|mistral] (default: claude).

## Template: Image/Visual
Role: [Art director] for [Medium].
Task: Generate visual concept for [Subject].
Input: [Mood, lighting, focal point, style references].
Process: [Atmosphere] → [Composition] → [Details] → [Technical specs].
Constraints: [Aspect ratio, content policy, resolution].
Output: [Single descriptive paragraph, technical parameters].
Tone: [Visual aesthetic].
Level: [L1/L2/L3/L4].
Domain: [fintech|medical|legal|gaming|ecommerce|security|edu|creative] (optional).
Model: [claude|gpt4o|gemini|llama3|mistral] (default: claude).

## Template: Frontend Component (No AI Slop)
Role: [Frontend specialist] with [X] years. Expert in [Framework].
Task: Build [Component] for [Context].
Purpose: [What it does]. [Who uses it].
Tone: [One extreme aesthetic]. Commit fully.
Frontend Design:
- Typography: [Specific font choices]. NO generic fonts.
- Color: [Palette with CSS variables]. Sharp accents.
- Motion: [Animation strategy]. CSS-first. High-impact moments.
- Spatial: [Layout approach]. Asymmetry or controlled density.
- Background: [Atmospheric effect]. Depth, texture, pattern.
- NO AI slop: No Inter, no purple gradients, no centered cards, no generic animations.
Build-Test-Validate: Component complete. Test interactions. Validate accessibility.
Constraints: [Framework, performance, accessibility].
Output: [Component structure, props, behavior, styling approach].
Level: [L1/L2/L3/L4].
Domain: [fintech|medical|legal|gaming|ecommerce|security|edu|creative] (optional).
Model: [claude|gpt4o|gemini|llama3|mistral] (default: claude).
