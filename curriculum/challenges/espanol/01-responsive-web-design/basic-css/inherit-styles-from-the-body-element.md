---
id: bad87fee1348bd9aedf08746
title: Hereda estilos del elemento body
challengeType: 0
videoUrl: 'https://scrimba.com/c/c9bmdtR'
forumTopicId: 18204
dashedName: inherit-styles-from-the-body-element
---

# --description--

Ahora hemos demostrado que cada página HTML tiene un elemento `body`, y que a este elemento `body` también se le puede dar estilo con CSS.

Recuerda, puedes dar estilo a tu elemento `body` como a cualquier otro elemento HTML, y todos los demás elementos heredarán los estilos del elemento `body`.

# --instructions--

First, create an `h1` element with the text `Hello World`.

Luego, demos el color `green` (verde) a todos los elementos de tu página, añadiendo `color: green;` a tu declaración de estilo del elemento `body`.

Finalmente, da a tu elemento `body` un valor para font-family de `monospace` añadiendo `font-family: monospace;` a la declaración de estilo del elemento `body`.

# --hints--

Debes crear un elemento `h1`.

```js
assert.isNotEmpty(document.querySelectorAll('h1'));
```

Tu elemento `h1` debe contener el texto `Hello World`.

```js
assert.match(
  document.querySelector('h1').textContent,
  /hello world/i
);
```

Tu elemento `h1` debe tener una etiqueta de cierre.

```js
const commentlessCode = __helpers.removeHtmlComments(code);
assert.match(commentlessCode, /<\/h1>/g);
assert.match(commentlessCode, /<h1/g);
assert.lengthOf(commentlessCode.match(/<\/h1>/g), commentlessCode.match(/<h1/g).length);
```

Tu elemento `body` debe tener la propiedad `color` con el valor `green`.

```js
const bodyElement = document.querySelector('body');
const color = window.getComputedStyle(bodyElement)['color']; 
assert.strictEqual(color, 'rgb(0, 128, 0)');
```

Tu elemento `body` debe tener la propiedad `font-family` con el valor `monospace`.

```js
const bodyElement = document.querySelector('body');
const fontFamily = window.getComputedStyle(bodyElement)['font-family'];
assert.include(fontFamily.toLowerCase(), "monospace");
```

Tu elemento `h1` debe heredar la fuente `monospace` de tu elemento `body`.

```js
const h1Element = document.querySelector('h1');
const fontFamily = window.getComputedStyle(h1Element)['font-family'];
assert.include(fontFamily.toLowerCase(), "monospace");
```

Tu elemento `h1` debe heredar el color `green` de tu elemento `body`.

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
