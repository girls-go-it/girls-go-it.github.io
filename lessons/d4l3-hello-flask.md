---
layout: default
title: Hello Flask
---

#Hello Flask

Imaginați-vă că v-aș ruga să tăiați o bucată de hârtie cu dimensiunile de 5 metri pe 5 metri. Bănuiesc că ați face asta relativ de ușor. Acum vă rog să tăiați 1000 de bucăți de hârtie de aceleași dimensiuni. Nu e eficient să măsori bucățile de hârtie de 1000 de ori. O metodă de a rezolva această problemă ar fi să faceți un mulaj (un schelet) al unei forme ce ar permite tăierea hârtiei cu dimensiunile dorite. Cam aceasta ar însemna să folosești un framework (cadru, schelet) care ar permite efectuarea sarcinilor complicate sau repetitive rapid și eficient. Flask este un framework ce facilitează crearea unui site web.

În acest capitol veți învăța cum să instalați și utilizați **Flask**-ul. Tot de ce este nevoie este un computer cu Python instalat pe el.

###Utilizarea ”Mediului Virtual” *(Virtual Environments)*
Cea mai convenabilă metodă de a instala Flask-ul este printr-un mediu virtual. Acum vă întrebați: "ce este un mediu virtual" *(virtual environment)*, ...nu? Hmm, oricum o să vă explic:
Un mediu virtual, în contextul respectiv, ar putea fi asociat cu hainele și lucrurile pe care la aveți la voi în dependență de  unde plecați:

> imagine

Așa e și cu mediu virtual, instalezi doar ceea de ce ai nevoie.
Pentru început, să verificăm dacă acest program de creare a mediilor virtuale este instalat. Rulați următoarea instrucțiune:

```bash
$ virtualenv --version
```

Cel mai probabil este că o să vă fie afișată o eroare ce vă va zice că nu aveți instalat așa program. Acest lucru se remediază foarte ușor, dat fiind că Ubuntu permite instalarea programelor chiar din terminal. Tot ce trebuie să faceți pentru ca să-l instalăm este să scriem:

```bash
$ sudo apt-get install python-virtualenv
```

După aceasta, hai, să creăm un folder (mapă) unde să creăm un mediu virtual unde o să creăm primul vostru proiect Flask.

```bash
$ mkdir awesomeFlaskProject
$ cd awesomeFlaskProject
```
Următorul pas e să creăm mediul virtual cu ajutorul comenzii `virtualenv`. După această comandă trebuie să urmeze numele folderului unde va fi creat mediul virtual, de obicei acest nume este `venv`, de la **v**irtual **env**ironment cu un output similar.

```bash
$ virtualenv venv
Running virtualenv with interpreter /usr/bin/python2
New python executable in venv/bin/python2
Also creating executable in venv/bin/python
Installing setuptools, pip...done
```

Acum că avem acest mediu virtual atât de mult râvnit în folderul `venv` trebuie să-l activăm, altfel nu-i nici un *tolk* din el. Pentru a face asta e nevoie de următoare instrucțiune (ori de câte ori nu o să vreți să lucrați la proiectele voastre, o să fiți nevoiți să rulați această instruțiune):

```bash
$ source venv/bin/activate
```
sau

```bash
$ . venv/bin/activate
```

Acum în terminal ar trebui să vi se menționeze că mediul virtual este activat printr-un `venv` în fața numelui:

```bash
(venv)flask@ubuntu:~ $
```

A rămas doar să instalăm framework-ul Flask și o să putem crea site-uri. Asigurați-vă că `(venv)` este în fața numelui din terminal, apoi rulați:

```bash
$ pip install flask
```

Perfect, acum că avem totul setat bine, hai, să creăm un fișier. Eu o să-l numesc `hello.py`, dar voi ați putea să-l numiți cum vreți atâta timp cât extensia fișierului (vă mai amintiți ce v-a vorbit azi Sergiu) este `.py`.
În fișier o să scriem:

```python
from flask import Flask
app = Flask(__name__)

@app.route('/')
def hello_world():
	return 'Hello World!'

if __name__ == '__main__':
	app.run()
```

Următorul lucru pe care trebuie să facem, e să-l rulați în consolă (nu uitați să salvați modificările efectuate în fișier):

```bash
$ python hello.py
* Running on http://127.0.0.1:5000/ (Press CTRL+C to quit)
```

Acum să mergem și să vedem ce site frumos și interesant am creat scriind adresa respectivă în browser:

`127.0.0.1:5000` sau `localhost:5000`

> imagine

Felicitări ați creat un site!

Hai să analizăm ce am scris în super programul nostru. Toate aplicațiile Flask trebuie să conțină o instanță a aplicației noastre:

