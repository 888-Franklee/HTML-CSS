# CSSセレクタ完全ガイド

## ✅1. CSSセレクタとは

CSSセレクタは、**スタイルを適用したいHTML要素を選択するためのルール**です。  
セレクタを使って対象の要素を指定し、装飾やレイアウトを設定します。

---

## ✅2. 主なセレクタ

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

### 2.3 IDセレクタ（ID選択子）

IDセレクタは、HTML要素の `id` 属性を使ってスタイルを適用するセレクタです。  
`#id名` の形式で記述し、**1つのHTML文書内で一意（1回だけ）使える要素**を指定します。  

---

####  🔹基本例

```html
<div id="header">ヘッダー部分</div>
<div id="footer">フッター部分</div>
```

```css
#header {
  background-color: lightblue;
}

#footer {
  background-color: lightgray;
}
```

 `id="header"` を持つ要素だけに `#header` のスタイルが適用されます。

---

####  🔹クラスセレクタとの違い

```html
<div class="box">クラスセレクタ</div>
<div id="unique-box">IDセレクタ</div>
```

```css
.box {
  color: green;
}

#unique-box {
  color: red;
}
```

- クラスセレクタ（`.box`）は **複数の要素に使える**（再利用向き）  
- IDセレクタ（`#unique-box`）は **1つの要素だけに使う**（一意性が必要）  
- **優先度は `#id` > `.class` > `要素セレクタ`** の順に高い  

---

####  🔹JavaScriptとの連携が簡単

`id` はJavaScriptでも要素取得が簡単です。  

```html
<button id="btn">送信</button>
```

```css
#btn {
  background: tomato;
  color: white;
}
```

```javascript
const btn = document.getElementById('btn');
btn.addEventListener('click', () => {
  alert('クリックされました');
});
```

 `id` が一意なので、JavaScriptでの操作がしやすいのもメリットです。

---

####  🔹IDセレクタのメリット
1. 一意なので **1つの要素をピンポイントで指定できる**  
2. クラスや要素セレクタより **優先度が高い**  
3. JavaScriptとの相性が良く、イベント処理などで便利  

---

####  🔹IDセレクタのデメリット・注意点
1. **再利用ができない**（複数の要素に同じスタイルを当てられない）  
2. **優先度が高すぎるため、上書きが難しくなる**  
3. クラスと混在させるとスタイル管理が複雑化しやすい  

 大規模サイトでは **汎用スタイルはクラスで定義し、特定の要素だけIDで指定** するのがベストです。

---
#### 🔹まとめ  
- IDセレクタは **1ページに1つしかない特定の要素**を指定するときに使う  
- スタイルを複数の要素に適用したい場合はクラスセレクタを使う  
- 優先度が高すぎるので多用は避け、必要な箇所だけに使うのが理想  

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
