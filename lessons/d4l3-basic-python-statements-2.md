---
layout: default
title: Basic Python Statements, Playing with "a" Python
---

#Basic Python Statements, <br> Playing with "a" Python

###**Data și Timpul**
####**Librăria datetime**
De foarte multe ori, în programare, și mai ales în programarea web, e necesar de stabilit și de salvat data și ora exactă a unei informații. Gândiți-vă, spre exemplu, la *Facebook*. În *Facebook* e păstrată și chiar afișată data și ora exactă a fiecărei postări sau comentariu. În *Python*, putem păstra aceste informații, legate de timp, folosind librăria ``datetime``.
####**Obținerea de date și timp**
Pentru a obține data și ora curentă, putem folosi funcția numită ``datetime.now()``.

```python
from datetime import datetime
print datetime.now()
```
Prima linie de cod importă librăria ``datetime``, astfel încât s-o putem utiliza. A doua linie afișează data și ora curentă.
###*Exercițiu:*
Creați o variabilă numită ``acum`` și stocați în ea rezultatul funcției ``datetime.now()``. Apoi, afișați valoarea lui ``acum``. Nu uitați de ``import``!

```python
from datetime import datetime
acum = datetime.now()
print acum
```
####**Extragerea informației**
Observați cum arată output-ul: ``2015-08-25 23:45:14.317454``. Cum veți proceda în cazul în care nu doriți să se afișeze întreaga dată și oră?

Simplu!
```Pythom
from datetime import datetime
acum = datetime.now()
anul_curent = acum.year
luna_curenta = acum.month
ziua_curenta = acum.day
```
Primele două linii deja le înțelegeți. În linia a treia, am luat ``anul`` din variabila ``acum`` și l-am stocat în ``anul_curent``. În liniile patru și cinci, am stocat ``luna`` și ``ziua`` din ``acum``.

###*Live coding:*
Să zicem că noi dorim să afișăm data de azi în formatul următor: *lună/ziuă/an*. Cum putem face asta? Aici ne vine în ajutor **substituția ``string``-urilor**!

```python
from datetime import datetime
acum = datetime.now()

print '%s-%s-%s' % (acum.year, acum.month, acum.day)
# se va afisa: 2015-08-19
```

Amintiți-vă că operatorul ``%`` va găsi toate scrierile ``%s`` din ``string`` și toate argumentele din paranteze. El le va afișa în ordinea corespunzătoare.
Vi s-a afișat data corect?

###*Exercițiu:*
Afișați data curentă în formatul: *zi/lună/an*. Pentru asta trebuie doar să înlocuiți simbolurile ``–`` cu ``/``  și să schimbați ordinea a ``now.month``, ``now.day`` și ``now.year``.

```python
from datetime import datetime
acum = datetime.now()
print '%s/%s/%s' % (acum.day, acum.month, acum.year)
```

Sunteți bravo! Haideți să implementăm aceeași logică pentru ore, minute și secunde.

```python
from datetime import datetime
acum = datetime.now()

print acum.hour
print acum.minute
print acum.second
```

În exemplul de mai sus, noi am afișat ora, minuta și secunda curentă.

###*Exercițiu:*
Exact ca și în exercițiul anterior, afișați timpul curent în forma: *oră:minută:secundă*.

Schimbați ``string``-ul pe care-l veți afișa, astfel încât să aveți caracterul ``:`` între ``%s``.
Modificați luna, ziua și anul în ``acum.hour``, ``acum.minute`` și ``acum.second``.

```python
from datetime import datetime
acum = datetime.now()
print '%s:%s:%s' % (acum.hour, acum.minute, acum.second)
```

###**Marea provocare!**
Ați reușit să afișați data și timpul în mod separat și într-o formă foarte drăguță! Bravo! Haideți acum să le combinăm!

```python
from datetime import datetime
acum = datetime.now()

print '%s/%s/%s' % (acum.month, acum.day, acum.year)
print '%s:%s:%s' % (acum.hour, acum.minute, acum.second)
```
În exemplul de mai sus, se va afișa data. Apoi, dintr-o linie nouă, se va afișa timpul.

Haideți să le afișăm pe toate pe aceeași linie într-o singură instrucțiune ``print``!

###*Exercițiu:*
Afișați data și timpul împreună în forma: *lună/zi/an oră:minută:secundă*.