```python
from flask import Flask
app = Flask(__name__)
```

>menționez că `app` poate fi orice altă denumire?

###Back in time - **URL**-uri

Înainte să continuăm analiza programului nostru, vă mai amintiți ce este un URL?
Exact, URL este un acronim pentru **U**niform **R**esource **L**ocator, și este utilizat pentru a specifica adresa (a ceva) pe internet *(the World Wide Web)*.

###Rute și Funcții View *(Routes and View Functions)*

Clenții, cum ar fi browserele trimit **cereri** la serverele web (ceea ce am creat noi acum 2 minute), care, la rândul lor, trimit cererile la aplicația noastră Flask.  Aplicația trebuie să știe ce cod să ruleze pentru fiecare cerere URL, așa că ea crează o **asociere** a URL-urilor cu funcțiile Python. Asociere dintre un URL și o funcție se numește un **route** (rută, cale, traseu).
În următorul exemplu se demonstrează cum se face această mapare în Flask:

```python
@app.route('/')
def index():
	return 'Hello World!'
```

Aici funcția `index()` este înregistrată la URL de bază al aplicației: `/`. Dacă aplicația ar fi lansată pe un server asociat cu domeniul `www.exemplu.com`, atunci dacă veți naviga la `http://www.exemplu.com`, atunci funția `index()` va fi rulată pe server și vă va fi afișat *Hello World!*, aceasta fiind un **response** (răspuns),  valoare returnată de funcție.
Funcții ca și `index()` se numesc **view functions**, funcții care afișează. Un response returnat de o funcție view poate fi un simplu **string** (ca și în cazul nostru), sau poate fi ceva mai complicat, după cum veți vedea mai târziu.


###Modul Debug

Haideți să facem o modificare la valoare returnată de funcția `index()`, să salvăm fișierul, și să facem un refresh la pagina din browser. 
După cum vedeți, serverul nu a inclus schimbarea, deoarece el rulează după o versiune mai veche a fișierului `hello.py`.
Un truc foarte util este modul **debug** care zice serverului să fie atent la toate schimbările ce au loc. Pe lângă asta, atunci când serverul va întâlni o eroare, el va încerca să analizeze cauza și vă va da o sugestie la cum să remediați greșeala. Tot ce trebuie să faceți pentru a activa acest mod este să adăugați următoarea linie de cod:

```python
app.debug = True
app.run() #această linie deja există în fișier
```

sau să includeți paramentrul în interiorul chemării metodei `run()`

```python
app.run(debug = True)
```

Ambele metode au exact același efect.

>rămâne să introduc o eroare intenționată

###Adăugăm URL-uri

Dacă ai fost atent la adresa ce-ți apare sus, în browser, atunci probabil ai observat că multe dintre aceste URL-uri au părți variabile. De exemplu URL-ul pentru pagina ta de Facebook este `http://www.facebook.com/<nume-utilizator>` , adică numele tău de utilizator este parte din URL. Următorul exemplu demonstrează aceeași funcționalitate a Flask-ului:

```python
@app.route('/user/<name>')
def user(name):
	return 'Hello, %s' % name
```

Porțiunea dintre `< >` este partea dinamică, așa că orice URL care coincide cu partea statică (`localhost:5000/user/`) va fi asociată cu funcția `user()`. Când funcția este chemată, Flask trimite partea dinamică ca o variabilă (argument), astfel `name` va fi trimisă în funcție ca parametru.

Salvăm fișierul și mergem în browser și accesăm adresa: 
`localhost:5000/user/numele-vostru`

>imagine

###Fișiere statice

După cum numele presupune, Flask permite utilizarea fișierelor statice. Pentru că el este un framework inteligent, el o să caute fișierele statice în folderul `/static` din proiect. Hai, să creăm folderul, un fișier cu extensia `.html` și să accesăm acest fișier la `localhost:5000/static/<numele-fișierului>`

>imagine(imagini)

#Bonus
###Zi-i vecinului să-ți acceseze site-ul
Pentru a face site-ul vizibil (și accesibil) tuturor **de pe rețeaua locală** 
trebuie să menționăm acest lucru lui Flask. Modificați ultima linie de cod ca să arate în felul următor:

```python
app.run(host = '0.0.0.0', debug = True)
```

După trebuie să aflăm ce adresă ne-a dat routerul. Pentru a face asta rulați instrucțiunea:

```bash
ifconfig
```

Aceasta va afișa multă informație în consolă, căutați ultima coloană, unde scrie  `wlan0` și căutați `inet addr`. Această adresă trebuie o dăm vecinului este aceasta.

>imagine
