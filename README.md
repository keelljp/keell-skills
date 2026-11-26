# KEELL Skills

KEELL（キール）をClaudeから使うための、KEELL公式のSkillです。

KEELLのコネクタ（MCP）をつなぐと、Claudeから KEELL のタスクやストリームを確認・作成・更新できるようになります。このSkillを入れておくと、Claudeが KEELL の用語・日付の扱い・安全な操作の手順を知った状態で動くため、「今日のタスクを教えて」と頼むだけで、正しい期限で、確認を取りながら操作できます。

> KEELLとは：タスク（担当者の視点）とフロー（管理者の視点）を一元管理する業務管理ツールです。→ [KEELL](https://keell.jp/saas)

## このSkillでできること

- 今日・今週が期限のタスク、期限切れのタスクを一覧にする
- KEELLの仕様（権限、定期作成、マイタスクの公開範囲など）について答える
- タスクを作る・完了にする・スキップする・期限をまとめてずらす
- テンプレートからストリームを起動する（下書きで作り、確認してから公開）
- ストリームの進み具合（完了・着手できる・待ち）をまとめる
- レポート（作業時間・待ち時間など）を確認する

依頼の例は [使い方](docs/usage.md) にまとめています。

## はじめかた

必要なもの：

- KEELLのStandardプラン（トライアル中も使えます。無料プランでは使えません）
- Claudeのアカウント（カスタムコネクタとSkillを使います。Skillを使うには、設定で「コード実行とファイル作成」をオンにします）

手順は2つです。

1. **KEELLのコネクタをつなぐ**（Claudeの「カスタマイズ → コネクタ → 探索」で「KEELL」を検索） → [Claudeにコネクタをつなぐ](docs/setup-connector.md)
2. **このSkillを入れる** → [Skillを入れる](docs/install-skill.md)

### いちばん早い入れ方

| 使っているもの | 入れ方 |
|---|---|
| Claude（Web・デスクトップ・モバイル） | [keell.zip](https://github.com/keelljp/keell-skills/releases/latest/download/keell.zip) をダウンロードし、「カスタマイズ → Skills →「＋」→ Skillを作成 → Skillをアップロード」 |
| Claude Code | `/plugin marketplace add keelljp/keell-skills` → `/plugin install keell@keell-skills` |

## 更新

このリポジトリのSkillは、KEELLの機能追加や、実際に使って分かったことにあわせて更新していきます。変更点は [CHANGELOG](CHANGELOG.md) に書きます。

- Claude（Web・デスクトップ）：新しい keell.zip をダウンロードし、古い keell を削除してからアップロードし直してください
- Claude Code：`/plugin marketplace update keell-skills` で更新できます

GitHubの「Watch → Custom → Releases」を設定すると、新しい版が出たときに通知が届きます。

## ドキュメント

- [Claudeにコネクタをつなぐ](docs/setup-connector.md)
- [Skillを入れる](docs/install-skill.md)
- [使い方（依頼の例）](docs/usage.md)
- [よくある質問・うまくいかないとき](docs/faq.md)

KEELLそのものの使い方は [KEELL利用ガイド](https://doc.keell.jp/) をご覧ください。

## リポジトリの構成

```
.claude-plugin/marketplace.json   Claude Code のマーケットプレイス定義
plugins/keell/                    KEELLのプラグイン
  .claude-plugin/plugin.json
  skills/keell/SKILL.md           Skill本体
  skills/keell/references/        KEELLの仕様の参考ファイル（必要なときだけ読まれる）
docs/                             利用者向けのドキュメント
```

Skill本体は `plugins/keell/skills/keell/` の1か所だけです。keell.zip は、版を出すたびにこのフォルダから自動で作られます。

## ご意見・不具合

うまく動かない依頼や、こう動いてほしいという要望は、[Issues](https://github.com/keelljp/keell-skills/issues) からお寄せください。タスク名や顧客名など、業務の情報は書かないでください。

## ライセンス

[Apache License 2.0](LICENSE)

© 株式会社KEELL
