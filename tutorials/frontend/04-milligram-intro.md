---
layout: default
title: Milligram Intro
category: basic
---

## Intro

Una din cele mai plăcute ocupații este să studiezi [**HTML**](http://girls-go-it.github.io/tutorials/frontend/02-html-intro/) și [**CSS**](http://girls-go-it.github.io/tutorials/frontend/03-css-intro/), mai ales atunci când elementele create arată bine fără un efort adițional considerabil. Pentru acest scop, poate fi utilizat [**Milligram**](http://milligram.io/). 

[**Milligram**](http://milligram.io/) este un framework (set de unelte) care oferă un punct de pornire rapid și bine stilizat. Evident, acest framework poate fi utilizat nu doar pentru studii, dar și pentru crearea website-urilor complexe.

## Getting Started

[**Milligram**](http://milligram.io) poate fi inclus în pagină în 2 moduri. Primul mod este să descărcăm pachetul de instalare care conține fișierul CSS de care avem nevoie. Al 2-lea mod este să indicăm calea către fișierul CSS care se află pe o [**rețea de distribuție a conținutului**](https://ro.wikipedia.org/wiki/Re%C8%9Bea_de_distribu%C8%9Bie_de_con%C8%9Binut). Mai jos sunt descrise ambele moduri.


#### Descărcare locală


1. Descărcă de [**aici**](http://milligram.io/) pachetul de instalare
2. După descărcare, dezarhivează dosarul. Dosarul dezarhivat are următoarea structură

    ```
    milligram/
    ├── examples/
    │   └── index.html
    ├── dist/
    │   ├── milligram.css
    │   └── milligram.min.css
    ├── license
    └── readme.md
    ```
3. Loacalizează fișierele CSS din dosarul *milligram/dist.*

    *milligram.min.css* - este versiunea minimizată care ocupă mai puțin spațiu, dar este mai puțin lizibilă.

    *milligram.css* - este versiunea necomprimată care e mai ușor de citit, dar ocupă mai mult spațiu.

    De obicei, includem în pagini versiunea minimizată. Versiunea necomprimată poate fi utilizată atunci când e nevoie de modificat sau analizat stilurile folosite de framework.
4. În dosarul unde sunt sau vor fi paginile HTML, crează un dosar nou cu numele *css* și mută în el fișierul *milligram.min.css* sau *milligram.css.*
5. În paginile HTML, în secțiunea ```<head>``` indică calea către fișierul CSS. De exemplu, dacă dosarul unde se află paginile HTML se numește *my-cool-website* și în el avem un fișier *index.html*, vom indica

  ```html
  <head>
      <link rel="stylesheet" type="text/css" href="css/milligram.min.css">
  </head>
  ```
6. Felicitări! Acum toate elementele HTML din paginile unde ai adăugat link-ul căre fișierul CSS vor fi stilizate de [**Milligram**](http://milligram.io).

#### Cu ajutorul unei rețele de distribuție a conținutului
În paginile HTML, în secțiunea **<head>** indică calea către fișierul CSS extern. Ca și în cazul descărcării locale există versiunea minimizată și  versiunea necomprimată. Versiunea minimizată ocupă mai puțin spațiu, dar este mai puțin lizibilă. Versiunea necomprimată e mai ușor de citit, dar ocupă mai mult spațiu.
  
De obicei, includem în pagini versiunea minimizată. Versiunea necomprimată poate fi utilizată atunci când e nevoie de modificat sau analizat stilurile folosite de framework.

**Versiunea minimizată**
```html
<head>            
   <link rel="stylesheet" type="text/css" href="https://cdnjs.cloudflare.com/ajax/libs/milligram/1.3.0/milligram.min.css">
</head>
``` 
**Versiunea necomprimată**
```html
<head>
    <link rel="stylesheet" type="text/css" href="https://cdnjs.cloudflare.com/ajax/libs/milligram/1.3.0/milligram.css">
</head>
```
Felicitări! Acum toate elementele HTML din paginile unde ai adăugat link-ul către fișierul CSS vor fi stilizate de Milligram.

## Generalități

Milligram stilizează tag-urile standarte HTML și pune la dispoziție mai multe clase pentru a customiza elementele. Mai jos sunt prezentate exemple de cod și ce se generează în pagină.

### Heading

Cu ajutorul heading-ului putem adăuga rubrici. De menționat, că în imaginea cu ceea ce se generează, lângă **pixeli**, este indicată și valoarea în **rem**. **Rem** e o prescurtare de la “*root em”*. Aceasta e o valoare relativă față de mărimea indicată prin ```font-size``` tag-ului ```<html>```. În Milligram, pentru conveniență **1 rem = 10px**.

![heading image](https://d2mxuefqeaa7sj.cloudfront.net/s_B462AB980EA85B737E04B441011D535E772BEFD41FC10791E4447313B73E06A5_1500541758693_heading.png)

```html
<h1>Heading</h1>
<h2>Heading</h2>
<h3>Heading</h3>
<h4>Heading</h4>
<h5>Heading</h5>
<h6>Heading</h6>
```

## Citate

Citatele pot fi adăugate cu ajutorul tag-ului ```<blockquote>```

![blockquote image](https://d2mxuefqeaa7sj.cloudfront.net/s_B462AB980EA85B737E04B441011D535E772BEFD41FC10791E4447313B73E06A5_1500542085031_blockquote.png)

```html
<blockquote>
    <p><em>Milligram e cool!</em></p>
</blockquote>
```

## Butoane

Butoanele sunt parte esențială a experienței unui utilizator. [**Milligram**](http://milligram.io/) poate stiliza butoanele în 3 feluri cu ajutorul claselor ```.button```, ```.button-outline``` și ```.button-clear``` . Aceste clase pot fi aplicate oricărui din tag-urile ```<button>```, ```<input>``` sau ```<a>``` . Mai jos sunt câteva exemple. 

![buttons image](https://d2mxuefqeaa7sj.cloudfront.net/s_B462AB980EA85B737E04B441011D535E772BEFD41FC10791E4447313B73E06A5_1500541670294_buttons2.png)

```html
<!-- Buton implicit -->
<a class="button" href="#">Button Implicit</a>

<!-- Buton cu contur-->
<button class="button button-outline">Buton cu contur</button>

<!-- Buton fara contur -->
<input class="button button-clear" type="submit" value="Button fara contur">
```

## Liste

Listele sunt o metodă versatilă și comodă pentru afișarea elementelor. Listele neordonate ```<ul>``` sunt marcate cu cercuri, cele ordonate ```<ol>``` cu numere, iar cele descriptive ```<dl>``` cu spații. Mai jos sunt câteva exemple.

![lists image](https://d2mxuefqeaa7sj.cloudfront.net/s_B462AB980EA85B737E04B441011D535E772BEFD41FC10791E4447313B73E06A5_1500543628540_liste.png)

```html
<!-- Listă neordonată -->
<ul>
    <li>Element neordonat 1</li>
    <li>Element neordonat 2</li>
</ul>

<!-- Listă ordonată -->
<ol>
    <li>Element ordonat 1</li>
    <li>Element ordonat 2</li>
</ol>

<!-- Listă descriptivă -->
<dl>
    <dt>Element descriptiv 1</dt>
    <dd>Element descriptiv 1.1</dd>
</dl>
```

## Tabele

Tabelele sunt o formă convenabilă de reprezentare a datelor cu ajutorul rândurilor și coloanelor. Atunci când se crează un ```<table>``` se recomandă utilizarea tag-urilor ```<thead>``` și ```<tbody>```. 

```<thead>``` e o prescurtare de la *“table head”* și indică antetul tabelului. 

```<tbody>``` e o prescurtare de la *“table body”* și indică corpul tabelului.

Mai jos e demonstrată utilizarea acestor tag-uri.

![table image](https://d2mxuefqeaa7sj.cloudfront.net/s_B462AB980EA85B737E04B441011D535E772BEFD41FC10791E4447313B73E06A5_1500544636350_table.png)

```html
<table>
 <thead>
     <tr>
         <th>Numele</th>
         <th>Vârsta</th>
         <th>Înălțimea</th>
         <th>Localitatea</th>
     </tr>
 </thead>
 <tbody>
     <tr>
         <td>Andrei Barbu</td>
         <td>27</td>
         <td>1,85</td>
         <td>Țânțăreni, Anenii Noi</td>
     </tr>
     <tr>
         <td>Alina Bujor</td>
         <td>25</td>
         <td>1,80</td>
         <td>Inculeț, Orhei</td>
     </tr>
 </tbody>
</table>
```

## Grid

Grid-ul este un sistem fluid cu o lățime maximă de `112.0rem` (1120px), care se repoziționează în dependență de browser/dispozitiv. De menționat, că lățimea maximă poate fi modificată. Această modificare va schimba și lățimea coloanelor constituente ale grid-ului.

Un sistem de grid poate fi creat cu ajutorul claselor ```.container```, ```.row``` și ```.column```  

```.container``` este un ambalaj (wrapper) care conține ```.row``` și ```.column``` 
Asemănător cu ```.table``` atunci când creăm un tabel. Acestă clasă centrează conținutul.

```.row``` stabilește un rând nou și conține ```.column```

```.column``` stabilește o coloană nouă.

Față de alte framework-uri, în Milligram pot fi adăugate orice număr de coloane, totuși se recomandă să se urmeze practicile standarte a unui sistem de grid. 

![grid image](https://d2mxuefqeaa7sj.cloudfront.net/s_B462AB980EA85B737E04B441011D535E772BEFD41FC10791E4447313B73E06A5_1500548096634_grid.png)

```html
<!-- .container este clasa ambalaj (wrapper) de bază care centrează conținutul -->
<div class="container">
  <div class="row">
    <div class="column">.column</div>
    <div class="column">.column</div>
    <div class="column">.column</div>
    <div class="column">.column</div>
</div>

<div class="row">
    <div class="column"><span class="column-demo">.column</span></div>
    <div class="column column-50 column-offset-25">.column column-50 
    column-offset-25</div>
</div>

</div>

<!-- Orice .column adăugat într-un .row va ocupa un spațiu egal ca și celelalte coloane. -->
```
