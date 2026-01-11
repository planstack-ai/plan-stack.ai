# Add "Why" Section: LLM Context Architecture

## Summary
Add "Why this works" technical reasoning to complement the existing "How to use" workflow explanation.
Position PlanStack as an inevitable solution based on LLM attention/context window constraints.

## Background
Current site focuses on workflow features (Research → Plan → Implement → Review).
Missing: Technical justification for why structured context beats "dump everything" approaches in the 200K+ token era.

## Approach

### 1. New Section: "Beyond the Context Window Paradox"
**Position:** After Hero, before The Workflow section

**Structure:**
- Visual comparison: Legacy (dump everything) vs PlanStack (structured stacks)
- Key message: "Context capacity ≠ comprehension ability"
- Technical keywords: Attention dilution, S/N ratio, structured inference

**Copy:**
```
LLMs have massive context windows—but attention is finite.

Throwing 200K tokens at a model doesn't mean it understands 200K tokens equally.
Attention dilutes. Signal gets buried in noise. Critical decisions get forgotten.

PlanStack structures your context like an engineer structures code:
modular, focused, and composable.
```

### 2. New Section: "Designed for Cognitive Alignment"
**Position:** After The Workflow section

**Structure:** 3 icon cards
1. **Limited Attention**
   - "Both humans and LLMs have finite processing capacity. PlanStack blocks the noise."
2. **Step-by-Step Reasoning**
   - "Plan → Review → Implement. Each phase catches errors before they compound."
3. **Compound Knowledge**
   - "Plans aren't disposable. They're assets that improve future inference."

### 3. Hero Copy Update
**Current:**
- Badge: "AI-native Development Workflow"
- Main: "Stop losing context. Start stacking plans."
- Sub: "A development methodology where implementation plans are accumulated..."

**Proposed:**
- Badge: **"Beyond the Context Window Paradox"**
- Main: Keep existing (it's strong)
- Sub: "The workflow that treats LLMs not as magic, but as reasoning engines with constraints. Optimized for the 200K+ token era."

### 4. Use Case Enhancement (Optional)
**Before/After format:**

Before (Without PlanStack):
- "Gave the LLM my entire codebase. Got suggestions that broke existing patterns."

After (With PlanStack):
- "Isolated context per domain. LLM follows existing conventions perfectly."

## Files to Change
- `index.html` - Add new sections, update Hero badge/subtitle

## Visual Design

### Context Paradox Diagram Concept
```
[Legacy Approach]                    [PlanStack]
┌─────────────────────────┐         ┌─────────────────────────┐
│ ░░░░░░░░░░░░░░░░░░░░░░│         │                         │
│ ░░ ALL CODE ░░░░░░░░░░│         │  ┌─────────────────┐   │
│ ░░░░░░░░░░░░░░░░░░░░░░│         │  │ Active Plan     │   │
│ ░░░░░░░░░░░░░░░░░░░░░░│         │  │ (Focused)       │   │
│ ░░░ OLD DECISIONS ░░░░│  →      │  └─────────────────┘   │
│ ░░░░░░░░░░░░░░░░░░░░░░│         │  ┌───┐ ┌───┐ ┌───┐    │
│ ░░░░ NOISE ░░░░░░░░░░│         │  │ P │ │ P │ │ P │    │
│ ░░░░░░░░░░░░░░░░░░░░░░│         │  └───┘ └───┘ └───┘    │
│       ATTENTION: ▓░░░ │         │  Referenced Plans      │
│       (Diluted)       │         │       ATTENTION: ▓▓▓▓ │
└─────────────────────────┘         │       (Focused)       │
                                    └─────────────────────────┘
```

## Implementation Order
1. Update Hero badge text
2. Add "Beyond the Context Window Paradox" section with visual comparison
3. Add "Cognitive Alignment" section (3 cards)
4. Update Hero subtitle (optional)

## Risks
- Too technical for non-engineers
  - Mitigation: Lead with visuals, keep text as supporting context
- Page becomes too long with new sections
  - Mitigation: Consider integrating Cognitive Alignment into The Workflow section

## Success Criteria
- "Why dump-everything fails" is instantly clear from the visual
- Keywords "Attention", "S/N ratio", "Structure" appear naturally
- Engineers feel "this is technically sound" when reading the page