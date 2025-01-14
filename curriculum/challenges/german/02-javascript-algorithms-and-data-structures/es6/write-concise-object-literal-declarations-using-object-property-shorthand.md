---
id: 587d7b8a367417b2b2512b4f
title: Prägnante Objektliteraldeklarationen mit der Kurzform für Objekteigenschaften schreiben
challengeType: 1
forumTopicId: 301225
dashedName: write-concise-object-literal-declarations-using-object-property-shorthand
---

# --description--

ES6 adds some nice support for easily defining object literals.

Schau dir den folgenden Code an:

```js
const getMousePosition = (x, y) => ({
  x: x,
  y: y
});
```

`getMousePosition` ist eine einfache Funktion, die ein Objekt mit zwei Eigenschaften zurückgibt. ES6 bietet den syntaktischen Zucker, um die Redundanz zu beseitigen, die das Schreiben von `x: x` mit sich bringt. Du kannst einfach einmal `x` schreiben, und es wird unter der Haube in `x: x` (oder etwas Gleichwertiges) umgewandelt. Hier ist die gleiche Funktion von oben, die umgeschrieben wurde, um die neue Syntax zu verwenden:

```js
const getMousePosition = (x, y) => ({ x, y });
```

# --instructions--

Verwende die Kurzform für Objekteigenschaften mit Objektliteralen, um ein Objekt mit den Eigenschaften `name`, `age` und `gender` zu erstellen und zurückzugeben.

# --hints--

`createPerson("Zodiac Hasbro", 56, "male")` sollte `{name: "Zodiac Hasbro", age: 56, gender: "male"}` zurückgeben.

```js
assert.deepEqual(
  { name: 'Zodiac Hasbro', age: 56, gender: 'male' },
  createPerson('Zodiac Hasbro', 56, 'male')
);
```

Dein Code sollte nicht `key:value` verwenden.

```js
assert(!__helpers.removeJSComments(code).match(/:/g))
```

# --seed--

## --seed-contents--

```js
const createPerson = (name, age, gender) => {
  // Only change code below this line
  return {
    name: name,
    age: age,
    gender: gender
  };
  // Only change code above this line
};
```

# --solutions--

```js
const createPerson = (name, age, gender) => {
  // Only change code below this line
  /*return {
    name: name,
    age: age,
    gender: gender
  };*/
  return {
    name,
    age,
    gender
  };
  // Only change code above this line
};
```
