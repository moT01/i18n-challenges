---
id: 5e94a54cc7b022105bf0fd2c
title: Frecuencia de palabras
challengeType: 1
forumTopicId: 393913
dashedName: word-frequency
---

# --description--

Given a text string and an integer n, return the n most common words in the file (and the number of their occurrences) in decreasing frequency.

# --instructions--

Write a function to count the occurrences of each word and return the n most commons words along with the number of their occurrences in decreasing frequency.

La función debe devolver un arreglo 2D con cada uno de los elementos de la siguiente forma: `[word, freq]`. `word` debe ser la versión en minúscula de la palabra y `freq` el número que indica el conteo.

La función debe devolver un arreglo vacío, si no se proporciona ninguna cadena.

La función debe ser insensible a mayúsculas, por ejemplo, las cadenas "Hola" y "hola" deben ser tratadas de la misma manera.

Puede tratar palabras que tienen caracteres especiales como guiones bajos, guiones, apóstrofes, comas, etc., como palabras distintas.

Por ejemplo, dada la cadena "Hello hello goodbye", tu función debe devolver `[['hello', 2], ['goodbye', 1]]`.

# --hints--

`wordFrequency` debe ser una función.

```js
assert.isFunction(wordFrequency);
```

`wordFrequency` debe devolver un arreglo.

```js
assert.isArray(wordFrequency('test'));
```

`wordFrequency("Hello hello world", 2)` debe retornar `[['hello', 2], ['world', 1]]`

```js
const example_1 = 'Hello hello world';
const example_1_solution = [['hello', 2], ['world', 1]];

assert.deepEqual(wordFrequency(example_1, 2), example_1_solution);
```

`wordFrequency("The quick brown fox jumped over the lazy dog", 1)` debe retornar `[['the', 2]]`

```js
const example_2 = 'The quick brown fox jumped over the lazy dog';
const example_2_solution = [['the', 2]];

assert.deepEqual(wordFrequency(example_2, 1), example_2_solution);
```

`wordFrequency("Opensource opensource open-source open source", 1)` debería devolver `[['opensource', 2]]`

```js
const example_3 = 'Opensource opensource open-source open source';
const example_3_solution = [['opensource', 2]];

assert.deepEqual(wordFrequency(example_3, 1), example_3_solution);
```

`wordFrequency("Apple App apply aPP aPPlE", 3)` deberá devolver `[['app', 2], ['apple', 2], ['apply', 1]]` o `[['apple', 2], ['app', 2], ['apply', 1]]`

```js
const example_4 = 'Apple App apply aPP aPPlE';
const example_4_solution = [["app", 2],["apple", 2],["apply", 1]];

const arr = wordFrequency(example_4, 3);
assert.includeDeepMembers(arr, example_4_solution);
```

`wordFrequency("c d a d c a b d d c", 4)` deberá retornar `[['d', 4], ['c', 3], ['a', 2], ['b', 1]]`

```js
const example_5 = 'c d a d c a b d d c';
const example_5_solution = [['d', 4], ['c', 3], ['a', 2], ['b', 1]];

assert.deepEqual(wordFrequency(example_5, 4), example_5_solution);
```

`wordFrequency("", 5)` deberá retornar `[]`

```js
const example_6 = '';
const example_6_solution = [];

assert.deepEqual(wordFrequency(example_6, 5), example_6_solution);
```

# --seed--

## --seed-contents--

```js
function wordFrequency(txt, n) {

}
```

# --solutions--

```js
function wordFrequency(txt, n) {
  var words = txt.split(/\s+/);
  var wordCount = {};
  words.forEach(word => {
    if (word == '') {
      return;
    }
    const lowerWord = word.toLowerCase();
    wordCount[lowerWord] =
      lowerWord in wordCount ? wordCount[lowerWord] + 1 : 1;
  });

  var wordsArray = [];
  for (let [word, count] of Object.entries(wordCount)) {
    wordsArray.push([word, count]);
  }

  wordsArray.sort((a, b) => {
    if (a[1] !== b[1]) {
      return b[1] - a[1];
    } else if (a[0] !== b[0]) {
      return a[0] < b[0] ? -1 : 1;
    }
    return 0;
  });
  return wordsArray.slice(0, n);
}
```
