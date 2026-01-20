# 日本LPデザインルール

## フォント

### 日本語Webフォント（Google Fonts）

```html
<!-- head内に追加 -->
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Noto+Sans+JP:wght@400;500;700;900&display=swap" rel="stylesheet">
```

### フォント設定
```css
:root {
  --font-main: 'Noto Sans JP', 'Hiragino Kaku Gothic ProN', 'Hiragino Sans', sans-serif;
  --font-accent: 'M PLUS Rounded 1c', sans-serif; /* 親しみやすさ重視の場合 */
}

body {
  font-family: var(--font-main);
  font-weight: 400;
  font-size: 16px;
  line-height: 1.8;
  color: #333;
}

h1, h2, h3 {
  font-weight: 700;
  line-height: 1.4;
}
```

### サイズ目安（PC）
| 要素 | サイズ | 用途 |
|------|--------|------|
| h1（メインキャッチ） | 36-48px | ファーストビュー |
| h2（セクション見出し） | 28-32px | 各セクションタイトル |
| h3（小見出し） | 20-24px | カード内タイトル等 |
| 本文 | 16px | 通常テキスト |
| キャプション | 12-14px | 補足、注釈 |

### サイズ目安（スマホ）
| 要素 | サイズ |
|------|--------|
| h1 | 24-32px |
| h2 | 22-26px |
| h3 | 18-20px |
| 本文 | 15-16px |

---

## カラー

### 業種別推奨カラー

#### BtoB・コンサル・士業
```css
:root {
  --primary: #2563EB;      /* 青 - 信頼・専門性 */
  --secondary: #1E40AF;
  --accent: #3B82F6;
  --cta: #22C55E;          /* 緑のCTA */
}
```

#### IT・テック
```css
:root {
  --primary: #6366F1;      /* インディゴ */
  --secondary: #4F46E5;
  --accent: #818CF8;
  --cta: #F97316;          /* オレンジのCTA */
}
```

#### 美容・健康・女性向け
```css
:root {
  --primary: #EC4899;      /* ピンク */
  --secondary: #DB2777;
  --accent: #F472B6;
  --cta: #22C55E;          /* 緑のCTA */
}
```

#### 金融・保険
```css
:root {
  --primary: #0D9488;      /* ティール */
  --secondary: #0F766E;
  --accent: #14B8A6;
  --cta: #F97316;          /* オレンジのCTA */
}
```

#### 教育・スクール
```css
:root {
  --primary: #F59E0B;      /* アンバー */
  --secondary: #D97706;
  --accent: #FBBF24;
  --cta: #22C55E;          /* 緑のCTA */
}
```

### CTAボタン色

**最も効果的な色:**
```css
/* オレンジ（最も汎用的、行動促進） */
.cta-orange {
  background: linear-gradient(180deg, #FF8C42 0%, #FF6B35 100%);
}

/* 緑（安心感、BtoB向き） */
.cta-green {
  background: linear-gradient(180deg, #34D399 0%, #22C55E 100%);
}

/* 赤（緊急性、セール向き） */
.cta-red {
  background: linear-gradient(180deg, #F87171 0%, #EF4444 100%);
}
```

**避けるべき色:**
- グレー（押したくならない）
- ページ背景と同系色（溶け込む）
- 青（リンクと混同されやすい）

### 信頼バッジ色
```css
.badge-gold {
  background: linear-gradient(135deg, #D4AF37 0%, #F4E4BA 50%, #D4AF37 100%);
  color: #333;
}

.badge-silver {
  background: linear-gradient(135deg, #C0C0C0 0%, #E8E8E8 50%, #C0C0C0 100%);
  color: #333;
}
```

---

## レイアウト

### コンテナ幅
```css
.container {
  max-width: 1200px;  /* PC */
  margin: 0 auto;
  padding: 0 20px;
}

/* LP専用（読みやすさ重視） */
.lp-container {
  max-width: 900px;   /* やや狭め */
  margin: 0 auto;
  padding: 0 20px;
}
```

