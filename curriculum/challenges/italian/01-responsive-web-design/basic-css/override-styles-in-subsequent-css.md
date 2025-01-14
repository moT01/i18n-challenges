---
id: bad87fee1348bd9aedf04756
title: Sovrascrivere gli stili nei CSS successivi
challengeType: 0
videoUrl: 'https://scrimba.com/c/cGJDQug'
forumTopicId: 18253
dashedName: override-styles-in-subsequent-css
---

# --description--

Our `pink-text` class overrode our `body` element's CSS declaration!

Abbiamo appena dimostrato che le nostre classi sovrascriveranno il CSS dell'elemento `body`. Quindi la prossima domanda logica è: che cosa possiamo fare per sovrascrivere la nostra classe `pink-text`?

# --instructions--

Crea una classe CSS aggiuntiva chiamata `blue-text` che dia ad un elemento il colore blu. Assicurati che sia sotto la tua dichiarazione di classe `pink-text`.

Applica la classe `blue-text` al tuo elemento `h1` in aggiunta alla tua classe `pink-text`, e vediamo quale vince.

Applying multiple class attributes to an HTML element is done with a space between them like this:

```html
class="class1 class2"
```

**Nota:** Non importa in quale ordine sono elencate le classi nell'elemento HTML.

Quello che veramente conta è l'ordine delle dichiarazioni di `class` nella sezione `<style>`. La seconda dichiarazione avrà sempre la precedenza sulla prima. Poiché `.blue-text` viene dichiarato per secondo, esso sovrascrive gli attributi di `.pink-text`.

# --hints--

Il tuo elemento `h1` dovrebbe avere la classe `pink-text`.

```js
assert.isTrue(document.querySelector('h1').classList.contains('pink-text'));
```

L'elemento `h1` dovrebbe avere la classe `blue-text`.

```js
assert.isTrue(document.querySelector('h1').classList.contains('blue-text'));
```

Entrambe le classi `blue-text` e `pink-text` dovrebbero essere associate al tuo elemento `h1`.

```js
assert.isTrue(document.querySelector('.pink-text').classList.contains('blue-text'));
```

Il tuo elemento `h1` dovrebbe essere blu.

```js
const h1Element = document.querySelector('h1');
const color = window.getComputedStyle(h1Element)['color']; 
assert.strictEqual(color, 'rgb(0, 0, 255)');
```

# --seed--

## --seed-contents--

```html
<style>
  body {
    background-color: black;
    font-family: monospace;
    color: green;
  }
  .pink-text {
    color: pink;
  }
</style>
<h1 class="pink-text">Hello World!</h1>
```

# --solutions--

```html
<style>
  body {
    background-color: black;
    font-family: monospace;
    color: green;
  }
  .pink-text {
    color: pink;
  }

  .blue-text {
    color: blue;
  }  
</style>
<h1 class="pink-text blue-text">Hello World!</h1>
```
