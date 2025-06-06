---
title: <g>
slug: Web/SVG/Reference/Element/g
l10n:
  sourceCommit: c2fd97474834e061404b992c8397d4ccc4439a71
---

**`<g>`** は [SVG](/ja/docs/Web/SVG) の要素で、他の SVG 要素をグループ化するために用いられるコンテナーです。

`<g>` 要素に適用された座標変換は、その全ての子要素に対して実行されます。適用された属性は子要素に継承されます。加えて、多数のオブジェクトをグループ化しておくと後に {{SVGElement("use")}} 要素で参照することができます。

## 例

```css hidden
html,
body,
svg {
  height: 100%;
}
```

```html
<svg viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg">
  <!-- Using g to inherit presentation attributes -->
  <g fill="white" stroke="green" stroke-width="5">
    <circle cx="40" cy="40" r="25" />
    <circle cx="60" cy="60" r="25" />
  </g>
</svg>
```

{{EmbedLiveSample('Example', 100, '100%')}}

## 使用可能な場所

{{svginfo}}

## 仕様書

{{Specifications}}

## ブラウザーの互換性

{{Compat}}