Pentru a face asta:

- importați librăria ``datetime``;
- creați o variabilă numită ``acum`` și atribuiți-I funcția ``datetime.now()``;
- afișați data și timpul după cum vi s-a cerut mai sus. Nu uitați de: ``%s``, ``%``, ``/``, ``-`` și de ordinea variabilelor din paranteze.

```python
from datetime import datetime
acum = datetime.now()

print '%s/%s/%s %s:%s:%s' % (acum.month, acum.day, acum.year, acum.hour, acum.minute, acum.second)
```

**Concluzie:**
În acest capitol voi ați învățat două lucruri: ce înseamnă librăria ``datetime`` și cum are loc importarea de librării!

##**Funcții**
De multe ori, voi, ca viitori programatori, vă veți întâlni cu situația în care veți fi nevoiți să reutilizați o anumită secvență de program, dar deja cu alte valori. Pentru a nu scrie de fiecare dată codul din nou, este mult mai simplu să definiți o **funcție**, care poate fi reutilizată oricând.

Funcția este un concept important în programare (la fel ca și în matematică). Fiecare programator trebuie să poată să scrie funcții.
###**Sintaxa funcțiilor**

Funcțiile sunt constituite din două componente.

Primul component este **header**-ul funcției, care include: cuvântul-cheie ``def``, **numele** funcției și **parametrii** pe care-i transmiteți funcției. Parametrii sunt opționali. Vedeți mai jos un exemplu de funcție fără parametri:

```python
def hello_world(): # acesta este header-ul unei functii fara parametri
```
Al doilea component este **corpul** funcției, care descrie, propriu-zis, ce face funcția voastră. Corpul funcției trebuie să fie **indentat**, la fel ca și în cazul instrucțiunilor condiționale. *(Vă amintiți de indentarea condiționalelor?)*

```python
print "Hello World!" # acesta este corpul functiei
```
Mai jos puteți vedea întreaga funcție, scrisă de la început până la sfârșit:

```python
def hello_world():
    print "Hello World!"
```
Pentru a **apela** funcția dată, se scrie numele ei, urmat de două paranteze ``( )``.

```python
hello_world()
```
###*Exercițiu:*
Creați o funcție numită ``felicitare``, care afișează ``string``-ul ``"La multi ani!"``, după care apelați funcția dată.

```python
def felicitare():
    print "La multi ani!"

felicitare()
```

```python
def calcul(n):
    patrat = n**2
    print str(n) + " la patrat este " + str(patrat)
    return patrat

calcul(10)
```
####**Parametri și Argumente**

În exemplul de mai sus, ``n`` este **parametrul** funcției ``calcul``. ``10`` este **argumentul** transmis.

> **Notă:** Unei funcții îi puteți transmite atâția parametri, de câți aveți nevoie. Când apelați funcția, ar fi bine să-i transmiteți tot atâtea argumente, câți parametri ați definit.

###*Exercițiu:*
Analizați funcția ``putere`` de mai jos. Ea cere doi parametri: o bază și un exponent. Primul parametru este ridicat la puterea parametrului al doilea. După cum vedeți, funcția nu este completă, de aceea adăugați de sine-stătător parametrii: ``baza`` și ``exponent``. Apoi, apelați funcția cu argumentele: ``2`` pentru bază și ``3`` pentru exponent.

```python
def putere(___, ___):  # adaugati aici parametrii
    rezultat = baza**exponent
    print "%s la puterea a %s este %s." % (baza, exponent, rezultat)

putere(__,__)  # adaugati aici argumentele
```
*Rezultatul vostru trebuie să arate așa:*

```python
def putere(baza, exponent):  # adaugati aici parametrii
    rezultat = baza**exponent
    print "%s la puterea a %s este %s." % (baza, exponent, rezultat)

putere(2, 3)  # adaugati aici argumentele
```
Vi s-a dat rezultatul corect? Sunt sigură că da!
###**Funcții apelând funcții**

###*Live coding:*
Ați văzut deja funcții care pot afișa texte sau care pot face operații aritmetice, dar funcțiile pot fi mult mai puternice decât atât! De exemplu, o funcție poate apela o altă funcție:

```python
def func_one(n):
    return n * 5

def func_two(m):
    return func_one(m) + 7
```

