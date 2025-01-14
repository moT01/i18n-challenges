---
id: bad87fee1348bd9aedf08820
title: 給圖片添加鏈接
challengeType: 0
videoUrl: 'https://scrimba.com/p/pVMPUv/cRdBnUr'
forumTopicId: 18327
dashedName: turn-an-image-into-a-link
---

# --description--

You can make elements into links by nesting them within an `a` element.

如果我們要把圖片嵌套進 `a` 元素， 這是一個示例：

```html
<a href="#"><img src="https://cdn.freecodecamp.org/curriculum/cat-photo-app/relaxing-cat.jpg" alt="Three kittens running towards the camera."></a>
```

如果把 `a` 的 `href` 屬性值設置爲 `#`，創建的是一個死鏈接（不跳轉到其他畫面）。

# --instructions--

請把現存的圖片嵌套進 `a`（ *錨點*）元素中。

完成後，請你把鼠標光標懸停在你的圖像上， 鼠標光標將變成點擊光標。 於是圖片就變成了鏈接。

# --hints--

應將 `img` 嵌套進 `a` 元素中。

```js
const anchor = document.querySelectorAll('a')[1];
const children = anchor.querySelectorAll("img");
assert.notEmpty(children);
```

你的 `a` 元素應該是一個死鏈接，具有值爲 `#` 的 `href` 屬性。

```js
const anchor = document.querySelectorAll('a')[1];
const parentHREF = anchor.querySelector("img").parentNode.getAttribute('href');
assert.match(parentHREF,new RegExp('#'));
```

每個 `a` 元素都應該有一個結束標籤。

```js
assert.match(code,/<\/a>/g);
assert.match(code,/<a/g);
assert.strictEqual(code.match(/<\/a>/g).length, code.match(/<a/g).length)
```

# --seed--

## --seed-contents--

```html
<h2>CatPhotoApp</h2>
<main>
  <p>Click here to view more <a href="#">cat photos</a>.</p>

  <img src="https://cdn.freecodecamp.org/curriculum/cat-photo-app/relaxing-cat.jpg" alt="A cute orange cat lying on its back.">

  <p>Kitty ipsum dolor sit amet, shed everywhere shed everywhere stretching attack your ankles chase the red dot, hairball run catnip eat the grass sniff.</p>
  <p>Purr jump eat the grass rip the couch scratched sunbathe, shed everywhere rip the couch sleep in the sink fluffy fur catnip scratched.</p>
</main>
```

# --solutions--

```html
<h2>CatPhotoApp</h2>
<main>
  <p>Click here to view more <a href="#">cat photos</a>.</p>

  <a href="#"><img src="https://cdn.freecodecamp.org/curriculum/cat-photo-app/relaxing-cat.jpg" alt="A cute orange cat lying on its back."></a>

  <p>Kitty ipsum dolor sit amet, shed everywhere shed everywhere stretching attack your ankles chase the red dot, hairball run catnip eat the grass sniff.</p>
  <p>Purr jump eat the grass rip the couch scratched sunbathe, shed everywhere rip the couch sleep in the sink fluffy fur catnip scratched.</p>
</main>
```
