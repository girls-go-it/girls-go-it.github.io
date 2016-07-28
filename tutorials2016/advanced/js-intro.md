---
layout: default
title: Intro to Javascript
<!--category: advanced-->
---

# Hello Javascript!

Stiati voi oare ca aveti un puterea unui limbaj de programare in aplicatia folosita zi de zi - browserul vostru? 

Acest limbaj se numeste `javascript`. Haideti sa incercam sa vedem cum il putem dresa sa ne asculte!


## Experiments

Cel mai simplu mod sa incepeti sa experimentati cu `javascript` este sa deschideti consola browserului vostru si sa incepeti a scrie direct acolo.
In Firefox sau Chrome, pentru a porni consola, tastati in orice pagina `F12`, si treceti la tab'ul `Console` in fereastra magica deschisa.

Chrome:
![Chrome console](/images/js-intro/chrome-dev.png)

Firefox:
![Firefox console](/images/js-intro/firefox-dev.png)
In firefox instructiunile javascript le puteti scrie jos.

Sa testam cateva operatii matematice. Scrieti urmatoarea linie in consola si tastati [Enter]:

```javascript
(16 + 21*4) / 2 - 8
```

Obtinem raspunsul la univers si tot absolut:
![Console run](/images/js-intro/console-run.png)

Desigur putem folosi consola din browser si javascript ca un calculator in continuare, dar... e totusi un limbaj intreg, poate mult mai multe!

## Variabile

Javascript e un limbaj de programare. Orice limbaj de programare are notiunea de variabila.
Variabila este ceva ce poate sa se schimbe, e variabila :). Ii setati o valoare, apoi puteti sa-i setati alta, daca vreti. Puteti sa cititi valoarea ei accesandu-i numele, puteti s-o transmiteti ca parametru la functii, etc.
Variabila e elementul cheie a oricarui limbaj de programare, in Pascal la fel aveti variabile, si au fix acelasi rol.

Pentru a defini o variabila, cu valoarea 10, puteti scrie asa:

```javascript
var number = 10;
```

Aici am declarat variabila `number` cu valoarea `10`. Observati ca nu am zis de ce tip e `number` - Javascript e un limbaj dinamic, el incearca sa inteleaga automat de ce tip sunt variabilelel, in cazul dat - un numar.

Putem folosi aceasta variabila in alte declaratii:

```javascript
var otherNumber = number + 5;
```
Desigur `otherNumber` va avea valoarea 15.

Pentru a defini un sir de caractere doar punem in jurul textului ghilimele simple sau duble:

```javascript
var h = "Hello "
var w = 'World!'
console.log(h + w)
```
Observati ca nu am pus `;` la sfasitul instructiunilor de data asta, in javascript `;` la sfarsit sunt optionale, limbajul le cere doar in cazuri rare cand nu poate deduce singur cand se termina o instructiune si se incepe alta.
`console.log()` e functie ce afiseaza la consola, in cazul dat ea va afisa `Hello World!`.