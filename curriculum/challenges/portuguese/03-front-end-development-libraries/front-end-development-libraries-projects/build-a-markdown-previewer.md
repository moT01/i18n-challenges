---
id: bd7157d8c242eddfaeb5bd13
title: Criar um pré-visualizador de markdown
challengeType: 3
forumTopicId: 301372
dashedName: build-a-markdown-previewer
---

# --description--
**Note:** **React 18 has known incompatibilities with the tests for this project (see [issue](https://github.com/freeCodeCamp/freeCodeCamp/issues/45922))**

**Objetivo:** criar uma aplicação que funcione de modo semelhante ao que vemos em: <a href="https://markdown-previewer.freecodecamp.rocks/" target="_blank" rel="noopener noreferrer nofollow">https://markdown-previewer.freecodecamp.rocks/</a>.

Atenda às histórias de usuário abaixo e faça com que todos os testes passem. Use quaisquer bibliotecas ou APIs de que você precisar. Dê ao projeto o seu próprio estilo pessoal.

Você pode usar qualquer mistura de HTML, JavaScript, CSS, Bootstrap, SASS, React, Redux e JQuery para completar este projeto. Você deve usar um framework de front-end (como React por exemplo) porque essa seção trata de aprender frameworks de front-end. Tecnologias adicionais não listadas acima não são recomendadas e usá-las é por sua conta e risco. Estamos buscando apoiar outros frameworks de front-end, como Angular e Vue, mas eles não são atualmente suportados. Vamos aceitar e tentar corrigir todos os relatórios de problemas que usem o conjunto de tecnologias sugeridas para esse projeto. Boa programação para você!

**História de usuário nº 1:** eu consigo ver um elemento `textarea` com o `id="editor"` correspondente.

**História de usuário nº 2:** eu consigo ver um elemento com o `id="preview"` correspondente.

**História de usuário nº 3:** quando eu insiro texto no elemento `#editor`, o elemento `#preview` é atualizado enquanto eu escrevo para exibir o conteúdo do textarea.

**História de usuário nº 4:** quando insiro marcação do GitHub no elemento `#editor`, o texto é renderizado como HTML no elemento `#preview` enquanto eu escrevo (DICA: você não precisa analisar a marcação você mesmo - você pode importar a biblioteca Marked para isso: <https://cdnjs.com/libraries/marked>).

**História de usuário nº 5:** quando meu pré-visualizador de marcação carregar pela primeira vez, o texto padrão no campo `#editor` deve conter uma marcação válida que represente pelo menos um de cada um dos elementos a seguir: um elemento (tamanho H1), um subelemento de título (tamanho H2), um link, um código em linha, um código de bloco, uma lista de item, um blockquote, uma imagem e um texto em negrito.

**História de usuário nº 6:** quando meu pré-visualizador de marcação carregar pela primeira vez, a marcação padrão no campo `#editor` deve ser renderizada como HTML no elemento `#preview`.

**Bônus opcional (você não precisa de aprovação nesse teste):** meu pré-visualizador de marcação interpreta o retorno de carro e o renderiza como elementos `br` (quebra de linha).

You can build your project by <a href='https://codepen.io/pen?template=MJjpwO' target='_blank' rel="noopener noreferrer nofollow">using this CodePen template</a> and clicking `Save` to create your own pen. If you prefer to use another environment, then put this `<script>` tag into the body of your `index.html` file: `<script src="https://cdn.freecodecamp.org/testable-projects-fcc/v1/bundle.js"></script>`

Quando você terminar, envie o URL do seu projeto depois de ele haver passado em todos os testes.

# --solutions--

```js
// solution required
```
