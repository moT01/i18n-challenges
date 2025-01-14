---
id: 587d78b1367417b2b2512b09
title: Rendere un'immagine responsiva
challengeType: 0
forumTopicId: 301140
dashedName: make-an-image-responsive
---

# --description--

Making images responsive with CSS is actually very simple. You just need to add these properties to an image:

```css
img {
  max-width: 100%;
  height: auto;
}
```

La `max-width` di `100%` assicurerà che l'immagine non sia mai più larga del contenitore in cui si trova, e l'`height` impostata a `auto` farà in modo che l'immagine mantenga le sue proporzioni originali.

# --instructions--

Aggiungi le regole di stile alla classe `responsive-img` per renderla responsiva. Non dovrebbe mai essere più grande del suo contenitore (in questo caso la finestra di anteprima) e dovrebbe mantenere il suo rapporto di aspetto originale. Dopo aver aggiunto il codice, ridimensiona l'anteprima per vedere come si comportano le immagini.

# --hints--

La tua classe `responsive-img` dovrebbe avere una `max-width` impostata a `100%`.

```js
assert.strictEqual(getComputedStyle(document.querySelector('.responsive-img')).maxWidth, '100%');
```

La tua classe `responsive-img` dovrebbe avere una `height` impostata su `auto`.

```js
assert.match(code, /height:\s*?auto;/g);
```

# --seed--

## --seed-contents--

```html
<style>
.responsive-img {


}

img {
  width: 600px;
}
</style>

<img
  class="responsive-img"
  src="https://cdn.freecodecamp.org/curriculum/responsive-web-design-principles/FCCStickerPack.jpg"
  alt="freeCodeCamp stickers set"
/>
<img
  src="https://cdn.freecodecamp.org/curriculum/responsive-web-design-principles/FCCStickerPack.jpg"
  alt="freeCodeCamp stickers set"
/>
```

# --solutions--

```html
<style>
  .responsive-img {
    max-width: 100%;
    height: auto;
  }

  img {
    width: 600px;
  }
</style>

<img
  class="responsive-img"
  src="https://cdn.freecodecamp.org/curriculum/responsive-web-design-principles/FCCStickerPack.jpg"
  alt="freeCodeCamp stickers set"
/>
<img
  src="https://cdn.freecodecamp.org/curriculum/responsive-web-design-principles/FCCStickerPack.jpg"
  alt="freeCodeCamp stickers set"
/>
```
