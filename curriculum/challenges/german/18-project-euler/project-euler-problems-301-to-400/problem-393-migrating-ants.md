---
id: 5900f4f61000cf542c510008
title: 'Problem 393: Wandernde Ameisen'
challengeType: 1
forumTopicId: 302058
dashedName: problem-393-migrating-ants
---

# --description--

Ein $n × n$-Gitter aus Quadraten enthält $n^2$ Ameisen, eine Ameise pro Quadrat.

Alle Ameisen entscheiden sich gleichzeitig für ein benachbartes Feld (in der Regel 4 Möglichkeiten, außer für Ameisen am Rand des Gitters oder in den Ecken).

Wir definieren $f(n)$ als die Anzahl der Möglichkeiten, wie dies geschehen kann, ohne dass Ameisen auf demselben Feld enden und ohne dass zwei Ameisen dieselbe Kante zwischen zwei Feldern überqueren.

Es ist gegeben, dass $f(4) = 88$ ist.

Finde $f(10)$.

# --hints--

`migratingAnts()` sollte `112398351350823100` zurückgeben.

```js
assert.strictEqual(migratingAnts(), 112398351350823100);
```

# --seed--

## --seed-contents--

```js
function migratingAnts() {

  return true;
}

migratingAnts();
```

# --solutions--

```js
// solution required
```
