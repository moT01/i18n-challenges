---
id: bad87fee1348bd9aedf07756
title: Important 的優先級最高
challengeType: 0
videoUrl: 'https://scrimba.com/c/cm24rcp'
forumTopicId: 18249
dashedName: override-all-other-styles-by-using-important
---

# --description--

Yay! We just proved that inline styles will override all the CSS declarations in your `style` element.

不過， 還有一種方式可以覆蓋重新 CSS 樣式。 這是所有方法裏面最強大的一個。 在此之前，我們要考慮清楚，爲什麼我們要覆蓋 CSS 樣式。

很多時候，你會使用 CSS 庫， CSS 庫中的樣式會意外覆蓋你的 CSS 樣式。 如果想保證你的 CSS 樣式不受影響，你可以使用 `!important`。

讓我們回到 `pink-text` 類聲明。 `pink-text` 類的顏色樣式已被之後的 class 聲明、id 聲明以及行內樣式所覆蓋。

# --instructions--

給粉紅文本元素的顏色聲明添加關鍵詞 `!important`，以確保 `h1` 元素爲粉紅色。

如下所示：

```css
color: red !important;
```

# --hints--

`h1` 元素應包含 `pink-text` class。

```js
assert.isTrue(document.querySelector('h1').classList.contains('pink-text'));
```

`h1` 元素應包含 `blue-text` class。

```js
assert.isTrue(document.querySelector('h1').classList.contains('blue-text'));
```

`h1` 元素應有 `id`， 值爲 `orange-text`。

```js
assert.strictEqual(document.querySelector('h1').getAttribute('id'), 'orange-text');
```

`h1` 元素應有一個內聯樣式 `color: white`。

```js
const commentessCode = __helpers.removeHtmlComments(code);
assert.match(commentessCode, /<h1.*style/gi);
assert.match(commentessCode, /<h1.*style.*color\s*?:/gi);
```

`pink-text` class 應有 `!important` 關鍵詞 ，以覆蓋其他聲明。

```js
assert.match(__helpers.removeCssComments(code), /\.pink-text\s*?\{[\s\S]*?color:.*pink.*!important\s*;?[^\.]*\}/g);
```

`h1` 元素應爲粉紅色。

```js
const h1Element = document.querySelector('h1');
const color = window.getComputedStyle(h1Element)['color'];
assert.strictEqual(color, 'rgb(255, 192, 203)');
```

# --seed--

## --seed-contents--

```html
<style>
  body {
    background-color: black;
    font-family: monospace;
    color: green;
  }
  #orange-text {
    color: orange;
  }
  .pink-text {
    color: pink;
  }
  .blue-text {
    color: blue;
  }
</style>
<h1 id="orange-text" class="pink-text blue-text" style="color: white">Hello World!</h1>
```

# --solutions--

```html
<style>
  body {
    background-color: black;
    font-family: monospace;
    color: green;
  }
  #orange-text {
    color: orange;
  }
  .pink-text {
    color: pink !important;
  }
  .blue-text {
    color: blue;
  }
</style>
<h1 id="orange-text" class="pink-text blue-text" style="color: white">Hello World!</h1>
```
