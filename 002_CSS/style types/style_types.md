# CSSのスタイル指定方法

CSS（Cascading Style Sheets）には、HTMLにスタイルを適用する3つの主な方法があります。  
それぞれの特徴を理解して使い分けることが重要です。

---

## 1. 内部スタイルシート（内部CSS）

内部スタイルシートは、HTMLファイル内の`<head>`タグ内に`<style>`タグを使用して記述する方法です。  
HTMLとCSSを1つのファイルにまとめられるので、小規模なページに向いています。

### 記述例
```html
<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="UTF-8">
  <title>内部スタイルシートの例</title>
  <style>
    p {
      color: blue;
      font-size: 16px;
    }
  </style>
</head>
<body>
  <p>これは内部スタイルシートの例です。</p>
</body>
</html>
```

---

## 2. 行内スタイルシート（インラインCSS）

行内スタイルシートは、HTMLタグの`style`属性に直接CSSを記述する方法です。  
特定の要素だけにスタイルを適用したいときに使われますが、管理が難しくなるため多用は避けます。

### 記述例
```html
<p style="color: red; font-weight: bold;">これはインラインCSSの例です。</p>
```

---

## 3. 外部スタイルシート（外部CSS）

外部スタイルシートは、CSSを別ファイル（例：style.css）として分離し、HTMLファイルの`<head>`タグで`<link>`要素を使って読み込む方法です。  
複数ページで同じデザインを共有できるため、最も推奨される方法です。

### 記述例
#### HTMLファイル
```html
<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="UTF-8">
  <title>外部スタイルシートの例</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <p>これは外部スタイルシートの例です。</p>
</body>
</html>
```

#### style.css ファイル
```css
p {
  color: green;
  font-size: 18px;
}
```

---

## まとめ

| 種類           | メリット                     | デメリット                       |
|----------------|------------------------------|-----------------------------------|
| 内部CSS        | HTMLとCSSを1ファイルで完結    | 複数ページでの再利用ができない     |
| インラインCSS  | その場で簡単に適用できる      | コードが汚くなり、管理が大変       |
| 外部CSS        | 複数ページで再利用可能、管理しやすい | 外部ファイルを読み込む必要がある   |

**基本的には「外部スタイルシート」を使い、必要に応じて内部CSSやインラインCSSを組み合わせるのがおすすめです。**
