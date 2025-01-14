---
id: 6617aef05b87c334e7ae8016
title: Вивчіть основи функцій. Урок №5
challengeType: 15
dashedName: learn-function-basics-lesson-e
---

# --description--

Як ви бачили раніше, функції можуть повернути значення, використовуючи ключове слово `return`. Ключове слово `return` використовують, щоб повернути значення з функції. Якщо використано ключове слово `return`, то функція припинить виконуватись та поверне значення, вказане після ключового слова `return`.

```js
function add(a, b) {
  return a + b
}

console.log(add(2, 3)); // Output: 5
```

Але що відбувається, якщо ключове слово `return` використано перед кінцем функції? Щоб відповісти на це запитання, розгляньте приклад:

```js
function add(a, b) {
  if(a > 2){
    return b;
  }

  return a + b;
}

console.log(add(3, 7)); // Output: 7
```

Функція `add` в прикладі вище має умовну інструкцію, яка перевіряє, чи значення `a` більше за `2`. Якщо умова виконана, то функція поверне значення `b` і припинить виконуватись. Якщо умова не виконана, то функція поверне суму `a` та `b`.

# --questions--

## --text--

Як буде виглядати результат виконання даного коду?

```js
function add(a, b = 12) {
  if(b > 11){
    return b * 2;
  } else if(a > 3){
    return b;
  }

  return a + b;
}

console.log(add(3));
```

## --answers--

Вихідними даними буде `24`.

---

Вихідними даними буде `14`.

---

Вихідними даними буде `15`.

---

Вихідними даними буде `12`.

## --video-solution--

1
