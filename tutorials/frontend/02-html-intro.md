---
layout: default
title: HTML Intro
category: basic
---

## Ce este HTML?

Hai să începem tutorialul prin a arăta paşii simpli pe care îi facem pentru a verifica de exemplu starea vremii pe www.meteo.md.

1. Deschid browser-ul (ex. FireFox, Chrome, etc.) 
2. Scriu în căsuţa de căutare www.meteo.md 
3. Vizualizez rezultatul căutării mele (nişte text, imagini etc.)
 
Pentru a clarifica lucrurile trebuie să înţelegem cât mai simplu ce stă în spatele acestor 3 simpli paşi pe care i-am făcut.

În primul rând browser-ul nu este nimic altceva decât o aplicaţie care ne permite să accesăm pe internet anumite link-uri în urma cărora noi obţinem “ceva". 
Acest “ceva" îl numim - resursă şi ea este obţinută în rezultatul accesării link-ului, iar browser-ul ştie cum să prezinte această resursă. 

Această resursă nu reprezintă nimic complicat, este foarte simplu - doar un fişier cu text. Desigur acest fişier cu text are o anumită structura bine definită după anumite standarde şi are extensia `.html`. 

La baza oricărei pagini web pe care am dori să o accesăm stă un fişier cu extensia `.html` sau simplu să îl numim fişier `HTML`, iar după cum am spus browser-ul ştie cum să ne reprezinte acest tip de fişier. 

După cum ai aflat din lecţia precedentă internetul lucrează la nivel înalt pe principiul "eu cer tu îmi răspunzi" (Client-Server connection, clientul cere - serverul îi oferă un răspuns). În cazul nostru eu (Clientul - browserul) accesând www.meteo.md cer o resursă, iar Serverul ce răspunde de adresa dată (în caz că nu sunt erori) îmi returnează o resursă `index.html` care conţine toate detaliile paginii pe care eu am vizualizat-o în final. 

Cunoscând deja că acest fişier cu extensia `.html` reprezintă doar text scris conform anumitor reguli, desigur că şi noi îl putem simplu crea şi deschide cu browser-ul nostru care poate citi orice fişier cu acest format. Ceea ce ne rămâne este să studiem care sunt aceste reguli - ceea ce urmează să facem în continuare. 

***
#### Cum se descifreaza HTML?

HTML sau HyperText Markup Language este unul dintre cele mai vechi limbaje de marcare web. Un limbaj de marcare (în engleză: markup language) este o metodă de formatare a unui text de pe o pagină web, care combină textul cu informațiile suplimentare despre acel text.

#### Ce reprezinta fisierele HTML?

De fapt fișierele HTML nu sunt nimic altceva decât simple fișiere text cum am spus, respectiv pentru a începe a scrie cod HTML nu ai nevoie de nimic mai mult decât un editor de text. Toate sistemele de operare au deja unul preinstalat. Spre exemplu Notepad pe sistemul de operare Windows și TextEdit pe sistemul de operare Mac OSX. Noi vom folosi un editor de text larg utilizat de developerii din întreaga lume `Sublime Text`.

