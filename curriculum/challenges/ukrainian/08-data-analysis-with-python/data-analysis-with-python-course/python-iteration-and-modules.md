---
id: 5e9a093a74c4063ca6f7c167
title: 'Python: ітерація та модулі'
challengeType: 11
videoId: XzosGWLafrY
bilibiliIds:
  aid: 633068913
  bvid: BV1db4y127M4
  cid: 409024056
dashedName: python-iteration-and-modules
---

# --description--

*Instead of using notebooks.ai like it shows in the video, you can use Google Colab instead.*

Додаткові ресурси:

-  <a href="https://github.com/ine-rmotr-curriculum/ds-content-python-under-10-minutes" target="_blank" rel="noopener noreferrer nofollow">Notebooks on GitHub</a>
-  <a href="https://colab.research.google.com/github/googlecolab/colabtools/blob/master/notebooks/colab-github-demo.ipynb" target="_blank" rel="noopener noreferrer nofollow">Як відкрити блокноти з GitHub використовуючи Google Colab.</a>

# --questions--

## --text--

Як за допомогою ітерації надрукувати ключі та значення словника `user`?

## --answers--

```python
for key in user.items():
    print(key)
```

---

```python
for key, value in user.all():
    print(key, value)
    print(value)
```

---

```python
for key, value in user.items():
    print(key, value)
```

---

```python
for key, value in user
    print(key, value)
```

## --video-solution--

3

