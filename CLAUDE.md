# このリポジトリについて

> **最優先ルール①：作業開始前に SKILLS を優先して読み込むこと。**
> **最優先ルール②：並列で作業できる場合は、並列でエージェントを動かすこと。**

**GitHub Pages リポジトリ** — 静的HTMLファイルを直接プッシュして公開する。React/Next.js等は使わない。

- **リポジトリ:** https://github.com/YamaBookHub/daini-vonheur-lp
- **公開URL:** https://yamabookhub.github.io/daini-vonheur-lp/[ファイル名].html
- **ローカルパス:** `/Users/yamabook/Desktop/daini-vonheur-lp/`

---

## LP制作 役割・フロー

**制作担当：やまbook（Claude）**
- 渡された情報をもとに制作するのみ
- 社長とは直接やりとりしない
- 折衝担当（メイちゃん）から情報を受け取り、成果物を渡す

**折衝担当：メイちゃん**
- 社長ヒアリング・承認を担当
- 各CPの承認を取り、決まった内容を制作担当に渡す

### チェックポイント（CP）

| CP | 内容 | 状態 |
|---|---|---|
| CP0 | ベクトル合わせ（参考LP構成で進める） | ✅ 一部完了 |
| CP1 | 情報収集（ターゲット/ストーリー/料金/写真） | ⬜ 待ち |
| CP2 | 方向性承認（思想・構成・ターゲット） | ⬜ |
| CP3 | コピー承認（全セクション文言） | ⬜ |
| CP4 | 見た目承認（実ページ・スマホ表示） | ⬜ |
| CP5 | 公開（ボタン確認・社長GO・デプロイ） | ⬜ |

**現在：CP1待ち。メイちゃんから以下が揃ったら制作開始：**
- ターゲット・悩み言葉
- 社長のストーリー・思想の素材
- 料金・プラン・実績データ
- 写真・素材

---

## 絶対ルール
- **itabashi-v1.html は絶対に触らない**（指標・バックアップ。読み取り専用扱い）
- V2（itabashi-v2.html）が作業版

---

## ファイル構成

| ファイル | 内容 |
|---|---|
| `index-v3.html` | 第弐ヴォヌール LP v3（現行メイン） |
| `index-v4.html` | v4 |
| `index-v5.html` | v5 |
| `itabashi.html` | 板橋インスタサポート LP（完全コピー） |
| `checkpoint.html` | LP制作チェックポイント |
| `copy.md` | LP用コピー原稿 |
| `images/` | 画像素材 |

---

## 作業ルール

### デプロイ
- `git add → commit → push` を**確認なしで即実行**してよい（ユーザーから明示許可済み）
- デプロイは push するだけで GitHub Pages が自動反映

### コピーライティング
- 他社比較表現（「〜と違い」「大手に比べて」等）は**禁止**
- 自社の強みは事実だけで語る

### LP バージョン戦略
- `v1-simple` = 応急処置用バックアップ。触らない
- `v2-draft` 以降 = 本命の完成系方向。こちらをベースに作業
- バージョンは `index-v[N].html` で管理

### トークン節約
- ファイルは必要な部分だけ読む
- 返答は短く簡潔に

### 効率化ルール（実作業で詰まった教訓）
1. **Python編集は必ずファイル経由（`/tmp/*.py`）＋先頭に `# -*- coding: utf-8 -*-`**
   - `python3 -c "..."` に日本語直書きはエンコーディングエラーで失敗する。スクリプトをWriteしてから実行する。
2. **スマホ確認は 390px の iframe ＋ DOM実測（getComputedStyle / getBoundingClientRect）で行う**
   - `resize_window` は効かず、スクショAPIも不安定。iframe埋め込み＋計測が唯一安定して確認できる方法。
3. **コピー（文言）変更は「実装前に案を提示 → OKをもらってから反映」**
   - 勝手に変えると手戻りになる。特にキャッチ・見出し。
4. **GitHub Pages は反映に数秒〜十数秒の遅延。確認時は必ずキャッシュバスター（`?cb=<時刻>`）を付ける**
5. **数値・実績は「実在するもの」のみ掲載。ただし会社情報に記載の実績（例：自社初投稿20万インプ）は事実なので使用可**
6. **編集後は「完了」と言う前に、ローカル＋リモート両方を grep で検証する**

---

## クライアント情報：株式会社第弐ヴォヌール

- **規模:** 4名の少数精鋭SNSマーケ代理店
- **拠点:** 東京都板橋区
- **設立:** 2023年11月
- **事業:** Instagram/TikTok運用代行、ショート動画制作、販売導線設計、Makuakeクラウドファンディング、TikTok LIVE/Shop
- **強み:** 社長（CM撮影業界出身）直接対応、SNS×動画×販売導線の一気通貫、中小向け価格
- **詳細:** `/Users/yamabook/Downloads/daini_vonheur_company_prompt.md`

---

## 板橋インスタサポート LP（itabashi.html）

元サイト: https://itabashi-insta-bsvu9feo.manus.space/

- 運営: 階方くるみ・鈴木藍里（板橋在住ママ2名）
- ブランド: @itabashi_mama（Instagram）
- 内容: Instagram運用代行サービスのLP
- 画像ホスト: `https://d2xsxph8kpxj0f.cloudfront.net/310519663071634244/Bsvu9FEoJBBT43dB4xqDWE/`
- カラー: #FAFAF7（背景）/ #2A2520（テキスト）/ #E8B84B（ゴールド）/ #89C4D4（ブルー）/ #E07A5F（コーラル）
- フォント: Shippori Mincho / Noto Sans JP / DM Serif Display

---

## もう一つのリポジトリ（混同注意）

`/Users/yamabook/marketing-site/` は別プロジェクト（Next.js、Vercel連携）。
このLP作業はそこではなく **必ずこの `daini-vonheur-lp/` リポジトリ** で行う。
