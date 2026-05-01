# Prompt Genealogy Tracker

## Overview
Every prompt generated is part of an evolutionary tree. Track lineage. Enable time travel.

## Genealogy Schema (Descriptive Only)

Every prompt node has these properties described in natural language:

- **ID**: A unique identifier for this prompt version.
- **Parent ID**: The identifier of the prompt this evolved from. Null if this is the first prompt.
- **Generation**: A number counting how many evolutions this prompt is from the root. Zero means it is the original prompt.
- **Branch Name**: A label for this line of evolution. Default is "main". Experiments get their own branch names.
- **Timestamp**: When this prompt was created.
- **User Request**: The original words the user spoke.
- **Output**: The final prompt description that was delivered.
- **Scores**: Measurements of quality including overall composite score, ambiguity level, completeness, security rating, token density percentage, and memory alignment.
- **Agent Council Result**: The approval percentage from the agent council, how many debate rounds occurred, and which agents if any dissented.
- **Autonomous Cycles**: How many self-improvement loops ran, what the final strategy was, and whether the loop hit a plateau.
- **Children**: Identifiers of any prompts that evolved from this one.
- **Status**: Whether this prompt is currently active, archived as deprecated, merged into another branch, or reverted from.

## Genealogy Operations

### Spawn
Create a child prompt from the current prompt. This happens when recursive refinement runs, the autonomous loop generates a new version, the user edits the prompt, or the user explicitly requests a new branch.

### Revert
Return to any previous prompt by specifying its generation number or its unique identifier. The current prompt is abandoned and the chosen ancestor becomes the new current prompt.

### Branch
Create a named experimental line from any existing prompt. The new branch starts as a copy of the chosen prompt but can evolve independently. Useful for trying risky changes without affecting the main line.

### Merge
Combine two successful branches into a single new prompt. The merge takes the strongest elements from each branch and resolves any conflicts using the agent council priority chain.

### Prune
Archive dead branches that have low scores and no children. This keeps the genealogy tree clean and focused on high-quality lines of evolution.

### Compare
Show the differences between any two prompts in the tree. Highlight what was added, removed, or changed.

## Genealogy Commands

| Command | Action |
|---|---|
| "revert to generation three" | Return to the third generation prompt. |
| "revert to prompt identifier" | Return to a specific prompt by its unique identifier. |
| "branch with name experimental dark mode" | Create a new branch from the current prompt. |
| "merge branch alpha and branch beta" | Combine the best of both branches into one. |
| "show family tree" | Display the lineage of all prompts as a tree. |
| "prune dead branches" | Archive low-score prompts with no children. |
| "compare generation two and generation five" | Show differences between two generations. |
| "compare prompt A and prompt B" | Show differences between two specific prompts. |
| "show best branch" | Identify which branch has the highest average quality score. |
| "promote branch gamma to main" | Make branch gamma the new primary line. |

## Tree Visualization (Descriptive)

The main branch starts at generation zero. Each generation spawns children. Some children become new branches. Branches can be merged back. The tree grows downward from root to leaves.

Example structure described in words:
- The main branch begins at generation zero with a root prompt scoring eighty-five.
- From the root, generation one has two children. One child scores eighty-eight and continues the main branch. The other child scores eighty-seven and starts a side branch.
- The main branch child at generation eighty-eight spawns generation two scoring ninety-two, which in turn spawns generation three scoring ninety-five. This is the current active prompt.
- The side branch at generation eighty-seven remains as an alternative path.
- A separate experimental branch begins at generation zero and grows through generation one scoring ninety-one and generation two scoring ninety-four.