###*Exercițiu:*
Să analizăm următoarele două funcții: ``o_afisare`` (care adună 1 la un număr pe care-l ia ca argument) și ``merita_alta_afisare`` (care adună 2).

```python
def o_afisare(n):
    return n + 1

def merita_alta afisare(n):
    return n + 2
```
Schimbați corpul funcției ``merita_alta_afisare`` astfel încât ea să adune 2 la output-ul funcției ``o_afisare``:

```python
def o_afisare(n):
    return n + 1

def merita_alta_afisare(n):
    return o_afisare(n) + 2

```

####**Practice Makes Perfect**

###*Exercițiu:*
Definiți ``(def)`` o funcție numită ``cub`` care cere un parametru numit ``numar``. Nu uitați de paranteze și de două puncte!

Faceți ca funcția să returneze ``(return)`` cubul unui număr (adică un număr ridicat la puterea a treia).

Definiți a doua funcție, numită ``mai_mare``, care cere un argument numit ``numar``.

Dacă ``(if)`` acel număr este mai mare decât 100, atunci ``mai_mare`` trebuie să apeleze funcția ``cub(numar)`` și să returneze rezultatul acesteia. În caz contrar, ``mai_mare`` trebuie să returneze ``False``.

Nu uitați că instrucțiunile condiționale ``if`` și ``else`` necesită ``:`` la sfârșitul liniei!

```python
def cub(numar):
    return numar ** 3

def mai_mare(numar):
    if numar > 100:
        return cub(numar)
    else:
        return False
```
###**Importarea modulelor**
Acum, să trecem la un capitol din *Python* extrem de interesant și, în același timp foarte important - importarea modulelor!

Ce înseamnă un modul?

Un **modul** este un fișier care conține multe definiții, inclusiv variabile și funcții, pe care le puteți folosi odată ce el, acest modul, a fost importat în programul vostru.
###*Live coding:*
Înainte de a importa ceva, haideți să vedem ce știe *Python* implicit, adică fără de importuri. Vom lua exemplul funcției radical. Linia de mai jos trebuie să afișeze ``5``.

```python
print sqrt(25)
```
Hey, dar nu ni s-a afișat ``5``! Se pare că avem o eroare. Să analizăm mesajul:

```python
NameError: name 'sqrt' is not defined
```

*Python* ne-a spus: ``"NameError: name 'sqrt' is not defined."`` *Python* nu știe ce înseamnă extragerea rădăcinii… până când!

În *Python* există un modul, numit ``math`` (de la matematică), care include un număr mare de variabile și funcții utile, iar ``sqrt()`` este una dintre aceste funcții. Pentru a accesa ``math``, tot de ce avem nevoie este cuvântul-cheie ``import``.

```python
import modul
```
Acest fel de import de module (ca cel de mai sus) se numește **import generic**.
###*Exercițiu:*
În acest exercițiu, trebuie să faceți două lucruri.

Primul lucru este să scrieți ``import math`` în prima linie de cod.

Al doilea lucru este să scrieți ``math.sqrt()`` cu argumentul ``25`` și să afișați rezultatul. În felul acesta îi veți spune lui *Python* nu doar să importe ``math``, dar și să extragă rădăcina dintr-un număr.

```python
import math
print math.sqrt(25)
```
####**Importarea funcțiilor**

Minunat! Acum *Python* știe cum să extragă rădăcina pătrată dintr-un număr!

Totuși, noi am avut nevoie, de fapt, doar de funcția ``sqrt``, iar să scrii mereu ``math.sqrt()`` poate deveni frustrant.

În *Python*, este posibil de importat doar unele din multiplele variabile sau funcții dintr-un anumit modul. Pentru asta, avem nevoie de cuvântul-cheie ``from``:

```python
from modul import functie
```
În acest fel, puteți scrie doar ``sqrt()`` pentru a obține rădăcina pătrată a unui număr. Nu mai aveți nevoie de ``math.sqrt()``!
###*Live coding:*
Haideți să importăm doar funcția ``sqrt`` din modulul ``math``. (Nu avem nevoie de ``()`` după ``sqrt``!)

```python
from math import sqrt
```
####**Importurile universale**

Fain! Am găsit o modalitate corectă de a selecta variabile și funcții din modulul pe care-l vrem!

