# 小红书封面制作 Skill

[简体中文](./README.md) | [English](./README.en.md) | 日本語

> 👉 こちらもどうぞ [小红书文案 Skill](https://github.com/beatra-ai/xiaohongshu-copywriter-skill)

写真 1 枚やテーマから、クリーンな背景、はっきりした主役、文字を置ける余白を備えた縦型 3:4 の小紅書カバーを作成。美容、グルメ、ファッション、ライフスタイル投稿向け。Claude Code、Cursor、Codex、Windsurf、Cline、OpenClaw のどれからでもそのまま使えます。

> [!IMPORTANT]
> 生成には [Beatra](https://beatra.ai?utm_source=github&utm_medium=flagship&utm_campaign=xiaohongshu-cover-maker-skill) アカウントが必要で、クレジットを消費します。スキル自体のインストールは無料です。

| 項目 | 内容 |
| --- | --- |
| **できること** | 写真1枚やテーマのアイデアから、スクロールを止める縦型 3:4 の小紅書（REDnote）カバーを作成。クリーンな背景、際立つ構図、テキストスペースを確保し、美容、グルメ、ファッション、ライフスタイル投稿に対応。 |
| **モデル** | Qwen Image 2.0 Fast、Qwen Image 3.0、Qwen Image 3.0 Pro、Wan Image 2.7 Fast、Qwen Image 2.0 Pro、Wan Image 2.7 Pro、GPT Image 2.5 Flare、GPT Image 2.5 Sunburst、GPT Image 2、MiniMax Image 01 Live |
| **動作要件** | Python 3.10 以上と、`SKILL.md` を読み込めるエージェント |
| **費用** | インストールは無料。生成のたびに Beatra アカウントのクレジットを消費しますが、課金されるのは、その生成を明示的に依頼したとき、または確認カードを承認したときだけです。 |
| **対応エージェント** | Claude Code、Cursor、Codex、Windsurf、Cline、OpenClaw |

<p align="center"><img src="assets/hero.webp" width="800" alt="テーマのブリーフから生成した縦型 3:4 の小紅書ノートカバー 3 枚：ノーブランドの美容液ボトルを置いたスキンケアのフラットレイに見出し「干皮秋冬护肤清单」、卵トースト・アボカド・トマトの朝食に「15分钟快手早餐」、モデルなしの通勤コーデのフラットレイに「通勤穿搭一周不重样」。Beatra AI で生成。"></p>

*テーマのブリーフから生成した縦型 3:4 の小紅書ノートカバー 3 枚：ノーブランドの美容液ボトルを置いたスキンケアのフラットレイに見出し「干皮秋冬护肤清单」、卵トースト・アボカド・トマトの朝食に「15分钟快手早餐」、モデルなしの通勤コーデのフラットレイに「通勤穿搭一周不重样」。Beatra AI で生成。*

| Skill | Entry point | Version |
| --- | --- | --- |
| [`zhongcao-cover-maker`](skills/zhongcao-cover-maker) | [SKILL.md](skills/zhongcao-cover-maker/SKILL.md) | 0.2.9 |

このリポジトリは [beatra-ai/beatra-skills](https://github.com/beatra-ai/beatra-skills/tree/main/skills/zhongcao-cover-maker) から自動的に公開されています。問題の報告はそちらへお願いします。

## インストール

[`skills`](https://skills.sh) CLI を使う場合：

```bash
npx skills add beatra-ai/xiaohongshu-cover-maker-skill
```

GitHub CLI を使う場合：

```bash
gh skill install beatra-ai/xiaohongshu-cover-maker-skill zhongcao-cover-maker
```

または、このリポジトリをクローンして `skills/zhongcao-cover-maker` を次の場所にコピーします：Claude Code は `~/.claude/skills/`、Cursor は `~/.cursor/skills/`、Codex は `~/.agents/skills/`、Windsurf は `~/.codeium/windsurf/skills/`、Cline は `~/.cline/skills/`、OpenClaw は `~/.openclaw/skills/`。

または、次の文をエージェントに貼り付けてください：

```text
https://github.com/beatra-ai/xiaohongshu-cover-maker-skill から zhongcao-cover-maker スキル（フォルダ skills/zhongcao-cover-maker）をインストールし、その SKILL.md に従って私の Beatra アカウントに接続してください。
```

## 技術仕様と出力上限

2026-10-18 時点。最新の一覧：https://docs.beatra.ai/ja/docs/models

- **アップロード** — 1 ファイルあたり最大 100 MB。下記の各モデルの入力制限も適用されます
- **画像から画像** — 10 モデル（Qwen Image 2.0 Fast、Qwen Image 3.0、Qwen Image 3.0 Pro、Wan Image 2.7 Fast、Qwen Image 2.0 Pro、Wan Image 2.7 Pro、GPT Image 2.5 Flare、GPT Image 2.5 Sunburst、GPT Image 2、MiniMax Image 01 Live）／PNG／1 リクエストあたり最大 4 枚／キャンバス最大 16.8 MP
  - 16.8 MP（4K ティア）：GPT Image 2.5 Flare、GPT Image 2.5 Sunburst、GPT Image 2（1 リクエストにつき 1 枚）
  - 入力画像：1 リクエストあたり最大 4 枚、各 10〜20 MB／BMP、GIF、JPEG、PNG、TIFF、WEBP
- **テキストから画像** — 10 モデル（Qwen Image 2.0 Fast、Qwen Image 3.0、Qwen Image 3.0 Pro、GPT Image 2.5 Flare、GPT Image 2.5 Sunburst、GPT Image 2、Wan Image 2.7 Fast、Qwen Image 2.0 Pro、Wan Image 2.7 Pro、MiniMax Image 01 Live）／PNG／1 リクエストあたり最大 4 枚／キャンバス最大 16.8 MP
  - 16.8 MP（4K ティア）：Wan Image 2.7 Pro（1 リクエストあたり最大 4 枚）／GPT Image 2.5 Flare、GPT Image 2.5 Sunburst、GPT Image 2（1 リクエストにつき 1 枚）
- **画像編集** — 6 モデル（Qwen Image 2.0 Fast、Qwen Image 3.0、Qwen Image 3.0 Pro、Wan Image 2.7 Fast、Qwen Image 2.0 Pro、Wan Image 2.7 Pro）／PNG／1 リクエストあたり最大 4 枚／キャンバス最大 4.2 MP
  - 4.2 MP（2K ティア）：Qwen Image 2.0 Fast、Qwen Image 3.0、Qwen Image 3.0 Pro、Wan Image 2.7 Fast、Qwen Image 2.0 Pro、Wan Image 2.7 Pro（1 リクエストあたり最大 4 枚）
  - 入力画像：1 リクエストあたり最大 4 枚、各 10〜20 MB／BMP、GIF、JPEG、PNG、TIFF、WEBP

## 得られるもの

- **フィードのために設計** — 縦型3:4カバーは小紅書のデュアルカラムウォーターフォールレイアウトでより大きな表示スペースを占め、目に留まりやすくなります。
- **テキストスペース確保** — すべてのカバーにクリーンなテキストスペース（上部3分の1、中央、下部）を確保。大胆な見出しテキストが画像と干渉せずに配置できます。
- **カテゴリー別スタイリング** — 美容は明るくエアリー、グルメは温かく食欲をそそる、ファッションはエディトリアルでミニマル。カバーがコンテンツカテゴリーのビジュアル言語に合わせて調整されます。

## 活用シーン

- **美容・スキンケアカバー** — 明るくクリーンなソフトフォーカス背景、パステルカラー、自然な肌質。商品レビュー、チュートリアル、ルーティン共有に最適。
- **グルメ・カフェカバー** — 温かく食欲をそそるグルメ写真。浅い被写界深度、自然な窓光、料理が主役。
- **ファッション・OOTDカバー** — エディトリアル構図、全身または半身、クリーンな都市やスタジオ背景、強いカラーコーディネート。
- **知識・Tipsカバー** — クリーンなフラットレイアウト、高コントラスト、インフォグラフィック対応構成。大胆な見出しテキスト用のスペースを確保。

## よくある質問

### グルメ写真からカバーを作れますか？

はい。グルメ写真をアップロードすると、温かく食欲をそそる縦型カバーに変換されます。浅い被写界深度、自然な照明、料理が主役として配置されます。

### 写真なしでカバーを生成できますか？

はい。ノートのテーマとスタイルの方向性を説明すると、その説明からカバーが生成されます。縦型3:4キャンバスとテキストスペース付き。

### 見出しテキスト用のスペースはありますか？

はい。すべてのカバーにクリーンなテキストスペース（上部3分の1、中央、下部）が確保されており、大胆な見出しオーバーレイを画像と干渉せずに追加できます。

### 選んだカバーの特定のエリアを修正できますか？

はい。選んだカバーをアップロードし、修正したい箇所（邪魔なオブジェクト、色温度、傷）を指定すると、そのエリアだけが編集され、他の部分は変わりません。

## 更新とセキュリティ

2026 年 10 月のリリース以降、このスキルに自動更新機能はありません。インストールしたファイルだけを実行し、
自動的に置き換えることはありません。更新はインストールに使ったツール（`npx skills update zhongcao-cover-maker` または
`gh skill update zhongcao-cover-maker`）で行ってください。詳細はスキル内の `references/updates-and-security.md` を参照してください。

## ライセンス

[MIT-0](LICENSE)：商用を含め、自由に使用・改変・再配布できます。クレジット表記は不要です。ClawHub 上のこれらのスキルと同じ条件です。

## リンク

- ウェブサイト — https://beatra.ai?utm_source=github&utm_medium=flagship&utm_campaign=xiaohongshu-cover-maker-skill
- ドキュメント — https://docs.beatra.ai?utm_source=github&utm_medium=flagship&utm_campaign=xiaohongshu-cover-maker-skill
- コンソール — https://console.beatra.ai
- AI エージェント向け — https://beatra.ai/llms.txt （インデックス）· https://beatra.ai/llms-full.txt （全スキルを 1 ファイルに）
