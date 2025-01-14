---
id: 587d7b7c367417b2b2512b1a
title: 使用方括號訪問屬性名稱
challengeType: 1
forumTopicId: 301150
dashedName: access-property-names-with-bracket-notation
---

# --description--

In the first object challenge we mentioned the use of bracket notation as a way to access property values using the evaluation of a variable. For instance, imagine that our `foods` object is being used in a program for a supermarket cash register. We have some function that sets the `selectedFood` and we want to check our `foods` object for the presence of that food. This might look like:

```js
let selectedFood = getCurrentFood(scannedItem);
let inventory = foods[selectedFood];
```

上述代碼會先讀取 `selectedFood` 變量的值，並返回 `foods` 對象中以該值命名的屬性所對應的屬性值。 若沒有以該值命名的屬性，則會返回 `undefined`。 有時候對象的屬性名在運行之前是不確定的，或者我們需要動態地訪問對象的屬性值。在這些場景下，方括號表示法就變得十分有用。

# --instructions--

我們已經定義了 `checkInventory` 函數，它接受一個被掃描到的商品名作爲輸入參數。 請讓這個函數返回 `foods` 對象中，以 `scannedItem` 的值所命名的屬性對應的屬性值。 在本挑戰中，只有合理有效的屬性名會作爲參數傳入 `checkInventory`，因此你不需要處理參數無效的情況。

# --hints--

`checkInventory` 應是一個函數。

```js
assert.strictEqual(typeof checkInventory, 'function');
```

`foods` 對象應只包含以下鍵值對：`apples: 25`、`oranges: 32`、`plums: 28`、`bananas: 13`、`grapes: 35`、`strawberries: 27`。

```js
assert.deepEqual(foods, {
  apples: 25,
  oranges: 32,
  plums: 28,
  bananas: 13,
  grapes: 35,
  strawberries: 27
});
```

`checkInventory("apples")` 應返回 `25`。

```js
assert.strictEqual(checkInventory('apples'), 25);
```

`checkInventory("bananas")` 應返回 `13`。

```js
assert.strictEqual(checkInventory('bananas'), 13);
```

`checkInventory("strawberries")` 應返回 `27`。

```js
assert.strictEqual(checkInventory('strawberries'), 27);
```

# --seed--

## --seed-contents--

```js
let foods = {
  apples: 25,
  oranges: 32,
  plums: 28,
  bananas: 13,
  grapes: 35,
  strawberries: 27
};

function checkInventory(scannedItem) {
  // Only change code below this line

  // Only change code above this line
}

console.log(checkInventory("apples"));
```

# --solutions--

```js
let foods = {
  apples: 25,
  oranges: 32,
  plums: 28,
  bananas: 13,
  grapes: 35,
  strawberries: 27
};

function checkInventory(scannedItem) {
  return foods[scannedItem];
}
```
