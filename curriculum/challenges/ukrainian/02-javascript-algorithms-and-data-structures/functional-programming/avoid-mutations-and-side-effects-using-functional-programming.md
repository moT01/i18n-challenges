---
id: 587d7b8e367417b2b2512b5e
title: Уникнення мутацій та побічних ефектів завдяки функційному програмуванню
challengeType: 1
forumTopicId: 301228
dashedName: avoid-mutations-and-side-effects-using-functional-programming
---

# --description--

If you haven't already figured it out, the issue in the previous challenge was with the `splice` call in the `tabClose()` function. Unfortunately, `splice` changes the original array it is called on, so the second call to it used a modified array, and gave unexpected results.

Це малий приклад набагато більшого шаблону: ви викликаєте функцію на змінній, масиві чи об’єкті, а функція змінює змінну чи щось в об’єкті.

Один з основних принципів функційного програмування — нічого не змінювати. Зміни призводять до помилок. Легше уникнути помилок, знаючи, що ваші функції нічого не змінюють, включно з аргументами функцій чи будь-якою глобальною змінною.

У попередньому прикладі не було складних операцій, але метод `splice` змінив вихідний масив і видав помилку.

Пригадаємо, що у функційному програмуванні зміну називають <dfn>мутацією</dfn>, а наслідок називають <dfn>побічним ефектом</dfn>. В ідеалі функція повинна бути <dfn>чистою</dfn>, тобто не спричиняти жодних побічних ефектів.

Спробуємо опанувати цю дисципліну і не будемо змінювати будь-які змінні чи об’єкти в нашому коді.

# --instructions--

Заповніть код функції `incrementer` так, щоб вона повертала значення глобальної змінної `fixedValue`, збільшене на один.

# --hints--

Ваша функція `incrementer` не повинна змінювати значення `fixedValue` (дорівнює `4`).

```js
incrementer();
assert(fixedValue === 4);
```

Ваша функція `incrementer` повинна повертати значення, яке більше на одиницю за `fixedValue`.

```js
const __newValue = incrementer();
assert(__newValue === 5);
```

Ваша функція `incrementer` повинна повертати значення на основі значення глобальної змінної `fixedValue`.

```js
(function () {
  fixedValue = 10;
  const newValue = incrementer();
  assert(fixedValue === 10 && newValue === 11);
  fixedValue = 4;
})();
```

# --seed--

## --seed-contents--

```js
// The global variable
let fixedValue = 4;

function incrementer() {
  // Only change code below this line


  // Only change code above this line
}
```

# --solutions--

```js
let fixedValue = 4

function incrementer() {
  return fixedValue + 1
}
```
