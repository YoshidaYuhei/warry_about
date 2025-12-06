<!-- OPENSPEC:START -->
# OpenSpec 指示書

この指示書はこのプロジェクトで作業するAIアシスタント向けです。

以下のリクエストの場合は常に`@/openspec/AGENTS.md`を開いてください:
- 計画や提案に言及する場合（proposal、spec、change、planなどの単語）
- 新機能、破壊的変更、アーキテクチャの変更、大規模なパフォーマンス/セキュリティ作業を導入する場合
- 曖昧に聞こえ、コーディング前に権威あるスペックが必要な場合

`@/openspec/AGENTS.md`を使用して以下を学習:
- 変更提案の作成と適用方法
- スペックの形式と規約
- プロジェクト構造とガイドライン

'openspec update'が指示を更新できるよう、この管理ブロックを維持してください。

<!-- OPENSPEC:END -->

# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

warry_about - A Python project (currently in initial setup phase).

## Development Setup

This project uses Python. Based on the .gitignore, it may use one of these package managers:
- uv
- poetry
- pdm
- pipenv
- pip with requirements.txt

Once dependencies are defined, install them with the appropriate tool.

## Commands

Commands will be added here as the project develops. Common Python commands include:
- `pytest` - Run tests
- `ruff check .` - Lint code
- `ruff format .` - Format code
