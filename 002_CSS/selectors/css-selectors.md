# CSSセレクタ完全ガイド

## ✅1. CSSセレクタとは

CSSセレクタは、**スタイルを適用したいHTML要素を選択するためのルール**です。  
セレクタを使って対象の要素を指定し、装飾やレイアウトを設定します。

---

## ✅2. 主なセレクタとサンプルコード

### 2.1 タイプセレクタ（要素セレクタ）

```html
<p>この段落が赤になります</p>
<p>これも赤です</p>
```

```css
p {
  color: red;
}
```

---

### 2.2 クラスセレクタ

```html
<p class="highlight">この段落が黄色背景になります</p>
<p>これは通常の段落です</p>
```

```css
.highlight {
  background-color: yellow;
}
```

---

### 2.3 IDセレクタ

```html
<div id="header">ヘッダー部分</div>
```

```css
#header {
  background-color: lightblue;
}
```

---

### 2.4 子孫セレクタ

```html
<div>
  <p>divの中のpが緑色</p>
</div>
<p>このpは対象外</p>
```

```css
div p {
  color: green;
}
```

---

### 2.5 子セレクタ（`>`）

```html
<ul>
  <li>直下のli（対象）</li>
  <li>
    <ul>
      <li>入れ子のli（対象外）</li>
    </ul>
  </li>
</ul>
```

```css
ul > li {
  border: 1px solid gray;
}
```

---

### 2.6 隣接兄弟セレクタ（`+`）

```html
<h1>見出し</h1>
<p>h1の直後のpだけオレンジ</p>
<p>このpは対象外</p>
```

```css
h1 + p {
  color: orange;
}
```

---

### 2.7 一般兄弟セレクタ（`~`）

```html
<h1>見出し</h1>
<p>このpは斜体</p>
<p>これも斜体</p>
```

```css
h1 ~ p {
  font-style: italic;
}
```

---

### 2.8 属性セレクタ

```html
<input type="text" placeholder="名前を入力">
<input type="password" placeholder="パスワード">
```

```css
input[type="text"] {
  border: 2px solid blue;
}
```

---

### 2.9 疑似クラスセレクタ

```html
<a href="#">リンク</a>
```

```css
a:hover {
  text-decoration: underline;
  color: red;
}
```

---

### 2.10 疑似要素セレクタ

```html
<p>最初の1行が太字になります</p>
```

```css
p::first-line {
  font-weight: bold;
}
```

---

## ✅3. セレクタの組み合わせ

```html
<div class="container">
  <button class="button">ボタン</button>
</div>
```

```css
.container .button:hover {
  background: red;
  color: white;
}
```

---

## ✅4. まとめ

- セレクタはHTML要素を選ぶための仕組み  
- クラス・ID・階層構造・状態に応じて指定できる  
- 組み合わせるとより細かい制御が可能

