---
id: 5a24c314108439a4d4036161
title: Дізнайтесь про самозакриваючі теги JSX
challengeType: 6
forumTopicId: 301396
dashedName: learn-about-self-closing-jsx-tags
---

# --description--

So far, you’ve seen how JSX differs from HTML in a key way with the use of `className` vs. `class` for defining HTML classes.

Іншою важливою відмінністю JSX від HTML є самозакриваючі теги.

У HTML майже всі елементи мають початковий та кінцевий тег: `<div></div>`; кінцевий тег завжди має скісну риску перед назвою тегу, який ви закриваєте. However, there are special instances in HTML called <dfn>void elements</dfn>, or elements that don’t require both an opening and closing tag before another element can start.

Наприклад, тег розриву рядка можна записати як `<br>` або `<br />`, але не можна записати як `<br></br>`, оскільки він не містить жодного вмісту.

Правила в JSX трішки відрізняються. Будь-який елемент JSX можна написати з самозакриваючим тегом та кожен елемент має бути закритим. Наприклад, тег розриву рядка завжди потрібно писати як `<br />`, щоб він був дійсним JSX, який може бути транспільованим. А ось `<div>` можна написати як `<div />` або `<div></div>`. Різниця в тому, що у першій версії синтаксису неможливо помістити щось всередині `<div />`. У наступних завданнях ви побачите, що цей синтаксис корисний при відтворенні компонентів React.

# --instructions--

Виправте помилки в редакторі коду, щоб він був дійсним JSX і успішно транспільованим. Переконайтеся, що не змінили вміст: вам потрібно лише закрити теги там, де потрібно.

# --hints--

Константа `JSX` має повернути елемент `div`.

```js
assert.strictEqual(JSX.type, 'div');
```

`div` має містити тег `br`.

```js
assert(Enzyme.shallow(JSX).find('br').length === 1);
```

`div` має містити тег `hr`.

```js
assert(Enzyme.shallow(JSX).find('hr').length === 1);
```

# --seed--

## --after-user-code--

```jsx
ReactDOM.render(JSX, document.getElementById('root'))
```

## --seed-contents--

```jsx
const JSX = (
  <div>
    <h2>Welcome to React!</h2> <br >
    <p>Be sure to close all tags!</p>
    <hr >
  </div>
);
```

# --solutions--

```jsx
const JSX = (
<div>
  <h2>Welcome to React!</h2> <br />
  <p>Be sure to close all tags!</p>
  <hr />
</div>
);
```
