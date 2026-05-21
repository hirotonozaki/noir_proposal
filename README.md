[README.md](https://github.com/user-attachments/files/28082375/README.md)
# NOIR MEN'S CLINIC ｜ Web Production Proposal

男性向けメディカル・エステティッククリニック「NOIR MEN'S CLINIC」公式サイトの **制作企画書** です。
全 9 ページの企画書を HTML / CSS のみで構築し、ブラウザでそのまま閲覧・ブラウザの印刷機能から A4 PDF として書き出しできます。

> **Quiet Luxury — 静かな高級感。**
> 黒の余白とゴールドの輝きで、語りすぎないラグジュアリーを表現したコーポレートサイトの制作企画書です。

---

## 関連リンク

| 種別 | URL |
| --- | --- |
| **公式サイト（実装版）** | https://hirotonozaki.github.io/noir-clinic-main/ |
| **GitHub リポジトリ（実装版）** | https://github.com/hirotonozaki/noir-clinic-main |
| 企画書（本リポジトリ） | https://github.com/hirotonozaki/noir_proposal |

> 本企画書で提案しているサイトは、オリジナル WordPress テーマとして設計・実装しています。
> 実装版のソースコードと公開URLは上記をご参照ください。

---

## 概要

| 項目 | 内容 |
| --- | --- |
| 種別 | クリニック／コーポレートサイトの制作企画書 |
| 構成 | A4 縦・全 9 ページ |
| 技術 | HTML5 / CSS3（外部ライブラリ不使用） |
| フォント | Cormorant Garamond / Noto Serif JP / Noto Sans JP（Google Fonts） |
| 出力 | ブラウザの印刷機能から A4 PDF として保存可能 |
| 担当範囲 | 企画・情報設計・デザイン・コーディング |

---

## ページ構成

| No. | セクション | 内容 |
| --- | --- | --- |
| 00 | 目次・制作概要 | プロジェクトの目的と前提 |
| 01 | 制作概要 | プロジェクト基本情報 |
| 02 | ターゲット・課題設定 | ペルソナと解決すべき 4 つの課題 |
| 03 | デザインコンセプト | 黒 × ゴールドの配色・タイポグラフィ |
| 04 | 情報設計・サイト構成 | サイトマップと導線設計 |
| 05 | 主要ページ・機能 | 予約フォーム・症例・施術メニュー |
| 06 | WordPress テーマ設計 | template-parts 分割と運用性 |
| 07 | 使用技術・工夫した点 | 技術スタックと実装上の工夫 |
| 08 | 完成イメージ・アクセス情報 | モックアップ・QR・GitHub リポジトリ・今後の改善点 |

---

## ファイル構成

```
noir_proposal/
├── index.html               企画書のマークアップ（全9ページ）
├── noir_proposal.pdf        A4書き出し済みの提出用PDF
├── README.md
├── css/
│   └── style.css            スタイル定義（A4ページ設計・配色・レイアウト）
└── assets/
    └── images/
        ├── preview.png      サイトモックアップ（PC・スマートフォン）
        └── qrcode.jpg       公式サイト QR コード
```

`index.html` から `css/style.css` および `assets/images/` 配下の画像を参照する構成です。
この位置関係を保ったままご確認ください。

---

## 閲覧方法

### 1. ブラウザで企画書を確認する

リポジトリをクローン、または ZIP でダウンロードしたうえで、`index.html` をブラウザで開いてください。

```bash
git clone https://github.com/hirotonozaki/noir_proposal.git
```

外部ライブラリへの依存がないため、`index.html` をブラウザで開くだけで全ページが表示されます。

### 2. PDF として書き出す

画面右上の **「PDFとして保存 / 印刷」** ボタンから、A4・全 9 ページの PDF として書き出せます。
印刷ダイアログでは以下の設定を推奨します。

- 用紙サイズ … **A4**
- 余白 … **なし**
- 背景グラフィック … **有効**

書き出し済みの PDF は `noir_proposal.pdf` としてリポジトリに同梱しています。

---

## スクリーンショット

![NOIR MEN'S CLINIC サイトモックアップ](assets/images/preview.png)

> PC・スマートフォン両デバイスでの表示イメージ — 企画書 08 完成イメージ・アクセス情報ページ より

---

## デザイン仕様

### カラーパレット

| 役割 | 値 | 用途 |
| --- | --- | --- |
| NOIR BLACK | `#0B0B0D` | ベース色・本文 |
| GOLD | `#C9A44C` | アクセント・罫線 |
| GOLD BRIGHT | `#E7C977` | 見出し・CTA |
| WARM PAPER | `#FAF8F3` | 紙面背景 |

すべて `:root` の CSS 変数で一元管理し、ページ全体のトーンを統一しています。

### タイポグラフィ

- **欧文見出し** … Cormorant Garamond（セリフ体・品格と歴史性）
- **和文見出し** … Noto Serif JP（明朝体・医療機関らしい誠実さ）
- **本文** … Noto Sans JP（ゴシック体・可読性）
- **字間** … 広めのトラッキングで余裕と高級感を付与

### レイアウト・印刷対応

- A4 サイズ（210mm × 297mm）を基準にページ単位で設計
- Flexbox / Grid によるモダンなレイアウト
- `@page` および `@media print` でブラウザ PDF 出力に最適化
- 外部 CSS / JS ライブラリ不使用（フォントのみ Google Fonts を読み込み）

---

## 今後の改善案

企画書の最終ページに記載している、提案サイトの発展案です。

- 外部予約システム・カレンダー連携による空き状況のリアルタイム反映
- 症例コンテンツのカテゴリ・悩み別の絞り込み機能
- 画像の遅延読み込み・WebP 化によるパフォーマンス最適化
- コントラスト比・キーボード操作対応などアクセシビリティの向上
- 訪日・在日外国人男性向けの英語ページ追加

---

## 備考

- 本リポジトリの「NOIR MEN'S CLINIC」は、ポートフォリオ用に制作した **架空のクリニック** です。
- 企画書内に記載のサイト URL・ログイン情報は、ポートフォリオ確認用のものです。

---

<sub>Designed & Developed by [@hirotonozaki](https://github.com/hirotonozaki)</sub>
