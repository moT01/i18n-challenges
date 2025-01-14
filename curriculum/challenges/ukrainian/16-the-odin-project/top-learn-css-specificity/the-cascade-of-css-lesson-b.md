---
id: 6489c96782cf2e4f86f03ae2
title: Каскадність CSS. Урок №2
challengeType: 15
dashedName: the-cascade-of-css-lesson-b
---

# --description--

Чим специфічніше оголошення CSS, тим у нього більше переваги над іншими. Вбудовані стилі, які ви розглянули минулого уроку, мають найвищу специфічність серед інших селекторів, хоча кожен тип селектора має власний рівень специфічності, який сприяє специфічності оголошення. Інші селектори сприяють специфічності, але ми фокусуємось лише на тих, які вже розглянули:

1. селектори ID (найспецифічніший селектор);
2. селектори класу;
3. селектори типу.

Специфічність враховується лише тоді, коли елемент має декілька конфліктуючих оголошень, націлених на себе. Селектор ID завжди переважатиме будь-яку кількість селекторів класу, селектор класу завжди переважатиме будь-яку кількість селекторів типу, а селектор типу завжди переважатиме будь-яку кількість менш специфічних селекторів. Якщо жодне оголошення не має селектору вищої специфічності, то більша кількість селектору переважає меншу кількість того самого селектору.

# --questions--

## --text--

Що з переліченого показує правильний порядок специфічності селекторів CSS (від найбільш специфічного до найменш специфічного)?

## --answers--

Селектори типу, селектори класу, селектори ID

---

Селектори ID, селектори класу, селектори типу

---

Селектори класу, селектори типу, селектори ID

---

Селектори ID, селектори типу, селектори класу

## --video-solution--

2
