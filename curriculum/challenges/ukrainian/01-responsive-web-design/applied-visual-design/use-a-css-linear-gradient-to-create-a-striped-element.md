---
id: 587d78a5367417b2b2512ad7
title: Використання лінійного градієнта CSS для створення смугастого елемента
challengeType: 0
videoUrl: 'https://scrimba.com/c/c6bmQh2'
forumTopicId: 301072
dashedName: use-a-css-linear-gradient-to-create-a-striped-element
---

# --description--

The `repeating-linear-gradient()` function is very similar to `linear-gradient()` with the major difference that it repeats the specified gradient pattern. `repeating-linear-gradient()` accepts a variety of values, but for simplicity, you'll work with an angle value and color stop values in this challenge.

Значення кута - це напрямок градієнта. Стоп-кольори або кольорові обмежувачі - схожі значення ширини, що позначають місце, де відбувається перехід, і вони подаються у відсотках або у кількості пікселів.

У прикладі, який подано в редакторі коду, градієнт починається з кольору `yellow` (жовтий) на рівні 0 пікселів, який зливається з другим кольором `blue` (синій) на рівні 40 пікселів від початку. Оскільки наступний стоп-колір також знаходиться на рівні 40 пікселів, градієнт негайно змінюється на третій колір `green` (зелений), який сам по собі зливається з четвертим значенням кольору `red` (червоний), оскільки він розташований на рівні 80 пікселів від початку градієнта.

Для цього прикладу слід уявляти собі стоп-кольори як пари, де кожні два кольори зливаються.

```css
0px [yellow -- blend -- blue] 40px [green -- blend -- red] 80px
```

Якщо обидва значення стоп-кольорів однакові, злиття непомітне, оскільки воно відбувається між тим самим кольором, після чого здійснюється різкий перехід до наступного кольору, тому в результаті виходять смуги.

# --instructions--

Смуги можна зробити змінивши `repeating-linear-gradient()` таким чином, щоб використати градієнтний кут `45deg`, потім налаштувати перші два стоп-кольори на `yellow` (жовтий), а вкінці два інші стоп-кольори - на `black` (чорний).

# --hints--

Кут `repeating-linear-gradient()` повинен складати 45 градусів.

```js
assert.match(code,/background:\s*?repeating-linear-gradient\(\s*?45deg/gi);
```

Кут `repeating-linear-gradient()` повинен складати не більше 90 градусів

```js
assert.notMatch(code, /90deg/gi);
```

Стоп-колір на рівні 0 пікселів повинен бути `yellow` (жовтий).

```js
assert.match(code, /yellow\s+?0(px)?/gi);
```

Перший стоп-колір на 40 пікселях повинен бути `yellow`.

```js
assert.match(code, /yellow\s+?40px/gi);
```

Другий стоп-колір на рівні 40 пікселів повинен бути `black` (чорний).

```js
assert.match(code, /yellow\s+?40px,\s*?black\s+?40px/gi);
```

Останній стоп-колір на рівні 80 пікселів повинен бути `black` (чорний).

```js
assert.match(code, /black\s+?80px/gi);
```

# --seed--

## --seed-contents--

```html
<style>

  div{
    border-radius: 20px;
    width: 70%;
    height: 400px;
    margin:  50 auto;
    background: repeating-linear-gradient(
      90deg,
      yellow 0px,
      blue 40px,
      green 40px,
      red 80px
    );
  }

</style>

<div></div>
```

# --solutions--

```html
<style>
  div{
    border-radius: 20px;
    width: 70%;
    height: 400px;
    margin:  50 auto;
    background: repeating-linear-gradient(
      45deg,
      yellow 0px,
      yellow 40px,
      black 40px,
      black 80px
    );
  }
</style>
<div></div>
```
