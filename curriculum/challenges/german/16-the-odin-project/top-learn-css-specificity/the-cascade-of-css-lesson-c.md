---
id: 6489cb0b82cf2e4f86f03ae3
title: The Cascade of CSS Lesson C
challengeType: 15
dashedName: the-cascade-of-css-lesson-c
---

# --description--

Lass uns einige kurze Beispiele anschauen, um zu veranschaulichen, wie Spezifität funktioniert. Betrachte den folgenden HTML- und CSS-Code:

```html
<!-- index.html -->

<div class="main">
  <div class="list subsection"></div>
</div>
```

```css
/* rule 1 */
.subsection {
  color: blue;
}

/* rule 2 */
.main .list {
  color: red;
}
```

Im vorstehenden Beispiel verwenden beide Regeln nur Klassenselektoren, aber Regel 2 ist spezifischer, da sie mehr Klassenselektoren verwendet.

# --questions--

## --text--

Auf der Grundlage des gegebenen HTML- und CSS-Codes würde das `<div class="list subsection"></div>`-Element in welcher Farbe dargestellt werden?

## --answers--

blau

---

rot

---

lila

---

schwarz

## --video-solution--

2
