---
id: 5a24c314108439a4d4036153
title: Registrar um listener de store
challengeType: 6
forumTopicId: 301446
dashedName: register-a-store-listener
---

# --description--

Another method you have access to on the Redux `store` object is `store.subscribe()`. This allows you to subscribe listener functions to the store, which are called whenever an action is dispatched against the store. One simple use for this method is to subscribe a function to your store that simply logs a message every time an action is received and the store is updated.

# --instructions--

Escreva uma função de callback que incrementa a variável global `count` toda vez que a store receber uma ação, e passe esta função para o método `store.subscribe()`. Você verá que `store.dispatch()` é chamado três vezes seguidas, a cada vez que passa diretamente em um objeto de ação. Assista a saída do console entre os despachos de ação para ver as atualizações que ocorrem.

# --hints--

Despachar a ação `ADD` na store deve incrementar o estado por `1`.

```js
assert(
  (function () {
    const initialState = store.getState();
    store.dispatch({ type: 'ADD' });
    const newState = store.getState();
    return newState === initialState + 1;
  })()
);
```

Deve haver uma função de listener inscrita na store usando `store.subscribe`.

```js
assert.match(code, /store\s*\.\s*subscribe\(/gm);
```

O `store.subscribe` deve receber uma função.

```js
assert.match(code, /(\s*function\s*)|(\s*\(\s*\)\s*=>)/gm);
```

The function passed to `store.subscribe` should not be called.

```js
assert.notMatch(code, /store\.subscribe\(.+\(\)\)/);
```

A função de callback para `store.subscribe` também deve incrementar a variável global `count` à medida que a store é atualizada.

```js
assert.strictEqual(store.getState(), count);
```

# --seed--

## --before-user-code--

```js
count = 0;
```

## --seed-contents--

```js
const ADD = 'ADD';

const reducer = (state = 0, action) => {
  switch(action.type) {
    case ADD:
      return state + 1;
    default:
      return state;
  }
};

const store = Redux.createStore(reducer);

// Global count variable:
let count = 0;

// Change code below this line

// Change code above this line

store.dispatch({type: ADD});
console.log(count);
store.dispatch({type: ADD});
console.log(count);
store.dispatch({type: ADD});
console.log(count);
```

# --solutions--

```js
const ADD = 'ADD';

const reducer = (state = 0, action) => {
  switch(action.type) {
    case ADD:
      return state + 1;
    default:
      return state;
  }
};

const store = Redux.createStore(reducer);
 let count = 0;
// Change code below this line

store.subscribe( () =>
 {
 count++;
 }
);

// Change code above this line

store.dispatch({type: ADD});
store.dispatch({type: ADD});
store.dispatch({type: ADD});
```
