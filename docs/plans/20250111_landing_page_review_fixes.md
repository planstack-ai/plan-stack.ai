# Landing Page Review Fixes

## Summary
Improve the landing page based on external review feedback. Address issues with logical flow, wording, and missing content.

## Background
External review identified the following issues:
- Weak logical connections between sections
- Some expressions are overstated or lack basis
- Target audience not explicitly stated
- No concrete example of what a plan looks like

## Changes

### 1. Rewrite Hero Section
**Before:**
- Generic "context loss" pain points
- Explanatory text after punchline dilutes impact

**After:**
- Focus on AI-specific problems
- End with punchline, remove explanatory text

New copy:
```
You are losing context every time you use AI to code.

- The AI suggests changes that break invariants it never knew existed
- You /clear and lose hours of accumulated understanding
- The next session starts from zero — again
- Your codebase grows, but the AI's memory doesn't

The code exists. The tests exist.
The reasoning does not.
```

### 2. Merge Section 2 and 3
**Before:**
- Section 2: The Real Problem (AI cannot recover intent)
- Section 3: Why Existing Practices Fail (table of failed approaches)

**After:**
- Single unified section
- Flow: "AI cannot recover intent → existing practices don't solve this either"

### 3. Add Target Persona
Add below Hero or as intro text:
```
For developers using AI coding assistants like Claude Code, Cursor, or Copilot.
```

### 4. Change "The one rule" Wording
**Before:** "The one rule that makes everything work"
**After:** "The entry point"

Rationale: The single CLAUDE.md line is the entry point, not the entire system.

### 5. Remove Specific Number
**Before:** "A good plan captures all of that in 200–300 lines."
**After:** "A good plan captures all of that in a few hundred lines."

Rationale: The 200-300 number lacks stated basis.

### 6. Unify CTA Buttons
**Before:** Hero = "View on GitHub", Footer CTA = "Star on GitHub"
**After:** Both use "View on GitHub"

### 7. Add Plan Example
Add a simplified plan sample to show what a plan looks like in practice.

Sample content:
```markdown
# Staff Message Feature

## Summary
Add staff-to-customer messaging in admin panel.

## Key Decisions
- Use existing notification infrastructure
- Store in messages table, not comments
- Async delivery via Sidekiq

## Files to Modify
- app/models/message.rb
- app/controllers/admin/messages_controller.rb
- app/views/admin/messages/

## Edge Cases
- Customer has notifications disabled → show in dashboard
- Staff sends during maintenance → queue for later
```

### 8. Minor Wording Fixes
| Before | After |
|--------|-------|
| Long AI sessions | Extended AI sessions |
| This cost repeats forever | This cost compounds with every change |
| capture correctness, not original reasoning | capture correctness, not intent |

## Implementation Order
1. Hero section rewrite
2. Merge Section 2+3
3. Add persona
4. Add plan example
5. Change "The one rule" wording
6. Remove specific number
7. Unify CTAs
8. Minor wording fixes

## Out of Scope
- Major design/layout changes
- New pages
- JavaScript functionality
