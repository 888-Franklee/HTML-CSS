
# CSSの `text-decoration` プロパティについて

## 1.  概要

`text-decoration` プロパティは、**テキストに装飾（下線、上線、取り消し線など）を加える**ために使用されます。
また、`text-decoration` はショートハンド（複合）プロパティであり、いくつかの個別プロパティをまとめて指定することも可能です。

---

## 2.  基本構文

```css
selector {
  text-decoration: 値;
}
```

もしくはショートハンドで使用する場合：

```css
text-decoration: <line> <style> <color>;
```

---

## 3. 主な値（基本）

| 値 | 意味 | 説明 |
|----|------|------|
| `none` | 装飾なし | テキスト装飾を取り除く |
| `underline` | 下線 | テキストの下に線を引く |
| `overline` | 上線 | テキストの上に線を引く |
| `line-through` | 取り消し線 | テキストの中央に線を引く |
| `blink` | 点滅（非推奨） | テキストが点滅（現在のブラウザでは無効） |

---

## 4. 応用（スタイルや色を加える）

### ショートハンドで使用する場合：

```css
text-decoration: underline dotted red;
```

この例では、「赤色の点線の下線」が適用されます。

---

## 5. 関連プロパティ（個別指定）

| プロパティ | 説明 |
|------------|------|
| `text-decoration-line` | `underline` や `line-through` などの線の種類を指定 |
| `text-decoration-style` | 線のスタイル（`solid`, `dashed`, `dotted`, `double`, `wavy`）を指定 |
| `text-decoration-color` | 線の色を指定 |

---

## 6. 使用例

```html
<p style="text-decoration: underline;">これは下線付きのテキストです。</p>
<p style="text-decoration: line-through;">これは取り消し線付きのテキストです。</p>
<p style="text-decoration: overline;">これは上線付きのテキストです。</p>
<p style="text-decoration: underline wavy blue;">これは青色の波線の下線です。</p>
```

---

## 7. 注意点

- `a` タグ（リンク）にはデフォルトで `underline` が付いています。
- `none` を指定することでリンクの下線を消すことが可能ですが、視認性を保つ工夫が必要です。
- `text-decoration` はインライン要素にもブロック要素にも適用可能です。

---

## 8. 関連仕様

- CSS Text Decoration Module Level 3
- https://developer.mozilla.org/ja/docs/Web/CSS/text-decoration
