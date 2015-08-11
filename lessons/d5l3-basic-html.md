---
layout: default
title: Basic HTML and CSS
---

#Basic HTML

##Ce este HTML?


Html sau HyperText Markup Language este unul dintre cele mai vechi limbaje de marcare web. Un limbaj de marcare (în engleză: markup language) este o metodă de formatare a unui text de pe o pagină web, care combină textul cu informațiile suplimentare despre acel text.

Aici vei învăța cum să creezi propria pagină html. Pentru început trebuie doar să deschizi terminalul în directoria proiectului. Scrie în terminal următorul rând:

```bash
	subl index.html
```

<p>    În sublime, scrie următorul cod:</p>


```	<!DOCTYPE html>
	<html>
	<head>
		<title></title>
	</head>
	<body>

	</body>
	</html>
```

Salvează modificările făcute în documentul index.html. Dezchizând din nou terminalul, scrie:

```
sensible-browser index.html
```

Ceea ce ai în față este o pagină HTML goală. Observi că numele paginii corespunde cu numele documentului  cu extensia .html pe care l-ai creat anterior. Pentru a schimba denumirea paginii, tot ce trebuie să faci este să scrii titlul pe care-l dorești între tag-urile ```<title></title>.```
Spre exemplu: 


```html
<title>Pagina mea</title>
```
Salvează modificările făcute în documentul index.html. Apoi poți vedea că titlul s-a schimbat scriind din nou în terminal comanda:</p>


```html
sensible-browser index.html
```
<div class="custom-image"><img src="https://40.media.tumblr.com/fba61613287c284b5f58579395b34b3a/tumblr_nswmvmhWVH1udztn8o10_540.jpg" /></div>


Începem totorialul de învățare cu clasicul : ”Hello, world!”. Pentru asta, scrie între tagurile 
```html
	<body> </body>
```
textul: “Hello, world!”. Mergi în browser și fă refresh la pagină, apăsând F5.

<div class="custom-image"><img src="https://40.media.tumblr.com/fe7658f88c2817ab5b7a3fc3eefaa7eb/tumblr_nswmvmhWVH1udztn8o4_540.jpg" /></div>

<br>
<br>
<p>
Următorul pas este învățarea paragrafelor. Pentru a scrie un paragraf, mergi în sublime și scrie orice secțiune de text care-ți trece prin mine, încadrată între tagurile 
```html
		<p></p>
```
<p>precum în exemplul de mai jos:</p>

```html
<p>Vulpile sunt cele mai frumoase animale.</p>
```

<div class="custom-image"><img src="https://41.media.tumblr.com/848b15514e78182321c1a98a0b715f12/tumblr_nswmvmhWVH1udztn8o8_540.jpg" /></div>

<p>
	Fiindcă deja cunoști cum se face un paragraf, este exact timpul potrivit să înveți cum se scriu așa numitele titluri, sau ”headings”. Pentru a scrie un heading, trebuie să incluzi între taguri denumirea acestuia. Reține, tagurile pentru heading încep de la 1 până la 6, iar dimensiunea este descrescătoare odată cu mărirea numărului de pe lângă h. Deci, pentru a vedea diferența, scrie următoarele rânduri în fișirul .html:
</p>

```
	<h1>Acesta este titlul cu dimensiunea 1.</h1>
	<h2>Acesta este titlul cu dimensiunea 2.</h2>
	<h3>Acesta este titlul cu dimensiunea 3.</h3>
	<h4>Acesta este titlul cu dimensiunea 4.</h4>
	<h5>Acesta este titlul cu dimensiunea 5.</h5>
	<h6>Acesta este titlul cu dimensiunea 6.</h6>
```
<div class="custom-image"><img src="https://41.media.tumblr.com/b34f48e4dc817447e64763b7afc125bb/tumblr_nswmvmhWVH1udztn8o3_540.jpg" /></div>

<p>
	Poți la fel de bine să icluzi și câteva paragrafe, după titlul pe care l-ai scris. Drept exemplu îți servește porțiunea de cod scrisă mai jos:
</p>

```html
<h1>Vulpile.</h1>
	<p>Vulpile sunt cele mai frumoase creaturi.</p>
	<p>Vulpile sunt cele mai frumoase creaturi.</p>
<h2>Lupii</h2>
	<p>Vulpile oricum sunt cele mai frumoase creaturi.</p>
```
<p>
	Un alt truc pe care-l poți face în HTML, este să creezi liste atât ordonate cât și neordonate, sau de definiție.
	
	Liste ordonate sunt extrem de simple. Un exemplu îl ai chiar în față:
</p>

