# ipa-exam-skills

IPA 情報処理技術者試験の対策アプリを、IPA が公開している PDF から作るための Claude Code スキル集です。

| スキル | やること |
|---|---|
| `ipa-exam-app` | 試験区分ごとに、対策アプリ（Django アプリ）を1本作る。苦手な分野を重点的に出題する |
| `ipa-questions` | アプリに取り込む問題と技術解説を、公開 PDF を読んで JSON で作る |

## 使い方

### 1. 資料を集める

受けたい区分の資料を IPA のサイト（https://www.ipa.go.jp/shiken/ ）から落とし、好きなフォルダにまとめます。

- 試験要綱
- シラバス
- 公開問題（サンプル問題・過去問題）と解答例

PDF の読み取りに `pdftotext` を使います。

```bash
brew install poppler
```

Debian/Ubuntu では `sudo apt install poppler-utils`。

### 2. インストール

Claude Code で次を実行します。

```
/plugin marketplace add hirahiratriangle/ipa-exam-skills
/plugin install ipa-exam-skills@ipa-exam-skills
```

### 3. スキルを使う

資料を置いたフォルダで Claude Code を開き、頼むだけです。

```
基本情報技術者試験の対策アプリを作ってください
```

```
セキュリティの問題を30問、解説つきで作ってください
```

資料が別の場所にあるときは、フォルダを添えて頼んでください。資料が足りなければ、何が足りないかを Claude が伝えます。

## 参照実装

基本情報技術者試験版の実装は [hirahira_room の `fe/`](https://github.com/hirahiratriangle/hirahira_room/tree/main/fe) です。

## 注意

作った問題の正解や解説は、必ず IPA の解答例やシラバスと照らし合わせてください。過去問を使うときは、IPA の利用条件に従ってください。

## ライセンス

MIT
