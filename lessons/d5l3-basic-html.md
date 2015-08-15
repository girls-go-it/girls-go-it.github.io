---
layout: default
title: Basic HTML&CSS
---

#Basic HTML

##Ce este HTML?


Html sau HyperText Markup Language este unul dintre cele mai vechi limbaje de marcare web. Un limbaj de marcare (în engleză: markup language) este o metodă de formatare a unui text de pe o pagină web, care combină textul cu informațiile suplimentare despre acel text.

Aici vei învăța cum să creezi propria pagină html. Pentru început trebuie doar să deschizi terminalul în directoriul proiectului, in folderul `static`. Scrie în terminal următorul rând:

```bash
$ subl index.html
```

În sublime, scrie următorul cod:

```HTML	
<!DOCTYPE html>
<html>
<head>
	<title></title>
</head>
<body>

</body>
</html>
```

Salvează modificările făcute în documentul index.html. Dezchizând din nou terminalul, scrie:

```bash
$ sensible-browser index.html
```

Ceea ce ai în față este o pagină HTML goală. Observi că numele paginii corespunde cu numele documentului  cu extensia .html pe care l-ai creat anterior. Pentru a schimba denumirea paginii, tot ce trebuie să faci este să scrii titlul pe care-l dorești între tag-urile `<title></title>.`
Spre exemplu: 


```html
<title>My page</title>
```

Salvează modificările făcute în documentul index.html. Apoi poți vedea că titlul s-a schimbat scriind din nou în terminal comanda:


```bash
$ sensible-browser index.html
```

<div class="custom-image"><img src="https://40.media.tumblr.com/f24c47044eb096aa26d351646ae7e47c/tumblr_nt175dbOWZ1udztn8o1_1280.png" /></div>


Începem totorialul de învățare cu clasicul : ”Hello, world!”. Pentru asta, scrie textul: “Hello, world!” între taguri, precum în exemplu

```html
<body>Hello, world!</body>
```

Mergi în browser și fă refresh la pagină, apăsând F5.

<div class="custom-image"><img src="https://40.media.tumblr.com/608939367baa09e1eff7587c72bf58f3/tumblr_nt16zrdU6x1udztn8o1_1280.png" /></div>


Următorul pas este învățarea paragrafelor. Pentru a scrie un paragraf, deschide sublime-ul și scrie orice secțiune de text care-ți trece prin mine, încadrată între tagurile `<p></p>`, precum în exemplul de mai jos:

```html
<p style="color:blue; font-size: 24px; text-align: center">Savannah is the most beautiful place.</p>
```

Stilizează ace paragraf, dăndu-i proprietățile: 

```html
<p style="color:blue; font-size: 24px; text-align: center">
```

<div class="custom-image"><img src="https://41.media.tumblr.com/eb521c67b6c25039afbfc7b3ea11d5f2/tumblr_nt4t86jlRq1udztn8o2_1280.png" /></div>


Fiindcă deja cunoști cum se face un paragraf, este exact timpul să înveți cum se scriu așa numitele titluri, sau ”headings”. Pentru a scrie un heading, trebuie să incluzi între taguri denumirea acestuia. Reține, tagurile pentru heading încep de la 1 până la 6, iar dimensiunea este descrescătoare odată cu mărirea numărului de pe lângă h. Deci, pentru a vedea diferența, scrie următoarele rânduri în fișirul .html:

```html
    <p style="color:blue; font-size: 24px; text-align: center">Savannah animals I like:</p> -->
    <h1 style="color: #696969; font-family: Ubuntu">Lions</h1>
    <h2 style="color: #500000 ; font-family: Ubuntu">Cheetah</h2>
    <h3 style="color: #00CC33; font-family: Ubuntu">Leopards</h3>
    <h4 style="color: #00FFFF; font-family: Ubuntu">Elefhants</h4>
    <h5 style="color: #6633CC; font-family: Ubuntu">Giraffe</h5>
    <h6 style="color: #696969; font-family: Ubuntu">Zebra</h6>
```

Observi că fiecărui heading i s-a atribuit proprietăți de culoare și family-font. Poți să le schimbi după propriul plac.

<div class="custom-image"><img src="https://36.media.tumblr.com/47b3e53e129ccc817da46176c9aeef3f/tumblr_nt4t86jlRq1udztn8o1_1280.png" /></div>

