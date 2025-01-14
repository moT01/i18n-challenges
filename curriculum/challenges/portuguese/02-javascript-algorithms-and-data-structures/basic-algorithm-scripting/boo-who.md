---
id: a77dbc43c33f39daa4429b4f
title: Identificar verdadeiro ou falso
challengeType: 1
forumTopicId: 16000
dashedName: boo-who
---

# --description--

Verifique se um valor é classificado como booleano primitivo. Retorna `true` ou `false`.

Os booleanos primitivos são `true` e `false`.

# --hints--

`booWho(true)` deve retornar `true`.

```js
assert.isTrue(booWho(true));
```

`booWho(false)` deve retornar `true`.

```js
assert.isTrue(booWho(false));
```

`booWho([1,2,3])` deve retornar `false`.

```js
assert.isFalse(booWho([1, 2, 3]));
```

`booWho([].slice)` deve retornar `false`.

```js
assert.isFalse(booWho([].slice));
```

`booWho({"a": 1})` deve retornar `false`.

```js
assert.isFalse(booWho({ a: 1 }));
```

`booWho(1)` deve retornar `false`.

```js
assert.isFalse(booWho(1));
```

`booWho(NaN)` deve retornar `false`.

```js
assert.isFalse(booWho(NaN));
```

`booWho("a")` deve retornar `false`.

```js
assert.isFalse(booWho('a'));
```

`booWho("true")` deve retornar `false`.

```js
assert.isFalse(booWho('true'));
```

`booWho("false")` deve retornar `false`.

```js
assert.isFalse(booWho('false'));
```

# --seed--

## --seed-contents--

```js
function booWho(bool) {
  return bool;
}

booWho(null);
```

# --solutions--

```js
function booWho(bool) {
  return typeof bool === 'boolean';
}

booWho(null);
```
