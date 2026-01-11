# Landing Page Redesign: Context Engineering Focus

## Summary

Redesign the index.html landing page to align with the "2M Token Trap" article and Plan Stack README.md, emphasizing context engineering principles (Isolation, Chaining, Headroom).

## Background

### Reference Materials

**dev.to Article "The 2M Token Trap":**
- Context capacity ≠ comprehension
- "Lost in the Middle" phenomenon
- Claude Code's 75% rule
- Three principles: Isolation, Chaining, Headroom

**Plan Stack README.md:**
- Context engineering as core concept
- Workflow: Research → Plan → Execute → Review
- /clear pattern for context reset
- Plans as first-class artifacts

### Problem with Previous Design

- Three principles (Isolation, Chaining, Headroom) not explicitly stated
- "Context engineering" concept underdeveloped
- Strong hook ("2M Token Trap") not utilized

## Key Decisions

1. **Lead with the hook**: "The 2M Token Trap" as hero badge
2. **Three principles as central section**: Visual cards for Isolation, Chaining, Headroom
3. **Stats-driven problem section**: 62x, 75%, "Lost in the Middle"
4. **Workflow-principle mapping**: Each workflow step linked to a principle
5. **Simplified structure**: Remove Paradox Visual and Cognitive Architecture sections

## New Section Structure

```
1. Hero
   - Badge: "The 2M Token Trap"
   - Title: "Context Engineering for AI-Assisted Development"
   - Subtitle: 62x growth, quality didn't follow

2. The Problem
   - Stats grid: 62x, 75%, Lost in the Middle
   - Key insight: Context is cognitive load, not storage

3. Three Principles (NEW)
   - Isolation: Minimum effective context
   - Chaining: Artifacts between stages
   - Headroom: Reserve space for reasoning

4. Plan Stack Solution
   - First-class artifacts concept
   - Distilled research (50 files → 300 lines)

5. Workflow
   - Research → Plan → Execute → Review
   - Principle tags on each step

6. The /clear Pattern
   - Visual: Before (95%) → After (15%)
   - "Restart at 0% without restarting work"

7. Get Started
   - One-line CLAUDE.md instruction
   - Self-reinforcing loop explanation

8. CTA
```

## Removed Sections

- Context Paradox Visual → Merged into /clear Pattern
- Cognitive Architecture → Replaced by Three Principles
- Comparison table → Replaced by stats grid

## Files Modified

- `index.html` - Complete rewrite with new structure

## CSS Changes

- Added `.stats-grid`, `.stat-card` for problem section
- Added `.principles-grid`, `.principle-card` for three principles
- Added `.clear-pattern`, `.clear-card` for /clear visualization
- Added `.workflow-principle` tags
- Added `--warning` color variable for hero badge
- Removed unused CSS (paradox, cognitive grid)

## Verification

1. Open index.html in browser
2. Check responsive design on mobile/tablet
3. Verify all GitHub links work
4. Confirm visual hierarchy: Hook → Problem → Solution → Action