Iar dacă noi în continuare dorim să obținem toate variabilele și funcțiile dintr-un modul, dar nu vrem să scriem permanent ``math.``, ce facem?

**Importul universal** vine cu o soluție! Sintaxa acestuia este:

```python
from module import *
```
###*Live coding:*
Haideți să utilizăm ``from modul import *`` pentru a importa tot din modulul ``math``.

```python
from math import *
```
Totul e bine, dar...
Importurile universale pot să pară ok din exterior, dar ele nu sunt o idee bună dintr-un motiv foarte important: ele fac programul vostru plin de o groază de variabile și funcții inutile sau care vă pot crea probleme.

Să zicem că ați creați funcția voastră și ați numit-o ``sqrt``. Tot în același program, ați importat modulul ``math``. În acest caz, funcția voastră ``sqrt`` va fi în siguranță: veți avea funcția pe care ați creat-o – ``sqrt``, și funcția din modul – ``import.sqrt``. Însă, dacă ați fi scris ``from math import *``, v-ați fi confruntat cu o problemă: două funcții diferite, dar cu același nume. Iar dacă ați fi scris de mai multe ori în același program ``import *``, nu ați fi fost capabili să înțelegeți care variabilă sau care funcție din care modul vine.

Din aceste motive, cel mai bine este fie să utilizați fie ``import modul`` și apoi ``modul.nume``, fie pur și simplu să faceți ``import`` unor variabile și funcții specifice din diferite module.

###**Review: Funcții**
Okay! Să revizuim funcțiile!

```python
def dialog(mesaj):
    return mesaj

if fericit():
    dialog("Sunt fericit!")
elif trist():
    dialog("Sunt trist.")
else:
    dialog("Nu stiu ce simt...")
```
Exemplul de mai sus este scris pentru a vă reaminti de funcții și pentru a vă servi drept referință.
###*Exercițiu:*


Definiți (`def`) o funcție, numită `shut_down`, care cere un singur parametru `s`. Nu uitați de paranteze și de două puncte!

Dacă (`if`) funcția `shut_down` primește un `s` egal cu `"yes"`, ea trebuie să vă returneze `"Shutting down"`, iar dacă (`elif`) `s` este egal cu `"no"`, atunci funcția trebuie să vă returneze `"Shutdown aborted"`. În final, dacă `shut_down` nu primește nimic din cele spuse mai sus, atunci funcția trebuie să returneze `"Sorry"`.


```python
def shut_down(s):
  if s == "yes":
    return "Shutting down"
  elif s == "no":
     return "Shutdown aborted"
  else:
      return "Sorry"
```

###**Review: Module**
Să ne reamintim despre importarea modulelor (și, în mod special, ce este accesibil din modulul `math`).

###*Exercițiu:*
Imporați modulul `math` prin oricare metodă doriți voi. Apelați funcția `sqrt` al acestui modul cu argumentul `13689` și afișați valoarea.

```python
from math import sqrt
print sqrt(13689)
```

###**Liste și Dicționare**
####**Introducere în liste**

**Listele** reprezintă un alt tip de date din *Python*. În liste puteți stoca date de orice tip sub numele unei singure variabile.

Listele sunt constituite dintr-un nume și din itemii atribuiți.

Puteți atribui itemi unei liste printr-o expresie de forma:

```python
nume_lista = [item_1, item_2]
```
Observați că itemii sunt scriși între paranteze patrate. O listă poate fi și goală:

```python
lista_goala = [].
```
###*Exercițiu:*

Lista de mai jos,  `zoo_animale`, are trei itemi:

```python
zoo_animale = ["urs", "vulpe", "tigru"]
```
Adăugați un al patrulea item listei! Introduceți numele animalului vostru preferat (ca un `string`) după `"tigru"`, prin virgulă.

```python
zoo_animale = ["urs", "vulpe", "tigru", "elefant"]
```
####**Accesarea după indice**


Puteți accesa un item al listei după indicele său. Un **indiciu** e ca o adresă care identifică locul itemului în listă. Indicele se scrie direct după numele listei, în paranteze patrate, cam așa: `nume_lista[indiciu]`.

Indicii listei încep cu 0, nu cu 1! (Da, da, la fel ca și la `string`-uri). Puteți să accesați primul element al unei liste în felul următor: `nume_lista[0]`. Al doilea item îl accesați așa: `nume_lista[1]`. Programatorii iubesc să numere de la zero.


