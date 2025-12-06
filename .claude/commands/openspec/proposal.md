---
name: "OpenSpec: 提案"
description: 新しいOpenSpec変更をスキャフォールドし、厳密に検証します。
category: OpenSpec
tags: [openspec, change]
---
<!-- OPENSPEC:START -->
**ガードレール**
- まずシンプルで最小限の実装を優先し、リクエストされた場合または明らかに必要な場合にのみ複雑さを追加する。
- 変更はリクエストされた結果に厳密にスコープを絞る。
- 追加のOpenSpec規約や明確化が必要な場合は`openspec/AGENTS.md`（`openspec/`ディレクトリ内にあります—見つからない場合は`ls openspec`または`openspec update`を実行）を参照する。
- 曖昧または不明確な詳細を特定し、ファイルを編集する前に必要なフォローアップの質問をする。
- 提案段階ではコードを書かない。設計ドキュメント（proposal.md、tasks.md、design.md、スペックデルタ）のみを作成する。実装は承認後のapply段階で行う。

**手順**
1. `openspec/project.md`を確認し、`openspec list`と`openspec list --specs`を実行し、関連するコードやドキュメント（例：`rg`/`ls`経由）を調査して、提案を現在の動作に基づかせる；明確化が必要なギャップをメモする。
2. 一意の動詞で始まる`change-id`を選択し、`openspec/changes/<id>/`の下に`proposal.md`、`tasks.md`、および`design.md`（必要な場合）をスキャフォールドする。
3. 変更を具体的な機能または要件にマッピングし、複数スコープの作業を明確な関係と順序を持つ個別のスペックデルタに分割する。
4. ソリューションが複数のシステムにまたがる場合、新しいパターンを導入する場合、またはスペックにコミットする前にトレードオフの議論が必要な場合は、`design.md`にアーキテクチャの理由を記録する。
5. `changes/<id>/specs/<capability>/spec.md`（機能ごとに1つのフォルダ）にスペックデルタを作成し、`## ADDED|MODIFIED|REMOVED Requirements`を使用して要件ごとに少なくとも1つの`#### Scenario:`を含め、関連する場合は関連機能を相互参照する。
6. `tasks.md`を、ユーザーに見える進捗を提供する小さく検証可能な作業項目の順序付きリストとして作成し、検証（テスト、ツーリング）を含め、依存関係や並列化可能な作業を強調する。
7. `openspec validate <id> --strict`で検証し、提案を共有する前にすべての問題を解決する。

**参考**
- 検証が失敗した場合は`openspec show <id> --json --deltas-only`または`openspec show <spec> --type spec`を使用して詳細を確認する。
- 新しい要件を書く前に`rg -n "Requirement:|Scenario:" openspec/specs`で既存の要件を検索する。
- `rg <keyword>`、`ls`、または直接ファイル読み取りでコードベースを探索し、提案が現在の実装の現実に沿うようにする。
<!-- OPENSPEC:END -->
