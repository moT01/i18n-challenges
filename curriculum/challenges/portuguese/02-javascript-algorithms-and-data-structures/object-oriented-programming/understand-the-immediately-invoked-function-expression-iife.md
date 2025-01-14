---
id: 587d7db2367417b2b2512b8b
title: Entender a expressão de função invocada imediatamente (IIFE)
challengeType: 1
forumTopicId: 301328
dashedName: understand-the-immediately-invoked-function-expression-iife
---

# --description--

A common pattern in JavaScript is to execute a function as soon as it is declared:

```js
(function () {
  console.log("Chirp, chirp!");
})();
```

Essa é uma expressão de função anônima que executa logo após ser declarada, e exibe imediatamente no console `Chirp, chirp!`.

Note que a função não possui nome e não é armazenada em uma variável. Os dois parênteses () ao final da expressão da função faz com que ela seja imediatamente executada ou invocada. Este padrão é conhecido como <dfn>immediately invoked function expression (expressão de função invocada imediatamente)</dfn> ou <dfn>IIFE</dfn>.

# --instructions--

Rescreva a função `makeNest` e remova a chamada a ela para que no lugar seja uma expressão de função imediatamente invocada (IIFE) anônima.

# --hints--

A função deve ser anônima.

```js
assert(/\((function|\(\))(=>|\(\)){?/.test(__helpers.removeJSComments(code).replace(/\s/g, '')));
```

A função deve ter parênteses no final da expressão para chamar ela imediatamente.

```js
assert(/\(.*(\)\(|\}\(\))\)/.test(__helpers.removeJSComments(code).replace(/[\s;]/g, '')));
```

# --seed--

## --seed-contents--

```js
function makeNest() {
  console.log("A cozy nest is ready");
}

makeNest();
```

# --solutions--

```js
(function () {
  console.log("A cozy nest is ready");
})();
```

---

```js
(function () {
  console.log("A cozy nest is ready");
}());
```

---

```js
(() => {
  console.log("A cozy nest is ready");
})();
```

---

```js
(() =>
  console.log("A cozy nest is ready")
)();
```
