---
id: 62a3bb9aeefe4b3fc43c6d7b
title: Paso 17
challengeType: 0
dashedName: step-17
---

# --description--

`button1` es una variable que no será reasignada. Si no vas a asignarle un nuevo valor a una variable, es una buena práctica usar la palabra reservada `const` para declararla, en lugar de la palabra reservada `let`. Esto le dirá a JavaScript que arroje un error si accidentalmente la reasignas.

Cambia tu variable `button1` para que sea declarada con la palabra reservada `const`.

# --hints--

Tu variable `button1` debe ser declarada usando `const`.

```js
assert.match(code, /const\s+button1/);
```

Tu variable `button1` debe tener aún el valor de tu elemento `#button1`.

```js
assert.deepEqual(button1, document.querySelector("#button1"));
```

# --seed--

## --seed-contents--

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <link rel="stylesheet" href="./styles.css">
    <title>RPG - Dragon Repeller</title>
  </head>
  <body>
    <div id="game">
      <div id="stats">
        <span class="stat">XP: <strong><span id="xpText">0</span></strong></span>
        <span class="stat">Health: <strong><span id="healthText">100</span></strong></span>
        <span class="stat">Gold: <strong><span id="goldText">50</span></strong></span>
      </div>
      <div id="controls">
        <button id="button1">Go to store</button>
        <button id="button2">Go to cave</button>
        <button id="button3">Fight dragon</button>
      </div>
      <div id="monsterStats"></div>
      <div id="text"></div>
    </div>
    <script src="./script.js"></script>
  </body>
</html>
```

```js
let xp = 0;
let health = 100;
let gold = 50;
let currentWeaponIndex = 0;
let fighting;
let monsterHealth;
let inventory = ["stick"];

--fcc-editable-region--
let button1 = document.querySelector("#button1");
--fcc-editable-region--
```
