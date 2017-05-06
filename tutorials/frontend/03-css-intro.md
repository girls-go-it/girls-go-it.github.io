---
layout: default
title: CSS Intro
category: basic
---

## Ce este CSS

Lecția trecuta am studiat cum sa cream o pagină web cu ajutorul HTML. Insă HTML este libajul care definește structura documentului și nu ne oferă posbilitatea de a face pagina noastră să arate frumos.
În ajutor ne poate veni CSS (Cascading style sheet), un standart care definește în ce mod o să arate pagina noastra.
Pentru inceput inceput hai sa creem un document HTML pe care apoi o sa-l folosim pentru a aplica sintaxa CSS si a face siteul tău mai frumos.

Pentru inceput in sublime creaza un fișier nou si scrie urmatorul cod.

```html
<!DOCTYPE html>
<html>
<head>
	<title></title>
</head>
<body>

</body>
</html>
```

## Sintaxa CSS

Pentru a incepe lucrul cu CSS trebuie sa întelegem sintaxa lui. Sintaxa CSS arată in felul urmator.
![CSS syntax](/images/css-intro/selector.gif)
Poți sa observi ca ea include un selector (un grup de elemente HTML) și proprietațile pe care le definește regula CSS.
Ca selector poate servi denumirea unui tag, o clasa, id, combinație de denumirea tagului clasa și id. Suna complicat? Cred ca dupa ce o sa vedem exemple reale iți vei da seama este foarte ușor de scris selectore CSS.
Creaza în interiorul tagului body un tag p (paragraph)
```html
<p>Salut</p>
```

Apoi adaugă în interiorului tagul head urmatorul text.
```html
<style type="text/css">
    p {
        color: red;
        font-size: 25px
    }
</style>
```

Dupa de deschizi pagina ta HTML în browser poti sa vezi urmatorul rezultat.
![Selector tag](/images/css-intro/selector_tag.png)

Drept selector poate servi o clasa, care defapt inseamna un grup de elemente care vor avea proprietăți comune.
Pentru a crea o un element HTML cu o clasa poti folosi urmatoare sintaxă.

```html
<div class='my-class'>Hello</div>
```

Apoi folosește sintaxa css pentru a defini stilul clasei tale.
```css
.my-class {
    background-color: orange;
    font-size: 30px;
}
```
Rezultatul va arăta in felul următor.
![Selector class](/images/css-intro/selector_class.png)

Ca selector poate fi folosit si id (identificator unic unui element HTML)
Ca și în cazul precedent creaza un element div folosind următoarea sintaxă.
```html
<div id='my-id'>¡Hola!</div>
```
La fel ca și pentru elementul HTML precedent este nevoie sa a definești stilurile noi pentru elementul nou creat.
```css
#my-id {
background-color: blue;
font-size: 40px;
}
```
![Selector id](/images/css-intro/selector_id.png)

Un selector poate fi și unul mai specific spre exemplu putem folosi combinație de selectori pentru unele elemente.
Spre exemplu acest selector css va selecta toate elementele cu clasa `.my-paragraph` a caror parinte este un `div` cu clasa `.myclass`
```css
div.my-class .my-paragraph-class {
color: red;
background-color: cian;
text-align: center;
}
```