Un alt truc pe care-l poți face în HTML, este să creezi liste atât ordonate, neordonate cât și definiție.

Liste ordonate sunt extrem de simple. Un exemplu îl ai chiar în față:

```html
<p>Savannah animals I like:</p> 
<ol style="font-family: Sans-serif;  color: #993333">
    <li>Lions</li>
    <li>Elefants</li>
    <li>Zebra</li>
</ol>
```

Stilizează această listă cu proprietățile:   style="font-family: Sans-serif;  color: #993333".

<div class="custom-image"><img src="https://36.media.tumblr.com/614374edfb15d1b0e858336506609c38/tumblr_nt4ssnu7em1udztn8o5_1280.png" /></div>

Drept provocare, te las să încerci și listele neordonate, prin înlocuirea tagurilor `<ol></ol>` cu `<ul></ul>`. 

Dacă curiozitatea este atributul tău principal, atunci poți să încerci și listele de definiție.

```html
    <p style="color:blue; font-size: 24px; text-align: center">Savannah animals I like:</p> 
    <dl>
        <dt>Lions :</dt>
        <dd>Rapid</dd>
        <dd>Strong</dd>
        <dt>Elefants</dt>
        <dd>Gray</dd>
    </dl>
```
<div class="custom-image"><img src="https://40.media.tumblr.com/7fc1ad894f396afdfbbaf305c66bf620/tumblr_nt4ssnu7em1udztn8o6_1280.png" /></div>

Element important îl mai reprezintă și tabele. Tabele se definesc prin intermediul tag-ului `<table>`. Tabele se împart în rânduri prin intermediul tag-urilor `<tr>`. Rândurile se împart în datele tabelului, cu ajutorul tagului `<td>`. Rândul unui tabel poate fi, la fel, divizat în titluri ale tabelului, utilizând tag-ul `<th>`. Pentru a face lucrurile mai clare, analizează codul de mai jos: 

```html
<table>
	<tr>
		<th>Nume</th>
		<th>Prenume</th>
		<th>Virsta</th>
	</tr>
	<tr>
		<td>Alex</td>
		<td>Cretu</td>		
		<td>25</td>
	</tr>
	<tr>
		<td>Alexandra</td>
		<td>Cretu</td>		
		<td>24</td>
	</tr>
	<tr>
		<td>Alexandrina</td>
		<td>Cretu</td>		
		<td>18</td>
	</tr>
</table>
```

<div class="custom-image"><img src="https://41.media.tumblr.com/e92c1c50400a708d115ada579a929654/tumblr_nt17f7AVKN1udztn8o1_1280.png" /></div>

Acum că ai însușit paragrafele, titlurile (header), tabelele și listele, poți să faci loc și link-urilor. În HTML link-urile sunt definite prin intermediul tag-ului `<a>` sub forma: `<a href="url">link text</a>`.

Exemplu:

```html
<a href="http://girls-go-it.github.io/lessons/aaa_vocabulary/">Vocabular tehnic</a>
```

Mai mult decât atât, dacă vrei să adaugi o imagine pe pagina ta, poți să utilizezi: 

```html
<img src="url " alt="Textul in cazul neaparitiei imaginii"/>
```

Exemplu:

```html
<img src="http://www.backdropsfantastic.com/backdrop_images/300's/OA-004-African-Savannah-4.jpg" alt="Formatul imaginii este necorespunzător"/>
```

Un pas la fel de simplu și interactiv este învățarea și aplicarea în practică a id-urilor și claselor. 
Un id este folosit pentru a identifica un singur tag dintr-o pagină. Acesta poate fi asemănat cu IDNP-ul unei persone, este unic. Cum arată un id definit?


```html
<div id="id-name">This is an id</div>
```

Clasa reprezintă un grup de taguri care au același stil. Avantajul, eficiența claselor constă în faptul că pot fi folosite la mai multe taguri html. Prin asta se înțelege că poate fi folosit  același stil pentru mai multe paragrafe, heading-uri etc. Singura diferență între definirea și folosirea claselor față de id-uri este că, în loc de # la definire, în css, folosim un “.”(punct), iar în interiorul tagului html în loc de id, scriem class. 

```html
<div class="class-name">This is a class.</div>
```

