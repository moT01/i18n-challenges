---
id: bad87fee1348bd9aedf08804
title: 給 HTML 添加註釋
challengeType: 0
videoUrl: 'https://scrimba.com/p/pVMPUv/cGyGbca'
forumTopicId: 16782
dashedName: comment-out-html
---

# --description--

Remember that in order to start a comment, you need to use `<!--` and to end a comment, you need to use `-->`

現在你需要在 `h2` 元素開始前終止註釋。

# --instructions--

註釋掉 `h1` 元素和 `p` 元素，保留 `h2` 元素。

# --hints--

應註釋掉 `h1` 元素，這樣它就從網頁上消失了。

```js
assert.isEmpty(document.querySelectorAll('h1'));
```

`h2` 元素應保持原樣，這樣網頁上還能看到它。

```js
assert.isNotEmpty(document.querySelectorAll('h2'));
```

應註釋掉 `p` 元素，這樣它就從網頁上消失了。

```js
assert.isEmpty(document.querySelectorAll('p'));
```

每一個註釋都應以 `-->` 結尾。

```js
assert.isAbove(code.match(/[^fc]-->/g).length, 1);
```

不要更改 `h1`、`h2`、`p` 元素的順序。

```js
assert.strictEqual(code.match(/<([a-z0-9]){1,2}>/g)[0],'<h1>');
assert.strictEqual(code.match(/<([a-z0-9]){1,2}>/g)[1],'<h2>');
assert.strictEqual(code.match(/<([a-z0-9]){1,2}>/g)[2],'<p>');
```

# --seed--

## --seed-contents--

```html
<!--
<h1>Hello World</h1>

<h2>CatPhotoApp</h2>

<p>Kitty ipsum dolor sit amet, shed everywhere shed everywhere stretching attack your ankles chase the red dot, hairball run catnip eat the grass sniff.</p>
-->
```

# --solutions--

```html
<!--<h1>Hello World</h1>-->
<h2>CatPhotoApp</h2> 
<!--<p>Kitty ipsum dolor sit amet, shed everywhere shed everywhere stretching attack your ankles chase the red dot, hairball run catnip eat the grass sniff.</p> -->
```
