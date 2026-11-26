# KEELL Official (keell-official)

KEELL（キール）をClaudeから使うための、KEELL公式のプラグインです。Skill `keell` を1つ含みます。

- KEELLのタスク・ストリーム・テンプレート・レポートを、正確な日付（日本時間）で、確認を取りながら操作する
- KEELLの仕様（権限、定期作成、マイタスクの公開範囲など）について、同梱の参考ファイルをもとに答える

使うには、KEELLのコネクタ（MCP）をつないでおく必要があります。KEELLのStandardプラン（トライアル中を含む）で使えます。

手順・使い方：https://github.com/keelljp/keell-skills

## About (English)

This is the official plugin from KEELL Inc. for using KEELL, a task and workflow management service, from Claude. It contains one skill, `keell`, which teaches Claude how to work with KEELL tasks, streams, templates and reports through the KEELL MCP connector.

With this plugin, Claude can:

- List tasks due today or this week, and overdue tasks, using the correct dates in Japan Standard Time
- Create, complete, skip and reschedule tasks, asking for confirmation before making changes
- Start a stream from a template as a draft, then publish it after you check it
- Summarize how far a stream has progressed, and review reports such as working time and waiting time
- Answer questions about how KEELL works (permissions, recurring tasks, visibility of My Tasks)

### Setup

1. Connect the KEELL connector (MCP) to Claude and sign in with your KEELL account. A KEELL Standard plan (including the free trial) is required.
2. Install this plugin. In Claude Code, run `/plugin marketplace add keelljp/keell-skills` and then `/plugin install keell-official@keell-skills`.

Then ask Claude things like "Show me my KEELL tasks due today". Full documentation (in Japanese) is at https://github.com/keelljp/keell-skills.

© 株式会社KEELL / Apache License 2.0