###*Exercițiu:*

Creați o listă, numită `numere,` cu itemii `5`, `6`, `7` și `8`. Din rând nou, afișați rezultatul adunării itemilor doi și patru din listă.

```python
numere = [5, 6, 7, 8]
print numere[1] + numere[3]
```
####**New Neighbors**
Știți deja cum se accesează un item al listei. (După indice).

```python
zoo_animale = ["urs", "vulpe", "tigru", "elefant"]
print zoo_animale[0]
# se va afisa "urs"
```
Buuuuuun.

Într-o listă, de asemenea, se pot realoca itemi:

```python
zoo_animale = ["urs", "vulpe", "tigru", "elefant"]
zoo_animale[2] = "girafa"
print zoo_animale
# se va afisa ["urs", "vulpe", "girafa", "elefant"]
```

###*Exercițiu:*

Scrieți codul prin care veți înlocui itemul cu valoarea `"elefant"` cu oricare alt animal doriți voi. Afișați lista finală.

```python
zoo_animale = ["urs", "vulpe", "girafa", "elefant"]
zoo_animale[3] = "zebra"
print zoo_animale
# se va afisa ["urs", "vulpe", "girafa", "zebra"]
```

####**Late Arrivals**

O listă nu e obligată să aibă lungime fixă. Puteți adăuga itemi într-o listă oricând vreți voi!

```python
litere = ['a', 'b', 'c']
litere.append('d')
print litere
```
În exemplul de mai sus, de la început, am creat o listă numită `litere`.

Apoi, am adăugat `string`-ul `"d"` la sfârșitul listei.

În final, s-a afișat `['a', 'b', 'c', 'd']`.

###*Exercițiu:*
Mai jos, aveți o listă goală, numită `bagaj`.

```python
bagaj = []
```
Adăugați în lista dată trei obiecte (ochelari de soare, spre exemplu). Folosiți metoda `append()`. Afișați lista finală.

```python
bagaj = []
bagaj.append("ochelari de soare")
bagaj.append("palarie")
bagaj.append("costum de baie")
print bagaj
```
####**List Slicing**
Uneori, veți avea nevoie să accesați doar o porțiune a listei.

###*Live coding:*
Să executăm codul de mai jos!

```python
litere = ['a', 'b', 'c', 'd', 'e']
slice = litere[1:3]
print slice
print litere
```

 În exemplul de mai sus, de la început am creat o listă nouă, numită `litere`.

Apoi, am luat o secvență din `litere` și am stocat-o în `slice`.

În rezultat, instrucțiunea `litere[1:3]` a afișat rezultatul `['b', 'c']`. E de înțeles de ce s-a afișat itemul `"b"` cu indicele `1`. Dar de ce itemul `"d"`, cu indicele `3`, nu s-a afișat? Deoarece acest mod de "feliere a listelor" se stopează cu un indice înainte de cel scris în instrucțiune.

În final, am afișat `['a', 'b', 'c', 'd', 'e']`, pentru a arăta că nu am modificat nimic din lista inițială.

###**Slicing Lists and Strings**
Puteți "felia" `string`-urile exact ca și listele! De fapt, `string`-urile se pot interpreta ca niște liste de caractere: fiecare caracter este un item din listă, care începe cu indicele 0.

Dacă secvența vostră de listă pe care vreți s-o afișați include primul sau ultimul item din listă, indicele pentru acest item nu trebuie inclus:

```python
print lista_mea[:2]
# afiseaza primii doi itemi ai listei lista_mea
print lista_mea[3:]
# afiseaza itemii de la al patrulea pana la ultimul
```

###*Live coding:*
Logica pe care am descris-o mai sus poate fi aplicată și asupra `string`-urilor, așa cum am mai menționat.

În continuare, voi afișa, de 3 ori, doar caracterele care reprezintă un animal din `string`-ul `zoo`:


```python
zoo = "urslupcerb"

print zoo[:3]
print zoo[3:6]
print zoo[6:]
```

####**Maintaining Order**
Uneori, avem nevoia să căutăm un item într-o listă.

```python
pasari = ["papagal", "flamingo", "colibri"]
print pasari.index("flamingo")
```
Inițial, am creat o listă numită `pasari` cu trei `string`-uri. Apoi, am afișat primul indiciu care conține `string`-ul `"flamingo"`. Rezultatul este `1`.