Înțelegerea claselor și a id-urilor pare destul de cețoasă. De aceea, aici se face un nou pas – introducerea CSS-ului. Ce reprezintă? CSS este acronimul pentru Cascading Style Sheets. CSS este un limbaj (style language) care definește "layout-ul" pentru documentele HTML. Acesta acoperă culori, font-uri, margini (borders), linii, înălțime, lățime, imagini de fundal, poziții avansate și multe alte opțiuni. În câteva cuvinte, CSS te ajută să stilizezi pagina după propriul plac.

Deschide terminalul și, în directoriul proiectului, în folderul static, creează un fișier cu extensia .css:

```bash
$ subl layout.css
```

Înainte de a scrie ceva în fișierul cu extensia .css, întoarce-te la fișierul .html. Pentru a include layout.css în index.html, în head-ul fișierului din urmă scrie: 

```html
<link rel="stylesheet" type="text/css" href="layout.css">
```

Următorul pas este crearea unui id și a unei clase. Pentru asta, ghidează-te după exemplul ce urmează:

```html
<div id="id-name">
	Statement number 1<br/>
	Statement number 2<br/>
	Statement number 3
</div>

```

<div class="custom-image"><img src="https://41.media.tumblr.com/7467ee203f42d312c89937970b9f130a/tumblr_nt1867Qx7k1udztn8o1_1280.png" /></div>

Tagul `<br/>` este pentru a trece în linie nouă.
Acum, în fișierul layout.css stilizează acest id după propriu plac. Pentru a stiliza un id, folosește #id-name înaintea acoladelor cu conținutul care stilizează:

```css
#id-name {
}
```

În interior poți deja să scrii și să stilizezi diferite proprietăți. Un exemplu ar fi:

```css
#id-name { 
	margin: 40px; 
	background-color: #ABC; 
	border-width: 10px;
	border-style: solid;
	border-color: #006;
	overflow: hidden;
}
```

<div class="custom-image"><img src="https://40.media.tumblr.com/dc1245c8e054cdd10b07d85766a30eeb/tumblr_nt16oyX6wh1udztn8o1_1280.png" /></div>

Există mult mai multe trucuri pe care le poți folosi și la care vei reveni ulterior. 

După ce ai înțeles cum să definești un id, continuă să studiezi clasele. O clasă se definește asemeni id-ului, cum a fost specificat mai sus. Deci, poți să exersezi în a învăța clasele, exact ca în model: 

```html
<div id="id-name"> 
	<div class="class-name"> Statement number 1</div> 
	<div class="class-name"> Statement number 2</div> 
	<div class="class-name"> Statement number 3</div> 
</div>
```

După cum îți spuneam, poți să stilizezi mai multe elemente, incluzându-le în aceeași clasă. 
În fișierul html stilizează clasa. Reține, clasa, în CSS se scrie cu ajutorul selectorului ”.” .
Poți utiliza exemplul de mai jos.

```css
.class-name{ 
	width: 100px; 
	height: 100px; 
	border-width:2px;
	border-style: solid;
	border-color: red; 
	margin: 20px; 
	float: left; 
}
```

<div class="custom-image"><img src="https://40.media.tumblr.com/bfd1448af43e9ec7cf59fa389a782d0b/tumblr_nt16skLDhT1udztn8o1_1280.png" /></div>

Aceleași proprietăți ale clasei pot fi aplicate și daca avem un al id. Drept provocare, creeaza un alt id, cu alte proprietati include in interior elemente din clasa creata anterior. Exemplu: 

```html
<div id="id-name-second"> 
	<div class="class-name"> Statement number 1.</div> 
	<div class="class-name"> Statement number 2</div> 
	<div class="class-name"> Statement number 3.</div> 
</div>
```

În fișierul layout.css, include:

```css
#id-name-second { 
	margin: 40px; 
	background-color: blue; 
	border-width: 10px;
	border-style: solid;
	border-color: #006;
	overflow: hidden;
} 
```

<div class="custom-image"><img src="https://40.media.tumblr.com/52f8c9d99c5249ce122a14e86f224392/tumblr_nt180hpumI1udztn8o1_1280.png" /></div>

Acum că știi cum se lucrează cu un id, cu o clasă, fii liber să încerci orice alte trucuri. Iată câteva trucuri simple, care-ți sunt recomandate:

- `color` – setează culoarea textului

- `background-color` – specifică culoarea fundalului

- `background-image` – indică imaginea de fundal a unui element

- `background-size` – specifică dimensiunea imaginii de fundal

- `border` – setează proprietatile marginilor/frontierelor unui element

