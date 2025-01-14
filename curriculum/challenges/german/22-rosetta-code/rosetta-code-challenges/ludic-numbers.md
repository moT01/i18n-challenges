---
id: 5ea281203167d2b0bdefca00
title: Ludische Zahlen
challengeType: 1
forumTopicId: 385282
dashedName: ludic-numbers
---

# --description--

Ludische Zahlen sind mit den Primzahlen verwandt, da sie durch ein Sieb erzeugt werden, ähnlich wie das Sieb des Eratosthenes zur Erzeugung von Primzahlen verwendet wird.

Die erste ludische Zahl ist 1.

Um aufeinanderfolgende ludische Zahlen zu erzeugen, erstellst du eine Reihe von aufsteigenden ganzen Zahlen, beginnend mit 2.

<code style='margin-left: 2em;'><span style='color:blue;font-weight:bold'>2</span> 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 ...</code>

(Schleife)

<ul>
  <li>Nimm das erste Glied der resultierenden Anordnung als die nächste ludische Zahl <span style='color:blue;font-weight:bold'>2</span>.</li>
  <li>Entfernt jedes <strong>2<sup>nd</sup></strong> indizierte Element aus der Anordnung (einschließlich des ersten).</li>
  <code style='margin-left: 2em;'><span style='color:blue;font-weight:bold;'><s>2</s></span> 3 <s>4</s> 5 <s>6</s> 7 <s>8</s> 9 <s>10</s> 11 <s>12</s> 13 <s>14</s> 15 <s>16</s> 17 <s>18</s> 19 <s>20</s> 21 <s>22</s> 23 <s>24</s> 25 <s>26</s> ...</code>
</ul>

<ul>
  <li>(Einige Schleifen abrollen...)</li>
  <li>Nimm das erste Glied der sich ergebenden Matrix als die nächste ludische Zahl <span style='color:blue;font-weight:bold'>3</span>.</li>
  <li>Entfernt jedes <strong>3<sup>rd</sup></strong> indizierte Element aus der Anordnung (einschließlich des ersten).</li>
  <code style='margin-left: 2em;'><span style='color:blue;font-weight:bold'><s>3</s></span> 5 7 <s>9</s> 11 13 <s>15</s> 17 19 <s>21</s> 23 25 <s>27</s> 29 31 <s>33</s> 35 37 <s>39</s> 41 43 <s>45</s> 47 49 <s>51</s> ...</code>
</ul>

<ul>
  <li>Nimm das erste Glied der sich ergebenden Matrix als die nächste ludische Zahl <span style='color:blue;font-weight:bold'>5</span>.</li>
  <li>Entfernt jedes <strong>5<sup>th</sup></strong> indizierte Element aus der Anordnung (einschließlich des ersten).</li>
  <code style='margin-left: 2em;'><span style='color:blue;font-weight:bold'><s>5</s></span> 7 11 13 17 <s>19</s> 23 25 29 31 <s>35</s> 37 41 43 47 <s>49</s> 53 55 59 61 <s>65</s> 67 71 73 77 ...</code>
</ul>

<ul>
  <li>Nimm das erste Glied der sich ergebenden Matrix als die nächste ludische Zahl <span style='color:blue;font-weight:bold'>7</span>.</li>
  <li>Entfernt jedes <strong>7<sup>th</sup></strong> indizierte Element aus der Anordnung (einschließlich des ersten).</li>
  <code style='margin-left: 2em;'><span style='color:blue;font-weight:bold'><s>7</s></span> 11 13 17 23 25 29 <s>31</s> 37 41 43 47 53 55 <s>59</s> 61 67 71 73 77 83 <s>85</s> 89 91 97 ...</code>
</ul>

<ul>
  <li><big><b> ... </b></big></li>
  <li>Nimm das erste Mitglied der aktuellen Anordnung als nächste ludische Zahl <span style='color:blue;font-weight:bold'>L</span>.</li>
  <li>Entfernt jedes <strong>L<sup>th</sup></strong> indizierte Element aus der Anordnung (einschließlich des ersten).</li>
  <li><big><b> ... </b></big></li>
</ul>

# --instructions--

Schreibe eine Funktion, die alle ludischen Zahlen zurückgibt, die kleiner oder gleich der angegebenen Zahl sind.

# --hints--

`ludic` sollte eine Funktion sein.

```js
assert(typeof ludic === 'function', '<code>ludic</code> should be a function.');
```

`ludic(2)` sollte ein Array zurückgeben.

```js
assert(Array.isArray(ludic(2)));
```

`ludic(2)` sollte `[1, 2]` zurückgeben.

```js
assert.deepEqual(ludic(2), [1, 2]);
```

`ludic(3)` sollte `[1, 2, 3]` zurückgeben.

```js
assert.deepEqual(ludic(3), [1, 2, 3]);
```

`ludic(5)` sollte `[1, 2, 3, 5]` zurückgeben.

```js
assert.deepEqual(ludic(5), [1, 2, 3, 5]);
```

`ludic(20)` sollte `[1, 2, 3, 5, 7, 11, 13, 17]` zurückgeben.

```js
assert.deepEqual(ludic(20), [1, 2, 3, 5, 7, 11, 13, 17]);
```

`ludic(26)` sollte `[1, 2, 3, 5, 7, 11, 13, 17, 23, 25]` zurückgeben.

```js
assert.deepEqual(ludic(26), [1, 2, 3, 5, 7, 11, 13, 17, 23, 25]);
```

# --seed--

## --seed-contents--

```js
function ludic(n) {

}
```

# --solutions--

```js
function ludic(n) {
  const makeArr = (s, e) => new Array(e + 1 - s).fill(s).map((e, i) => e + i);

  const filterAtInc = (arr, n) => arr.filter((e, i) => (i + 1) % n);

  const makeLudic = (arr, result) => {
    const iter = arr.shift();
    result.push(iter);
    return arr.length ? makeLudic(filterAtInc(arr, iter), result) : result;
  };

  const ludicResult = makeLudic(makeArr(2, n), [1]);

  return ludicResult;
}
```
