---
id: 587d8247367417b2b2512c37
title: helmet.hidePoweredBy() を使用して危険性のある情報を隠す
challengeType: 2
forumTopicId: 301580
dashedName: hide-potentially-dangerous-information-using-helmet-hidepoweredby
---

# --description--

注意点として、このプロジェクトは <a href="https://gitpod.io/?autostart=true#https://github.com/freeCodeCamp/boilerplate-infosec/" target="_blank" rel="noopener noreferrer nofollow">Gitpod</a> にある次のスタータープロジェクトをベースに構築されているか、または <a href="https://github.com/freeCodeCamp/boilerplate-infosec/" target="_blank" rel="noopener noreferrer nofollow">GitHub</a> からクローンされています。 質問などの際に <a href="https://forum.freecodecamp.org/t/how-to-use-gitpod-in-the-curriculum/668669#how-can-i-share-my-workspace-to-get-help-8" target="_blank" rel="noopener noreferrer nofollow">Gitpod ワークスペースを共有する方法はこちらを参照</a>してください。

サイトで Express を使用していることがハッカーに知られた場合、ハッカーは Express や Node の既知の脆弱性を悪用する可能性があります。 デフォルトでは、Express からリクエストが発生するたびに `X-Powered-By: Express` が送信されます。 `helmet.hidePoweredBy()` ミドルウェアを使用して X-Powered-By ヘッダーを削除してください。

# --hints--

helmet.hidePoweredBy() ミドルウェアを正しくマウントする必要があります。

```js
(getUserInput) =>
  $.get(getUserInput('url') + '/_api/app-info').then(
    (data) => {
      assert.include(data.appStack, 'hidePoweredBy');
      assert.notEqual(data.headers['x-powered-by'], 'Express');
    },
    (xhr) => {
      throw new Error(xhr.responseText);
    }
  );
```

