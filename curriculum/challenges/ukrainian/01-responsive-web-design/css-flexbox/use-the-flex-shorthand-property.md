---
id: 587d78ae367417b2b2512afe
title: Використовуйте властивість гнучких скорочень
challengeType: 0
videoUrl: 'https://scrimba.com/p/pVaDAv/cbpW2tE'
forumTopicId: 301112
dashedName: use-the-flex-shorthand-property
---

# --description--

There is a shortcut available to set several flex properties at once. The `flex-grow`, `flex-shrink`, and `flex-basis` properties can all be set together by using the `flex` property.

Для прикладу, `flex: 1 0 10px;` встановить позицію `flex-grow: 1;`, `flex-shrink: 0;`, та `flex-basis: 10px;`.

Параметри властивостей за замовчуванням `flex: 0 1 auto;`.

# --instructions--

Додайте властивість CSS `flex` до `#box-1` та`#box-2`. Вкажіть значення `#box-1` так, що його `flex-grow` складає `2`, його `flex-shrink` це `2`, і його `flex-basis` це`150px`. Вкажіть значення `#box-2` так, що його `flex-grow` становить `1`, його `flex-shrink` це `1`, та його `flex-basis` це `150px`.

Ці значення приведуть до того, що `#box-1` збільшиться, щоб заповнити додатковий простір з подвійною швидкістю коду `#box-2`, коли контейнер буде більше ніж 300px і зменшиться з подвійною швидкістю коду `#box-2`, коли контейнер буде менше ніж 300px. 300px - це сукупний розмір `flex-basis` значення двох комірок.

# --hints--

Елемент `#box-1` повинен мати властивість `flex` зі значенням `2 2 150px`.

```js
const boxOne = document.querySelector('#box-1');
const flexGrow = window.getComputedStyle(boxOne)['flex-grow'];
const flexShrink = window.getComputedStyle(boxOne)['flex-shrink'];
const flexBasis = window.getComputedStyle(boxOne)['flex-basis'];

assert.equal(flexGrow, '2');
assert.equal(flexShrink, '2');
assert.equal(flexBasis, '150px');
```

Елемент `#box-2` повинен мати властивість `flex` зі значенням `1 1 150px`.

```js
const boxTwo = document.querySelector('#box-2');
const flexGrow = window.getComputedStyle(boxTwo)['flex-grow'];
const flexShrink = window.getComputedStyle(boxTwo)['flex-shrink'];
const flexBasis = window.getComputedStyle(boxTwo)['flex-basis'];

assert.equal(flexGrow, '1');
assert.equal(flexShrink, '1');
assert.equal(flexBasis, '150px');
```

Ваш код має використовувати властивість `flex` для `#box-1` та `#box-2`.

```js
assert.lengthOf(code.match(/flex:\s*?\d\s+?\d\s+?150px;/g), 2);
```

# --seed--

## --seed-contents--

```html
<style>
  #box-container {
    display: flex;
    height: 500px;
  }
  #box-1 {
    background-color: dodgerblue;

    height: 200px;
  }

  #box-2 {
    background-color: orangered;

    height: 200px;
  }
</style>

<div id="box-container">
  <div id="box-1"></div>
  <div id="box-2"></div>
</div>
```

# --solutions--

```html
<style>
  #box-container {
    display: flex;
    height: 500px;
  }
  #box-1 {
    background-color: dodgerblue;
    flex: 2 2 150px;
    height: 200px;
  }

  #box-2 {
    background-color: orangered;
    flex: 1 1 150px;
    height: 200px;
  }
</style>

<div id="box-container">
  <div id="box-1"></div>
  <div id="box-2"></div>
</div>
```
