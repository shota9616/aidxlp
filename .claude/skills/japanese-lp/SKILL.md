---
name: japanese-lp
description: 日本市場向け高CVランディングページ制作スキル。LP、ランディングページ、セールスページ、商品ページ、サービス紹介ページの制作時に使用。PASONAの法則に基づく縦長構成、信頼要素（実績バッジ、お客様の声）、日本語フォント、CTAボタンの色心理学を適用し、シリコンバレー的ミニマルデザインを回避して日本市場で「受ける」LPを生成する。
---

# 日本LP制作スキル

日本市場向けの高コンバージョンランディングページを制作するためのスキル。

## 重要な原則

**絶対に避けること（AI slop）:**
- シリコンバレー的ミニマルデザイン
- 情報量の少ない「おしゃれ」なページ
- CTAボタン1箇所のみ
- 抽象的なキャッチコピー
- Inter、Roboto、Arial等の欧文フォント中心のデザイン

**必ず実現すること:**
- 縦長のセールスレター型構成
- 3秒で価値が伝わるファーストビュー
- 複数のCTAボタン配置（最低3箇所）
- 具体的な数字を使った実績訴求
- 日本語Webフォントの適切な使用

## 制作フロー

1. 要件確認（ターゲット、ゴール、実績データ）
2. 構成設計（references/structure.md参照）
3. コンポーネント配置（references/components.md参照）
4. デザイン適用（references/design-rules.md参照）
5. レスポンシブ対応（モバイルファースト）

## クイックリファレンス

### 構成（PASONAの法則）
```
1. Problem    - 悩み・課題の明確化
2. Affinity   - 共感（私も同じでした）
3. Solution   - 解決策としての商品紹介
4. Offer      - 具体的なオファー内容
5. Narrowing  - 限定性・緊急性
6. Action     - CTAで行動促進
```

### 必須セクション（省略禁止）
- ファーストビュー（キャッチコピー + ビジュアル + CTA + 実績バッジ）
- お悩み共感セクション
- 選ばれる3つの理由
- お客様の声（写真 + 具体的成果）
- 料金プラン
- よくある質問（FAQ）
- 限定オファー + 最終CTA

### CTAボタン
- 色: オレンジ(#FF6B35) または 緑(#28A745)
- 配置: ファーストビュー、中間、最下部の最低3箇所
- 文言: 「無料で相談する」「今すぐ申し込む」等、行動を促す

### フォント
```css
/* 本文 */
font-family: 'Noto Sans JP', sans-serif;
font-weight: 400; /* Regular */

/* 見出し */
font-family: 'Noto Sans JP', sans-serif;
font-weight: 700; /* Bold */

/* アクセント（親しみやすさ重視の場合） */
font-family: 'M PLUS Rounded 1c', sans-serif;
```

### 信頼バッジ
- 色: ゴールド系(#D4AF37, #B8860B)
- 内容例: 「〇〇No.1」「導入実績〇〇社」「満足度〇〇%」
- 配置: ファーストビュー内、目立つ位置

## 詳細リファレンス

より詳細な情報が必要な場合は以下を参照:

- **構成パターン詳細**: references/structure.md
- **コンポーネント仕様**: references/components.md  
- **デザインルール詳細**: references/design-rules.md

## 出力形式

### HTML/CSS（推奨）
- Tailwind CSS使用推奨
- レスポンシブ対応必須
- Google Fonts経由で日本語フォント読み込み

### React/Next.js
- コンポーネント分割して再利用性確保
- Tailwind CSS + shadcn/ui可

### Figma連携時
- Figma MCPでデザイン反映
- Auto Layoutでレスポンシブ対応
