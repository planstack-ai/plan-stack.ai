# GitHub Workflow: Claude AI Review

## Overview
Add a GitHub Actions workflow that performs automatic code review using Claude AI on pull requests.

## Background
- Improve PR code review quality
- AI detects basic issues before human review
- Dogfooding Plan Stack (using our own product)

## Research Required
- [ ] Investigate official Claude GitHub Action implementation
  - https://github.com/anthropics/claude-code-action
  - Or custom implementation using Anthropic API directly
- [ ] Setup method for required secrets (ANTHROPIC_API_KEY)
- [ ] File pattern configuration for review targets

## Implementation Options

### Option A: claude-code-action (Official)
```yaml
# .github/workflows/claude-review.yml
name: Claude Code Review
on:
  pull_request:
    types: [opened, synchronize]

jobs:
  review:
    runs-on: ubuntu-latest
    steps:
      - uses: anthropics/claude-code-action@v1
        with:
          anthropic_api_key: ${{ secrets.ANTHROPIC_API_KEY }}
```

### Option B: Custom Implementation
- Script that calls Anthropic API directly
- Allows more fine-grained customization

## Acceptance Criteria
- [ ] Review is automatically executed when PR is created/updated
- [ ] Review comments are posted to the PR
- [ ] API key is securely managed via secrets

## Files to Create/Modify
- `.github/workflows/claude-review.yml` (create new)

## Questions
- Review scope? (all files or specific patterns)
- Review tone/strictness?
- Review in Japanese or English?

## Status
- [x] Research - Adopted claude-code-action v1
- [x] Implementation - Created `.github/workflows/claude-review.yml`
- [ ] Testing - Create PR and verify behavior
- [ ] Documentation

## Implementation Notes
- Using `anthropics/claude-code-action@v1`
- Automatic review on PR creation/update
- Also responds to `@claude` mentions in comments
- **Required Setup**: Add `ANTHROPIC_API_KEY` in Repository Settings > Secrets
- **Required Permission**: `id-token: write` is needed for OIDC authentication with Anthropic API
