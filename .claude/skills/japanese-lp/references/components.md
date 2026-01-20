# 日本LP必須コンポーネント

## 1. ファーストビュー（FV）

LPで最も重要。3秒で価値を伝え、スクロールさせる。

### 必須要素
```html
<section class="first-view">
  <!-- 実績バッジ（左上または右上） -->
  <div class="badges">
    <span class="badge gold">採択率No.1</span>
    <span class="badge gold">年間200社支援</span>
  </div>
  
  <!-- メインキャッチコピー -->
  <h1 class="main-catch">
    <span class="sub">補助金申請のプロが</span>
    採択率90%で<br>あなたの申請をサポート
  </h1>
  
  <!-- サブコピー -->
  <p class="sub-catch">
    面倒な書類作成から申請まで丸投げOK
  </p>
  
  <!-- CTAボタン -->
  <a href="#form" class="cta-button primary">
    無料で相談する
    <span class="micro">＼ 最短30秒で完了 ／</span>
  </a>
  
  <!-- メインビジュアル -->
  <img src="hero.jpg" alt="サービスイメージ" class="hero-image">
</section>
```

### キャッチコピーの型
```
【数字訴求型】
「たった3ヶ月で売上2倍を実現」
「1日5分で英語がペラペラに」

【悩み解決型】
「もう補助金申請で悩まない」
「面倒な経理作業から解放される」

【ベネフィット直球型】
「採択率90%であなたの申請をサポート」
「初期費用0円で始められるIT導入」

【権威性型】
「累計1,000社が導入」
「業界シェアNo.1のシステム」
```

---

## 2. 実績バッジ

信頼性を瞬時に伝える。ファーストビューに必須。

### デザインパターン
```html
<!-- ゴールドバッジ -->
<div class="badge-container">
  <div class="badge gold">
    <span class="badge-label">採択率</span>
    <span class="badge-number">90%</span>
  </div>
  <div class="badge gold">
    <span class="badge-label">年間支援</span>
    <span class="badge-number">200社</span>
  </div>
  <div class="badge gold">
    <span class="badge-label">累計支援額</span>
    <span class="badge-number">5億円</span>
  </div>
</div>
```

### CSS
```css
.badge.gold {
  background: linear-gradient(135deg, #D4AF37 0%, #F4E4BA 50%, #D4AF37 100%);
  color: #333;
  padding: 8px 16px;
  border-radius: 4px;
  font-weight: bold;
  box-shadow: 0 2px 4px rgba(0,0,0,0.2);
}
```

---

## 3. お悩み共感セクション

ターゲットの悩みを言語化し、「自分のことだ」と思わせる。

### 実装例
```html
<section class="problems">
  <h2>こんな<span class="highlight">お悩み</span>ありませんか？</h2>
  
  <ul class="problem-list">
    <li>
      <span class="icon">😰</span>
      <p>補助金の種類が多すぎて、どれに申請すればいいかわからない</p>
    </li>
    <li>
      <span class="icon">😫</span>
      <p>申請書類が複雑で、本業に集中できない</p>
    </li>
    <li>
      <span class="icon">😢</span>
      <p>過去に自分で申請したが、不採択になってしまった</p>
    </li>
  </ul>
  
  <div class="empathy">
    <p class="lead">そのお悩み、<strong>すべて解決</strong>できます！</p>
  </div>
</section>
```

---

## 4. 選ばれる理由（3つの特徴）

なぜこのサービスを選ぶべきかを明確に。

### 実装例
```html
<section class="reasons">
  <h2><span class="company">〇〇</span>が選ばれる<span class="number">3</span>つの理由</h2>
  
  <div class="reason-cards">
    <div class="reason-card">
      <div class="reason-number">01</div>
      <div class="reason-icon">📊</div>
      <h3>採択率90%の圧倒的実績</h3>
      <p>年間200社以上の申請をサポート。業界トップクラスの採択率を誇ります。</p>
    </div>
    
    <div class="reason-card">
      <div class="reason-number">02</div>
      <div class="reason-icon">🤝</div>
      <h3>完全成功報酬型</h3>
      <p>採択されなければ費用は一切いただきません。リスクゼロで申請できます。</p>
    </div>
    
    <div class="reason-card">
      <div class="reason-number">03</div>
      <div class="reason-icon">📝</div>
      <h3>書類作成から申請まで丸投げOK</h3>
      <p>面倒な書類作成はすべてお任せ。本業に集中できます。</p>
    </div>
  </div>
</section>
```

---

## 5. お客様の声

社会的証明の最重要コンポーネント。

