---
id: bad87fee1348bd9aedf08801
title: Informar com o elemento de parágrafo
challengeType: 0
videoUrl: 'https://scrimba.com/p/pVMPUv/ceZ7DtN'
forumTopicId: 18202
dashedName: inform-with-the-paragraph-element
---

# --description--

The `p` element is the preferred element for paragraph text on websites. `p` is short for "paragraph".

Você pode criar um elemento de parágrafo da seguinte forma:

```html
<p>I'm a p tag!</p>
```

# --instructions--

Crie um elemento `p` abaixo do elemento `h2` e dê a ele o texto `Hello Paragraph`.

**Observação:** é uma convenção que todas as tags HTML sejam escritas em letras minúsculas (por exemplo, `<p></p>` em vez de `<P></P>`).

# --hints--

Seu código deve ter um elemento `p` válido.

```js
assert.lengthOf(document.querySelectorAll('p'),1);
```

O elemento `p` deve conter o texto `Hello Paragraph`.

```js
assert.match(document.querySelector('p').textContent,/hello(\s)+paragraph/gi);
```

O elemento `p` deve ter uma tag de fechamento.

```js
assert.match(code,/<\/p>/g);
assert.strictEqual(code.match(/<\/p>/g).length,code.match(/<p/g).length);
```

# --seed--

## --seed-contents--

```html
<h1>Hello World</h1>
<h2>CatPhotoApp</h2>
```

# --solutions--

```html
<h1>Hello World</h1>
<h2>CatPhotoApp</h2>
<p>Hello Paragraph</p>
```
