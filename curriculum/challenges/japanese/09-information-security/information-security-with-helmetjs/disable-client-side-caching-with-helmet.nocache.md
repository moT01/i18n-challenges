---
id: 587d8249367417b2b2512c3e
title: helmet.noCache() を使用してクライアントサイドのキャッシュを無効にする
challengeType: 2
forumTopicId: 301576
dashedName: disable-client-side-caching-with-helmet-nocache
---

# --description--

注意点として、このプロジェクトは <a href="https://gitpod.io/?autostart=true#https://github.com/freeCodeCamp/boilerplate-infosec/" target="_blank" rel="noopener noreferrer nofollow">Gitpod</a> にある次のスタータープロジェクトをベースに構築されているか、または <a href="https://github.com/freeCodeCamp/boilerplate-infosec/" target="_blank" rel="noopener noreferrer nofollow">GitHub</a> からクローンされています。 質問などの際に <a href="https://forum.freecodecamp.org/t/how-to-use-gitpod-in-the-curriculum/668669#how-can-i-share-my-workspace-to-get-help-8" target="_blank" rel="noopener noreferrer nofollow">Gitpod ワークスペースを共有する方法はこちらを参照</a>してください。

ウェブサイトのアップデートを行う際に、ユーザーに常に新しいバージョンをダウンロードしてもらいたい場合、クライアントのブラウザーでキャッシュの無効化を行う (または試みる) ことができます。 これは開発の場合にも役立ちます。 キャッシュにはパフォーマンス上の利点がありますが、それを失うことになるため、このオプションは本当に必要な場合にのみ使用してください。

# --instructions--

サーバーで `helmet.noCache()` メソッドを使用してください。

# --hints--

helmet.noCache() ミドルウェアを正しくマウントする必要があります。

```js
(getUserInput) =>
  $.get(getUserInput('url') + '/_api/app-info').then(
    (data) => {
      assert.include(data.appStack, 'nocache');
      assert.equal(
        data.headers['cache-control'],
        'no-store, no-cache, must-revalidate, proxy-revalidate'
      );
    },
    (xhr) => {
      throw new Error(xhr.responseText);
    }
  );
```

