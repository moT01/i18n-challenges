---
id: 5e46f983ac417301a38fb933
title: SHA-1 パスワードクラッカー
challengeType: 10
forumTopicId: 462374
helpCategory: Python
dashedName: sha-1-password-cracker
---

# --description--

このプロジェクトでは、<a href="https://gitpod.io/?autostart=true#https://github.com/freeCodeCamp/boilerplate-SHA-1-password-cracker" target="_blank" rel="noopener noreferrer nofollow">Gitpod のスターターコードを使って作業を行います</a>。質問などの際に <a href="https://forum.freecodecamp.org/t/how-to-use-gitpod-in-the-curriculum/668669#how-can-i-share-my-workspace-to-get-help-8" target="_blank" rel="noopener noreferrer nofollow">Gitpod ワークスペースを共有する方法はこちら</a>を参照してください。

Python カリキュラムの対話式教育コンテンツを引き続き開発中です。 現在、下記の freeCodeCamp.org YouTube チャンネルで、このプロジェクトの完了に必要なすべての知識について説明する動画をいくつか公開しています。

- <a href="https://www.freecodecamp.org/news/python-for-everybody/" target="_blank" rel="noopener noreferrer nofollow">「みんなの Python」ビデオコース</a> (14 時間)

- <a href="https://www.freecodecamp.org/news/learn-python-basics-in-depth-video-course/" target="_blank" rel="noopener noreferrer nofollow">Python の基礎を詳しく学ぶ</a> (4 時間)

- <a href="https://www.freecodecamp.org/news/intermediate-python-course/" target="_blank" rel="noopener noreferrer nofollow">Python 中級コース</a> (6 時間)

# --instructions--

パスワードはプレーンテキストで保存すべきではありません。 パスワードリストが暴露された場合に備えて、ハッシュとして保存する必要があります。 ただし、すべてのハッシュが同じように作成されるとは限りません。

このプロジェクトでは、SHA-1 を使用してハッシュ化されたパスワードの解読を試みるパスワードクラックプログラムを作成し、その作業を通じて適切なセキュリティを実現することの重要性を学びます。

パスワードの SHA-1 ハッシュを受け取り、パスワードがすでに使用されている上位 10,000 個のうちの 1 つである場合に、そのパスワードを返す関数を作成してください。 SHA-1 ハッシュがデータベースにあるパスワード「ではない」場合は、"PASSWORD NOT IN DATABASE" を返してください。

関数では、`top-10000-passwords.txt` から得られるそれぞれのパスワードをハッシュし、それらを関数に渡されたハッシュと比較する必要があります。

関数は、`use_salts` というオプションの 2 つ目の引数を受け取る必要があります。 この引数が true に設定されている場合は、`top-10000-passwords.txt` から得られる各パスワードの「前と後ろの両方」に、ファイル `known-salts.txt` から得られる各ソルト文字列を追加したうえで、ハッシュ化を行い、関数に渡されたハッシュと比較する必要があります。

関数のテストに使用できるハッシュ化されたパスワードの例を次に示します。

- `b305921a3723cd5d70a375cd21a61e60aabb84ec` は "sammy123" を返す
- `c7ab388a5ebefbf4d550652f1eb4d833e5316e3e` は "abacab" を返す
- `5baa61e4c9b93f3f0682250b6cf8331b7ee68fd8` は "password" を返す

`use_salts` を `True` に設定した場合に関数のテストに使用できるハッシュ化されたパスワードの例を次に示します。

- `53d8b3dc9d39f0184144674e310185e41a87ffd5` は "superman" を返す
- `da5a4e8cf89539e66097acd2f8af128acae2f8ae` は "q1w2e3r4t5" を返す
- `ea3f62d498e3b98557f9f9cd0d905028b3b019e1` は "bubbles1" を返す

`hashlib` ライブラリをあらかじめインポートしてあります。 このライブラリの使用を検討してください。 <a href="https://docs.python.org/3/library/hashlib.html" target="_blank" rel="noopener noreferrer nofollow">hashlib の詳細についてはこちらを参照してください</a>。

## 開発

`password_cracker.py` にコードを記述してください。 開発には `main.py` を使用してコードをテストすることができます。

## テスト

このプロジェクトの単体テストは `test_module.py` にあります。 すでに `test_module.py` から `main.py` にテストをインポートしてあります。

## 提出

プロジェクトの URL をコピーし、freeCodeCamp に提出してください。

# --hints--

すべての Python テストが成功する必要があります。

```js

```

# --solutions--

```py
  # Python challenges don't need solutions,
  # because they would need to be tested against a full working project.
  # Please check our contributing guidelines to learn more.
```
