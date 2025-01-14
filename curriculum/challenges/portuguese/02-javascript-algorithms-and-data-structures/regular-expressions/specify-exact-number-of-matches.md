---
id: 587d7db9367417b2b2512ba7
title: Especificar o número exato de capturas
challengeType: 1
forumTopicId: 301365
dashedName: specify-exact-number-of-matches
---

# --description--

You can specify the lower and upper number of patterns with quantity specifiers using curly brackets. Sometimes you only want a specific number of matches.

Para especificar este número, apenas escreva-o dentro das chaves.

Por exemplo, você pode escrever a regex `/ha{3}h/` para capturar a letra `a` `3` vezes na string `hah`.

```js
let A4 = "haaaah";
let A3 = "haaah";
let A100 = "h" + "a".repeat(100) + "h";
let multipleHA = /ha{3}h/;
multipleHA.test(A4);
multipleHA.test(A3);
multipleHA.test(A100);
```

As três chamadas a `test` acima retornam, na ordem, os valores: `false`, `true` e `false`.

# --instructions--

Modifique a regex `timRegex` para que capture quatro `m`s na string `Timber`.

# --hints--

A regex deve usar chaves.

```js
assert(timRegex.source.match(/{.*?}/).length > 0);
```

A regex não deve encontrar a string `Timber`

```js
timRegex.lastIndex = 0;
assert(!timRegex.test('Timber'));
```

A regex não deve encontrar a string `Timmber`

```js
timRegex.lastIndex = 0;
assert(!timRegex.test('Timmber'));
```

A regex não deve encontrar a string `Timmmber`

```js
timRegex.lastIndex = 0;
assert(!timRegex.test('Timmmber'));
```

A regex deve encontrar a string `Timmmmber`

```js
timRegex.lastIndex = 0;
assert(timRegex.test('Timmmmber'));
```

A regex não deve encontrar a string `Timber` se nela houver 30 `m`s.

```js
timRegex.lastIndex = 0;
assert(!timRegex.test('Ti' + 'm'.repeat(30) + 'ber'));
```

# --seed--

## --seed-contents--

```js
let timStr = "Timmmmber";
let timRegex = /change/; // Change this line
let result = timRegex.test(timStr);
```

# --solutions--

```js
let timStr = "Timmmmber";
let timRegex = /Tim{4}ber/; // Change this line
let result = timRegex.test(timStr);
```
