---
id: bad87fee1348bd9aec908857
title: Usa comentarios para aclarar el código
challengeType: 0
forumTopicId: 18347
dashedName: use-comments-to-clarify-code
---

# --description--

Cuando empecemos a usar jQuery, vamos a modificar elementos HTML sin necesidad de cambiarlos en HTML.

Vamos a asegurarnos de que todos sepan que no deben modificar nada de este código directamente.

Recuerda que puedes empezar un comentario con `<!--` y terminarlo con `-->`

Agrega un comentario en la parte superior de tu HTML que diga `Code below this line should not be changed`

# --hints--

Debes comenzar un comentario en la parte superior de tu HTML con `<!--`.

```js
assert.match(code,(/^\s*<!--/));
```

Tu comentario debe tener el texto `Code below this line should not be changed`.

```js
assert.match(code,(/<!--(?!(>|->|.*-->.*this line))\s*.*this line.*\s*-->/gi));
```

Debes cerrar tu comentario con`-->`.

```js
assert.match(code,(/-->.*\n+.+/g));
```

Debes tener el mismo número de aperturas y cierres de comentarios.

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
