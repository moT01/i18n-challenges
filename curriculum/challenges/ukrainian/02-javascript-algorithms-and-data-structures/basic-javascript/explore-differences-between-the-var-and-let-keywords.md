---
id: 587d7b87367417b2b2512b3f
title: Відмінності між ключовими словами var та let
challengeType: 1
forumTopicId: 301202
dashedName: explore-differences-between-the-var-and-let-keywords
---

# --description--

One of the biggest problems with declaring variables with the `var` keyword is that you can easily overwrite variable declarations:

```js
var camper = "James";
var camper = "David";
console.log(camper);
```

У вищезазначеному коді змінна `camper` спочатку була оголошена як `James`, а потім була переписана на `David`. Тому консоль показує рядок `David`.

У невеликій програмі вам, можливо, і не загрожуватиме така проблема. Але з поступовим збільшенням кодової бази, ви можете випадково переписати якусь змінну. Оскільки така дія не вважається помилковою, то й знайти та виправити такі похибки буде складніше.

Ключове слово `let` було введено в ES6 (важливе оновлення до JavaScript), щоб потенційно розв’язати цю проблему з ключовим словом `var`. Про інші функції ES6 ви дізнаєтеся у наступних завданнях.

Якщо ви заміните `var` на `let` у коді вище, це призведе до помилки:

```js
let camper = "James";
let camper = "David";
```

Помилку можна побачити у вашій консолі браузера.

Отже, на відміну від `var`, при використанні `let` змінну з такою самою назвою можливо оголосити лише один раз.

# --instructions--

Оновіть код так, щоб використовувалося лише ключове слово `let`.

# --hints--

`var` повинне бути відсутнім у коді.

```js
assert.notMatch(code, /var/g);
```

`catName` має бути рядком `Oliver`.

```js
assert.equal(catName, 'Oliver');
```

`catSound` має бути рядком `Meow!`

```js
assert.equal(catSound, 'Meow!');
```

# --seed--

## --seed-contents--

```js
var catName = "Oliver";
var catSound = "Meow!";
```

# --solutions--

```js
let catName = "Oliver";
let catSound = "Meow!";
```