```html
	<h1>Vulpile sunt:</h1>
	<ol>
		<li>roscate</li>
		<li>frumoase</li>
		<li>sirete</li>
	</ol>
```
<div class="custom-image"><img src="https://40.media.tumblr.com/c079532c3660045ce0c1e3d72b417af2/tumblr_nswmvmhWVH1udztn8o7_540.jpg" /></div>

<p>
Drept provocare, te las să încerci și listele neordonate, prin înlocuirea tagurilor</p> 
```html
<ol></ol>
``` 
<p>cu</p> 
```html
<ul></ul>
```

<p>
	Dacă curiozitatea este atributul tău principal, atunci poți să încerci și listele de definiție.
</p>

```html
<dl>
        <dt>Vulpe</dt>
        <dd>Frumoasa</dd>
        <dt>Lup</dt>
        <dd>Curajos</dd>
</dl>
```

<p>
Element important îl mai reprezintă și tabele. Tabele se definesc prin intermediul tag-ului 
```html
<table>
```
  Tabele se împart în rânduri prin intermediul tag-urilor 
```html
  <tr>
```
 Rândurile se împart în datele tabelului, cu ajutorul tagului 
```html
<td>.
```
 Rândul unui tabel poate fi, la fel, divizat în titluri ale tabelului, utilizând tag-ul 
```html
<th>
```
Pentru a face lucrurile mai clare, analizează codul de mai jos: 
</p>

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
<br>
<div class="custom-image"><img src="https://40.media.tumblr.com/4101ae25d1490623e4a3dbf139061198/tumblr_nswmvmhWVH1udztn8o9_1280.jpg" /></div>

<p>
	Acum că ai însușit paragrafele, titlurile (header), tabelele și listele, poți să faci loc și link-urilor. În HTML link-urile sunt definite prin intermediul tag-ului</p>
	
```html
<a>
```
<p>sub forma: </p>

```html
<a href="url">link text</a>
```
<p>Exemplu:
</p>
```html
<a href="http://fanny-pictures-site.com/wp-content/uploads/2014/11/internet-meme-red-fox_1.jpg">Vulpe</a>
```
<p>
	Mai mult decât atât, dacă vrei să adaugi o imagine pe pagina ta, poți să utilizezi: 
</p>

```
<img src="url " alt="Textul in cazul neaparitiei imaginii">
```
<p>
Exemplu:
</p>

```
<img src="http://www.audreypress.com/blog/wp-content/uploads/2012/02/winterfox1.jpg" alt="Formatul imaginii este necorespunzător" />
```
<p>
	Un pas la fel de simplu și interactiv este învățarea și aplicarea în practică a id-urilor și claselor. 
<br>
	Id este folosit pentru a identifica un singur tag dintr-o pagină. Acesta poate fi asemănat cu CNP-ul unei persone, este unic. Cum arata un id definit?
</p>

```html
<div id="numeId">Acesta este un id</div>
```
Clasa reprezintă un grup de taguri care au același stil. Avantajul, eficiența claselor constă în faptul că pot fi folosite la mai multe taguri html. Prin se înțelege că poate fi folosit  același stil pentru mai multe paragrafe, heading-uri etc. Singura diferenta între definirea și folosirea claselor față de id-uri este că, în loc de # la definire, folosim un punct, ex: “.”, iar în interiorul tagului html în loc de id, scriem class=”numele-clasei”. Să presupunem, că este o nuanță a culorii roșii și am căutat odata codul hexa pentru nuanța respectivă, și vrem să folosim această culoare și in paragrafe, și în titluri “heading-uri”, etc. Tot ce trebuie să facem, este să definim o clasă pentru această culoare. Exemplu:

```html
<div class="numeClasa">Aceasta este o clasa.</div>
```
Înțelegerea claselor și a Id-urile pare destul de cețoasă. De aceea, aici se face un nou pas – introducerea CSS-ului. Ce reprezintă? CSS este acronimul pentru Cascading Style Sheets. CSS este un limbaj (style language) care definește "layout-ul" pentru documentele HTML. CSS acoperă culori, font-uri, margini (borders), linii, înălțime, lățime, imagini de fundal, poziții avansate și multe alte opțiuni. În câteva cuvinte, CSS te ajută să-ți stilizezi pagina după propriul plac.
Deschide terminalul și în directoria proiectului creează un nou fișier cu extensia .css:
```html
	subl main.css
```
Înainte de a scrie ceva în fișierul cu extensia .css, întoarce-te la fișierul .html. Pentru a include main.css în index.html, în head-ul fișierului din urmă scrie: 
```html
<link rel="stylesheet" type="text/css" href="main.css">
```
Următorul pas este crearea unui id și a unei clase. Pentru asta, ghidează-te după exemplul ce urmează:
```html
<div id="cutie">
		Cutia numarul 1.<br>
		Cutia numarul 2.<br>
		Cutia numarul 3.
	</div>
```
<div class="custom-image"><img src="https://40.media.tumblr.com/9882fc80fc19e872c0aed58002be6d46/tumblr_nsworwarJe1udztn8o1_540.jpg" /></div>

