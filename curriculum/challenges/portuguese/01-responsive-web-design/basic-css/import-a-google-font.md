---
id: bad87fee1348bd9aedf08807
title: Importar uma tipografia do Google
challengeType: 0
videoUrl: 'https://scrimba.com/c/cM9MRsJ'
forumTopicId: 18200
dashedName: import-a-google-font
---

# --description--

In addition to specifying common fonts that are found on most operating systems, we can also specify non-standard, custom web fonts for use on our website. There are many sources for web fonts on the Internet. For this example we will focus on the Google Fonts library.

Google Fonts é uma biblioteca gratuita de tipografias que você pode usar em seu CSS ao referenciar o URL da tipografia.

Então, vamos importar e aplicar uma tipografia a partir do Google.

Para importar uma tipografia, você pode copiar a URL da tipografia a partir da biblioteca do Google Fonts e colá-la em seu HTML. Para esse desafio, vamos importar a tipografia `Lobster`. Para fazer isso, copie o seguinte fragmento de código e cole-o no começo de seu editor de código-fonte (antes da tag de abertura do elemento `style`):

```html
<link href="https://fonts.googleapis.com/css?family=Lobster" rel="stylesheet" type="text/css">
```

Agora você pode usar a fonte `Lobster` em seu CSS ao substituir FAMILY_NAME no código abaixo por `Lobster`:

```css
font-family: FAMILY_NAME, GENERIC_NAME;
```

O GENERIC_NAME é opcional e é uma tipografia alternativa caso a tipografia anterior não esteja disponível. Essa questão será abordada no próximo desafio.

O nome da família de uma tipografia diferencia maiúsculas de minúsculas e deve estar entre aspas caso possua mais de uma palavra. Por exemplo, você precisa de aspas para usar a fonte `"Open Sans"`, mas não para usar a fonte `Lobster`.

# --instructions--

Importe a tipografia `Lobster` na sua página web. Então, crie um seletor para o elemento `h2` e defina a propriedade `font-family` com o valor de `Lobster`.

# --hints--

Você deve importar a tipografia `Lobster`.

```js
assert.exists(document.querySelector('link[href*="googleapis" i]'));
```

O elemento `h2` deve usar a tipografia `Lobster`.

```js
const h2 = document.querySelector('h2'); 
const fontFamily = window.getComputedStyle(h2)['font-family']; 
assert.match(fontFamily, /lobster/i);
```

Você deve usar apenas um seletor para referenciar o elemento `h2` para alterar a tipografia.

```js
assert.match(__helpers.removeHtmlComments(code), /\s*[^\.]h2\s*\{\s*font-family\s*:\s*('|"|)Lobster\1\s*(,\s*('|"|)[a-z -]+\3\s*)?(;\s*\}|\})/gi);
```

O elemento `p` ainda deve usar a tipografia `monospace`.

```js
const paragraphElement = document.querySelector('p');
const fontFamily = window.getComputedStyle(paragraphElement)['font-family']; 
assert.match(fontFamily, /monospace/i);
```

# --seed--

## --seed-contents--

```html
<style>
  .red-text {
    color: red;
  }

  p {
    font-size: 16px;
    font-family: monospace;
  }
</style>

<h2 class="red-text">CatPhotoApp</h2>
<main>
  <p class="red-text">Click here to view more <a href="#">cat photos</a>.</p>

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
<link href="https://fonts.googleapis.com/css?family=Lobster" rel="stylesheet" type="text/css">
<style>
  .red-text {
    color: red;
  }

  p {
    font-size: 16px;
    font-family: monospace;
  }

  h2 {
    font-family: Lobster;
  }
</style>

<h2 class="red-text">CatPhotoApp</h2>
<main>
  <p class="red-text">Click here to view more <a href="#">cat photos</a>.</p>

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
