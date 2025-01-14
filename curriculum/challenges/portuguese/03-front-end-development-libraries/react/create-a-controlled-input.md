---
id: 5a24c314108439a4d4036178
title: Criar um input controlado
challengeType: 6
forumTopicId: 301385
dashedName: create-a-controlled-input
---

# --description--

Your application may have more complex interactions between `state` and the rendered UI. For example, form control elements for text input, such as `input` and `textarea`, maintain their own state in the DOM as the user types. With React, you can move this mutable state into a React component's `state`. The user's input becomes part of the application `state`, so React controls the value of that input field. Typically, if you have React components with input fields the user can type into, it will be a controlled input form.

# --instructions--

O editor de código tem o esqueleto de um componente chamado `ControlledInput` para criar um elemento controlado `input`. O `state` do componente já está inicializado com a propriedade `input` que possui uma string vazia. Esse valor representa o texto que o usuário digitou no campo `input`.

Primeiro, crie um método chamado `handleChange()` que tem um parâmetro chamado `event`. Quando o método é chamado, ele recebe um objeto `event` que contém a string do texto do elemento `input`. Você pode acessar essa string com `event.target.value` dentro do método. Atualize a propriedade `input` do `state` do componente com essa nova string.

No método `render`, crie o elemento `input` acima da tag `h4`. Adicione o atributo `value` o qual é igual a propriedade `input` do `state` do componente. Adicione a propriedade `onChange` ao método manipulador de eventos `handleChange()`.

Quando você digita na caixa de entrada, o texto é processado pelo método `handleChange()`, definido como a propriedade `input` no local `state`, e renderizado como o valor do `input` na página. O componente `state` é a única fonte de verdade em relação aos dados de entrada.

Por último, mas não menos importante, não se esqueça de adicionar as ligações necessárias no construtor.

# --hints--

`ControlledInput` deve retornar um elemento `div` que contém as tags `input` e `p`.

```js
assert(
  Enzyme.mount(React.createElement(ControlledInput))
    .find('div')
    .children()
    .find('input').length === 1 &&
    Enzyme.mount(React.createElement(ControlledInput))
      .find('div')
      .children()
      .find('p').length === 1
);
```

O estado de `ControlledInput` deve inicializar com a propriedade `input` definida para ser uma string vazia.

```js
assert.strictEqual(
  Enzyme.mount(React.createElement(ControlledInput)).state('input'),
  ''
);
```

Escrever no elemento input deve atualizar o estado e o valor do input, e o elemento `p` deve renderizar esse estado enquanto você digita.

```js
async () => {
  const waitForIt = (fn) =>
    new Promise((resolve, reject) => setTimeout(() => resolve(fn()), 250));
  const mockedComponent = Enzyme.mount(React.createElement(ControlledInput));
  const _1 = () => {
    mockedComponent.setState({ input: '' });
    return waitForIt(() => mockedComponent.state('input'));
  };
  const _2 = () => {
    mockedComponent
      .find('input')
      .simulate('change', { target: { value: 'TestInput' } });
    return waitForIt(() => ({
      state: mockedComponent.state('input'),
      text: mockedComponent.find('p').text(),
      inputVal: mockedComponent.find('input').props().value
    }));
  };
  const before = await _1();
  const after = await _2();
  assert(
    before === '' &&
      after.state === 'TestInput' &&
      after.text === 'TestInput' &&
      after.inputVal === 'TestInput'
  );
};
```

# --seed--

## --after-user-code--

```jsx
ReactDOM.render(<ControlledInput />, document.getElementById('root'))
```

## --seed-contents--

```jsx
class ControlledInput extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      input: ''
    };
    // Change code below this line

    // Change code above this line
  }
  // Change code below this line

  // Change code above this line
  render() {
    return (
      <div>
        { /* Change code below this line */}

        { /* Change code above this line */}
        <h4>Controlled Input:</h4>
        <p>{this.state.input}</p>
      </div>
    );
  }
};
```

# --solutions--

```jsx
class ControlledInput extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      input: ''
    };
    this.handleChange = this.handleChange.bind(this);
  }
  handleChange(event) {
    this.setState({
      input: event.target.value
    });
  }
  render() {
    return (
      <div>
        <input
          value={this.state.input}
          onChange={this.handleChange} />
        <h4>Controlled Input:</h4>

        <p>{this.state.input}</p>
      </div>
    );
  }
};
```
