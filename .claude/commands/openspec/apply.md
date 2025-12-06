---
name: "OpenSpec: 適用"
description: 承認されたOpenSpec変更を実装し、タスクを同期します。
category: OpenSpec
tags: [openspec, apply]
---
<!-- OPENSPEC:START -->
**ガードレール**
- まずシンプルで最小限の実装を優先し、リクエストされた場合または明らかに必要な場合にのみ複雑さを追加する。
- 変更はリクエストされた結果に厳密にスコープを絞る。
- 追加のOpenSpec規約や明確化が必要な場合は`openspec/AGENTS.md`（`openspec/`ディレクトリ内にあります—見つからない場合は`ls openspec`または`openspec update`を実行）を参照する。

**手順**
これらの手順をTODOとして追跡し、1つずつ完了する。
1. `changes/<id>/proposal.md`、`design.md`（存在する場合）、および`tasks.md`を読んで、スコープと受け入れ基準を確認する。
2. タスクを順番に進め、編集を最小限に抑え、リクエストされた変更に焦点を当てる。
3. ステータスを更新する前に完了を確認する—`tasks.md`のすべての項目が完了していることを確認する。
4. すべての作業が完了したらチェックリストを更新し、各タスクが`- [x]`としてマークされ、現実を反映するようにする。
5. 追加のコンテキストが必要な場合は`openspec list`または`openspec show <item>`を参照する。

**参考**
- 実装中に提案から追加のコンテキストが必要な場合は`openspec show <id> --json --deltas-only`を使用する。
<!-- OPENSPEC:END -->
