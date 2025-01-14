---
id: bad87fee1348bd9aedf08746
title: Herdar estilos do elemento body
challengeType: 0
videoUrl: 'https://scrimba.com/c/c9bmdtR'
forumTopicId: 18204
dashedName: inherit-styles-from-the-body-element
---

# --description--

Now we've proven that every HTML page has a `body` element, and that its `body` element can also be styled with CSS.

Lembre-se de que você pode definir o estilo do elemento `body` como qualquer outro elemento HTML, e todos os outros elementos herdarão os estilos do elemento `body`.

# --instructions--

First, create an `h1` element with the text `Hello World`.

Então, vamos dar a todos os elementos da página a cor `green` adicionando `color: green;` à declaração de estilo do elemento `body`.

Por fim, dê ao elemento `body` a tipografia `monospace` adicionando `font-family: monospace;` à declaração de estilo do elemento `body`.

# --hints--

Você deve criar um elemento `h1`.

```js
assert.isNotEmpty(document.querySelectorAll('h1'));
```

O elemento `h1` deve conter o texto `Hello World`.

```js
assert.match(
  document.querySelector('h1').textContent,
  /hello world/i
);
```

O elemento `h1` deve ter uma tag de fechamento.

```js
const commentlessCode = __helpers.removeHtmlComments(code);
assert.match(commentlessCode, /<\/h1>/g);
assert.match(commentlessCode, /<h1/g);
assert.lengthOf(commentlessCode.match(/<\/h1>/g), commentlessCode.match(/<h1/g).length);
```

O elemento `body` deve ter a propriedade `color` com o valor `green`.

```js
const bodyElement = document.querySelector('body');
const color = window.getComputedStyle(bodyElement)['color']; 
assert.strictEqual(color, 'rgb(0, 128, 0)');
```

O elemento `body` deve ter a propriedade `font-family` com o valor `monospace`.

```js
const bodyElement = document.querySelector('body');
const fontFamily = window.getComputedStyle(bodyElement)['font-family'];
assert.include(fontFamily.toLowerCase(), "monospace");
```

O elemento `h1` deve herdar a fonte `monospace` do elemento `body`.

```js
const h1Element = document.querySelector('h1');
const fontFamily = window.getComputedStyle(h1Element)['font-family'];
assert.include(fontFamily.toLowerCase(), "monospace");
```

O elemento `h1` deve herdar a cor `green` do elemento `body`.

```js
const h1Element = document.querySelector('h1');
const color = window.getComputedStyle(h1Element)['color'];
assert.strictEqual(color, 'rgb(0, 128, 0)');
```

# --seed--

## --seed-contents--

```html
<style>
  body {
    background-color: black;
  }

</style>
```

# --solutions--

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