Te rugăm să parcurgi următorii pași:

 1. Descarcă `Sublime Text` de pe [site-ul oficial](https://www.sublimetext.com/3).
 2. Parcurge procedura standard de instalare (next, next, next, install).
 3. Deschide `Sublime Text`.
 4. De acum înainte îl vom numi simplu — `Sublime`.

În fereastra `Sublime` scrie un mesaj scurt, de exemplu:

```html
I love HTML!
```
După, salvează acest fișier și numește-l `index.html` 
(Ca o conventie -  intr-un proiect Web fisierul de baza il numim index.html)

Acest mic `index.html` este prima ta pagină web. Pentru a vizualiza rezultatul trebuie să deschizi acest document `html` în browser-ul tău preferat (ex. Chrome, Firefox, Safari, Opera sau Internet Explorer).

Acum putem trece la chestii puțin mai complexe. Chiar dacă fișier-ul HTML este un simplu document text, putem adăuga puțin marcaj pentru a defini noi tipuri de conținut.

Mai jos găsești structura generală a unui document HTML.

```html
<!DOCTYPE html>
<html>
	<head>
		<title>My page</title>
	</head>
	<body>
		I love HTML!
	</body>
</html>
```
Interpretarea acestui cod este mult mai simplă decât pare la prima vedere. 

Documentele HTML trebuie să înceapă cu așa numitul `Doctype`, el se scrie în felul următor `<!DOCTYPE html>` și definește versiunea codului HTML, în cazul dat versiunea 5. Astfel browser-ul înțelege cum exact trebuie să interpreteze codul ce urmează.

Până a trece la cea de-a doua linie, trebuie să menționăm că în procesul învățării limbajului de marcare HTML va trebuie să ții minte doar două noțiuni. Prima este noțiunea de `Tag` și a doua — noțiunea de `Atribut`.

HTML-ul dispune de o gamă largă de tag-uri care marchează începutul și sfârșitul unui tip de conținut. În exemplul precedent avem tag-ul `<html>` care marchează începutul documentului HTML și tag-ul de închidere `</html>` care marchează sfârșitul documentului HTML. Totul ce se află între tag-ul `<body>` și `</body>` este conținutul principal al documentului care se va afișa în browser, iar tag-ul `<head>` conține informație despre pagina curentă și codul amplasat înăuntrul acestui tag nu se va afișa pe pagină.

Tag-ul `<title>` despre care nu am vorbit încă, reprezintă titlul paginii care se va afișa sus pe bara de titlu a browser-ului tău.

Odată ce avem structura de bază a documentului HTML, ne putem juca cu mai multe tag-uri și tipuri de conținut.

Tag-ul `<p>` este folosit pentru a defini un paragraf.
```html
<p>This is a paragraph.</p>
```
Textele care au un rol mai important pe pagină sunt definite cu ajutorul tag-urilor `<h1>`, `<h2>`, `<h3>`, `<h4>`, `<h5>` și `<h6>`, unde cel mai important este `<h1>` și cel mai puțin important este `<h6>`.
```html
<h1>Page title</h1>
<h2>Page subtitle</h2>
```

În HTML avem două tipuri de liste: ordered `<ol>` și unordered `<ul>` list. Fiecare element din listă este definit cu ajutorul tag-ului `<li>`. 

```html
<ul>
	<li>List item</li>
	<li>List item</li>
	<li>List item</li>
</ul>
```
În acest caz, ierarhia este strictă și obligatorie. Tag-ul `<li>` poate fi doar copilul imediat al tag-ului `<ul>` sau `<ol>` și nu poate exista în afara acestora. 

Ce poate fi mai interesant în construirea unei pagini web decât crearea link-urilor? Pentru a crea un link nou folosește tag-ul `<a>` și în conținutul acestuia scrie textul link-ului.

```html
<a>Go to Google</a>
``` 
Totul arată bine, doar că browser-ul nu are de unde să știe spre ce adresă trebuie să fie redirecționat utilizatorul care dă click pe textul `Go to Google`. Și dacă-ți aduci aminte, la începutul acestui articol am spus că trebuie să ții minte doar două noțiuni — `tag` și `atribut`. Păi uite că a venit timpul să vorbim și despre a doua noțiune. Atributele sunt de fapt mici segmente informaționale care se aplică asupra tag-ului de deschidere pentru a caracteriza mai bine tag-ul curent. În cazul dat vom folosi atributul `href=""` pentru a seta adresa de redirecționare a utilizatorului.


```html
<a href="https://www.google.com">Go to Google</a>
``` 

În timp ce există o listă de atribute comune, atributul `href=""` nu poate fi aplicat pe orice alt tag.

Dacă să revenim la tag-uri, trebuie să menționez că sunt două tipuri de tag-uri, care au sau nu tag de închidere. Toate tag-urile care le-am enumerat până acum au fost tag-uri care pot avea conținut, dar un exemplu de tag care nu poate avea conținut și care respectiv nu se închide este tag-ul `<br>` care este folosit pentru a trece textul pe următorul rând.
```html
<p>
	— I love HTML!<br>
	— Do you?
</p>
```

Un alt exemplu de tag care nu se închide este tag-ul `<img>`. Folosește acest tag pentru a afișa o imagine. Și pentru că browser-ul trebuie să știe unde poate găsi imaginea de care ai nevoie, vei folosi atributul `src=""` cu adresa completă a imaginii.

```html
<img src="https://unsplash.it/200/300">
```
Mai avem o categorie nouă de tag-uri care ne ajută să caracterizăm structura paginii (a nu fi confundată cu structura documentului HTML). De regulă toate paginile au o structură relativ asemănătoare care-și iau rădăcinile din tipografia ziarelor. Avem un `<header>` unde stă logo-ul și menu-ul, avem mai multe `<section>`-uri în care este divizat conținutul principal al site-ului și jos avem un `<footer>` unde de regulă stă mesajul de copyright.

```html
<header>
	<a href="/">
		<img src="http://plachold.it/20x20" alt="Logo">
	</a>
	<nav>
		<ul>
			<li>
				<a href="index.html">Home</a>
			</li>
			<li>
				<a href="about.html">About</a>
			</li>
			<li>
				<a href="contacts.html">Contacts</a>
			</li>
		</ul>
	</nav>
</header>

<section>
	<h1>Page Title</h1>
	<p>Page Description</p>
</section>

<footer>
	<p>All rights reserved.</p>
</footer>
```
Pe lângă toate aceste tag-uri care definesc secțiuni specifice ale paginii mai există încă un tag popular și des utilizat, este vorba de tag-ul `<div>` care este o prescurtare a cuvântului `division`. Cum îți poți da seama din denumirea acestuia, el este folosit pentru a diviza secțiuni și elemente în sub-elemente.
```html
<header>
	<div>Left side of the header</div>
	<div>Right side of the header</div>
</header>
```
Mă bucur că ai ajuns la sfârșitul acestui articol. Acestea sunt cele 20% din limbajul de marcare HTML, care-ți permit să realizezi 80% din posibilitățile acestui, tot de ce ai nevoie este doar răbdare și curiozitate.

Te invit să vizitezi următoarea secțiune pentru a afla ce-i aia CSS și cum să dai viață paginii tale aplicând noi culori și forme.

## Exemplu
Pentu a vedea un exemplu de o pagina creată pur cu HTML (desigur că are și ceva stilizare ascunsă), descarcă [HTML Template](https://github.com/sarguvlad/HTML-Template/archive/master.zip).

Dezarhivezi fișierul zip într-un folder, și deschide `index.html` pentru a-l vedea.
