---
id: 587d8248367417b2b2512c3d
title: Disabilitare il precaricamento DNS con helmet.dnsPrefetchControl()
challengeType: 2
forumTopicId: 301577
dashedName: disable-dns-prefetching-with-helmet-dnsprefetchcontrol
---

# --description--

As a reminder, this project is being built upon the following starter project on <a href="https://gitpod.io/?autostart=true#https://github.com/freeCodeCamp/boilerplate-infosec/" target="_blank" rel="noopener noreferrer nofollow">Gitpod</a>, or cloned from <a href="https://github.com/freeCodeCamp/boilerplate-infosec/" target="_blank" rel="noopener noreferrer nofollow">GitHub</a>. Learn <a href="https://forum.freecodecamp.org/t/how-to-use-gitpod-in-the-curriculum/668669#how-can-i-share-my-workspace-to-get-help-8" target="_blank" rel="noopener noreferrer nofollow">how to share your Gitpod workspace to get help</a>.

Per migliorare le prestazioni, la maggior parte dei browser precarica i record DNS per i link in una pagina. In questo modo l'ip di destinazione è già noto quando l'utente fa clic su un link. Questo può portare ad un uso eccessivo del servizio DNS (se possedete un grande sito web, visitato da milioni di persone…), problemi di privacy (un origliatore potrebbe dedurre che sei su una determinata pagina), o un'alterazione delle statistiche di pagina (alcuni link possono apparire visitati anche se non lo sono). Se hai esigenze di sicurezza elevata, è possibile disabilitare il precaricamento DNS, al costo di una perdita di prestazioni.

# --instructions--

Usa il metodo `helmet.dnsPrefetchControl()` sul tuo server.

# --hints--

Il middleware helmet.dnsPrefetchControl() deve essere montato correttamente

```js
(getUserInput) =>
  $.get(getUserInput('url') + '/_api/app-info').then(
    (data) => {
      assert.include(data.appStack, 'dnsPrefetchControl');
      assert.equal(data.headers['x-dns-prefetch-control'], 'off');
    },
    (xhr) => {
      throw new Error(xhr.responseText);
    }
  );
```

