---
title: margin-top
slug: Web/CSS/margin-top
l10n:
  sourceCommit: b2833ddfd45cae1bb5e050d24637865e9327408d
---

{{CSSRef}}

**`margin-top`** は [CSS](/ja/docs/Web/CSS) のプロパティで、要素の上側の[マージン領域](/ja/docs/Web/CSS/CSS_box_model/Introduction_to_the_CSS_box_model#マージン領域)を設定します。正の数を指定すると、隣との間が遠くなるように配置され、負の数を指定すると、近くなるように配置します。

{{InteractiveExample("CSS デモ: margin-top")}}

```css interactive-example-choice
margin-top: 1em;
```

```css interactive-example-choice
margin-top: 10%;
```

```css interactive-example-choice
margin-top: 10px;
```

```css interactive-example-choice
margin-top: 0;
```

```html interactive-example
<section id="default-example">
  <div id="container">
    <div class="row"></div>
    <div class="row transition-all" id="example-element"></div>
    <div class="row"></div>
  </div>
</section>
```

```css interactive-example
#container {
  width: 300px;
  height: 200px;
  display: flex;
  align-content: flex-start;
  flex-direction: column;
  justify-content: flex-start;
}

.row {
  height: 33.33%;
  display: inline-block;
  border: solid #ce7777 10px;
  background-color: #2b3a55;
  flex-shrink: 0;
}

#example-element {
  border: solid 10px #ffbf00;
  background-color: #2b3a55;
}
```

このプロパティは、[置換要素](/ja/docs/Web/CSS/CSS_images/Replaced_element_properties)ではないインライン要素、例えば {{HTMLElement("span")}} や {{HTMLElement("code")}} には効果がありません。

## 構文

```css
/* <length> 値 */
margin-top: 10px; /* 絶対的な寸法 */
margin-top: 1em; /* 文字の寸法からの相対 */
margin-top: 5%; /* 直近のブロックコンテナーの幅からの相対 */

/* キーワード値 */
margin-top: auto;

/* グローバル値 */
margin-top: inherit;
margin-top: initial;
margin-top: revert;
margin-top: revert-layer;
margin-top: unset;
```

`margin-top` プロパティは `auto` キーワード、または `<length>` や `<percentage>` で指定されます。正の数、ゼロ、負の数が指定できます。

### 値

- {{cssxref("&lt;length&gt;")}}
  - : マージンの寸法を固定値で表したものです。
- {{cssxref("&lt;percentage&gt;")}}
  - : マージンの寸法を[包含ブロック](/ja/docs/Web/CSS/CSS_display/Containing_block)のインラインサイズ（{{cssxref("writing-mode")}} で横書き言語と定義されている場合は _width_）に対するパーセント値で示したものです。
- `auto`
  - : ブラウザーが適切な値を選択して使用します。 {{cssxref("margin")}} を参照してください。

## 公式定義

{{cssinfo}}

## 形式文法

{{csssyntax}}

## 例

### 正と負の上マージンの設定

```css
.content {
  margin-top: 5%;
}
.side-box {
  margin-top: 10px;
}
.logo {
  margin-top: -5px;
}
#footer {
  margin-top: 1em;
}
```

## 仕様書

{{Specifications}}

## ブラウザーの互換性

{{Compat}}

## 関連情報

- {{cssxref("margin-right")}}, {{cssxref("margin-bottom")}}, {{cssxref("margin-left")}}
- 一括指定の {{cssxref("margin")}}
- {{cssxref("margin-block-start")}}, {{cssxref("margin-block-end")}}, {{cssxref("margin-inline-start")}}, {{cssxref("margin-inline-end")}}
- 一括指定の {{cssxref("margin-block")}} と {{cssxref("margin-inline")}}
- [CSS ボックスモデル](/ja/docs/Web/CSS/CSS_box_model)モジュール
