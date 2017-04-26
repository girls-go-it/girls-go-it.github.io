---
layout: default
title: Hello Flask
---

# Hello Flask

Imaginează-ţi că te-aş ruga să tai o bucată de hârtie cu dimensiunile de 50 centimetri pe 50 centimetri. Bănuiesc că ai face asta destul de ușor. Acum taie 1000 de bucăți de hârtie de aceleași dimensiuni. Nu e foarte eficient să măsori bucățile de hârtie de 1000 de ori. O metodă de a soluţiona această problemă ar fi să faci un cadru al unei forme de 50 cm pe 50 cm ce ar permite tăierea hârtiei cu dimensiunile dorite fără măsurarea ei. Cam aceasta ar însemna să folosești un framework (cadru, schelet). Un framework permite efectuarea sarcinilor complicate sau repetitive rapid și eficient. Flask este un **web framework**, adică un framework ce facilitează crearea unui site web.

În acest capitol vei învăța cum să instalezi și să utilizezi **Flask**-ul. Tot de ce este nevoie este un computer cu Python instalat pe el.

### Utilizarea ”Mediului Virtual” *(Virtual Environments)*

Cea mai bună metodă de a instala Flask-ul este printr-un mediu virtual. Dar ce este un mediu virtual *(virtual environment)*? Pentru a înțelege mai bine acest concept, să facem o analogie cu viața reală. Gândeşte-te la un mediu virtual ca la situația când trebuie să-ţi alegi anumite lucruri în dependență de unde pleci. Un *contra-exemplu* a necesităţii unui mediu virtual este geanta (poşeta) unei fete - acolo, mereu, poţi găsi de toate.

Așa e și cu mediu virtual, instalezi doar ceea ce ai nevoie. <br>
Pentru început, verificaţi dacă acest program de creare a mediilor virtuale este instalat.<br>
Rulează următoarea instrucțiune:

```bash
$ virtualenv --version
```

Cel mai probabil este că o să fie afișată o eroare ce va zice că nu ai instalat așa program. Acest lucru se remediază foarte ușor, dat fiind că Ubuntu permite instalarea programelor chiar din terminal. Tot ce trebuie să faci pentru ca să-l instalezi este:

```bash
$ sudo apt-get install python-virtualenv
```

După aceasta, crează un folder cu mediul virtual unde vei păstra primul tău proiect Flask.

```bash
$ mkdir savanna-tweet
$ cd savanna-tweet
```

Următorul pas e să creezi mediul virtual cu ajutorul comenzii `virtualenv`. După această comandă trebuie să urmeze numele folderului unde va fi creat mediul virtual, de obicei acest nume este `venv`, de la **v**irtual **env**ironment.

```bash
$ virtualenv venv
```

Iar output-ul va fi următorul:

```bash
Running virtualenv with interpreter /usr/bin/python2
New python executable in venv/bin/python2
Also creating executable in venv/bin/python
Installing setuptools, pip...done
```

Acum că ai acest mediu virtual atât de mult râvnit în folderul `venv`, trebuie să-l activezi, altfel nu-i nici un *tolk* din el. Pentru a face asta e nevoie de următoarea instrucțiune **(ori de câte ori o să vrei să lucrezi la proiectul tău, o să fii nevoit să rulezi această instrucțiune)**:

```bash
$ source venv/bin/activate
```
sau

```bash
$ . venv/bin/activate
```

Acum în terminal, printr-un `venv` în fața numelui, ar trebui să ţi se menționeze că mediul virtual este activat:

```bash
(venv)flask@ubuntu:~ $
```

Îţi mai aminteşti ce este relaţia **client - server**? Exact, *clientul* solicită un serviciu (ex: vizualizarea unei pagini de Facebook), iar *serverul*, după ce a primit cererea, transmite un răspuns (ex: informaţia necesară browserului pentru ca el să afişeze pagina solicitată).

În cazul nostru, Flask va îndeplini rolul de *server*, iar browserul - *clientul*.

Acum să instalăm programul care ne va permite să instalăm (descărcăm) programe (module) pentru `Python`:

```bash
$ sudo apt-get install python-pip
```

Pentru ca Flask-ul să îndeplinească rolul de *server*, el trebuie instalat.  Asigură-te că `(venv)` este în fața numelui din terminal, apoi rulează:

```bash
$ pip install flask
```