### 実装例
```html
<section class="testimonials">
  <h2>お客様の<span class="highlight">声</span></h2>
  
  <div class="testimonial-cards">
    <div class="testimonial-card">
      <div class="testimonial-header">
        <img src="customer1.jpg" alt="田中様" class="customer-photo">
        <div class="customer-info">
          <p class="customer-name">田中 太郎 様</p>
          <p class="customer-company">株式会社〇〇 代表取締役</p>
        </div>
      </div>
      
      <div class="testimonial-result">
        <span class="result-label">補助金採択額</span>
        <span class="result-number">450万円</span>
      </div>
      
      <blockquote class="testimonial-text">
        「自分で申請しようとしたときは書類作成だけで1ヶ月かかりましたが、
        お任せしたら2週間で申請完了。しかも一発採択でした！」
      </blockquote>
    </div>
    <!-- 他の声も同様に -->
  </div>
</section>
```

### ポイント
- 顔写真は必須（信頼性3倍）
- 具体的な成果（数字）を入れる
- 会社名・役職を明記（許可取得済みの場合）
- 最低3件、理想は5件以上

---

## 6. 料金プラン

明確でわかりやすく。比較しやすい表形式推奨。

### 実装例
```html
<section class="pricing">
  <h2>料金<span class="highlight">プラン</span></h2>
  
  <div class="pricing-cards">
    <div class="pricing-card">
      <div class="plan-name">ライトプラン</div>
      <div class="plan-price">
        <span class="currency">¥</span>
        <span class="amount">50,000</span>
        <span class="unit">〜</span>
      </div>
      <ul class="plan-features">
        <li>✓ 補助金診断</li>
        <li>✓ 申請書類レビュー</li>
        <li>✗ 書類作成代行</li>
      </ul>
      <a href="#form" class="cta-button secondary">詳しく見る</a>
    </div>
    
    <div class="pricing-card recommended">
      <div class="recommend-badge">人気No.1</div>
      <div class="plan-name">スタンダードプラン</div>
      <div class="plan-price">
        <span class="currency">¥</span>
        <span class="amount">150,000</span>
        <span class="unit">〜</span>
      </div>
      <ul class="plan-features">
        <li>✓ 補助金診断</li>
        <li>✓ 申請書類レビュー</li>
        <li>✓ 書類作成代行</li>
      </ul>
      <a href="#form" class="cta-button primary">申し込む</a>
    </div>
  </div>
</section>
```

---

## 7. FAQ（よくある質問）

購入前の不安を解消。アコーディオン形式推奨。

### 実装例
```html
<section class="faq">
  <h2>よくある<span class="highlight">ご質問</span></h2>
  
  <div class="faq-list">
    <details class="faq-item">
      <summary class="faq-question">
        Q. 補助金が採択されなかった場合、費用はかかりますか？
      </summary>
      <div class="faq-answer">
        <p>A. いいえ、採択されなかった場合は費用は一切いただきません。
        完全成功報酬型ですので、リスクなくお申し込みいただけます。</p>
      </div>
    </details>
    <!-- 他のFAQも同様に -->
  </div>
</section>
```

### 入れるべきFAQ例
- 費用・支払い方法について
- 申込〜完了までの期間
- キャンセル・返金について
- サポート体制について
- 対象外のケースについて

---

## 8. CTAボタン

コンバージョンの要。デザインと配置が重要。

### デザイン
```css
.cta-button {
  display: inline-block;
  background: linear-gradient(180deg, #FF8C42 0%, #FF6B35 100%);
  color: white;
  font-size: 18px;
  font-weight: bold;
  padding: 16px 48px;
  border-radius: 8px;
  text-decoration: none;
  box-shadow: 0 4px 15px rgba(255, 107, 53, 0.4);
  transition: transform 0.2s, box-shadow 0.2s;
}

.cta-button:hover {
  transform: translateY(-2px);
  box-shadow: 0 6px 20px rgba(255, 107, 53, 0.5);
}

/* マイクロコピー */
.cta-button .micro {
  display: block;
  font-size: 12px;
  font-weight: normal;
  margin-top: 4px;
}
```

### 配置ルール
1. **ファーストビュー**: 必須
2. **選ばれる理由の後**: 推奨
3. **お客様の声の後**: 推奨
4. **料金プランの後**: 必須
5. **ページ最下部**: 必須

最低3箇所、理想は5箇所

---

## 9. 限定オファー

緊急性・限定性で行動を促す。

### 実装例
```html
<section class="limited-offer">
  <div class="offer-badge">期間限定キャンペーン</div>
  
  <h2>今だけ！<span class="highlight">初回相談無料</span></h2>
  
  <div class="offer-details">
    <div class="offer-item">
      <span class="label">通常価格</span>
      <span class="price strikethrough">¥30,000</span>
    </div>
    <div class="offer-item special">
      <span class="label">キャンペーン価格</span>
      <span class="price">¥0</span>
    </div>
  </div>
  
  <div class="urgency">
    <p>🔥 毎月先着<strong>10社</strong>様限定</p>
    <p class="remaining">今月残り <span class="count">3</span> 枠</p>
  </div>
  
  <a href="#form" class="cta-button large">
    今すぐ無料相談を予約する
  </a>
</section>
```
