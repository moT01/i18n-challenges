---
id: 595671d4d2cdc305f0d5b36f
title: 2 つの配列からハッシュを作成する
challengeType: 1
forumTopicId: 302283
dashedName: hash-from-two-arrays
---

# --description--

与えられた 2 つの配列を使用して、一方の配列の要素 (キー) と他方の要素 (値) を連結したハッシュオブジェクトを作成します。

例:

```js
const firstArr = [1, 2, 3];
const secondArr = ["a", "b", "c"];
const hashObj = arrToObj(firstArr, secondArr);
```

上記の配列から作成されるハッシュオブジェクトは `{1: "a", 2: "b", 3: "c"}` となります。

# --hints--

`arrToObj` は関数とします。

```js
assert(typeof arrToObj === 'function');
```

`arrToObj([1, 2, 3, 4, 5], ["a", "b", "c", "d", "e"])` は`{ 1: "a", 2: "b", 3: "c", 4: "d", 5: "e" }`を返す必要があります。

```js
assert.deepEqual(arrToObj(...testCases[0]), res[0]);
```

`arrToObj([1, 2, 3, 4, 5], ["a", "b", "c", "d"])`は`{ 1: "a", 2: "b", 3: "c", 4: "d", 5: undefined }`を返す必要があります。

```js
assert.deepEqual(arrToObj(...testCases[1]), res[1]);
```

`arrToObj([1, 2, 3], ["a", "b", "c", "d", "e"])` は`{ 1: "a", 2: "b", 3: "c" }`を返す必要があります。

```js
assert.deepEqual(arrToObj(...testCases[2]), res[2]);
```

`arrToObj(["a", "b", "c", "d", "e"], [1, 2, 3, 4, 5])` は `{ "a": 1, "b": 2, "c": 3 , "d": 4, "e": 5 }`を返す必要があります。

```js
assert.deepEqual(arrToObj(...testCases[3]), res[3]);
```

`arrToObj(["a", "b", "c", "d", "e"], [1, 2, 3, 4])` は `{ "a": 1, "b": 2, "c": 3 , "d": 4, "e": undefined }`を返す必要があります。

```js
assert.deepEqual(arrToObj(...testCases[4]), res[4]);
```

`arrToObj(["a", "b", "c"], [1, 2, 3, 4, 5])` は`{ "a": 1, "b": 2, "c": 3 }`を返す必要があります。

```js
assert.deepEqual(arrToObj(...testCases[5]), res[5]);
```

# --seed--

## --after-user-code--

```js
const testCases = [
  [[1, 2, 3, 4, 5], ['a', 'b', 'c', 'd', 'e']],
  [[1, 2, 3, 4, 5], ['a', 'b', 'c', 'd']],
  [[1, 2, 3], ['a', 'b', 'c', 'd', 'e']],
  [['a', 'b', 'c', 'd', 'e'], [1, 2, 3, 4, 5]],
  [['a', 'b', 'c', 'd', 'e'], [1, 2, 3, 4]],
  [['a', 'b', 'c'], [1, 2, 3, 4, 5]]
];

const res = [
  { 1: 'a', 2: 'b', 3: 'c', 4: 'd', 5: 'e' },
  { 1: 'a', 2: 'b', 3: 'c', 4: 'd', 5: undefined },
  { 1: 'a', 2: 'b', 3: 'c' },
  { a: 1, b: 2, c: 3, d: 4, e: 5 },
  { a: 1, b: 2, c: 3, d: 4, e: undefined },
  { a: 1, b: 2, c: 3 }
];
```

## --seed-contents--

```js
function arrToObj (keys, vals) {

  return true;
}
```

# --solutions--

```js
function arrToObj (keys, vals) {
  return keys.reduce((map, key, index) => {
    map[key] = vals[index];
    return map;
  }, {});
}
```
