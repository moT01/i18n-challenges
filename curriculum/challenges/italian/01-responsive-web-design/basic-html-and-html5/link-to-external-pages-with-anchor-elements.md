---
id: bad87fee1348bd9aedf08816
title: Collegare a pagine esterne con elementi di ancoraggio
challengeType: 0
videoUrl: 'https://scrimba.com/p/pVMPUv/c8EkncB'
forumTopicId: 18226
dashedName: link-to-external-pages-with-anchor-elements
---

# --description--

You can use `a` (*anchor*) elements to link to content outside of your web page.

Gli elementi `a` richiedono un indirizzo web di destinazione, inserito in un attributo `href`. Hanno bisogno anche di un testo di ancoraggio. Ecco un esempio:

```html
<a href="https://www.freecodecamp.org">this links to freecodecamp.org</a>
```

A questo punto il tuo browser visualizzerà il testo: `this links to freecodecamp.org` come link cliccabile. E quel link ti porterà all'indirizzo web `https://www.freecodecamp.org`.

# --instructions--

Crea un elemento `a` che si colleghi a `https://www.freecatphotoapp.com` e abbia "cat photos" come testo di ancoraggio.

# --hints--

Il tuo elemento `a` dovrebbe avere il testo di ancoraggio: `cat photos`.

```js
assert.match(document.querySelector('a').textContent,/cat photos/gi);
```

Hai bisogno di un elemento `a` che si colleghi a `https://www.freecatphotoapp.com`

```js
assert.match(document.querySelector('a').getAttribute('href'),/^https?:\/\/(www\.)?freecatphotoapp\.com\/?$/i);
```

Il tuo elemento `a` dovrebbe avere un tag di chiusura.

```js
assert.match(code,/<\/a>/g);
assert.strictEqual(code.match(/<\/a>/g).length,code.match(/<a/g).length);
```

# --seed--

## --seed-contents--

```html
<h2>CatPhotoApp</h2>
<main>



  <img src="https://cdn.freecodecamp.org/curriculum/cat-photo-app/relaxing-cat.jpg" alt="A cute orange cat lying on its back.">

  <p>Kitty ipsum dolor sit amet, shed everywhere shed everywhere stretching attack your ankles chase the red dot, hairball run catnip eat the grass sniff.</p>
  <p>Purr jump eat the grass rip the couch scratched sunbathe, shed everywhere rip the couch sleep in the sink fluffy fur catnip scratched.</p>
</main>
```

# --solutions--

```html
<h2>CatPhotoApp</h2>
<main>

  <img src="https://cdn.freecodecamp.org/curriculum/cat-photo-app/relaxing-cat.jpg" alt="A cute orange cat lying on its back.">

  <a href="https://www.freecatphotoapp.com">cat photos</a>
  <p>Kitty ipsum dolor sit amet, shed everywhere shed everywhere stretching attack your ankles chase the red dot, hairball run catnip eat the grass sniff.</p>
  <p>Purr jump eat the grass rip the couch scratched sunbathe, shed everywhere rip the couch sleep in the sink fluffy fur catnip scratched.</p>
</main>
```