De asemenea, noi putem insera itemi într-o listă.

```python
pasari.insert(1, "paun")
print pasari
```
Am inserat `"paun"` la indicele `1`, ceea ce va mișca totul de la 1 spre dreapta.
În final, am afișat `["papagal", "paun", "flamingo", "colibri"]`

###*Exercițiu:*
Mai jos aveți o listă, numită `culori`, care conține 4 itemi.

```python
culori = [ 'negru', 'rosu', 'albastru', 'verde' ]
```

Folosiți funcția `.index(item)` pentru a găsi indicele culorii verde. Atribuiți acest rezultat unei variabile numite `verde_index`. Apoi, inserați prin `.insert(index, item)` `string`-ul `"galben"` la indicele `verde_index`.

```python
culori = [ 'negru', 'rosu', 'albastru', 'verde' ]

verde_index = culori.index("verde")
culori.insert(verde_index, "galben")
print culori
```

O listă poate fi și sortată după ordinea alfabetică. Asta nu e complicat! Priviți aici:

```python
culori.sort()
# se va afisa ['albastru', 'galben', 'negru', 'rosu', 'verde']
```
Metoda `.sort()` a aranjat `string`-urile în ordine alfabetică în mai puțin de o secundă!


####**Remove a Few Things**

Uneori, avem nevoie să ștergem ceva și dintr-o listă.

```python
beatles = [ "john", "paul", "george", "ringo", "stuart" ]
beatles.remove("stuart")
print beatles
# se va afisa ["john", "paul", "george", "ringo"]
```

În exemplul de mai sus, am creat o listă cu 5 `string`-uri.

Apoi, am eliminat primul item din `beatles` care coincide cu `string`-ul `"stuart"`. Țineți minte că `.remove(item)` nu returnează nimic.

În final, am afișat lista pentru a ne asigura că `"stuart"` într-adevăr a fost eliminat.

###*Exercițiu:*
Creați o listă nouă, numită `rechizite`. Lista trebuie să aibă minim 5 itemi. Ulterior, eliminați un item la dorința voastră și afișați rezultatul!

```python
rechizite = ['pix', 'creion', 'radiera', 'rigla', 'compas']
rechizite.remove('radiera')
print rechizite
```

###**Dicționare**

Un **dicționar** este asemănător cu o listă, doar că în cazul dicționarelor puteți să accesați valorile prin intermediul unei chei, și nu prin intermediul unui indice. O **cheie** poate fi un `string` sau un număr. Dicționarele se scriu între acolade, în felul următor:

```python
dictionar = {'cheie1' : 1, 'cheie2' : 2, 'cheie3' : 3}
```
Mai sus avem exemplul unui dicționar cu trei perechi *cheie-valoare*. Cheia `cheie1` are valoarea `1`, `cheie2` - valoarea `2` ș.a.m.d.

Dicționarele sunt utile pentru asemenea lucruri, ca: lista numerelor de telefoane (având perechile *nume - număr*), pagini de logare (având perechile *adresa de e-mail - nume de utilizator*) și nu doar!

###*Live coding:*
Mai jos, vă prezint un exemplu de dicționar, care stochează informația pentru perechile *e-mail - parolă*.

```python
d = { 'alexandru@gmail.com' : 2345,
    'olga@yahoo.com' : 6789,
    'daniela@mail.md' : 0123 }
```

Accesarea unei valori din dicționar după o cheie e aceeași cum am accesa valorile din liste după indici:

```python
print d['alexandru@gmail.com']
```
###*Exercițiu:*
Din dicționarul de mai sus, accesați valoarea perechii a doua și a treia (după cheie). Pentru aceasta, de la început, copiați dicționarul `d` în Sublime Text. Afișați rezultatele.

```python
d = { 'alexandru@gmail.com' : 2345,
    'olga@yahoo.com' : 6789,
    'daniela@mail.md' : 0123 }

print d['olga@yahoo.com']
print d['daniela@mail.md']
```

####**New Entries**

La fel ca listele, dicționarele sunt "flexibile".  Aceasta înseamnă că ele pot fi schimbate după ce au fost create. Un avantaj al acestui fapt este ceea că putem adăuga în dicționarele deja create noi perechi *cheie-valoare*, în felul următor:

