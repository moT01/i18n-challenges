---
id: 5900f3c71000cf542c50feda
title: 'Problem 91: Rechtwinklige Dreiecke mit ganzzahligen Koordinaten'
challengeType: 1
forumTopicId: 302208
dashedName: problem-91-right-triangles-with-integer-coordinates
---

# --description--

Die Punkte ${P}(x_1, y_1)$ und ${Q}(x_2, y_2)$ werden an ganzzahligen Koordinaten aufgetragen und mit dem Ursprung ${O}(0, 0)$ verbunden, um ${\Delta}OPQ$ zu bilden.

<img alt="ein Diagramm, das die Punkte P (x_1, y_1) und Q(x_2, y_2) mit ganzzahligen Koordinaten aufzeichnet, die mit dem Ursprung O (0, 0) verbunden sind" src="https://cdn-media-1.freecodecamp.org/project-euler/right-triangles-integer-coordinates-1.png" style="background-color: white; padding: 10px; display: block; margin-right: auto; margin-left: auto; margin-bottom: 1.2rem;" />

Es gibt genau vierzehn Dreiecke, die einen rechten Winkel enthalten, der gebildet werden kann, wenn jede Koordinate zwischen 0 und einschließlich 2 liegt; das heißt, $0 ≤ x_1, y_1, x_2, y_2 ≤ 2$.

<img alt="ein Diagramm mit den 14 Dreiecken, die einen rechten Winkel enthalten und gebildet werden können, wenn jede Koordinate zwischen 0 und 2 liegt" src="https://cdn-media-1.freecodecamp.org/project-euler/right-triangles-integer-coordinates-2.png" style="background-color: white; padding: 10px; display: block; margin-right: auto; margin-left: auto; margin-bottom: 1.2rem;" />

Unter der Voraussetzung $0 ≤ x_1, y_1, x_2, y_2 ≤ limit$, wie viele rechtwinklige Dreiecke können gebildet werden?

# --hints--

`rightTrianglesIntCoords(2)` sollte eine Zahl zurückgeben.

```js
assert(typeof rightTrianglesIntCoords(2) === 'number');
```

`rightTrianglesIntCoords(2)` sollte `14` zurückgeben.

```js
assert.strictEqual(rightTrianglesIntCoords(2), 14);
```

`rightTrianglesIntCoords(10)` sollte `448` zurückgeben.

```js
assert.strictEqual(rightTrianglesIntCoords(10), 448);
```

`rightTrianglesIntCoords(25)` sollte `3207` zurückgeben.

```js
assert.strictEqual(rightTrianglesIntCoords(25), 3207);
```

`rightTrianglesIntCoords(50)` sollte `14234` zurückgeben.

```js
assert.strictEqual(rightTrianglesIntCoords(50), 14234);
```

# --seed--

## --seed-contents--

```js
function rightTrianglesIntCoords(limit) {

  return true;
}

rightTrianglesIntCoords(2);
```

# --solutions--

```js
function rightTrianglesIntCoords(limit) {
  function isRightTriangle(points) {
    for (let i = 0; i < points.length; i++) {
      const pointA = points[i];
      const pointB = points[(i + 1) % 3];
      const pointC = points[(i + 2) % 3];
      const vectorAB = [pointB[0] - pointA[0], pointB[1] - pointA[1]];
      const vectorAC = [pointC[0] - pointA[0], pointC[1] - pointA[1]];

      if (isRightAngleBetween(vectorAB, vectorAC)) {
        return true;
      }
    }
    return false;
  }

  function isRightAngleBetween(vector1, vector2) {
    return vector1[0] * vector2[0] + vector1[1] * vector2[1] === 0;
  }

  function getSetKey(points) {
    return (
      '0.0,' +
      points
        .sort((a, b) => a[0] - b[0])
        .map(point => point.join('.'))
        .join(',')
    );
  }

  const pointO = [0, 0];
  const rightTriangles = new Set();
  for (let x1 = 1; x1 <= limit; x1++) {
    for (let y1 = 0; y1 <= limit; y1++) {
      const pointP = [x1, y1];
      for (let x2 = 0; x2 <= limit; x2++) {
        for (let y2 = 1; y2 <= limit; y2++) {
          const pointQ = [x2, y2];
          if (pointP[0] === pointQ[0] && pointP[1] === pointQ[1]) {
            continue;
          }
          if (isRightTriangle([pointO, pointP, pointQ])) {
            rightTriangles.add(getSetKey([pointP, pointQ]));
          }
        }
      }
    }
  }
  return rightTriangles.size;
}
```
