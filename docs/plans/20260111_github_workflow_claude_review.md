# GitHub Workflow: Claude AI Review

## Overview
PRに対してClaude AIによる自動コードレビューを実行するGitHub Actionsワークフローを追加する。

## Background
- PRのコードレビュー品質を向上させたい
- 人間のレビュー前にAIが基本的な問題を検出
- Plan Stackのドッグフーディング（自分たちのプロダクトで使う）

## Research Required
- [ ] Claude GitHub Action の公式実装を調査
  - https://github.com/anthropics/claude-code-action
  - または anthropic API を直接使用するカスタム実装
- [ ] 必要な secrets (ANTHROPIC_API_KEY) の設定方法
- [ ] レビュー対象のファイルパターン設定

## Implementation Options

### Option A: claude-code-action (公式)
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

### Option B: カスタム実装
- Anthropic API を直接呼び出すスクリプト
- より細かいカスタマイズが可能

## Acceptance Criteria
- [ ] PRが作成/更新されたときに自動でレビューが実行される
- [ ] レビューコメントがPRに投稿される
- [ ] API キーが secrets で安全に管理されている

## Files to Create/Modify
- `.github/workflows/claude-review.yml` (新規作成)

## Questions
- レビューの対象範囲は？（全ファイル or 特定パターン）
- レビューのトーン/厳しさは？
- 日本語でレビューするか英語か？

## Status
- [x] Research - claude-code-action v1 を採用
- [x] Implementation - `.github/workflows/claude-review.yml` 作成
- [ ] Testing - PR作成して動作確認
- [ ] Documentation

## Implementation Notes
- `anthropics/claude-code-action@v1` を使用
- PR作成/更新時に自動レビュー
- `@claude` メンションでコメントにも対応
- **必要な設定**: Repository Settings > Secrets > `ANTHROPIC_API_KEY` を追加
