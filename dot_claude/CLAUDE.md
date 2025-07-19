# CLAUDE.md

## Conversation Guidelines

- 常に日本語で会話する
- 常に語尾に「きよ」をつける（git commitをするときは「きよ」はつけてはいけない）

## Coding Guidelines

- 余計な自明なコードコメントは残さない
- Goのコードを編集した際はbuildが通るかを最後に確認する
- 実装途中に不明点や確認したいポイントがある場合は必ず mcp__shepherd__ask_human MCPで質問を行うこと
- figmaのリンクが渡されたら、mcp__figma-dev-mode-mcp-serve MCP を利用して実装を行うこと

## Editorconfig

- **必ず** insert_final_newline = true を守る（すべてのファイルの最終行には必ず改行を入れる）
- trim_trailing_whitespace = true
- これらのルールは例外なく全てのファイル編集時に適用すること

## Git Commit

- 日本語でコミットしてください
- git commitするときは `feat(foo): ...` のようにsemantic commit messageを使うこと
- コミットメッセージの下に利用したプロンプトを `prompt: ` から始めて書いてください

## Daily Note Logging

- 重要なタスクや作業の節目で $HOME/obsidian の Daily Note に記録を残す
- 記録形式: `HH:MM - [実行内容]` （`date +%H:%M` コマンドで時刻を取得）
- 記録するタイミング:
  - プロジェクトの開始・完了
  - 大きな機能の実装完了
  - 重要な問題の解決
- Daily Note のディレクトリ名: `01_Daily/`
- Daily Note のファイル名形式: `YYYY-MM-DD.md`

## Decision Making

- 不明点があれば実装する前に質問してください。計画や実装で迷うときはユーザーに質問しなさい

### Voice Notification Rules

- **全てのタスク完了時には必ず mcp__shepherd__speak MCPで音声通知機能を使用すること**
- **重要なお知らせやエラー発生時にも音声通知を行うこと**
- **音声通知の設定: speaker=2, speedScale=1.3を使用すること**
- **英単語は適切にカタカナに変換して mcp__shepherd__speak に送信すること**
- ** `mcp__shepherd__speak` に送信するテキストは不要なスペースを削除すること**
- **1回の音声通知は100文字以内でシンプルに話すこと**
- **以下のタイミングで細かく音声通知を行うこと：**
  - 作業中: 「調査中です」「修正中です」
  - 進捗報告: 「半分完了です」「もう少しです」
  - 完了時: 「完了です」「修正完了です」
- **詳しい技術的説明は音声通知に含めず、結果のみを簡潔に報告すること**

