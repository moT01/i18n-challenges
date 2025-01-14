---
id: 587d8249367417b2b2512c3e
title: 使用 helment.noCache() 禁用客戶端緩存
challengeType: 2
forumTopicId: 301576
dashedName: disable-client-side-caching-with-helmet-nocache
---

# --description--

As a reminder, this project is being built upon the following starter project on <a href="https://gitpod.io/?autostart=true#https://github.com/freeCodeCamp/boilerplate-infosec/" target="_blank" rel="noopener noreferrer nofollow">Gitpod</a>, or cloned from <a href="https://github.com/freeCodeCamp/boilerplate-infosec/" target="_blank" rel="noopener noreferrer nofollow">GitHub</a>. Learn <a href="https://forum.freecodecamp.org/t/how-to-use-gitpod-in-the-curriculum/668669#how-can-i-share-my-workspace-to-get-help-8" target="_blank" rel="noopener noreferrer nofollow">how to share your Gitpod workspace to get help</a>.

如果你正在爲你的網站發佈更新，而你希望用戶總是下載較新的版本，你可以（嘗試）在客戶的瀏覽器上禁用緩存。 它在開發中也很有用。 緩存具有性能優勢，你將失去這些優勢，因此只有在真正需要時才使用此選項。

# --instructions--

在你的服務器上使用 `helmet.noCache()` 方法。

# --hints--

應正確加載 helmet.noCache() 中間件

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

