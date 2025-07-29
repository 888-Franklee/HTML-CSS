
# CSSの `font-family` プロパティ解説

## **1. `font-family` とは？**

`font-family` プロパティは、HTML要素に適用する**フォントの種類（書体）を指定するためのCSSプロパティ**です。  
テキストの見た目を整えるために使用され、複数のフォントを指定することで、ユーザー環境に依存せずできるだけ意図したデザインを表示できます。

---

## **2. 基本構文**

```css
selector {
  font-family: フォント1, フォント2, フォント3, ... , 汎用フォント;
}
```

- 複数のフォント名をカンマで区切って指定します。
- 左から順番に利用可能なフォントが適用されます。  
- 最後に必ず**汎用フォント（serif, sans-serif, monospace など）**を指定するのが推奨されます。

---

## **3. 使用例**

```css
p {
  font-family: "Helvetica Neue", Arial, sans-serif;
}
```

上記の場合：
1. 「Helvetica Neue」がインストールされていればそれが使われます。
2. なければ「Arial」が適用されます。
3. どちらもない場合は、**sans-serif系の既定フォント**が使われます。

---

## **4. フォント名にスペースがある場合**

フォント名に空白がある場合は **ダブルクォーテーション(" ")** または **シングルクォーテーション(' ')** で囲みます。

```css
h1 {
  font-family: "Times New Roman", serif;
}
```

---

## **5. 汎用フォントファミリーの種類**

汎用フォントは次の5種類がよく使われます。

1. **serif**（セリフ体）  
   - 例: Times New Roman  
   - 装飾的なうろこ（セリフ）がある書体  

2. **sans-serif**（サンセリフ体）  
   - 例: Arial  
   - セリフのないシンプルな書体  

3. **monospace**（等幅フォント）  
   - 例: Courier New  
   - 全ての文字幅が同じ  

4. **cursive**（筆記体風）  
   - 例: Comic Sans MS  

5. **fantasy**（装飾的フォント）  
   - 例: Papyrus  

---

## **6. ポイント**

- 環境ごとにインストールされているフォントが異なるため、**複数フォントを順番に指定**するのが基本。
- Webフォント（Google Fontsなど）を使うとデザイン性を統一しやすい。

---

## **7. 応用例：日本語フォント指定**

```css
body {
  font-family: "Hiragino Sans", "Noto Sans JP", "Meiryo", sans-serif;
}
```

- Mac → Hiragino Sans
- Google Fonts → Noto Sans JP
- Windows → Meiryo
- 最後は sans-serif をフォールバック
