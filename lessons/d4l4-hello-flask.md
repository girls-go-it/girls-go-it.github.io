---
layout: default
title: Hello Flask
---


#Hello Flask

Imaginați-vă că v-aș ruga să tăiați o bucată de hârtie cu dimensiunile de 5 metri pe 5 metri. Bănuiesc că ați face asta destul de ușor. Acum tăiați 1000 de bucăți de hârtie de aceleași dimensiuni. Nu e foarte eficient să măsori bucățile de hârtie de 1000 de ori. O metodă de a soluţiona această problemă ar fi să faceți un mulaj (un schelet) al unei forme ce ar permite tăierea hârtiei cu dimensiunile dorite. Cam aceasta ar însemna să folosești un framework (cadru, schelet). Un framework permite efectuarea sarcinilor complicate sau repetitive rapid și eficient. Flask este un framework ce facilitează crearea unui site web.

În acest capitol veți învăța cum să instalați și să utilizați **Flask**-ul. Tot de ce este nevoie este un computer cu Python instalat pe el.

###Utilizarea ”Mediului Virtual” *(Virtual Environments)*
Cea mai bună metodă de a instala Flask-ul este printr-un mediu virtual. Dar ce este un mediu virtual *(virtual environment)*? Pentru a înțelege mai bine acest concept, să facem o analogie cu viața reală. Gândiți-vă la un mediu virtual ca la situația când trebuie să vă alegeți anumite lucruri în dependență de unde plecați:

> imagine

Așa e și cu mediu virtual, instalezi doar ceea ce ai nevoie. <br>
Pentru început, să verificăm dacă acest program de creare a mediilor virtuale este instalat.<br>
Rulați următoarea instrucțiune:

```bash
$ virtualenv --version
```

Cel mai probabil este că o să fie afișată o eroare ce va zice că nu aveți instalat așa program. Acest lucru se remediază foarte ușor, dat fiind că Ubuntu permite instalarea programelor chiar din terminal. Tot ce trebuie să faceți pentru ca să-l instalați este:

```bash
$ sudo apt-get install python-virtualenv
```

După aceasta, creați un folder cu mediul virtual unde veți păstra primul vostru proiect Flask.

```bash
$ mkdir awesomeFlaskProject
$ cd awesomeFlaskProject
```

Următorul pas e să creăm mediul virtual cu ajutorul comenzii `virtualenv`. După această comandă trebuie să urmeze numele folderului unde va fi creat mediul virtual, de obicei acest nume este `venv`, de la **v**irtual **env**ironment.

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


Acum că avem acest mediu virtual atât de mult râvnit în folderul `venv`, trebuie să-l activăm, altfel nu-i nici un *tolk* din el. Pentru a face asta e nevoie de următoarea instrucțiune **(ori de câte ori o să vreți să lucrați la proiectele voastre, o să fiți nevoiți să rulați această instrucțiune)**:

```bash
$ source venv/bin/activate
```
sau

```bash
$ . venv/bin/activate
```

Acum în terminal, printr-un `venv` în fața numelui, ar trebui să vi se menționeze că mediul virtual este activat :

```bash
(venv)flask@ubuntu:~ $
```

A rămas doar să instalăm framework-ul Flask și o să putem crea site-ul. Asigurați-vă că `(venv)` este în fața numelui din terminal, apoi rulați:

```bash
$ pip install flask
```

Perfect, acum să creăm un fișier. Eu o să-l numesc `hello.py`, dar voi puteți să-l numiți cum vreți atâta timp cât extensia fișierului este `.py`. *(Vă mai amintiți ce v-a vorbit azi Sergiu despre extensiile fişierelor?)* <br>
Scrieți în fișier:

```python
from flask import Flask
app = Flask(__name__)

@app.route('/')
def index():
	return 'Hello World!'

if __name__ == '__main__':
	app.run()
```

Înainte să rulați comanda în terminal, salvați modificările din fișier:

