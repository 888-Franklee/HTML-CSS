
# CSSの:hover 擬似クラスについて詳しく解説

## ✅概要

`:hover` は、CSSの擬似クラスの一つで、ユーザーが要素の上にマウスカーソルを置いたときにスタイルを変更するために使用されます。インタラクティブなUIを作成する際によく使われます。

## ✅基本的な使い方

```css
button:hover {
  background-color: blue;
  color: white;
}
```

この例では、マウスカーソルが `button` 要素の上にあるときに、背景色が青、文字色が白に変わります。

## ✅対象要素

`:hover` は、次のようなほとんどのHTML要素に使用できます：

- リンク (`<a>`)
- ボタン (`<button>`, `<input type="button">` など)
- 画像 (`<img>`, 背景画像含む)
- 任意のブロック要素 (`<div>`, `<section>`, `<article>` など)

## ✅使用例

### 1. リンクのホバー効果

```css
a:hover {
  text-decoration: underline;
  color: red;
}
```

### 2. メニューアイテムのホバーエフェクト

```css
.nav-item:hover {
  background-color: #eee;
  cursor: pointer;
}
```

### 3. トランジションと組み合わせた滑らかな効果

```css
.card {
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.card:hover {
  transform: scale(1.05);
  box-shadow: 0 4px 15px rgba(0, 0, 0, 0.2);
}
```

### 4. 背景画像に対するホバー効果

```css
.banner {
  background-image: url('banner.jpg');
  transition: background-image 0.3s ease;
}

.banner:hover {
  background-image: url('banner-hover.jpg');
}
```

### 5. SVG要素のホバー

```css
svg:hover {
  fill: orange;
  cursor: pointer;
}
```

## ✅注意点

- スマートフォンなどのタッチデバイスでは `:hover` が期待通りに動作しない場合があります。
- CSSセレクタの優先度に注意し、必要に応じてより具体的なセレクタを使うと意図したスタイルが適用されやすくなります。
- 他の擬似クラス（`:focus`, `:active`, `:visited`など）と併用して、より細かいUI制御が可能です。

## ✅よくある質問（FAQ）

### Q. `:hover` は `display: none` の要素にも効きますか？

A. 効きません。表示されていない要素にマウスオーバーすることはできません。

### Q. 複数の擬似クラスは組み合わせられますか？

A. はい、可能です：

```css
a:hover:active {
  color: green;
}
```

### Q. JavaScriptで `:hover` と同じ動作を再現できますか？

A. はい、可能ですが、CSSだけで済むならパフォーマンスやメンテナンス性の観点からCSSを使うのが推奨されます。

## ✅応用テクニック

### 子要素にだけホバーエフェクトをかけたいとき

```css
.parent:hover .child {
  color: blue;
}
```

### FlexboxやGridとの組み合わせ

```css
.grid-item:hover {
  background-color: lightgray;
  transform: translateY(-5px);
}
```

### カスタムプロパティ（CSS変数）と組み合わせる

```css
:root {
  --hover-color: coral;
}

.button:hover {
  background-color: var(--hover-color);
}
```

## ✅まとめ

`:hover` を使うことで、インタラクティブで視覚的にわかりやすいUIを構築できます。トランジションやアニメーションと組み合わせることで、より洗練されたデザインを実現可能です。基本から応用までを理解して、ユーザー体験の向上を目指しましょう。
