---
id: bad87fee1348bd9aedf08804
title: HTML auskommentieren
challengeType: 0
videoUrl: 'https://scrimba.com/p/pVMPUv/cGyGbca'
forumTopicId: 16782
dashedName: comment-out-html
---

# --description--

Remember that in order to start a comment, you need to use `<!--` and to end a comment, you need to use `-->`

Hier musst du den Kommentar beenden, bevor dein `h2`-Element beginnt.

# --instructions--

Kommentiere dein `h1`-Element und dein `p`-Element aus, aber nicht dein `h2`-Element.

# --hints--

Dein `h1`-Element sollte auskommentiert werden, damit es auf der Seite nicht sichtbar ist.

```js
assert.isEmpty(document.querySelectorAll('h1'));
```

Dein `h2`-Element sollte nicht auskommentiert werden, damit es auf der Seite sichtbar ist.

```js
assert.isNotEmpty(document.querySelectorAll('h2'));
```

Dein `p`-Element sollte auskommentiert werden, damit es auf der Seite nicht sichtbar ist.

```js
assert.isEmpty(document.querySelectorAll('p'));
```

Jeder deiner Kommentare sollte mit `-->` abgeschlossen werden.

```js
assert.isAbove(code.match(/[^fc]-->/g).length, 1);
```

Du solltest die Reihenfolge des `h1`, `h2`, oder `p` Elements in deinem Code nicht ändern.

```js
assert.strictEqual(code.match(/<([a-z0-9]){1,2}>/g)[0],'<h1>');
assert.strictEqual(code.match(/<([a-z0-9]){1,2}>/g)[1],'<h2>');
assert.strictEqual(code.match(/<([a-z0-9]){1,2}>/g)[2],'<p>');
```

# --seed--

## --seed-contents--

```html
<!--
<h1>Hello World</h1>

<h2>CatPhotoApp</h2>

<p>Kitty ipsum dolor sit amet, shed everywhere shed everywhere stretching attack your ankles chase the red dot, hairball run catnip eat the grass sniff.</p>
-->
```

# --solutions--

```html
<!--<h1>Hello World</h1>-->
<h2>CatPhotoApp</h2> 
<!--<p>Kitty ipsum dolor sit amet, shed everywhere shed everywhere stretching attack your ankles chase the red dot, hairball run catnip eat the grass sniff.</p> -->
```