```python
nume_dict[cheie_noua] = valoare_noua
```
O pereche goală de acolade este un dicționar gol, la fel cum o pereche goală de `[]` este o listă goală.

###*Live coding:*

Haideți să creăm un dicționar nou, numit `meniu`.

```python
meniu = {}
```
Acum să adăugăm în acest dicționar o pereche *cheie-valoare*:

```python
meniu['Supa cu ciuperci'] = 40.00
```
În final, să afișăm prețul supei cu ciuperci:

```python
print meniu['Supa cu ciuperci']
```

###*Exercițiu:*
Adăugați, la meniul de mai sus, cel puțin trei feluri de bucate și indicați-le prețul. Vă puteți orienta după exercițiul de mai sus!

```python
meniu['Pizza cu broccoli']   = 60.00
meniu['Cartofi prajiti']     = 35.00
meniu['Inghetata cu zmeura'] = 29.00
```

####**Changing Your Mind**

Deoarece dicționarele sunt flexibile, ele pot fi modificate în diverse moduri. Itemii pot fi eliminați dintr-un dicționar cu comanda `del`:

```python
del nume_dict[nume_cheie]
```
Codul de mai sus va șterge din dicționar cheia `nume_cheie` și valoarea asociată acesteia.

O valoare nouă poate fi asociată unei chei prin atribuire:

```python
nume_dict[cheie] = valoare_noua
```
###*Exercițiu:*
Mai jos, aveți creat un dicționar cu animalele de la Grădina Zoologică și un exemplu de cum se elimină unul din itemi.

```python
# cheie - nume_animal : valoare - locatia
zoo_animale = { 'Maimuta' : 'Africa',
        'Tigru' : 'Asia',
        'Cangur' : 'Australia',
        'Unicorn' : 'Wonderland' }

# stergem 'Unicorn'. (Unicornii sunt excesiv de scumpi.)
del zoo_animale['Unicorn']
```

Eliminați și maimuța din acest dicționar. Apoi, atribuiți-i altă locație tigrului. În final, afișați dicționarul!

```python
del zoo_animale["Maimuta"]
zoo_animale["Tigru"] = "America de Sud"
print zoo_animale
```

####**It's Dangerous to Go Alone!**

Să rezumăm un pic dicționarele:

```python
my_dict = {
    "ziua": [ "d", "u", "m", "i", "n", "i", "c", "a" ],
    "cash": -4483,
    "stare": "obosit"
}
print my_dict["ziua"][0]
```
În exemplul de mai sus, am creat un dicționar care conține diferite tipuri de valori.

Cheia `"ziua"` are o listă, cheia `"cash"` are un `int` și cheia `"stare"` are un `string`.

În final, am afișat litera `"d"`. Când accesăm o valoare într-un dicționar de genul `my_dict["ziua"]`, avem acces direct la valoare. Astfel, putem accesa itemul de la indicele `'0'` din listă stocat de cheia `"ziua"`.

###*Exercițiu:*

Analizați sevența de cod de mai jos:

```python
liceu = {
    'elevi' : 500,
    'olimpici' : ['matematica', 'informatica', 'geografie'], # am atribuit o lista la cheia 'olimpici'
    'premii' : ['sport', 'teatru', 'dans', 'pictura']
}

# adaugam o cheie noua 'cursuri' si ii atrinuim o lista
liceu['cursuri'] = ['programare', 'antreprenoriat', 'engleza']

# sortam lista cu cheia 'olimpici'
liceu['olimpici'].sort()
```
Adăugați o nouă cheie la dicționarul `liceu`, numită `'fesivitati'`.
Valoarea sub cheia `'festivitati'` trebuie să fie o listă ce va conține: `'halloween'`, `'revelion'` și  `'ultimul sunet'`.

Prin `.sort()`, sortați itemii listei `premii`. Apoi, eliminați din această listă, prin `.remove()`, itemul stocat sub cheia `'teatru'`.

Adăugați `50` la numărul stocat sub cheia `"elevi"`.


```python
liceu["festivitati"] = ["halloween", "revelion", "ultimul sunet"]
liceu['premii'].sort()
liceu["premii"].remove("teatru")
liceu['elevi'] = liceu['elevi'] + 50
```