```bash
$ python hello.py
* Running on http://127.0.0.1:5000/ (Press CTRL+C to quit)
```

Acum să mergem și să vedem ce site frumos și interesant am creat. În browser accesăm adresa respectivă:<br>
`127.0.0.1:5000` sau `localhost:5000`

<div class="custom-image-shadow"><img src="/images/hello_flask/hello_world.png" /></div>

Felicitări, ați creat un site!

Acum, să analizăm ce am scris în super programul nostru. <br>
După convenţie toate aplicațiile Flask trebuie să conțină o instanță a aplicației noastre:

```python
from flask import Flask
app = Flask(__name__)
```

###Back in time - **URL**-uri

Înainte să continuăm analiza programului nostru, vă mai amintiți ce este un URL? <br>
Exact, URL este un acronim pentru **U**niform **R**esource **L**ocator, și este utilizat pentru a specifica adresa (a unui fișier sau resursă) pe internet *(the World Wide Web)*.

###Rute și Funcții View *(Routes and View Functions)*

Clienții, cum ar fi browserele, trimit **cereri** la serverele web (ceea ce aţi creat voi acum două minute), care, la rândul lor, trimit cererile la aplicația voastră Flask.  Aplicația trebuie să știe ce cod să ruleze pentru fiecare cerere URL, așa că ea creează o **asociere** a URL-urilor cu funcțiile Python. Asocierea dintre un URL și o funcție se numește un **route** (rută, cale, traseu, drum, cărărușă, itinerar, șosea, canal, marșrut, șleau). <br>
În următorul exemplu se demonstrează cum se face această mapare în Flask:

```python
@app.route('/')
def index():
	return 'Hello World!'
```

Înainte de a crea funcţia, definim `route`-ul aşa: `@app.route('/<adresa route-lui>')`. <br>
Aici, funcția `index()` este înregistrată la URL-ul de bază al aplicației: **`/`**. Dacă aplicația ar fi lansată pe un server asociat cu domeniul `www.exemplu.com` și veți naviga la `http://www.exemplu.com`, atunci funția `index()` va fi rulată pe server și va fi afișat *Hello World!*, aceasta fiind un **response** (răspuns) - valoare returnată de funcție. <br>
Funcțiile, ca și `index()`, se numesc **view functions**, funcții care afișează. Un response returnat de o funcție view poate fi un simplu **string** (ca și în cazul nostru), sau poate fi ceva mai complicat, după cum veți vedea mai târziu.


###Modul Debug

Haideți să facem o modificare la valoare returnată de funcția `index()`, să salvăm fișierul și să facem un refresh la pagina din browser. 
După cum vedeți, serverul nu a inclus schimbarea, deoarece el rulează după o versiune mai veche a fișierului `hello.py`. <br>
Un truc foarte util este modul **debug** care zice serverului să fie atent la toate schimbările ce au loc. Pe lângă asta, atunci când serverul va întâlni o eroare, el va încerca să analizeze cauza și vă va da o sugestie la cum să remediați greșeala. Tot ce trebuie să faceți pentru a activa acest mod este să adăugați următoarea linie de cod:

```python
app.debug = True
app.run() #această linie deja există în fișier
```

sau să includeți paramentrul în interiorul chemării metodei `run()`

```python
app.run(debug = True)
```

Ambele procedee au exact același efect.

###Adăugăm URL-uri

Pentru început să adăugăm unul simplu, ca şi cel pe care l-avem deja. Adăugaţi următorul cod după funcţia `index()`.

```python
@app.route('/date')
def show_date():
	return 'Azi este ' + 20 + ' august.'
```

Salvaţi modificările şi mergeţi la `localhost:5000/date`. <br>
Rezultatul ar trebuie să fie următorul:

<div class="custom-image-shadow"><img src="/images/hello_flask/first_error.png" /></div>