- `border-color` –setează culoarea marginii

- `border-radius` – setează curbura colțurilor unei casete

- `border-width` - setează dimensiunea tuturor marginilor

- `border-style` - setează stilul marginilor(none, hidde, dotted, dashed, solid, double, groove, ridge, inset, outset, initial, inherit)

- `box-shadow` - atașează una sau mai multe umbre la un element.

- `position` – specifică metoda poziționării unui element  (static, absolute, relative sau fixed)

- `font-family` – specifică familia textului

- `font-size` – specifică mărimea textului

- `font-style` – specifică stilul textului

- `margin` - setează proprietățile tutulor marginilor

- `max-width` - setează dimensiunea maximă a unui element

- `overflow` - specifică proprietatea pe care o ia elementul în caz că se conțin alte elemente

- `text-align` - specifică aranjarea, pe orizontală, a textului

Selectori css:

`.class-name` - selectează elementul class, cu denumirea **class-name**

`css#id-name` - selectează elementele având valoarea id-ului ***id-name***

`p` - selectează toate elementele `<p>`

`div, p` - selectează toate elementele `<div>` și elementele `<p>`

`div p` - selectează toate elementele `<p>` care se află în interiorul elementelor `<div>`

Mai multe proprietăți poți găsi la (http://www.w3schools.com/cssref/) .

Exercițiu:
Aici vei simula prima ta pagină web. Urmează instrucțiunile.

Într-un directoriu aparte creează fișierul index.html și fișierul main.css. Nu uita să le relaționezi.

```html
<!DOCTYPE html>
<html>
<head>
	<title></title>
	<link rel="stylesheet" type="text/css" href="main.css">
</head>
<body>

</body>
</html>
```

Pune un titlu paginii, spre exemplu: "My Page".

```html
<title>My Page</title>
```

Creează o clasă cu numele ”class-name” și include în interiorul acesteia un header cu cea mai mare dimensiune(h1).

```html
<div class="class-name">
	<h1>This is my first web page</h1>
</div>
```

Stilizează această clasă în main.css, dându-i proprietățile: 

```css
.class-name {
	text-align: center;
	margin: 50px;
	height: 890px;
	background-color: #F8F8FF;
	font-family: Ubuntu;
}
```

Stilizează și heading-ul:

```css
h1 {
	color: #696969;
	font-family: Ubuntu;
	font-size: 48px;
}
```
În ”class-name” include o listă neordonată ce conține o clasă cu valoarea class=”navigation-bar”. Elementele listei vor fi ”page1”, ”page2” și ”page3”. Codul tău, la moment, trebuie să arate așa:

```html
<!DOCTYPE html>
<html>
<head>
	<title>My page</title>
	<link rel="stylesheet" type="text/css" href="main.css">
</head>
<body>
	<div class="class-name">
		<h1>This is my first web page</h1>
		<hr>
		<ul class="navigation-bar">
			<li>page1</li>
			<li>page2</li>
			<li>page3</li>
		</ul>
	</div>
</body>
</html>
```

Stilizează elementele listei neordonale, în fișierul main.css, dându-i proprietățile:

```css
ul li {
	display: inline-block;
	padding-left: 20px;
}
```

Desenează o nouă linie orizontală, după care, îndată după tagul `<hr>`, include un id cu valoarea id=”cover-photo”, în interiorul căruia vei introduce o imagine.

```html
<hr>
<div id="cover-photo">
	<img src="http://hdwallpapers.cat/wallpaper/zebras_on_savannah_sunlight_grassland_tree_hd-wallpaper-1249130.jpg">
</div>
```

Pentru a aranja imaginea frumos stilizeaz-o fișierul main.css:

```css
img {
	max-width: 100%;
}
```
Daca vreai ca liniile orizonatale să arate și ele mai ”fancy”, poți să le stilizezi și pe ele. Fie analizezi exemplul de mai jos, fie googluiești și găsești o soluție mai bună.

```css
hr {
	height: 12px;
    border: 0;
    box-shadow: inset 0 12px 12px -12px rgba(0, 0, 0, 0.5);
}
```
În final, pagina ta ar trebui să arate exact ca în imagine.

<div class="custom-image"><img src="https://41.media.tumblr.com/34e5ba5eb2e18557c228dd5952a811a5/tumblr_nt13kv48mD1udztn8o1_1280.jpg" /></div>
