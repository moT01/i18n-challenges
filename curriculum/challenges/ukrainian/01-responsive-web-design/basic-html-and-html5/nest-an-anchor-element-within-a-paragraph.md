---
id: bad87fee1348bd9aede08817
title: Вставте якірний елемент в Абзац
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

Давайте зупинимося на прикладі. Звичайний текст поміщений в елемент:`p`:

```html
<p> Here's a ... for you to follow. </p>
```

Далі йде   *anchor* element `<a>` (який вимагає кінцевого тегу `</a>`):

```html
<a> ... </a>
```

`target` це атрибут прив’язного тегу, який визначає, де відкрити посилання. Значення вказує на відкриття посилання в новій вкладці`_blank`. `href` є атрибутом прив’язки, який містить URL адресу посилання:

```html
<a href="https://www.freecodecamp.org" target="_blank"> ... </a>
```

Текст `link to www.freecodecamp.org`, усередині `a`елемента, який називається <dfn>anchor text</dfn> буде відображати посилання, на яке потрібно натиснути:

```html
<a href=" ... " target="...">link to freecodecamp.org</a>
```

Кінцевий результат прикладу буде виглядати наступним чином:

Here's a <a href="https://www.freecodecamp.org" target="_blank">link to www.freecodecamp.org</a> for you to follow.

# --instructions--

Вкласти існуючий `a`елемент в новий `p` елемент. Не створюйте нову мітку для прив'язки. У новому абзаці має бути текст із зазначенням `View more cat photos` де `cat photos` є посиланням, а решта - простим текстом.

# --hints--

У вас має бути тільки один елемент `a`.

```js
assert.lengthOf(document.querySelectorAll('a'), 1 );
```

Eлемент `a` повинен покликатись на `https://www.freecatphotoapp.com`".

```js
assert.lengthOf(document.querySelectorAll('a[href="https://www.freecatphotoapp.com"]'),1);
```

Ваш `a` елемент повинен складатися з ідентифікатору `cat photos`

```js
assert.match(document.querySelector('a').textContent,/cat\sphotos/gi)
```

Ви повинні створити новий  елемент `p`. У вашому HTML-коді повинно бути не менше трьох тегів.`p`.

```js
assert.lengthOf(document.querySelectorAll('p'),3)
```

Ваш `a` елемент повинен бути вкладений в новий елемент `p`.

```js
const anchorParent = document.querySelector('a[href="https://www.freecatphotoapp.com"]').parentNode;
assert.strictEqual(anchorParent.tagName,"P")
```

Елемент `p` повинен мати текст `View more` (з пропуском після нього).

```js
const textContent = document.querySelector('a[href="https://www.freecatphotoapp.com"]').parentNode.textContent;
assert.match(textContent,/View\smore\s/gi);
```

Ваш елемент `a` <em>not</em> не повинен мати текст `View more`.

```js
assert.notMatch(document.querySelector('a').textContent,/View\smore/gi); 
```

Кожен елемент `p` повинен мати кінцевий тег.

```js
assert.match(code,/<\/p>/g);
assert.match(code,/<p/g);
assert.strictEqual(code.match(/<\/p>/g).length,code.match(/<p/g).length);
```

Кожен елемент `a` повинен мати кінцевий тег.

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
