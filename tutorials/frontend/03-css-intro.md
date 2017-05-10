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
Spre exemplu acest selector css va selecta toate elementele cu clasa `.my-paragraph` a caror parinte este un `div` cu clasa `.my-class`
```css
div.my-class .my-paragraph-class {
    color: red;
    background-color: cian;
    text-align: center;
}
```
```html
<div class="my-class">
  <p class="my-paragraph-class">Bonjour</p>
<div>
```
Mai multe despre selectore poți să afli [aici](https://www.w3schools.com/cssref/css_selectors.asp).

## Cum sa folosesc CSS
Sunt 3 metode de a include stilurile in pagina ta HTML.
1. Fișier extern css declarat în tagul
`<link rel="stylesheet" type="text/css" href="style.css">`
2. Tagul `style` în `head` al documentului HTML
`<style> p { text-indent: 25px; }</style>`
3. Inline style
`<p style="text-indent: 25px">Hola!</p>`
Trebuie sa ții minte ca stilurile care sunt declarate inline au o prioritate mai mare, apoi se aplica cele declarate cu ajutorului tagului `style` sau din fișier extern după ordinea declarării.

## Culori și background
Pentru ca să setezi coloarea unui text poți folosi proprietatea `color` care poate să primeasca valori ca numele culorii `red`, `green`, `blue`.
La fel poți specifica coloare prin codul hexadecimal `#ff00ff` sau rgb `rgb(255, 0, 0)`.

```css
p {
    color: #ff00ff;
    color: rgb(255, 0, 0);
    color: red;
}
```

Pentru a seta culoarea background unui element folosește proprietatea `background-color`.
```css
div {
    background-color: lightblue;
}
```
În caz ca dorești să setezi o imagine pe fundal, ai la îndemină proprietatea `background-image` unde trebuie sa specifici adresa imaginii.
```css
div {
    background-image: url("paper.gif");
}
```

## Stilizarea textelor și fonturi

Pentru a seta un font pentru textul poți folosi proprietatea `font-family`.
```css
p {
    font-family: "Times New Roman", Times, serif;
}
```
Aceasta va seta fontul *Times New Roman* pentru elementul tau. In caz ca acest font lipsește pe calculatorul utilizatorului se va aplica fontul *Times*, si apoi se va recurge la familia de fonutri *serif* în cazul ca nici ultimul font nu este prezent pe calculatorul utilizatorului.
În caz ca vrei sa modifici marimea fontului folosește proprietatea `font-size`.
```css
h1 {
    font-size: 40px;
}
```
Mai multe despre fonturi poți să afli [aici](https://www.w3schools.com/css/css_font.asp)
Pentru ca să schimbi modul în care aratp textului poți folosi urmatoarele proprietăți:

|Proprietatea | Descrierea|
|------------ | -------------|
|color | Setează culoarea textului|
|letter-spacing	| Mărește sau micșoreaza spatiul între litere|
|line-height | Setează înălțimea liniei|
|text-align | Specifică alinierea oriznotală a textului|
|text-decoration | Specifică modul de decorare a textului|
|text-indent | Setează indentarea textului |

Mai multe despre proprietățile CSS care specifică cum va arăta textul tău poți să afli [aici](https://www.w3schools.com/css/css_text.asp)

## Box model
![Box model](/images/css-intro/box-model.png)
Box model este concept care ne permite usor să vizualizăm și întelegem conceptul de margin, padding, border și width / height a unui element.
Un element HTML poate fi reprezentat în forma de niște *cutii* care îl înconjoară, ele fiind:
* margin - distanța în jurul elementului, este transparentă
* border - chenarul elementului
* padding - distanța între conținutul elementului și chenar
* conținutul - spațuil unde este afișat textul interior / imaginea

Înaltimea și lungimea elemetului HTML se calculează în dependeță de cele 4 componente, spre exemplu daca am avea un element cu următoarele proprietăți:
```css
div {
    width: 320px;
    padding: 10px;
    border: 5px solid gray;
    margin: 0; 
}
```
Lățimea lui va fi de 350px, 320px + 20px (left + padding right) + 10px (left + right border) + 0px (left + right margin).

## Poziționare

Proprietatea CSS *position* specifică metoda prin care un element HTML va fi poziționat în pagină.
Există 4 posibile valori pentru proprietatea *position*:
 - *static* (elementul este poziționat după setarea implicită a browserlui)
 ```css
 div.static {
    position: static;
    border: 3px solid #73AD21;
}
 ```
![Static element](/images/css-intro/static_element.png)

 - *relative* (elementul este poziționat relativ față de poziția lui inițială, însa ocupa spațiul rezervat)

```css
div.relative {
    position: relative;
    left: 30px;
    border: 3px solid red;
}
```
![Relative element](/images/css-intro/relative_element.png)

 - *absolute* (elementul este poziționat absolut față de primul părinte cu poziția *relative* 
sau dacă acesta nu este față de elemntul body al documentului HTML).
```css
div.relative {
    position: relative;
    width: 400px;
    height: 200px;
    border: 3px solid #73AD21;
} 
div.absolute {
    position: absolute;
    top: 80px;
    right: 0;
    width: 200px;
    height: 100px;
    border: 3px solid #73AD21;
}
```

![Absolute element](/images/css-intro/absolute_element.png)

 - *fixed* (specifică poziționarea fixă pe pagină, asta înseamnă ca elemntul va ramîne constant pe ecran, chiar dacă facem scroll).
```css
div.fixed {
    position: fixed;
    bottom: 0;
    right: 0;
    width: 300px;
    border: 3px solid #73AD21;
}
```

![Fixed element](/images/css-intro/fixed_element.png)

## Elemente plutitoare