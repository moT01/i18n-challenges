---
id: bad87fee1348bd9aedf08756
title: Priorisiere einen Stil über einen anderen
challengeType: 0
videoUrl: 'https://scrimba.com/c/cZ8wnHv'
forumTopicId: 18258
dashedName: prioritize-one-style-over-another
---

# --description--

Sometimes your HTML elements will receive multiple styles that conflict with one another.

Zum Beispiel kann dein `h1`-Element nicht grün und pink gleichzeitig sein.

Sehen wir mal was passiert, wenn wir eine Klasse erstellen die Text pink färbt und es auf ein Element anwenden. Wird unsere Klasse die CSS-Eigenschaft `color: green;` unseres `body`-Elements *überschreiben*?

# --instructions--

Erstelle eine CSS-Klasse namens `pink-text`, die einem Element die Farbe Pink gibt.

Weise deinem `h1`-Element die Klasse `pink-text` zu.

# --hints--

Dein `h1`-Element sollte die Klasse `pink-text` besitzen.

```js
assert.isTrue(document.querySelector('h1').classList.contains('pink-text'));
```

Dein `<style>` sollte eine `pink-text` CSS-Klasse haben, die `color` ändert.

```js
assert.match(__helpers.removeCssComments(code), /\.pink-text\s*\{\s*color\s*:\s*.+\s*;?\s*\}/g);
```

Dein `h1`-Element sollte pink sein.

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
</style>
<h1>Hello World!</h1>
```

# --solutions--

```html
<style>
  body {
    background-color: black;
    font-family: monospace;
    color: green;
  }
  .pink-text {
    color: pink;
  }
</style>
<h1 class="pink-text">Hello World!</h1>
```
