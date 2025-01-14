---
id: 587d7b7b367417b2b2512b17
title: 使用展開運算符合並數組
challengeType: 1
forumTopicId: 301156
dashedName: combine-arrays-with-the-spread-operator
---

# --description--

Another huge advantage of the <dfn>spread</dfn> operator is the ability to combine arrays, or to insert all the elements of one array into another, at any index. With more traditional syntaxes, we can concatenate arrays, but this only allows us to combine arrays at the end of one, and at the start of another. Spread syntax makes the following operation extremely simple:

```js
let thisArray = ['sage', 'rosemary', 'parsley', 'thyme'];

let thatArray = ['basil', 'cilantro', ...thisArray, 'coriander'];
```

`thatArray` 會有值 `['basil', 'cilantro', 'sage', 'rosemary', 'parsley', 'thyme', 'coriander']`

使用展開語法，我們就可以很方便的實現一個用傳統方法會寫得很複雜且冗長的操作。

# --instructions--

我們已經定義了一個返回 `sentence` 變量的 `spreadOut` 函數。 請修改這個函數，利用 <dfn>spread</dfn> 使該函數返回數組 `['learning', 'to', 'code', 'is', 'fun']`。

# --hints--

`spreadOut` 應返回 `["learning", "to", "code", "is", "fun"]`。

```js
assert.deepEqual(spreadOut(), ['learning', 'to', 'code', 'is', 'fun']);
```

`spreadOut` 函數裏應用到展開語法。

```js
assert.notStrictEqual(spreadOut.toString().search(/[...]/), -1);
```

# --seed--

## --seed-contents--

```js
function spreadOut() {
  let fragment = ['to', 'code'];
  let sentence; // Change this line
  return sentence;
}

console.log(spreadOut());
```

# --solutions--

```js
function spreadOut() {
  let fragment = ['to', 'code'];
  let sentence = ['learning', ...fragment, 'is', 'fun'];
  return sentence;
}
```
