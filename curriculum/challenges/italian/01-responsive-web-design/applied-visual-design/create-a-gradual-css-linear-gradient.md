---
id: 587d78a5367417b2b2512ad6
title: Creare un gradiente lineare con CSS
challengeType: 0
videoUrl: 'https://scrimba.com/c/cg4dpt9'
forumTopicId: 301047
dashedName: create-a-gradual-css-linear-gradient
---

# --description--

Applying a color on HTML elements is not limited to one flat hue. CSS provides the ability to use color transitions, otherwise known as gradients, on elements. This is accessed through the `background` property's `linear-gradient()` function. Here is the general syntax:

```css
background: linear-gradient(gradient_direction, color 1, color 2, color 3, ...);
```

Il primo argomento specifica la direzione da cui inizia la transizione del colore - può essere indicato in gradi, dove `90deg` crea un gradiente orizzontale (da sinistra a destra) e `45deg` crea un gradiente diagonale (dal basso a sinistra all'alto a destra). Gli argomenti seguenti specificano l'ordine dei colori usati nel gradiente.

Esempio:

```css
background: linear-gradient(90deg, red, yellow, rgb(204, 204, 255));
```

# --instructions--

Utilizza un `linear-gradient()` per il `background` dell'elemento `div`, e impostalo per cambiare il colore da `#CCFFFF` a `#FFCCCC` lungo una direzione di 35 gradi.

# --hints--

L'elemento `div` dovrebbe avere un `background` di tipo `linear-gradient` con la direzione e i colori specificati.

```js
const divElement = document.querySelector('div');
const divStyle = window.getComputedStyle(divElement); 
assert.match(divStyle?.background, /linear-gradient\(35deg, rgb\(204, 255, 255\), rgb\(255, 204, 204\)\)/gi);
```

# --seed--

## --seed-contents--

```html
<style>
  div {
    border-radius: 20px;
    width: 70%;
    height: 400px;
    margin: 50px auto;

  }

</style>

<div></div>
```

# --solutions--

```html
<style>
  div {
    border-radius: 20px;
    width: 70%;
    height: 400px;
    margin: 50px auto;
    background: linear-gradient(35deg, #CCFFFF, #FFCCCC);
  }
</style>
<div></div>
```
