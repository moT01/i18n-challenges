---
id: bad87fee1348bd9aedf08828
title: 创建一个有序列表
challengeType: 0
videoUrl: 'https://scrimba.com/p/pVMPUv/cQ3B8TM'
forumTopicId: 16824
dashedName: create-an-ordered-list
---

# --description--

HTML has another special element for creating <dfn>ordered lists</dfn>, or numbered lists.

有序列表以 `<ol>` 开始，中间包含一个或多个 `<li>` 元素。 最后以 `</ol>` 结束。

例如：

```html
<ol>
  <li>Garfield</li>
  <li>Sylvester</li>
</ol>
```

将创建一个包含 `Garfield` 和 `Sylvester` 的编号列表。

# --instructions--

请创建一个有序列表，内容是猫咪最讨厌的三样东西。

# --hints--

应包含一个有序列表，内容是猫咪最讨厌的三样东西（`Top 3 things cats hate:`）。

```js
const previousElement = document.querySelector('ol').previousElementSibling; 
assert.match(previousElement.textContent,/Top 3 things cats hate:/i);
```

应包含有一个无序列表，内容是猫咪最喜欢的东西（`Things cats love:`）。

```js
const previousElement = document.querySelector('ul').previousElementSibling; 
assert.match(previousElement.textContent,/Things cats love:/i);
```

页面应只包含一个 `ul` 元素。

```js
assert.lengthOf(document.querySelectorAll('ul'), 1);
```

页面应只包含一个 `ol` 元素。

```js
assert.lengthOf(document.querySelectorAll('ol'), 1);
```

`ul` 无序列表中应包含 3 个 `li` 元素。

```js
assert.lengthOf(document.querySelectorAll('ul li'), 3);
```

`ol` 有序列表应该包含 3 个 `li` 元素。

```js
assert.lengthOf(document.querySelectorAll('ol li'), 3);
```

`ul` 无序列表应有结束标签。

```js
assert.match(code,/<\/ul>/g);
assert.strictEqual(code.match(/<\/ul>/g).length ,code.match(/<ul>/g).length);
```

`ol` 有序列表应有结束标签。

```js
assert.match(code,/<\/ol>/g);
assert.strictEqual(code.match(/<\/ol>/g).length ,code.match(/<ol>/g).length);
```

`li` 元素应有结束标签。

```js
assert.match(code,/<\/li>/g);
assert.match(code,/<li>/g);
assert.strictEqual(code.match(/<\/li>/g).length ,code.match(/<li>/g).length);
```

无序列表里的 `li` 元素内容不应为空。

```js
[...document.querySelectorAll('ul li')].forEach((val) =>
  assert.isNotEmpty(__helpers.removeWhiteSpace(val.textContent))
);
```

有序列表里的 `li` 元素内容不应该为空。

```js
[...document.querySelectorAll('ol li')].forEach((val) =>
  assert.isNotEmpty(__helpers.removeWhiteSpace(val.textContent))
);
```

# --seed--

## --seed-contents--

```html
<h2>CatPhotoApp</h2>
<main>
  <p>Click here to view more <a href="#">cat photos</a>.</p>

  <a href="#"><img src="https://cdn.freecodecamp.org/curriculum/cat-photo-app/relaxing-cat.jpg" alt="A cute orange cat lying on its back."></a>

  <p>Things cats love:</p>
  <ul>
    <li>catnip</li>
    <li>laser pointers</li>
    <li>lasagna</li>
  </ul>
  <p>Top 3 things cats hate:</p>

</main>
```

# --solutions--

```html
<h2>CatPhotoApp</h2>
<main>
  <p>Click here to view more <a href="#">cat photos</a>.</p>

  <a href="#"><img src="https://cdn.freecodecamp.org/curriculum/cat-photo-app/relaxing-cat.jpg" alt="A cute orange cat lying on its back."></a>

  <p>Things cats love:</p>
  <ul>
    <li>catnip</li>
    <li>laser pointers</li>
    <li>lasagna</li>
  </ul>
  <p>Top 3 things cats hate:</p>
  <ol>
    <li>hate 1</li>
    <li>hate 2</li>
    <li>hate 3</li>
  </ol>
</main>
```