Perfect, acum să creăm un fișier. Pentru început să-l numim `hello.py`, dar tu poţi să-l numeşti cum vrei atâta timp cât extensia fișierului este `.py`. *(Vă mai amintiți ce a vorbit azi Sergiu despre extensiile fişierelor?)* <br>
Scrie în fișier:

> **Notă:** Structura curentă a proiectului este provizorie. Pentru moment o s-o folosim pe aceasta pentru că e mai simplă şi va facilita înţelegerea framework-ului. La sfârşitul lecţiei vom discuta despre structura recomandată a unui proiect Flask.

```python
from flask import Flask
app = Flask(__name__)

@app.route('/')
def index():
	return 'Hello World!'

if __name__ == '__main__':
	app.run()
```

Înainte să rulezi comanda în terminal, salvează modificările din fișier:

```bash
$ python hello.py
* Running on http://127.0.0.1:5000/ (Press CTRL+C to quit)
```

Acum să mergem și să vedem ce site frumos și interesant am creat. În browser accesează adresa respectivă: <br>
`127.0.0.1:5000` sau `localhost:5000`

<div class="custom-image-shadow"><img src="/images/hello_flask/hello_world.png" /></div>

Felicitări, ai creat un site!

Acum, să analizăm ce am scris în super programul nostru. <br>
Pentru început trebuie să importăm modului Flask. <br>
După convenţie toate aplicațiile Flask trebuie să conțină o instanță a aplicației noastre, pe care, convenabil, o numim `app`. Ea se defineşte în felul următor: 

```python
from flask import Flask
app = Flask(__name__)
```

### Back in time - **URL**-uri

Înainte să continuăm analiza programului nostru, îţi mai aminteşti ce este un URL? <br>
Întocmai, **URL** este un acronim pentru **U**niform **R**esource **L**ocator, și este utilizat pentru a specifica adresa (a unui fișier sau resursă) pe internet *(the World Wide Web)*.

###Rute și Funcții View *(Routes and View Functions)*

Clienții, cum ar fi browserele, trimit **cereri** la serverele web (ceea ce ai creat tu acum două minute), care, la rândul lor, trimit cererile la aplicația voastră Flask. Aplicația trebuie să știe ce cod să ruleze pentru fiecare cerere URL, așa că ea creează o **asociere** a URL-urilor cu funcțiile Python. Asocierea dintre un URL și o funcție se numește un **route** (rută, cale, traseu, drum, cărărușă, itinerar, șosea, canal, marșrut, șleau). <br>
În următorul exemplu se demonstrează cum se face această mapare în Flask:

```python
@app.route('/')
def index():
	return 'Hello World!'
```

Înainte de a crea funcţia, definim `route`-ul aşa: `@app.route('/<adresa route-lui>')`. <br>
Aici, funcția `index()` este înregistrată la URL-ul de bază al aplicației: **`/`**. Dacă aplicația ar fi lansată pe un server asociat cu domeniul `www.exemplu.com` și veți naviga la `http://www.exemplu.com`, atunci funția `index()` va fi rulată pe server și va fi afișat *Hello World!*, aceasta fiind un **response** (răspuns) - valoare returnată de funcție. <br>
Funcțiile, ca și `index()`, se numesc **view functions**, funcții care afișează. Un response returnat de o funcție view poate fi un simplu **string** (ca și în cazul nostru), sau poate fi ceva mai complicat, după cum veți vedea mai târziu.

### Modul Debug

Fă o modificare la valoare returnată de funcția `index()`, salvează fișierul și să fă un refresh la pagina din browser. 
După cum vezi, serverul nu a inclus schimbarea, deoarece el rulează după o versiune mai veche a fișierului `hello.py`. <br>
Un truc foarte util este modul **debug** care zice serverului să fie atent la toate schimbările ce au loc. Pe lângă asta, atunci când serverul va întâlni o eroare, el va încerca să analizeze cauza și vă va da o sugestie la cum să remediați greșeala. Tot ce trebuie să faci pentru a activa acest mod este să adaugi următoarea linie de cod:

```python
app.debug = True
app.run() #această linie deja există în fișier
```

sau să incluzi parametrul în interiorul chemării metodei `run()`

```python
app.run(debug = True)
```

Ambele procedee au exact același efect.

### Adăugăm URL-uri

