---
id: 587d8250367417b2b2512c5e
title: Дізнайтесь, як працює стек
challengeType: 1
forumTopicId: 301705
dashedName: learn-how-a-stack-works
---

# --description--

You are probably familiar with stack of books on your table. You have likely used the undo feature of a text editor. You are also probably used to hitting the back button on your phone to go back to the previous view in your app.

Знаєте, що у них спільного? Всі вони зберігають дані так, щоб ви могли повернутися до них.

Верхня книга у стосі — це та, яку поклали туди останньою. Якщо ви заберете цю книгу зі стосу, то побачите наступну — ту, яку поклали передостанньою, і так далі.

А тепер подумаємо: у всіх вищенаведених прикладах використано принцип <dfn>останнім прийшло — першим пішло</dfn>. Ми спробуємо зімітувати його за допомогою коду.

Така схема зберігання даних називається <dfn>стеком</dfn>. Зокрема, нам потрібно буде реалізувати метод `push()`, який переносить об’єкти JavaScript до вершини стеку, та метод `pop()`, який вилучає об’єкт JavaScript, що на цей момент знаходиться на вершині стеку.

# --instructions--

Вам дано стек домашніх завдань, поданих у вигляді масиву: `"BIO12"` розташовано знизу, а `"PSY44"` — зверху.

Змініть даний масив і розгляньте його як `stack`, використовуючи згадані вище методи JavaScript. Вилучіть верхній елемент `"PSY44"` зі стека. Потім додайте `"CS50"` як новий верхній елемент стеку.

# --hints--

`homeworkStack` повинен містити лише 4 елементи.

```js
assert(homeworkStack.length === 4);
```

Останнім елементом в `homeworkStack` має бути `"CS50"`.

```js
assert(homeworkStack[3] === 'CS50');
```

`homeworkStack` не повинен містити елемент `"PSY44"`.

```js
assert(homeworkStack.indexOf('PSY44') === -1);
```

Не змінюйте початкове оголошення `homeworkStack`.

```js
assert(
  __helpers.removeJSComments(code).match(/=/g).length === 1 &&
    /homeworkStack\s*=\s*\["BIO12"\s*,\s*"HIS80"\s*,\s*"MAT122"\s*,\s*"PSY44"\]/.test(
      __helpers.removeJSComments(code)
    )
);
```

# --seed--

## --seed-contents--

```js
var homeworkStack = ["BIO12","HIS80","MAT122","PSY44"];
// Only change code below this line
```

# --solutions--

```js
// solution required
```