Ce palpitant! Prima voastră eroare!
Dar să nu vă fie frică,  `debugger`-ul vă ajută să soluționați eroarea. Amintiți-vă ce v-a zis azi Diana despre convertirea `string`-urilor. Exact, Python nu poate concatena (uni) un `string` cu un non-string. Din această cauză trebuie să transformați **`20`** într-un `string`. <br>
Cum faceți asta? Exact! Aplicaţi metoda `str()` asupra numărului.<br>
Acum linia buclucaşă arată aşa:

```python
return 'Azi este ' + str(20) + ' august.'
```

Accesaţi acum `localhost:5000/date` şi totul trebuie să ruleze bine:

<div class="custom-image-shadow"><img src="/images/hello_flask/fixed_error.png" /></div>

Probabil o să vă întrebaţi: *"De ce nu am scris de la început `'Azi e 20 august.'`? Fără ca să ne mai batem capul de `string`-uri, `int`-uri, contatenare..."*<br>
Răspunsul e simplu: **flexibilitate**. Efectuând câteva modificări mici, puteţi face ca pagina voastră să afişeze data corect în fiecare zi a anului şi nu doar pe `20 august`. Importaţi modulul `datetime` despre care vi s-a vorbit la **Basic Python Statements**, care vă va permite să manipulaţi timpul ca ora sau data (dar nu; nu veţi putea să călătoriti în timp). Scrieţi următorul cod chiar sub `from flask import Flask`:


```python
from datetime import datetime 
```

iar funcţia `show_date()` o modificaţi până arată aşa:

```python
@app.route('/date')
def show_date():
	today = datetime.now()
	return 'Azi este ' + str(today.day) + ' august.'
```

Acum, în fiecare zi, data va fi corectă.

Dacă ați fost atenți atunci când navigați pe internet la adresa ce va apărut sus, în browser, atunci probabil ați observat că multe dintre aceste URL-uri au părți variabile. De exemplu URL-ul pentru pagina voastră de Facebook este `http://www.facebook.com/<nume-utilizator>` , adică numele vostru de utilizator este parte din URL. Următorul exemplu demonstrează aceeași funcționalitate a Flask-ului. Adăugați următorul cod după funcția `show_date()`:

```python
@app.route('/user/<name>')
def user(name):
	return 'Hello, %s!' % name
```

Porțiunea dintre `< >` este partea dinamică, așa că orice URL care coincide cu partea statică (`localhost:5000/user/`) va fi asociată cu funcția `user()`. Când funcția este chemată, Flask trimite partea dinamică ca o variabilă (argument), astfel `name` va fi trimisă în funcție ca parametru.

Salvați fișierul, mergeți în browser și accesați adresa: 
`localhost:5000/user/numele-vostru`

<div class="custom-image-shadow"><img src="/images/hello_flask/hello_user.png" /></div>


###Fișiere statice

După cum presupune numele, Flask permite utilizarea fișierelor statice (și se numesc așa pentru că aceste pagini afișează aceeași informație tuturor utilizatorilor site-ului). Pentru că Flask este un framework inteligent, el o să caute fișierele statice în folderul `/static` din proiect. Creați folderul și un fișier în interiorul lui cu extensia `.html`. După aceasta puteți accesa acest fișier la: `localhost:5000/static/<numele-fișierului>.html`

<div class="custom-image-shadow"><img src="/images/hello_flask/static_page.png" /></div>

#Bonus
###Zi-i vecinului să-ți acceseze site-ul
Pentru a face site-ul vizibil (și accesibil) tuturor **de pe rețeaua locală** 
trebuie să menționăm acest lucru lui Flask. Modificați ultima linie de cod ca să arate în felul următor:

```python
app.run(host = '0.0.0.0', debug = True)
```

După, trebuie să aflați ce adresă v-a dat bunul router. Pentru a face asta, rulați instrucțiunea:

```bash
ifconfig
```

Aceasta va afișa multă informație în consolă, căutați ultima coloană, unde scrie  `wlan0` și căutați `inet addr`. Adresa pe care o puteți da vecinului este aceasta.