Pentru început să adăugăm unul simplu, ca şi cel pe care l-avem deja. Adaugă următorul cod după funcţia `index()`.

```python
@app.route('/date')
def show_date():
	return 'Azi este ' + 20 + ' august.'
```

Salvează modificările şi mergi la `localhost:5000/date`. <br>
Rezultatul ar trebuie să fie următorul:

<div class="custom-image-shadow"><img src="/images/hello_flask/first_error.png" /></div>

Ce palpitant! Prima eroare!
Dar să nu-ţi fie frică,  `debugger`-ul te va ajuta să soluționezi eroarea. Aminteşte-ţi ce ţi-a zis Diana despre convertirea `string`-urilor. Bravo, Python nu poate concatena (uni) un `string` cu un non-string. Din această cauză trebuie să transformi **`20`** într-un `string`. <br>
Cum faci asta? Corect! Aplică metoda `str()` asupra numărului.<br>
Acum linia buclucaşă arată aşa:

```python
return 'Azi este ' + str(20) + ' august.'
```

Accesează acum `localhost:5000/date` şi totul trebuie să ruleze bine:

<div class="custom-image-shadow"><img src="/images/hello_flask/fixed_error.png" /></div>

Probabil o să te întrebi: *"De ce nu am scris de la început `'Azi e 20 august.'`? Fără ca să-mi mai bat capul de `string`-uri, `int`-uri, concatenare..."*<br>
Răspunsul e simplu: **flexibilitate**. Efectuând câteva modificări mici, poţi face ca pagina ta să afişeze data corect în fiecare zi a anului şi nu doar pe `20 august`. Importă modulul `datetime` despre care ţi s-a vorbit la **Basic Python Statements**, care îţi va permite să manipulezi timpul ca ora sau data (dar nu; nu vei putea să călătoreşti în timp). Scrie următorul cod chiar sub `from flask import Flask`:


```python
from datetime import datetime 
```

iar funcţia `show_date()` o modifici până arată aşa:

```python
@app.route('/date')
def show_date():
	today = datetime.now()
	return 'Azi este ' + str(today.day) + ' august.'
```

Acum, în fiecare zi, data va fi corectă.

Dacă ai fost atent atunci când navigai pe internet la adresa ce ţi-a apărut sus, în browser, atunci probabil ai observat că multe dintre aceste URL-uri au părți variabile. De exemplu URL-ul pentru pagina ta de Facebook este `http://www.facebook.com/<nume-utilizator>`, adică numele tău de utilizator este parte din URL. Următorul exemplu demonstrează aceeași funcționalitate a Flask-ului. Adaugă următorul cod după funcția `show_date()`:

```python
@app.route('/user/<name>')
def user(name):
	return 'Hello, %s!' % name
```

Porțiunea dintre `< >` este partea dinamică, așa că orice URL care coincide cu partea statică (`localhost:5000/user/`) va fi asociată cu funcția `user()`. Când funcția este chemată, Flask trimite partea dinamică ca o variabilă (argument), astfel `name` va fi trimisă în funcție ca parametru.

Salvează fișierul, mergi în browser și accesează adresa: <br>
`localhost:5000/user/numele-vostru`

<div class="custom-image-shadow"><img src="/images/hello_flask/hello_user.png" /></div>

Acum, fişierul tău `hello.py` ar trebuie să arate cam aşa:

```python
from flask import Flask
from datetime import datetime

app = Flask(__name__)

@app.route('/')
def index():
	return 'Hello World!'

@app.route('/date')
def show_date():
	today = datetime.now()
	return 'Azi este ' + str(today.day) + ' august.'

@app.route('/user/<name>')
def user(name):
	return 'Hello, %s!' % name

if __name__ == '__main__':
	app.run(debug = True)
```

### Structura unui proiect Flask

Acum, că fişierul a devenit atât de mare, cu mult cod şi funcţii, e timpul să vorbim despre structura recomandată a unui proiect Flask, altfel fişierul va continua să crească şi codul va deveni dificil de menţinut. <br>

<div class="custom-image-shadow"><img src="/images/hello_flask/project_structure.png" /></div>

```
savanna-tweet
	/app
		/static
			page.html
		__init__.py
		views.py
	/venv
	run.py
```

