---
id: 5a9036d038fddaf9a66b5d32
title: 使用 grid-template-columns 添加多列
challengeType: 0
videoUrl: 'https://scrimba.com/p/pByETK/c7NzDHv'
forumTopicId: 301117
dashedName: add-columns-with-grid-template-columns
---

# --description--

Simply creating a grid element doesn't get you very far. You need to define the structure of the grid as well. To add some columns to the grid, use the `grid-template-columns` property on a grid container as demonstrated below:

```css
.container {
  display: grid;
  grid-template-columns: 50px 50px;
}
```

上面的代码会在网格容器中添加两列，宽度均为 50px。 `grid-template-columns` 属性值的个数表示网格的列数，每个值表示相应的列宽度。

# --instructions--

请给网格容器设置三个列，每列宽度均为 `100px`。

# --hints--

class 为 `container` 的元素应具有 `grid-template-columns` 属性，该属性应有三个属性值，均为 `100px`。

```js
const templateColumns = new __helpers.CSSHelp(document).getStyle(
  '.container'
)?.gridTemplateColumns;
assert.strictEqual(templateColumns, '100px 100px 100px');
```

# --seed--

## --seed-contents--

```html
<style>
  .d1 {
    background: LightSkyBlue;
  }
  .d2 {
    background: LightSalmon;
  }
  .d3 {
    background: PaleTurquoise;
  }
  .d4 {
    background: LightPink;
  }
  .d5 {
    background: PaleGreen;
  }

  .container {
    font-size: 40px;
    width: 100%;
    background: LightGray;
    display: grid;
    /* Only change code below this line */


    /* Only change code above this line */
  }
</style>

<div class="container">
  <div class="d1">1</div>
  <div class="d2">2</div>
  <div class="d3">3</div>
  <div class="d4">4</div>
  <div class="d5">5</div>
</div>
```

# --solutions--

```html
<style>
  .container {
    grid-template-columns: 100px 100px 100px;
  }
</style>
```
