
# CSSの `margin` プロパティについて

## 1.  概要

`margin`（マージン）は、**要素の外側の余白**を指定するためのCSSプロパティです。  
他の要素との間隔を調整するのに使用され、要素の「外側」のスペースをコントロールします。

---

## 2.  基本構文

```css
selector {
  margin: 値;
}
```

`margin` プロパティは、**ショートハンド**（複合指定）であり、上下左右のマージンを一括で指定できます。

---

## 3.  値の指定方法（ショートハンド）

| 書き方 | 意味 |
|--------|------|
| `margin: 10px;` | 全方向（上・右・下・左）に10px |
| `margin: 10px 20px;` | 上下に10px、左右に20px |
| `margin: 10px 20px 30px;` | 上に10px、左右に20px、下に30px |
| `margin: 10px 20px 30px 40px;` | 上10px、右20px、下30px、左40px（時計回り） |

---

## 4.  個別プロパティ

| プロパティ名 | 説明 |
|--------------|------|
| `margin-top` | 上の余白 |
| `margin-right` | 右の余白 |
| `margin-bottom` | 下の余白 |
| `margin-left` | 左の余白 |

---

## 5.  自動調整 `auto`

`margin: auto;` を使うことで、**要素を中央に配置**することができます（特に左右のマージンで有効）。

例：

```css
div {
  width: 300px;
  margin: 0 auto;
}
```

この場合、`div` 要素は**水平方向の中央**に配置されます。

---

## 6.  使用例

```html
<div style="margin: 20px;">すべての方向に20pxの余白</div>
<div style="margin: 10px 30px;">上下10px、左右30px</div>
<div style="margin-top: 50px;">上だけ50pxの余白</div>
<div style="margin: 0 auto;">左右中央に配置</div>
```

---

##　7.  注意点

- マージン同士が上下に重なると「**マージンの相殺（margin collapse）**」が起こることがあります。
- `margin` は要素の**外部スペース**であり、内側のスペースを設定する `padding` とは異なります。
- `%` 単位で指定した場合は、**親要素の幅**に対する割合になります。

---

##　8.  関連リンク

- [MDN Web Docs - margin](https://developer.mozilla.org/ja/docs/Web/CSS/margin)
