---
id: 5ee127a03c3b35dd45426493
title: 将一个变量的值赋给另一个
challengeType: 1
forumTopicId: 418265
dashedName: assigning-the-value-of-one-variable-to-another
---

# --description--

After a value is assigned to a variable using the <dfn>assignment</dfn> operator, you can assign the value of that variable to another variable using the <dfn>assignment</dfn> operator.

```js
var myVar;
myVar = 5;
var myNum;
myNum = myVar;
```

以上代码声明了一个没有初始值的变量 `myVar`，然后给它赋值为 `5`。 紧接着，又声明了一个没有初始值的变量 `myNum`。 然后，变量 `myVar` 的内容（也就是 `5`）被赋给了变量 `myNum`。 现在，变量 `myNum` 的值也为 `5`。

# --instructions--

把变量 `a` 的内容赋给变量 `b`。

# --hints--

你不应该修改注释上面的代码。

```js
assert(/var a;/.test(__helpers.removeJSComments(code)) && /a = 7;/.test(__helpers.removeJSComments(code)) && /var b;/.test(__helpers.removeJSComments(code)));
```

`b` 的值应该为 `7`。

```js
assert(typeof b === 'number' && b === 7);
```

应该使用 `=` 将 `a` 赋给 `b`。

```js
assert(/b\s*=\s*a\s*/g.test(__helpers.removeJSComments(code)));
```

# --seed--

## --before-user-code--

```js
if (typeof a != 'undefined') {
  a = undefined;
}
if (typeof b != 'undefined') {
  b = undefined;
}
```

## --after-user-code--

```js
(function(a, b) {
  return 'a = ' + a + ', b = ' + b;
})(a, b);
```

## --seed-contents--

```js
// Setup
var a;
a = 7;
var b;

// Only change code below this line
```

# --solutions--

```js
var a;
a = 7;
var b;
b = a;
```
