---
id: bad87fee1348bd9aec908857
title: Використайте коментарі, щоб уточнити код
challengeType: 0
forumTopicId: 18347
dashedName: use-comments-to-clarify-code
---

# --description--

When we start using jQuery, we will modify HTML elements without needing to actually change them in HTML.

Потрібно переконатись, що всі знають, що цей код не потрібно змінювати напряму.

Пам’ятайте, що коментар починається з `<!--` та закінчується на `-->`

Додайте коментар зверху HTML, який повідомляє, що `Code below this line should not be changed`

# --hints--

Розпочніть коментар з `<!--` зверху свого HTML.

```js
assert.match(code,(/^\s*<!--/));
```

Коментар повинен мати текст `Code below this line should not be changed`.

```js
assert.match(code,(/<!--(?!(>|->|.*-->.*this line))\s*.*this line.*\s*-->/gi));
```

Завершіть коментар на `-->`.

```js
assert.match(code,(/-->.*\n+.+/g));
```

Кількість символів початку та кінця коментарів має бути однаковою.

```js
assert.equal(code.match(/<!--/g).length,code.match(/-->/g).length);
```

# --seed--

## --seed-contents--

```html
<div class="container-fluid">
  <h3 class="text-primary text-center">jQuery Playground</h3>
  <div class="row">
    <div class="col-xs-6">
      <h4>#left-well</h4>
      <div class="well" id="left-well">
        <button class="btn btn-default target" id="target1">#target1</button>
        <button class="btn btn-default target" id="target2">#target2</button>
        <button class="btn btn-default target" id="target3">#target3</button>
      </div>
    </div>
    <div class="col-xs-6">
      <h4>#right-well</h4>
      <div class="well" id="right-well">
        <button class="btn btn-default target" id="target4">#target4</button>
        <button class="btn btn-default target" id="target5">#target5</button>
        <button class="btn btn-default target" id="target6">#target6</button>
      </div>
    </div>
  </div>
</div>
```

# --solutions--

```html
<!-- Code below this line should not be changed -->
<div class="container-fluid">
  <h3 class="text-primary text-center">jQuery Playground</h3>
  <div class="row">
    <div class="col-xs-6">
      <h4>#left-well</h4>
      <div class="well" id="left-well">
        <button class="btn btn-default target" id="target1">#target1</button>
        <button class="btn btn-default target" id="target2">#target2</button>
        <button class="btn btn-default target" id="target3">#target3</button>
      </div>
    </div>
    <div class="col-xs-6">
      <h4>#right-well</h4>
      <div class="well" id="right-well">
        <button class="btn btn-default target" id="target4">#target4</button>
        <button class="btn btn-default target" id="target5">#target5</button>
        <button class="btn btn-default target" id="target6">#target6</button>
      </div>
    </div>
  </div>
</div>
```
