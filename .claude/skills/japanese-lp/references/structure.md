# 日本LP構成パターン

## PASONAの法則（基本構成）

日本の高CVランディングページは、PASONAの法則に基づいた縦長構成が基本。

### 1. Problem（問題提起）
**目的**: ユーザーの悩み・課題を言語化し、「自分のことだ」と思わせる

**実装パターン**:
```html
<section class="problem">
  <h2>こんなお悩みありませんか？</h2>
  <ul>
    <li>✗ 補助金申請が複雑で何から始めればいいかわからない</li>
    <li>✗ 申請書類の作成に時間がかかりすぎる</li>
    <li>✗ 過去に申請したが不採択だった</li>
  </ul>
</section>
```

**ポイント**:
- 3〜5個の具体的な悩みを列挙
- ✗マークやアイコンで視覚的に強調
- ターゲットが「あるある」と思う内容

### 2. Affinity（親近感・共感）
**目的**: 「この人は私の気持ちをわかってくれる」と思わせる

**実装パターン**:
```html
<section class="affinity">
  <div class="founder-message">
    <img src="founder.jpg" alt="代表者">
    <blockquote>
      私も起業当初、補助金の存在すら知らず、
      資金繰りに苦労しました。だからこそ...
    </blockquote>
  </div>
</section>
```

**ポイント**:
- 代表者や担当者の顔写真
- 過去の苦労体験を共有
- 「だからこそ」で解決策への橋渡し

### 3. Solution（解決策）
**目的**: 商品・サービスが悩みを解決できることを示す

**実装パターン**:
```html
<section class="solution">
  <h2>選ばれる3つの理由</h2>
  <div class="reasons">
    <div class="reason">
      <span class="number">01</span>
      <h3>採択率90%の実績</h3>
      <p>年間200社以上の申請をサポート</p>
    </div>
    <!-- 02, 03も同様 -->
  </div>
</section>
```

**ポイント**:
- 「3つの理由」「5つの特徴」等、数字で区切る
- 各理由に具体的な数字・実績を入れる
- アイコンやイラストで視覚的に

### 4. Offer（提案）
**目的**: 具体的なサービス内容と価格を提示

**実装パターン**:
```html
<section class="offer">
  <h2>サービス内容</h2>
  <div class="service-flow">
    <div class="step">STEP1: 無料相談</div>
    <div class="step">STEP2: 申請書類作成</div>
    <div class="step">STEP3: 申請代行</div>
  </div>
  <div class="pricing">
    <h3>料金プラン</h3>
    <!-- 料金表 -->
  </div>
</section>
```

### 5. Narrowing（絞り込み）
**目的**: 限定性・緊急性で「今すぐ行動」を促す

**実装パターン**:
```html
<section class="narrowing">
  <div class="limited-offer">
    <span class="badge">期間限定</span>
    <h3>今月末まで！初回相談無料</h3>
    <p>毎月先着10社様限定</p>
    <div class="countdown">残り3枠</div>
  </div>
</section>
```

**ポイント**:
- 「先着〇名」「〇月〇日まで」
- カウントダウンや残数表示
- 赤系の色で緊急性を演出

### 6. Action（行動喚起）
**目的**: CTAボタンで具体的な行動を促す

**実装パターン**:
```html
<section class="action">
  <div class="final-cta">
    <h2>まずは無料相談から</h2>
    <p>最短翌営業日にご連絡いたします</p>
    <a href="#form" class="cta-button">
      無料で相談する
      <span class="sub">＼ 30秒で完了 ／</span>
    </a>
  </div>
</section>
```

---

## セクション配置順序（推奨）

```
1. ファーストビュー（FV）
   └─ キャッチコピー + メインビジュアル + CTA + 実績バッジ

2. お悩み共感（Problem + Affinity）
   └─ 「こんなお悩みありませんか？」

3. 解決策提示（Solution）
   └─ 「選ばれる3つの理由」

4. 社会的証明
   └─ お客様の声、導入実績、メディア掲載

5. サービス詳細（Offer）
   └─ 利用の流れ、料金プラン

6. 信頼性補強
   └─ よくある質問（FAQ）、会社概要

7. クロージング（Narrowing + Action）
   └─ 限定オファー + 最終CTA

8. フッター
   └─ 追伸（P.S.）、連絡先
```

---

## 業種別カスタマイズ

### BtoB（コンサル、SaaS等）
- 「導入事例」セクションを厚めに
- ROI、コスト削減効果を数字で
- 無料トライアル or 資料請求がゴール

### BtoC（EC、サービス等）
- お客様の声を多めに（5件以上）
- ビフォーアフター写真
- 購入 or 申し込みがゴール

### 高額商材（50万円以上）
- 分割払い対応を明記
- 保証・返金ポリシーを手厚く
- 無料相談 → 成約の2ステップ