### セクション間余白
```css
section {
  padding: 80px 0;    /* PC */
}

@media (max-width: 768px) {
  section {
    padding: 60px 0;  /* スマホ */
  }
}
```

### カード
```css
.card {
  background: #fff;
  border-radius: 12px;
  padding: 24px;
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.08);
}
```

---

## レスポンシブ

### ブレイクポイント
```css
/* スマホ */
@media (max-width: 767px) { }

/* タブレット */
@media (min-width: 768px) and (max-width: 1023px) { }

/* PC */
@media (min-width: 1024px) { }
```

### モバイルファースト原則
```css
/* ベース = スマホ */
.container {
  padding: 0 16px;
}

/* PC以上で変更 */
@media (min-width: 1024px) {
  .container {
    padding: 0 40px;
  }
}
```

### タップ領域
```css
/* ボタン・リンクは最低44px確保 */
.cta-button {
  min-height: 44px;
  padding: 12px 24px;
}

a, button {
  min-height: 44px;
  min-width: 44px;
}
```

---

## アニメーション

### スクロールアニメーション（控えめに）
```css
.fade-in {
  opacity: 0;
  transform: translateY(20px);
  transition: opacity 0.6s ease, transform 0.6s ease;
}

.fade-in.visible {
  opacity: 1;
  transform: translateY(0);
}
```

### CTAボタンホバー
```css
.cta-button {
  transition: transform 0.2s ease, box-shadow 0.2s ease;
}

.cta-button:hover {
  transform: translateY(-2px);
  box-shadow: 0 6px 20px rgba(255, 107, 53, 0.4);
}
```

### 過度なアニメーションは避ける
- パララックス効果は控えめに
- 自動再生動画は避ける
- 点滅・回転は使わない

---

## 画像

### 最適化
```html
<!-- WebP形式推奨 -->
<picture>
  <source srcset="image.webp" type="image/webp">
  <img src="image.jpg" alt="説明" loading="lazy">
</picture>
```

### サイズ目安
| 用途 | 推奨サイズ | 容量目安 |
|------|-----------|---------|
| ファーストビュー | 1200x800px | 150KB以下 |
| お客様の声写真 | 200x200px | 30KB以下 |
| アイコン | 64x64px | 5KB以下 |

### alt属性
```html
<!-- ✗ 悪い例 -->
<img src="hero.jpg" alt="画像">
<img src="customer.jpg" alt="">

<!-- ✓ 良い例 -->
<img src="hero.jpg" alt="補助金申請サポートのイメージ">
<img src="customer.jpg" alt="田中太郎様（株式会社〇〇 代表）">
```

---

## Tailwind CSS設定例

```javascript
// tailwind.config.js
module.exports = {
  theme: {
    extend: {
      colors: {
        primary: '#2563EB',
        secondary: '#1E40AF',
        accent: '#3B82F6',
        cta: {
          orange: '#FF6B35',
          green: '#22C55E',
        },
        badge: {
          gold: '#D4AF37',
        }
      },
      fontFamily: {
        sans: ['Noto Sans JP', 'Hiragino Kaku Gothic ProN', 'sans-serif'],
      },
    },
  },
}
```

### よく使うクラス
```html
<!-- CTAボタン -->
<a class="inline-block bg-gradient-to-b from-orange-400 to-orange-500 
          text-white font-bold py-4 px-8 rounded-lg shadow-lg 
          hover:-translate-y-0.5 hover:shadow-xl transition-all">
  無料で相談する
</a>

<!-- セクション見出し -->
<h2 class="text-2xl md:text-3xl font-bold text-center mb-8">
  <span class="text-primary">選ばれる</span>3つの理由
</h2>

<!-- カード -->
<div class="bg-white rounded-xl p-6 shadow-lg">
  <!-- 内容 -->
</div>
```
