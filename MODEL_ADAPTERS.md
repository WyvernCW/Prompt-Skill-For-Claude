# Model Adapters

## Overview
Translate generated prompts for target model characteristics. Each model has different instruction-following quirks, context windows, and failure modes.

## claude (default)
### Profile
- Context: 200K tokens
- Format: Natural language, conversational
- Strengths: Long context, nuanced reasoning, safety-conscious
- Weaknesses: Can be overly cautious, may refuse edge cases
### Adaptation
No translation needed. Full feature set available. Use as baseline.

## gpt4o
### Profile
- Context: 128K tokens
- Format: System + user messages, clear role definition
- Strengths: Fast, multimodal, strong tool use
- Weaknesses: Can hallucinate structured output, less nuanced safety
### Adaptation
- Add explicit JSON schema if structured output required.
- Use "You must..." for critical constraints.
- Break long prompts into chunks if exceeding 64K tokens.
- Add examples for complex reasoning tasks.
- Use XML tags for structure: instruction, context, output.

## gemini
### Profile
- Context: 1M tokens (quality degrades at extremes)
- Format: Turn-based, explicit reasoning steps
- Strengths: Massive context, strong multimodal, Google ecosystem
- Weaknesses: Inconsistent instruction following, safety over-refusal
### Adaptation
- Use numbered steps for all instructions.
- Repeat critical constraints two to three times.
- Avoid nested conditionals. Prefer flat structure.
- Use bullet points over paragraphs.
- Add explicit reasoning instructions for complex tasks.

## llama3
### Profile
- Context: 8K to 128K depending on variant
- Format: System prompt plus instruction tags
- Strengths: Open, customizable, efficient
- Weaknesses: Shorter effective context, weaker reasoning at scale
### Adaptation
- Shorter prompts targeting under 4K effective tokens.
- More explicit examples.
- Simpler structure with fewer nested sections.
- Avoid caveman ultra mode. Use full or lite instead.
- Repeat constraints in both system and user prompts.

## mistral
### Profile
- Context: 32K to 128K depending on variant
- Format: Instruction tags with clear system boundaries
- Strengths: Strong reasoning, good code generation, efficient
- Weaknesses: Can be verbose, inconsistent with complex constraints
### Adaptation
- Use instruction tags around user content.
- Add repetition for critical constraints.
- Prefer lists over prose.
- Use system message tokens appropriately.
- Break complex instructions into numbered sub-tasks.

## Adaptation Rules

### Context Window
If prompt exceeds target model limit:
1. Compress to ultra caveman mode.
2. Split into core and extended sections.
3. Prioritize core sections.
4. Summarize extended sections.

### Instruction Format
Restructure for target model's preferred format:
- Claude: Conversational and natural.
- GPT-4o: System plus user messages with XML tags.
- Gemini: Numbered steps in flat structure.
- Llama3: Tagged headers with explicit content.
- Mistral: Instruction blocks with list formatting.

### Safety Calibration
Adjust constraint strength based on model's safety behavior:
- Over-cautious models: Soften constraints and add explicit harm exceptions.
- Under-cautious models: Harden constraints and add explicit prohibitions.

### Output Parsing
Add explicit parsing instructions for models with weaker structured output:
- GPT-4o: Provide JSON schema and demand valid JSON only.
- Gemini: Provide response template with exact format.
- Llama3: Provide few-shot examples of desired output format.