Acum, în fișierul main.css stilizează acest id după propriu plac. Pentru a stiliza un id, folosește #numeId înaintea acoladelor cu conținutul care stilizează:
```css
#cutie{
	
}
```
În interior poți deja să scrii și să stilizezi diferite proprietăți. Un exemplu ar fi:
```css
#cutie1{ 
		margin: 40px; 
		background-color: #ABC; 
		border: 10px solid #006; 
		overflow: hidden; 
}
```
<div class="custom-image"><img src="https://40.media.tumblr.com/a217a2e18e38acbe1f1d88a666986d9b/tumblr_nswmvmhWVH1udztn8o5_1280.jpg" /></div>

Există mult mai multe trucuri pe care le poți folosi și la care vei reveni ulterior. 


 După ce ai înțeles cum să definești un id, continuă să studiezi clasele. O clasă se definește asemeni id-ului, cum a fost specificat mai sus. Deci, poți să exersezi în a învăța clasele, exact ca în model: 
```html
 <div id="cutie1"> 
		<div class="cutie">Cutia numarul 1.</div> 
		<div class="cutie">Cutia numarul 2</div> 
		<div class="cutie">Cutia numarul 3.</div> 
	</div>
```
După cum îți spuneam, poți să stilizezi mai multe elemente, incluzându-le în aceeași clasă. 
În fișierul html stilizează clasa. Reține, clasa, în CSS se scrie cu ajutorul selectorului ”.” .
Poți utiliza exemplul de mai jos.
```css
.cutie{ 
	width: 100px; 
	height: 100px; 
	border:2px solid red; 
	margin: 20px; 
	float: left; 
}
```
<div class="custom-image"><img src="https://41.media.tumblr.com/40e88eecebf69cb2f723e928535d4bb0/tumblr_nswpk0FDnX1udztn8o1_540.jpg" /></div>

Aceleasi proprietati ale clasei pot fi aplicate si daca avem un al id. Drept provocare, creeaza un alt id, cu alte proprietati include in interior elemente din clasa creata anterior.
Exemplu:
În fișierul HTML, mai jos, include: 
```html
<div id="cutie2"> 
		<div class="cutie">Cutia numarul 1.</div> 
		<div class="cutie cool">Cutia numarul 2</div> 
		<div class="cutie cool">Cutia numarul 3.</div> 
	</div>
```
În fișierul main.css, include:
```html
#cutie2{ 
		margin: 40px; 
		background-color: blue; 
		border: 10px solid #006; 
		overflow: hidden; 
	} 
```
<div class="custom-image"><img src="https://41.media.tumblr.com/b5b6bcbf0e90a58f2bcabc1922edd725/tumblr_nswpoy4Mv41udztn8o1_540.jpg" /></div>

Acum că știi cum se lucrează cu un id, cu o clasă, fii liber să încerci orice altle trucuri. Iată cateva trucuri simple, care-ți sunt recomandate:
<br>
color – setează culoarea textului

 opacity – setează nivelul opacității unui element

background-color – Specifică culoarea fundalului

background-image – indică imaginea de fundal a unui element

background-size – Specifică dimensiunea imaginii de fundal

border – seteaza proprietatile marginilor/frontierelor

border-color –setează culoarea marginii

border-radius – seteasă curbura colțurilor unei casete

border-right – setează proprietăți pentru marginea dreaptă

border-left – setează proprietăți pentru marginea stângă

border-top – setează proprietăți pentru marginea de sus

border-botton – setează proprietăți pentru partea de jos

border-width – setează grosimea tuturor marginilor

position – specifică metoda poziționării unui element  (static, absolute, relative sau fixed)

text-align – specific aranjarea pe orizontală a textului

text-decoration – specific ă „decorul”  textului

text-shadow – adaugă umbre textului

font-family – specifică familia textului

font-size – specifică mărimea textului.

font-style – specifică stilul textului

Selectori css:
```css
.numeClasa 
```
– selecteaza elementul class, cu denumirea numeClasa

```css
#numeId 
```
– selectează elementele id cu denumirea numeId,

```css
p
```
 – selectează toate elementele <p>

```css
div, p
```
 – selectează toate elementele <div> și elementele<p>

```css 
div p
```
 – selectează toate elementele < p> care se află în interiorul elementelor < div>

```css
:hover
```
 – seleteaza elementele pe care se afla pozitionat șoricelul

```css
a:visitet
```
 – selectează link-urile vizitate
