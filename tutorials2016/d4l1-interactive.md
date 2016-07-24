---
layout: default
title: Interactive Pages
category: basic
---

# Interactive Web Pages

## Ce reprezintă pseudo-clasele în CSS?

Pseudo-clasele sunt utilizate pentru a defini o stare specială a unui element HTML. Spre exemplu, ele pot fi utilizate pentru:

 - a stiliza un element atunci cînd mouse-ul este deasupra
 - a stiliza link-urile accesate și neaccesate diferit
 - a stiliza un element atunci cînd deține focus-ul

## Syntax
Sintaxa pentru a utiliza pseudo-clasele în CSS este:

```css
selector:pseudo-class {
    property:value;
}
```

## Pseudo-clase pentru link-uri
Link-urile pot fi afișate în diferite moduri:

```css
/* unvisited link */
a:link {
    color: #FF0000;
}
/* visited link */
a:visited {
    color: #00FF00;
}
/* mouse over link */
a:hover {
    color: #FF00FF;
}
/* selected link */
a:active {
    color: #0000FF;
}
```

>`a:hover` trebuie să fie definită după `a:link` și `a:visited` pentru a avea efect, totodată, `a:active` trebuie să fie definită după `a:hover`.

Pentru demo click **[aici](https://jsfiddle.net/dfpno9ta/)**

## Pseudo-clasele pot fi folosite împreună cu clasele CSS
Pseudo-clasele pot fi combinate cu clasese definite de tine.

```css
a.my-class:pseudo-class {
    property:value;
}
```

## Hover asupra unui `<div>`
Iată un exemplu de a utiliza pseudo-clasa `:hover` asupta unui element `div`.

```css
div:hover {
    background-color: red;
}
```

Pentru demo click **[aici](https://jsfiddle.net/xbn8rbd2/)**

## Pseudo-clasa `:first-child`
Pseudo-clasa `:first-child` se utilizează pentru a selecta primul element copil al fiecărui element.

```css
/*match the first <p> element*/
p:first-child {
    color: blue;
}
/*match the first <i> element in all <p> elements*/
p i:first-child {
    color: blue;
}
```

Pentru demo click **[aici](https://jsfiddle.net/7byabsx2/)**

## Pseudo-clasa `:nth-child(n)`
Această pseudo-clasa se utilizează pentru a selecta fiecare element care este copilul n-lea al elementului părinte. `n` poate fi valoare, cuvînt cheie, funcție.

```css
/*select every <p> element that is the second child of its parent*/
p:nth-child(2) {
    background: red;
}
/*select odd and even p elements*/
p:nth-child(odd) {
    background: red;
}
p:nth-child(even) {
    background: blue;
}
```

Pentru demo click **[aici](https://jsfiddle.net/kkr0vu9r/)**

# Tranzițtii CSS
Tranzițiile CSS oferă programatorului un mod de a controla viteza de animare atunci cînd sunt schimbate proprietățile CSS ale elementelor HTML.
Pentru a utiliza tranzițiile, este nevoie de a specifica două lucruri:

 - proprietatea CSS la care dorești să aplici efectul
 - durata efectului

> Dacă durata efectului nu va fi specificată, atunci tranziția nu se va aplica deoarece valoarea implicită pentru dutară este 0.

## Exemplu
În exemplul de mai jos, putem observa că atunci cînd cursorul va fi peste un element `div`, se va modifica lungimea lui cu o durată de 2 secunde.

```css
div {
    width: 100px;
    height: 100px;
    background: red;
    transition: width 2s;
}
div:hover {
    width: 300px;
}
```

Pentru demo click **[aici](https://jsfiddle.net/yvknekh9/)**

## Tranziții cu întîrziere
Exemplul de mai jos demonstrează cum de utilizat proprietatea `transition-delay`.

```css
div {
    width: 100px;
    height: 100px;
    background: red;
    transition: width 3s;
    transition-delay: 1s;
}

div:hover {
    width: 300px;
}
```

Pentru demo click **[aici](https://jsfiddle.net/7z3ww5fj/)**

## Tranziții + Transformări

```css
div {
    width: 100px;
    height: 100px;
    background: red;
    transition: width 2s, height 2s, transform 2s;
}

div:hover {
    width: 300px;
    height: 300px;
    transform: rotate(180deg);
}
```

Pentru demo click **[aici](https://jsfiddle.net/smqurzas/)**

## **BONUS:** Blur Menu
Pentru că sunt foarte multe lucruri care pot fi efectuate cu tranzițiile și transformările în CSS, o să experimentăm cu scopul de a realiza un efect de blur asupra unei bare de meniu.

```css
body{
  background-image:
    url("http://tympanus.net/Tutorials/BlurMenu/images/pattern.png"),
    url("http://tympanus.net/Tutorials/BlurMenu/images/1.jpg");
}
.bmenu{
    padding: 0px;
    margin: 0 0 10px 0;
    position: relative;
}
.bmenu li{
    color: black;
    font-size: 50px;
    display: block;
}
.bmenu li a{
	color: transparent;
	display: block;
	text-transform: uppercase;
	text-shadow: 0px 0px 5px #fff;
	letter-spacing: 1px;
	-webkit-transition: all 0.3s ease-in-out;
	-moz-transition: all 0.3s ease-in-out;
	-o-transition: all 0.3s ease-in-out;
	-ms-transition: all 0.3s ease-in-out;
	transition: all 0.3s ease-in-out;
}
.bmenu:hover li a{
	text-shadow: 0px 0px 5px #0d1a3a;
}
.bmenu li a:hover{
	color: #fff;
	text-shadow: 0px 0px 1px #fff;
	padding-left: 10px;
}
```

Elementele HTML:

```html
<ul class="bmenu">
  <li><a href="#">About</a></li>
  <li><a href="#">Illustrations</a></li>
  <li><a href="#">Photography</a></li>
  <li><a href="#">Web Design</a></li>
  <li><a href="#">Personal Projects</a></li>
  <li><a href="#">Contact</a></li>
</ul>
```

Pentru demo click **[aici](https://jsfiddle.net/28d7yvdx/)**
