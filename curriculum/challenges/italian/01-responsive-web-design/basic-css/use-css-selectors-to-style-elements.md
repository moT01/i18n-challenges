---
id: bad87fee1348bd9aedf08805
title: Usare i selettori CSS per stilizzare gli elementi
challengeType: 0
videoUrl: 'https://scrimba.com/c/cJKMBT2'
forumTopicId: 18349
dashedName: use-css-selectors-to-style-elements
---

# --description--

With CSS, there are hundreds of CSS properties that you can use to change the way an element looks on your page.

Quando hai inserito `<h2 style="color: red;">CatPhotoApp</h2>`, hai definito quel singolo elemento `h2` con CSS (Cascading Style Sheets, cioè Fogli di Stile a Cascata) in linea.

Questo è un modo per specificare lo stile di un elemento, ma c'è un modo migliore per applicare CSS.

Nella parte superiore del codice, crea un blocco `style` come questo:

```html
<style>
</style>
```

All'interno di quel blocco di stile, puoi creare un <dfn>selettore CSS</dfn> per tutti gli elementi `h2`. Ad esempio, se desideri che tutti gli elementi `h2` siano rossi, dovresti aggiungere una regola di stile simile a questa:

```html
<style>
  h2 {
    color: red;
  }
</style>
```

Nota che è importante avere sia le parentesi graffe di apertura che quelle di chiusura (`{` e `}`) attorno alle regole di stile di ogni elemento. Devi anche assicurarti che la definizione di stile del tuo elemento si trovi tra i tag di stile di apertura e chiusura. Infine, assicurati di aggiungere un punto e virgola alla fine di ciascuna delle regole di stile del tuo elemento.

# --instructions--

Elimina l'attributo di stile dell'elemento `h2` e crea invece un blocco `style`. Aggiungi il CSS necessario per trasformare tutti gli elementi `h2` in blu.

# --hints--

L'attributo `style` dovrebbe essere rimosso dal tuo elemento `h2`.

```js
assert.notExists(document.querySelector('h2').getAttribute('style'));
```

Dovresti creare un elemento `style`.

```js
assert.exists(document.querySelector('style:not(.fcc-hide-header)'));
assert.isAtLeast(document.querySelectorAll('style:not(.fcc-hide-header)').length, 1);
```

Il tuo elemento `h2` dovrebbe essere blu.

```js
const h2Element = document.querySelector('h2');
const color = window.getComputedStyle(h2Element)['color']; 
assert.strictEqual(color, 'rgb(0, 0, 255)');
```

La dichiarazione `h2` del foglio di stile dovrebbe essere valida, con un punto e virgola e una parentesi graffa di chiusura.

```js
assert.match(__helpers.removeCssComments(code), /h2\s*\{\s*color\s*:.*;\s*\}/g);
```

Tutti i tuoi elementi `style` dovrebbero essere validi e avere dei tag di chiusura.

```js
assert.match(__helpers.removeHtmlComments(code), /<\/style>/g);

const closingElementLength = __helpers.removeHtmlComments(code).match(/<\/style>/g).length;
const openingElementsLength = __helpers.removeHtmlComments(code).match(/<style((\s)*((type|media|scoped|title|disabled)="[^"]*")?(\s)*)*>/g).length;
assert.strictEqual(closingElementLength, openingElementsLength);
```

# --seed--

## --seed-contents--

```html
<h2 style="color: red;">CatPhotoApp</h2>
<main>
  <p>Click here to view more <a href="#">cat photos</a>.</p>

  <a href="#"><img src="https://cdn.freecodecamp.org/curriculum/cat-photo-app/relaxing-cat.jpg" alt="A cute orange cat lying on its back."></a>

  <div>
    <p>Things cats love:</p>
    <ul>
      <li>catnip</li>
      <li>laser pointers</li>
      <li>lasagna</li>
    </ul>
    <p>Top 3 things cats hate:</p>
    <ol>
      <li>flea treatment</li>
      <li>thunder</li>
      <li>other cats</li>
    </ol>
  </div>

  <form action="https://freecatphotoapp.com/submit-cat-photo">
    <label><input type="radio" name="indoor-outdoor" checked> Indoor</label>
    <label><input type="radio" name="indoor-outdoor"> Outdoor</label><br>
    <label><input type="checkbox" name="personality" checked> Loving</label>
    <label><input type="checkbox" name="personality"> Lazy</label>
    <label><input type="checkbox" name="personality"> Energetic</label><br>
    <input type="text" placeholder="cat photo URL" required>
    <button type="submit">Submit</button>
  </form>
</main>
```

# --solutions--

```html
<style>
  h2 {
    color: blue;
  }
</style>
<h2>CatPhotoApp</h2>
<main>
  <p>Click here to view more <a href="#">cat photos</a>.</p>

  <a href="#"><img src="https://cdn.freecodecamp.org/curriculum/cat-photo-app/relaxing-cat.jpg" alt="A cute orange cat lying on its back."></a>

  <div>
    <p>Things cats love:</p>
    <ul>
      <li>catnip</li>
      <li>laser pointers</li>
      <li>lasagna</li>
    </ul>
    <p>Top 3 things cats hate:</p>
    <ol>
      <li>flea treatment</li>
      <li>thunder</li>
      <li>other cats</li>
    </ol>
  </div>

  <form action="https://freecatphotoapp.com/submit-cat-photo">
    <label><input type="radio" name="indoor-outdoor" checked> Indoor</label>
    <label><input type="radio" name="indoor-outdoor"> Outdoor</label><br>
    <label><input type="checkbox" name="personality" checked> Loving</label>
    <label><input type="checkbox" name="personality"> Lazy</label>
    <label><input type="checkbox" name="personality"> Energetic</label><br>
    <input type="text" placeholder="cat photo URL" required>
    <button type="submit">Submit</button>
  </form>
</main>
```
