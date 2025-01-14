---
id: bad87fee1348bd9aede08817
title: 將 a 嵌套在段落中
challengeType: 0
forumTopicId: 18244
dashedName: nest-an-anchor-element-within-a-paragraph
---

# --description--

You can nest links within other text elements.

```html
<p>
  Here's a <a target="_blank" href="https://www.freecodecamp.org"> link to www.freecodecamp.org</a> for you to follow.
</p>
```

讓我們來拆解一下這個例子。 通常，文本是被包裹在 `p` 元素內：

```html
<p> Here's a ... for you to follow. </p>
```

接下來是*錨*元素 `<a>`（它需要結束標籤 `</a>`）：

```html
<a> ... </a>
```

`target` 是錨元素的一個屬性，它用來指定鏈接的打開方式。 屬性值 `_blank` 表示鏈接會在新標籤頁打開。 `href` 是錨元素的另一個屬性，它用來指定鏈接的 URL：

```html
<a href="https://www.freecodecamp.org" target="_blank"> ... </a>
```

`a` 元素內的文本 `link to www.freecodecamp.org` 叫作<dfn>錨文本</dfn>，會顯示爲一個可以點擊的鏈接：

```html
<a href=" ... " target="...">link to freecodecamp.org</a>
```

此示例的最終輸出結果是這樣：

Here's a <a href="https://www.freecodecamp.org" target="_blank">link to www.freecodecamp.org</a> for you to follow.

# --instructions--

創建一個新的段落 `p` 元素來包裹 `a` 元素。 不要創建一個新的錨標籤。 新段落應有文本 `View more cat photos`，其中 `cat photos` 是一個鏈接，其餘是純文本。

# --hints--

應該只有一個 `a` 元素。

```js
assert.lengthOf(document.querySelectorAll('a'), 1 );
```

`a` 元素應該鏈接到 “`https://www.freecatphotoapp.com`”。

```js
assert.lengthOf(document.querySelectorAll('a[href="https://www.freecatphotoapp.com"]'),1);
```

`a` 元素應有錨文本 `cat photos`。

```js
assert.match(document.querySelector('a').textContent,/cat\sphotos/gi)
```

應該創建一個新的 `p` 元素。 頁面中應至少包含 3 個 `p` 標籤。

```js
assert.lengthOf(document.querySelectorAll('p'),3)
```

`a` 應嵌套在新創建的 `p` 元素內。

```js
const anchorParent = document.querySelector('a[href="https://www.freecatphotoapp.com"]').parentNode;
assert.strictEqual(anchorParent.tagName,"P")
```

`p` 元素應該包含文本 `View more`（在它後面有一個空格）。

```js
const textContent = document.querySelector('a[href="https://www.freecatphotoapp.com"]').parentNode.textContent;
assert.match(textContent,/View\smore\s/gi);
```

`a` 元素 <em>不</em> 應有文本 `View more`。

```js
assert.notMatch(document.querySelector('a').textContent,/View\smore/gi); 
```

確保每個 `p` 元素有結束標籤。

```js
assert.match(code,/<\/p>/g);
assert.match(code,/<p/g);
assert.strictEqual(code.match(/<\/p>/g).length,code.match(/<p/g).length);
```

確保每個 `a` 元素有結束標籤。

```js
assert.match(code,/<\/a>/g);
assert.match(code,/<a/g);
assert.strictEqual(code.match(/<\/a>/g).length,code.match(/<a/g).length);
```

# --seed--

## --seed-contents--

```html
<h2>CatPhotoApp</h2>
<main>

  <a href="https://www.freecatphotoapp.com" target="_blank">cat photos</a>

  <img src="https://cdn.freecodecamp.org/curriculum/cat-photo-app/relaxing-cat.jpg" alt="A cute orange cat lying on its back.">

  <p>Kitty ipsum dolor sit amet, shed everywhere shed everywhere stretching attack your ankles chase the red dot, hairball run catnip eat the grass sniff.</p>
  <p>Purr jump eat the grass rip the couch scratched sunbathe, shed everywhere rip the couch sleep in the sink fluffy fur catnip scratched.</p>
</main>
```

# --solutions--

```html
<h2>CatPhotoApp</h2>
<main>
  <p>View more <a target="_blank" href="https://www.freecatphotoapp.com">cat photos</a></p>

  <img src="https://cdn.freecodecamp.org/curriculum/cat-photo-app/relaxing-cat.jpg" alt="A cute orange cat lying on its back.">

  <p>Kitty ipsum dolor sit amet, shed everywhere shed everywhere stretching attack your ankles chase the red dot, hairball run catnip eat the grass sniff.</p>
  <p>Purr jump eat the grass rip the couch scratched sunbathe, shed everywhere rip the couch sleep in the sink fluffy fur catnip scratched.</p>
</main>
```
