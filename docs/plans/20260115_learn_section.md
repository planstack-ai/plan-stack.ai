# Claude Code Learning Section Implementation Plan

**Date**: 2026-01-15
**Feature**: Learn Section - Claude Code Tutorial Series

## Overview

Add a learning section for Claude Code tutorials at `/learn/` with:
- Introduction page
- Basics series (1-5) with "Next/Previous" navigation
- Practical series (1-7) with "Next/Previous" navigation
- Quiz pages after each series (3-5 multiple choice questions)
- Header/Footer links on all pages

Language: English only (Japanese support later via separate /ja/learn/ path)

## Content Topics (from GitHub Issues #8-19)

### Basics Series (5 lessons)
| # | Title | Key Message |
|---|-------|-------------|
| 1 | What is Context Window | "It's working memory, not storage" |
| 2 | What Consumes Tokens | "It consumes more than you think" |
| 3 | Why Accuracy Drops with Length | "The middle gets forgotten" |
| 4 | Context Design Principles | "Be intentional about what you pass" |
| 5 | Practical Workflow | "Here's how to actually do it" |

### Practical Series (7 lessons)
| # | Title | Key Message |
|---|-------|-------------|
| 1 | Think First | "Plan mode beats jumping in" |
| 2 | CLAUDE.md | "Notes for yourself with amnesia" |
| 3 | Context Window Limits | "Quality degrades at 20-40%, not 100%" |
| 4 | Prompting That Works | "Bad input = bad output" |
| 5 | MCP, Hooks, and Tools | "Don't leave value on the table" |
| 6 | When Claude Gets Stuck | "3 explanations = time to change" |
| 7 | Build Systems, Not One-Shots | "Claude as system component" |

## File Structure

```
learn/
├── index.html                 # Landing page with introduction
├── basics/
│   ├── 1.html                # What is Context Window
│   ├── 2.html                # What Consumes Tokens
│   ├── 3.html                # Why Accuracy Drops with Length
│   ├── 4.html                # Context Design Principles
│   ├── 5.html                # Practical Workflow
│   └── quiz.html             # Basics quiz (3-5 questions)
└── practical/
    ├── 1.html                # Think First
    ├── 2.html                # CLAUDE.md
    ├── 3.html                # Context Window Limits
    ├── 4.html                # Prompting That Works
    ├── 5.html                # MCP, Hooks, and Tools
    ├── 6.html                # When Claude Gets Stuck
    ├── 7.html                # Build Systems, Not One-Shots
    └── quiz.html             # Practical quiz (3-5 questions)
```

## Files to Modify

1. **index.html** - Add "Learn" link to header nav-links and footer-links
2. **articles/index.html** - Add "Learn" link to header nav-links and footer-links

## Navigation Flow

```
learn/index.html
     │
     ├─→ basics/1.html → basics/2.html → ... → basics/5.html → basics/quiz.html
     │                                                                │
     └─→ practical/1.html → practical/2.html → ... → practical/7.html → practical/quiz.html
```

| Page | Previous Link | Next Link |
|------|--------------|-----------|
| basics/1 | ../index.html | 2.html |
| basics/2-4 | [n-1].html | [n+1].html |
| basics/5 | 4.html | quiz.html |
| basics/quiz | 5.html | ../practical/1.html |
| practical/1 | ../index.html | 2.html |
| practical/2-6 | [n-1].html | [n+1].html |
| practical/7 | 6.html | quiz.html |
| practical/quiz | 7.html | ../index.html |

## Implementation Order

### Phase 1: Infrastructure
1. Create learn/index.html with landing page design
2. Update index.html header/footer with Learn link

### Phase 2: Basics Series
3. Create basics/1.html through basics/5.html
4. Create basics/quiz.html with quiz logic

### Phase 3: Practical Series
5. Create practical/1.html through practical/7.html
6. Create practical/quiz.html

### Phase 4: Final Integration
7. Update articles/index.html header/footer

## Technical Notes

- Reuse existing CSS variables and component patterns from index.html
- Quiz uses vanilla JavaScript (no external dependencies)
- Each lesson content derived from corresponding GitHub issue
- LocalStorage for progress tracking is a future enhancement

## Verification Checklist

- [ ] All "Next/Previous" links work correctly
- [ ] Progress dots reflect current position
- [ ] Header/footer links work from all pages
- [ ] Quiz scoring functions properly
- [ ] Results show correct/incorrect highlighting
- [ ] Mobile responsive design works
