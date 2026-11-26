# Skillを入れる

先に [コネクタをつないで](setup-connector.md) おいてください。

## Claude（Web・デスクトップ・モバイル）

1. [keell.zip](https://github.com/keelljp/keell-skills/releases/latest/download/keell.zip) をダウンロードする（解凍しない）
2. Claudeで「カスタマイズ → Skills」を開く
3. 「＋」→「Skillを作成」→「Skillをアップロード」を選び、keell.zip をアップロードする
4. 一覧に `keell` が表示され、オンになっていることを確かめる

Skillを使うには、設定で「コード実行とファイル作成」がオンになっている必要があります。Webやデスクトップで入れたSkillは、同じアカウントのモバイルアプリやClaude Codeでも使えます。

### 新しい版に入れ替える

1. 「カスタマイズ → Skills」で、いまの `keell` を削除する
2. 新しい keell.zip をダウンロードし、上の手順3からアップロードする

いま入っている版は、Skillの中身の末尾（例：`v0.2.0（2026-11-19）`）で確かめられます。最新版は [Releases](https://github.com/keelljp/keell-skills/releases) と [CHANGELOG](../CHANGELOG.md) で確かめられます。

### Team・Enterpriseプランで組織に配る

オーナーが keell.zip を組織のSkillとして追加すると、メンバー全員が使えるようになります。版を上げたときも、オーナーが入れ替えれば全員に反映されます。

## Claude Code

マーケットプレイスとして追加し、プラグインを入れます。

```text
/plugin marketplace add keelljp/keell-skills
/plugin install keell@keell-skills
```

更新するとき：

```text
/plugin marketplace update keell-skills
```

ターミナルから入れる場合は `claude plugin marketplace add keelljp/keell-skills` → `claude plugin install keell@keell-skills` です。

## 入ったかを確かめる

Claudeに「KEELLで今日が期限のタスクを教えて」と頼みます。ワークスペースを確かめ、期限の近い順に表で返ってくれば、Skillが使われています。

Skillが使われていないようなら、「keellのSkillを使って、今日のタスクを教えて」のように名前を出して頼んでください。