Pentru început, în folderul proiectului, creează un folder `/app`. În interiorul acestui folder `/app`, creează 2 fişiere: `__init__.py` şi `views.py`. <br>
`__init__.py` este un fişier special în limbajul `Python`, pentru că el permite ca directoriul (folderul) în care se află să devină un modul ce poate fi importat în alte fişiere `.py`. Aici o să includem instanţa aplicaţiei noastre şi o să importăm conţinutul fişierului `views.py`.

```python
from flask import Flask 
app = Flask(__name__)

from app import views
```

Ce au în comun toate funcţiile `index`, `show_date` şi `user` pe care le-am definit până acum? Da, toate sunt funcţii `views`, deci, logic, le vom pune în fişierul `views.py`. Acest fişier ar trebui să arate aşa:

```python
from app import app
from datetime import datetime

@app.route('/')
def index():
	return 'Hello World!'

@app.route('/date')
def show_date():
	today = datetime.now()
	return 'Azi este ' + str(today.day) + ' august.'

@app.route('/user/<name>')
def user(name):
	return 'Hello, %s!' % name
```

> **Notă** Am importat modului `datetime` aici, pentru că avem nevoie de el pentru funcţia `show_date`.

Ne-a mai rămas să creăm un singur fişier `.py` şi el se va numi `run.py`, pentru că, după cum ţi-ai dat seama, de aici o să pornească aplicaţia noastră. El se va afla la acelaşi nivel cu folderele `/app` şi `/venv`. În acest fişier vei include:

```python
from app import app

if __name__ == "__main__":
	app.run(debug = True)
```

**Nu am modificat nimic în cod decât să-l separăm.**

Ultimul folder pe care trebuie să-l creezi este `/static` şi se va alfa în folderul `/app`. Explic imediat pentru ce avem nevoie de el.

### Fișiere statice

După cum presupune numele, Flask permite utilizarea fișierelor statice (și se numesc așa pentru că aceste pagini afișează aceeași informație tuturor utilizatorilor site-ului). Pentru că Flask este un framework inteligent, el o să caute fișierele statice în folderul `/static` din proiect. Creați folderul și un fișier în interiorul lui cu extensia `.html`. Introdu un text asemănător în interiorul lui:

```html
Hello from the static page!
```

După aceasta poţi accesa acest fișier la: `localhost:5000/static/<numele-fișierului>.html`

<div class="custom-image-shadow"><img src="/images/hello_flask/static_page.png" /></div>

# Bonus
### Zi-i vecinului să-ți acceseze site-ul
Pentru a face site-ul vizibil (și accesibil) tuturor **de pe rețeaua locală** trebuie să menționăm acest lucru lui Flask. Modifică ultima linie de cod ca să arate în felul următor:

```python
app.run(host = '0.0.0.0', debug = True)
```

După, trebuie să afli ce adresă ţi-a dat bunul router. Pentru a face asta, rulează instrucțiunea:

```bash
ifconfig
```

Aceasta va afișa multă informație în consolă, caută ultima coloană, unde scrie `wlan0` și găseşte `inet addr`. Adresa pe care o poţi da vecinului este aceasta.

### *Exerciții:*
Creează workspace-ul pentru proiectul tău

1. Creează un folder unde o să păstrezi noul tău proiect
2. Creează mediul virtual `virtualenv`-ul (şi nu uita să-l activezi)
3. Instalează Flask-ul
4. Creează alt folder `/app` unde o să incluzi `__init__.py`, `views.py` şi folderul `/static`
5. Include codul necesar în fişierele `__init__.py` şi `views.py` (dacă nu-ţi aminteşti ce trebuie să scrii în ele, fă un scroll la **Structura unui proiect Flask**)
6. Creează fişierul `run.py` (la acelaşi nivel cu folderele `/app` şi `/venv`) unde să incluzi codul pentru pornirea aplicaţiei
6. Porneşte serverul, şi minunează-te

**Adiţional:**

* Creează o nouă rută cu URL dinamic (ex: `localhost:5000/string/ggit`) care să afişeze partea de după `/string/` de 3 ori. <br>
Pentru ruta de mai sus, output-ul corect este `ggitggitggit`
* Adaugă o pagină, ca şi `/date`, care pe lângă data curenta, va afişa şi ora. <br>
(ex: `"Azi e 20 august. Ora 19:03"`)
* Creează două pagini statice unde poţi să incluzi ce vrei tu în ele

