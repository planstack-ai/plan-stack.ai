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
- Product identity unclear (tool vs methodology?)
- Social proof buried in footer

## Key Decisions

1. **Hero label**: "AI-Native Workflow" (positive framing over technical problem)
2. **Product definition**: Clarify Plan Stack is a methodology, not a tool
3. **Social proof early**: Move credibility statement from footer to hero
4. **Three principles as central section**: Visual cards for Isolation, Chaining, Headroom
5. **Stats-driven problem section**: 62x, 75%, "Lost in the Middle"
6. **Workflow-principle mapping**: Each workflow step linked to a principle
7. **Copy improvements**: "cognitive load" and clearer 75% explanation

## New Section Structure

```
1. Hero
   - Badge: "AI-Native Workflow"
   - Title: "Context Engineering for AI-Assisted Development"
   - Subtitle: "Context windows grew 62x... cognitive load"
   - Definition: "Plan Stack is a methodology — no install required..."
   - Social Proof: "Proven with a 10-engineer team on a 500-table Rails app"
   - CTA: Get Started / GitHub

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

## CSS Added

- `.stats-grid`, `.stat-card` for problem section
- `.principles-grid`, `.principle-card` for three principles
- `.clear-pattern`, `.clear-card` for /clear visualization
- `.workflow-principle` tags
- `.hero-definition` for product definition
- `.hero-proof` for social proof with checkmark

## Copy Changes

| Location | Before | After |
|----------|--------|-------|
| Hero label | "The 2M Token Trap" | "AI-Native Workflow" |
| Hero subtitle | "Plan Stack brings structured context..." | "A context window is not storage. It is cognitive load." |
| 75% stat | "Claude Code improved dramatically..." | "Filling context to capacity degrades output quality." |
| Hero (new) | - | Product definition + Social proof |

## Verification

1. Open index.html in browser
2. Verify product identity is clear within 3 seconds
3. Check responsive design on mobile/tablet
4. Verify all GitHub links work
5. Confirm visual hierarchy: Label → Title → Problem → Definition → Proof → CTA
