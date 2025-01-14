---
id: 587d7da9367417b2b2512b6a
title: Повернення відсортованого масиву без зміни вихідного масиву
challengeType: 1
forumTopicId: 301237
dashedName: return-a-sorted-array-without-changing-the-original-array
---

# --description--

A side effect of the `sort` method is that it changes the order of the elements in the original array. In other words, it mutates the array in place. One way to avoid this is to first concatenate an empty array to the one being sorted (remember that `slice` and `concat` return a new array), then run the `sort` method.

# --instructions--

Використайте метод `sort` у функції `nonMutatingSort`, щоб відсортувати елементи масиву у порядку зростання. Функція повинна повернути новий масив і не змінювати змінну `globalArray`.

# --hints--

Ваш код повинен використовувати метод `sort`.

```js
assert(nonMutatingSort.toString().match(/\.sort/g));
```

Змінна `globalArray` не повинна змінюватись.

```js
assert(JSON.stringify(globalArray) === JSON.stringify([5, 6, 3, 2, 9]));
```

`nonMutatingSort(globalArray)` має повертати `[2, 3, 5, 6, 9]`.

```js
assert(
  JSON.stringify(nonMutatingSort(globalArray)) ===
    JSON.stringify([2, 3, 5, 6, 9])
);
```

Не закодовуйте `nonMutatingSort(globalArray)` складно.

```js
assert(!nonMutatingSort.toString().match(/\[.*?[23569].*?\]/gs));
```

Функція повинна повертати новий масив, а не переданий масив.

```js
assert(nonMutatingSort(globalArray) !== globalArray);
```

`nonMutatingSort([1, 30, 4, 21, 100000])` має повертати `[1, 4, 21, 30, 100000]`.

```js
assert(JSON.stringify(nonMutatingSort([1, 30, 4, 21, 100000])) ===
    JSON.stringify([1, 4, 21, 30, 100000]))
```

`nonMutatingSort([140000, 104, 99])` має повертати `[99, 104, 140000]`.

```js
assert(JSON.stringify(nonMutatingSort([140000, 104, 99])) ===
    JSON.stringify([99, 104, 140000]))
```

# --seed--

## --seed-contents--

```js
const globalArray = [5, 6, 3, 2, 9];

function nonMutatingSort(arr) {
  // Only change code below this line


  // Only change code above this line
}

nonMutatingSort(globalArray);
```

# --solutions--

```js
const globalArray = [5, 6, 3, 2, 9];
function nonMutatingSort(arr) {
  return [].concat(arr).sort((a,b) => a-b);
}
```
