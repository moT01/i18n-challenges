---
id: 587d824d367417b2b2512c53
title: Testen, ob ein String einen Substring enthält
challengeType: 2
forumTopicId: 301597
dashedName: test-if-a-string-contains-a-substring
---

# --description--

As a reminder, this project is being built upon the following starter project on <a href="https://gitpod.io/?autostart=true#https://github.com/freeCodeCamp/boilerplate-mochachai/" target="_blank" rel="noopener noreferrer nofollow">Gitpod</a>, or cloned from <a href="https://github.com/freeCodeCamp/boilerplate-mochachai/" target="_blank" rel="noopener noreferrer nofollow">GitHub</a>. Learn <a href="https://forum.freecodecamp.org/t/how-to-use-gitpod-in-the-curriculum/668669#how-can-i-share-my-workspace-to-get-help-8" target="_blank" rel="noopener noreferrer nofollow">how to share your Gitpod workspace to get help</a>.

`include()` und `notInclude()` funktionieren auch für Strings! `include()` überprüft, ob der aktuelle String den erwarteten Substring enthält.

# --instructions--

Ändere innerhalb `tests/1_unit-tests.js` unter dem Test mit der Beschriftung `#14` in der `Strings`-Suite, jeden `assert` in `assert.include` oder `assert.notInclude` um, damit der Test bestanden wird (sollte `true` ausgeben). Ändere nicht die Argumente, die an die Assertions übergeben werden.

# --hints--

Alle Tests sollten bestehen.

```js
(getUserInput) =>
  $.get(getUserInput('url') + '/_api/get-tests?type=unit&n=13').then(
    (data) => {
      assert.equal(data.state, 'passed');
    },
    (xhr) => {
      throw new Error(xhr.responseText);
    }
  );
```

Du solltest die richtige Methode für die erste Behauptung auswählen - `include` vs. `notInclude`.

```js
(getUserInput) =>
  $.get(getUserInput('url') + '/_api/get-tests?type=unit&n=13').then(
    (data) => {
      assert.equal(
        data.assertions[0].method,
        'include',
        "'Arrow' contains 'row'..."
      );
    },
    (xhr) => {
      throw new Error(xhr.responseText);
    }
  );
```

Du solltest die richtige Methode für die zweite Behauptung auswählen - `include` vs. `notInclude`.

```js
(getUserInput) =>
  $.get(getUserInput('url') + '/_api/get-tests?type=unit&n=13').then(
    (data) => {
      assert.equal(
        data.assertions[1].method,
        'notInclude',
        "... a 'dart' doesn't contain a 'queue'"
      );
    },
    (xhr) => {
      throw new Error(xhr.responseText);
    }
  );
```

