# font 複合プロパティの書き方について

CSSの `font` プロパティは、複数のフォント関連のプロパティを**一括で指定**できる**ショートハンド（略式）プロパティ**です。

---

## 1 書式（構文）：

```css
font: [font-style] [font-variant] [font-weight] [font-size]/[line-height] [font-family];
```

※中括弧 `[]` は省略可能な要素を表します。`font-size` と `font-family` は**必須**です。

---

## 2 各プロパティの意味：

| 項目 | 説明 |
|------|------|
| `font-style` | 斜体（italicなど）を指定 |
| `font-variant` | 小型大文字（small-caps）などを指定 |
| `font-weight` | 太さ（bold、normal、数値など）を指定 |
| `font-size` | フォントサイズ（例：16px、1.2em）※必須 |
| `line-height` | 行の高さ（例：1.5） |
| `font-family` | フォント名（例："Arial", sans-serif）※必須 |

---

## 3 例：

```css
font: italic small-caps bold 16px/1.5 "Times New Roman", serif;
```

この例では：

- 斜体 (`italic`)
- 小型大文字 (`small-caps`)
- 太字 (`bold`)
- フォントサイズ：16px
- 行の高さ：1.5
- フォントファミリー："Times New Roman", serif

が一括で指定されています。

---

## ■ 注意点：

- `font-size` と `font-family` は**省略できません**。
- 省略した値は、ブラウザの初期値が使われます。
- `font` プロパティを使うと、関連する個別のフォントプロパティが**すべて上書き**されます。
