---
id: 587d7dbd367417b2b2512bb5
title: 用 Sass 嵌套 CSS
challengeType: 0
forumTopicId: 301457
dashedName: nest-css-with-sass
---

# --description--

Sass allows nesting of CSS rules, which is a useful way of organizing a style sheet.

在 CSS 裏，每個元素的樣式都需要寫在獨立的代碼塊中，如下所示：

```scss
article {
  height: 200px;
}

article p {
  color: white;
}

article ul {
  color: blue;
}
```

對於一個大型項目，CSS 規則會很複雜。 這時，引入嵌套功能（即在對應的父元素中寫子元素的樣式）可以有效地簡化代碼：

```scss
article {
  height: 200px;

  p {
    color: white;
  }

  ul {
    color: blue;
  }
}

```

# --instructions--

根據上面關於嵌套的例子，來簡化 `.blog-post` 中兩個子元素的 CSS 代碼。 爲了通過測試，`h1` 應該出現在 `p` 元素之前。

# --hints--

應重新組織 CSS 規則，以便 `h1` 和 `p` 嵌套在 `.blog-post` 父元素中。

```js
assert(
  code.match(
    /\.blog-post\s*?{\s*?h1\s*?{\s*?text-align:\s*?center;\s*?color:\s*?blue;\s*?}\s*?p\s*?{\s*?font-size:\s*?20px;\s*?}\s*?}/gi
  )
);
```

# --seed--

## --seed-contents--

```html
<style type='text/scss'>
  .blog-post {

  }
  h1 {
    text-align: center;
    color: blue;
  }
  p {
    font-size: 20px;
  }
</style>

<div class="blog-post">
  <h1>Blog Title</h1>
  <p>This is a paragraph</p>
</div>
```

# --solutions--

```html
<style type='text/scss'>
  .blog-post {
    h1 {
      text-align: center;
      color: blue;
    }
    p {
      font-size: 20px;
    }
  }
</style>

<div class="blog-post">
  <h1>Blog Title</h1>
  <p>This is a paragraph</p>
</div>
```
