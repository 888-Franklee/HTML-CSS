#  CSSプロパティ: font-style

## 1. font-styleとは？
`font-style` は、**文字のスタイル（斜体や通常）を指定するためのCSSプロパティ**です。  
主にイタリック体やオブリーク体を指定する際に使用されます。

---

## 2. 指定方法

### 2-1. キーワードで指定
- **normal** : 標準のスタイル（通常の立ち文字）
- **italic** : イタリック体（筆記体風の斜体）
- **oblique** : オブリーク体（文字全体を傾けた斜体）

```css
p {
  font-style: italic;
}
```

---

## 3. サンプルコード

```html
<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="UTF-8">
  <title>font-styleサンプル</title>
  <style>
    p.normal { font-style: normal; }
    p.italic { font-style: italic; }
    p.oblique { font-style: oblique; }
  </style>
</head>
<body>
  <p class="normal">これは normal (標準) の文字です。</p>
  <p class="italic">これは italic (イタリック) の文字です。</p>
  <p class="oblique">これは oblique (オブリーク) の文字です。</p>
</body>
</html>
```

---

## 4. 注意点
- `italic` はフォントのイタリックスタイルを使用します。
- `oblique` は既存の文字を傾けるだけなので、italicと見た目が似ています。
- 日本語フォントでは italic や oblique が適用されないこともあります。

---
