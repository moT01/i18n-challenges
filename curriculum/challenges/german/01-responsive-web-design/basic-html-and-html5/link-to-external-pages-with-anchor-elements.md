---
id: bad87fee1348bd9aedf08816
title: Link zu externen Seiten mit Anker-Elementen
challengeType: 0
videoUrl: 'https://scrimba.com/p/pVMPUv/c8EkncB'
forumTopicId: 18226
dashedName: link-to-external-pages-with-anchor-elements
---

# --description--

You can use `a` (*anchor*) elements to link to content outside of your web page.

`a`-Elemente benötigen eine Ziel-Webadresse, ein sogenanntes `href`-Attribut. Sie benötigen auch einen Anker-Text. Hier ein Beispiel:

```html
<a href="https://www.freecodecamp.org">this links to freecodecamp.org</a>
```

Dann zeigt dein Browser den Text `this links to freecodecamp.org` als Link an, den du anklicken kannst. Und dieser Link führt dich zu der Webadresse `https://www.freecodecamp.org`.

# --instructions--

Erstelle ein `a`-Element, das auf `https://www.freecatphotoapp.com` verlinkt und "cat photos" als Ankertext hat.

# --hints--

Dein `a`-Element sollte den Ankertext `cat photos` haben.

```js
assert.match(document.querySelector('a').textContent,/cat photos/gi);
```

Du benötigst ein `a`-Element, das auf `https://www.freecatphotoapp.com` verlinkt

```js
assert.match(document.querySelector('a').getAttribute('href'),/^https?:\/\/(www\.)?freecatphotoapp\.com\/?$/i);
```

Dein `a`-Element sollte einen schließenden Tag besitzen.

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
