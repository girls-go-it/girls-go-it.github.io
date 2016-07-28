---
layout: default
title: Intro to Javascript
<!--category: advanced-->
---

# Hello Javascript!

Stiati voi oare ca aveti un puterea unui limbaj de programare in aplicatia folosita zi de zi - browserul vostru? 

Acest limbaj se numeste `javascript`. Haideti sa incercam sa vedem cum il putem dresa sa ne asculte!

[TOC]: # Teme adresate:

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
<br>Functia `console.log()` afiseaza ceva la consola, in cazul dat ea va afisa `Hello World!`.

Variabilele de tip boolean (de logica) se definesc la fel de simplu:

```javascript
var test = true
test = !test            // operatia NOT (negare)
test = test || true     // operatia OR  (sau)
test = test && false    // operatia AND (si)

console.log(test == true)   // testam pentru egalitate
console.log(test != true)   // testam pentru inegalitate
```

## IF (Conditionale)

In javascript putem pune o conditie, care ne va permite sa executam diferite actiuni in dependenta daca conditia asta se adevereste sau nu:

```javascript
var a = 10
if (a < 20) {
    console.log(a + ' e mai mic ca 20')
}
```

> Hint: cand apasati [Enter] consola, Chrome incearca sa execute instructiunea, si daca ea nu-i finisata, da eroare. 
Ca sa scrieti o instructiune pe mai multe randuri, tastati [Shift + Enter]

Observati ca e construit din cuvantul cheie `if`, intre `(...)` se pune conditia care o verificam, 
dupa care intre `{ ... }` scriem instructiunile care sa se execute in caz ca conditia intre `(...)` e adevarata
`

Putem adauga `else` la conditia `if` pentru a specifica instructiuni care sa se execute in caz daca conditia nu e adevarata:

```javascript 
var b = 25
if (b < 20) {
    console.log(b + ' e mai mic ca 20')            // se executa daca b < 20
} else {
    console.log(b + ' e mai mare sau egal cu 20')  // se executa daca !(b < 20), adica b >=20
}
```

Instructiunea `else if` ne permite sa adaugam o noua conditie in caz ca conditia `if` nu e adevarata:

```javascript
var c = 30
if (c < 30) {
    console.log(c + ' e mai mic ca 30')   // se executa daca c < 30
} else if (c > 30) {
    console.log(c + ' e mai mare ca 30')  // se executa daca c > 30
} else {
    console.log(c + ' este egal cu 30')   // se executa daca c == 30
}
```

## Switch

Instructiunea `switch` ne permite sa executam unul din mai multe blocuri in dependenta de conditie:

```javascript

```
